# Kubernetes
Kubernetes (k8s) is an open-source system for automating deployment, scaling, and management of containerized applications.

## Running minikube on a cloud instance on digital ocean
1. Configure a new ubuntu or centos image using digitalocean.com
2. Install a hypervisor
[Virtual Box](https://www.virtualbox.org/wiki/Linux_Downloads)
3. Install kuberctl
4. Download minikube image
5. `minikube start`

## Create a Configuration File
The example configuration defines two types of objects:

1. The PersistentVolumeClaim called csi-pvc which is responsible for locating the block storage volume by name if it already exists and creating the volume if it does not.

2. The Pod named my-csi-app, which will create containers, then add a mountpoint to the first object and mount the volume there.

[How to Add Block Storage Volumes to a Kubernetes Cluster](https://www.digitalocean.com/docs/kubernetes/how-to/add-persistent-storage/)
