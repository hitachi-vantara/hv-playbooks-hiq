# hv-playbooks-hiq
Ansible Playbooks for Hitachi iQ
##**Kubernetes Cluster Automation with Ansible**##

##**Overview**

This repository contains a set of Ansible playbooks designed to automate the setup and configuration of a Kubernetes cluster. The playbooks handle the entire lifecycle of the cluster, including:

- Installing and configuring HAProxy and Keepalived for high availability.
- Setting up a Virtual IP (VIP) for Keepalived.
- Installing Kubernetes on control plane and worker nodes.
- Deploying applications and services such as:
- Jupyter Notebook
- MinIO (object storage)
- Local Path Storage (persistent storage)
- PostgreSQL (database)


**Prerequisites**

- Ansible installed on your machine.
- Access to the target servers with proper SSH credentials.
- A configured inventory file with IP addresses of control plane and worker nodes.

**How to Use**

1. **Clone the Repository**

bash

Copy code

git clone https://github.com/hitachi-vantara/hv-playbooks-hiq.git

cd hitachi-iq-1

2. **Set Up Inventory**

Edit the inventory/inventory.ini file with the IP addresses of your control plane and worker nodes. Example:

ini

[control_plane]

192.168.1.10

192.168.1.11

[worker_nodes]

192.168.1.20

192.168.1.21

3. **Set Up Variables**

Edit the vars.yaml file with the k8s version, crio version. Example: 

kubernetes_version: "v1.30"
cri_o_version: "1.26"
load_balancer_ip: "10.76.40.223"
vip_interface: "ens17f0"


weka_namespace: "csi-wekafs"
secret_name: "csi-wekafs-api-secret"
storage_class_name: "storageclass-wekafs-dir-api"

weka_username: "admin"
weka_password: "admin"
weka_endpoints:
  - "172.31.41.54:14000"
  - "172.31.47.152:14000"




4. **Run Playbooks**

**Execute the playbooks as below**

ansible-playbook -i inventory.ini main.yaml -e @vars.yaml
