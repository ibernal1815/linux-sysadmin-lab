#  Ultra-Hardened Linux SysAdmin Lab
> **Hybrid Cyber-Defense & Infrastructure Automation Sandbox**

This repository contains the **Infrastructure as Code (IaC)** blueprints for a high-density Linux environment running on an **Intel i5-14400F** with **48GB DDR4**.

##  Architecture Overview
The lab is built on a **Zero Trust** model, utilizing ephemeral workloads to maximize the 48GB RAM overhead.



###  Key Capabilities
* **IaC Provisioning:** Terraform for Proxmox VM lifecycle.
* **Configuration Management:** Ansible for "Day 2" hardening and service deployment.
* **Security & SIEM:** Integrated Wazuh and ELK stack for real-time monitoring.
* **GitOps Flow:** Managed via GitHub Codespaces and automated CI/CD pipelines.

##  Repository Structure
- `/infrastructure`: Terraform & Packer templates.
- `/provision`: Ansible playbooks and roles.
- `/services`: Docker-compose stacks for core utilities.
- `/docs`: Network schemas and hardware documentation.

---
*“In an era of cloud, the master of the local metal is king.”*
