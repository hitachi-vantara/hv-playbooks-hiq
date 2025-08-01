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



**DISCLAIMER** All materials provided in this repository, including but not limited to Ansible Playbooks and Terraform Configurations, are made available as a courtesy. These materials are intended solely as examples, which may be utilized in whole or in part. Neither the contributors nor the users of this platform assert or are granted any ownership rights over the content shared herein. It is the sole responsibility of the user to evaluate the appropriateness and applicability of the materials for their specific use case.

 Use of the material is at the sole risk of the user and the material is provided “AS IS,” without warranty, guarantees, or support of any kind, including, but not limited to, the implied warranties of merchantability, fitness for a particular purpose, and non-infringement. Unless specified in an applicable license, access to this material grants you no right or license, express or implied, statutorily or otherwise, under any patent, trade secret, copyright, or any other intellectual property right of Hitachi Vantara LLC (“HITACHI”). HITACHI reserves the right to change any material in this document, and any information and products on which this material is based, at any time, without notice. HITACHI shall have no responsibility or liability to any person or entity with respect to any damages, losses, or costs arising from the materials contained herein.
