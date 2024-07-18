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
