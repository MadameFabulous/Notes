[SAPwned: SAP AI vulnerabilities expose customers’ cloud environments and private AI artifacts | Wiz Blog](https://www.wiz.io/blog/sapwned-sap-ai-vulnerabilities-ai-security)

# Bug 1 - Network Misconfiguraitons

SAP's AI instances run in Kubernetes which allow for code execution which starts the process at priv esc and lateral movement.
```
The first is `shareProcessNamespace`, which allowed us to share the process namespace with our sidecar container. Since our sidecar was the Istio proxy, we gained access to Istio’s configuration, including an access token to the cluster’s centralized Istiod server.
```

## Kubernetes Paths
### Path 1
shareProcessNamespace -> Istio proxy sidecar -> access token to cluster’s centralized Istiod server -> Unrestricted Network Permissions

### Path 2
runAsUser -> Istio’s UID -> Unrestricted Network Permissions

# Bug 2 - Exposed Grafana Loki config
## Loki leaks AWS tokens
```
We found an instance of Grafana Loki on the cluster, so we requested the `/config` endpoint to view Loki’s configuration. The API responded with the full configuration, including AWS secrets that Loki used to access S3:
```

Unrestricted networks ->Grafana Loki Instance->exposed config -> Exposed secrets for SAP's s3 bucket

## Bug 3 - Elastic File System and Exposed Customer Data
[The EKS Hacking Playbook: Lessons From 3 Years of Cloud Security Research (youtube.com)](https://www.youtube.com/watch?v=HcNmkCRXFdE)
Unrestricted networks -> Default Configuration for EFS -> Config set to public by default

```
A [common problem](https://youtu.be/HcNmkCRXFdE) with EFS instances is their default configuration as public – meaning credentials aren’t needed to view or edit files, as long as you have network access to their NFS ports.
```
## Bug 4 - Unauthenticated Helm server compromises internal Docker Registry and Artifactory
Communication with Tiller is made via its gRPC interface on port 44134, which is by default exposed without any authentication.
Unrestricted networks ->Tiler->  gRPC interface on port 44134 -> exposed credentials for Docker Registry and Artifactory-> customer AI builds readable

### Exploit Mechanics
```
Communication with Tiller is made via its gRPC interface on port 44134, which is by default exposed without any authentication.
```

### Access to
```
Using the secrets’ write access, an attacker could poison images and builds, conducting a supply-chain attack on SAP AI Core services.
```
## Bug 5 - Unauthenticated Helm server compromises K8s cluster, exposing Google access tokens and customer secrets 

```
The Helm server was exposed to both read and write operations. While the read access exposed sensitive secrets (as can be seen above), the server’s write access allowed for a complete cluster takeover.
```
Unrestricted networks -> Kubernetes Helm Misconfiguration  -> Tiler Write Access via Helm  -> Tiler install command -> Created new container with cluster admin privileges -> Kubernetes takeover
