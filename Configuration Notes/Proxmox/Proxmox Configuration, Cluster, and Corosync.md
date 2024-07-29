# Post-Install

[Proxmox VE Helper-Scripts (tteck.github.io)](https://tteck.github.io/Proxmox/#proxmox-ve-post-install)
```
bash -c "$(wget -qLO - https://github.com/tteck/Proxmox/raw/main/misc/post-pve-install.sh)"
```

https://dannyda.com/2020/05/17/how-to-remove-you-do-not-have-a-valid-subscription-for-this-server-from-proxmox-virtual-environment-6-1-2-proxmox-ve-6-1-2-pve-6-1-2/
```
sed -i.backup -z "s/res === null || res === undefined || \!res || res\n\t\t\t.data.status.toLowerCase() \!== 'active'/false/g" /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js && systemctl restart pveproxy.service
```

# Corosync
[Releases · corosync/corosync (github.com)](https://github.com/corosync/corosync/releases)
[Cluster Manager - Proxmox VE](https://pve.proxmox.com/wiki/Cluster_Manager)
[Setup a Proxmox Two-Node High Availability Cluster with a RaspberryPi as a third Quorum vote device (qdevice) - Florian Müller (florianmuller.com)](https://florianmuller.com/setup-a-proxmox-two-node-high-availability-cluster-with-a-raspberrypi-as-a-third-quorum-vote-device-qdevice)
## Execution and Stumbling Blocks
Small stumbling block on HA availability, reran the proxmox installl script and re-enabled HA on all nodes

Double check all pubic keys across the triad
You must have logged into each host so that they all are shared in the known_hosts file

I disabled 2fa when making the cluster because I didn't want to futz with mfa on the command line.

Login to each of the proxmox nodes and then install corosync
```
apt update && apt install corosync-qdevice
```

On the non-Proxmox member install the following as root (rasp pi for my initial deployment)
```
sudo su
apt update
apt install corosync-qnetd
apt install corosync-qdevice
```


From each of the Proxmox Nodes
```
pvecm qdevice setup <target_ip>
```

# Unclustering (hopefully not needed)
I found this while researching and wanted to save the thread just incase I need it in the future.
[Cluster or not... : r/Proxmox (reddit.com)](https://www.reddit.com/r/Proxmox/comments/sgyosg/cluster_or_not/)
