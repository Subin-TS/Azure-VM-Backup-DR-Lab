# Azure VM Backup & Cross-Region Disaster Recovery Lab

![Azure](https://img.shields.io/badge/Cloud-Microsoft%20Azure-0078D4?logo=microsoftazure)
![Ubuntu](https://img.shields.io/badge/OS-Ubuntu%2022.04-E95420?logo=ubuntu)
![NGINX](https://img.shields.io/badge/Web%20Server-NGINX-009639?logo=nginx)
![Linux](https://img.shields.io/badge/Linux-Bash-FCC624?logo=linux)

---

# Project Overview

This project demonstrates how to design and implement an **enterprise-grade Azure Backup and Disaster Recovery (BCDR)** solution using **Azure Backup** and **Azure Site Recovery (ASR)**.

An Ubuntu Linux Virtual Machine hosting an NGINX web application was deployed in Azure and protected using **Recovery Services Vault** for scheduled backups. The virtual machine was then replicated to a secondary Azure region using **Azure Site Recovery**, and a successful **Test Failover** was performed to validate business continuity during a regional disaster.

---

# Business Objective

The primary objective of this project is to protect business-critical workloads by implementing:

- Automated Virtual Machine Backup
- Cross-Region Disaster Recovery
- Continuous Replication
- Business Continuity
- Disaster Recovery Validation
- Recovery Point and Recovery Time optimization

---

# Solution Architecture

```
                           Internet
                               │
                               ▼
                        Azure Public IP
                               │
                               ▼
                  Ubuntu 22.04 Virtual Machine
                    (Primary Region - Central India)
                               │
                             NGINX
                               │
                     Sample Web Application
                               │
        ┌──────────────────────┴──────────────────────┐
        │                                             │
        ▼                                             ▼

 Azure Backup                               Azure Site Recovery

 Recovery Services Vault                    Recovery Services Vault

 (Central India)                            (South India)

        │                                             │

 Daily Recovery Points              Continuous Cross-Region Replication

        │                                             │

 VM Restore                         Replica Managed Disks

                                              │

                                              ▼

                                Test Failover Virtual Machine
                                    (Secondary Region)
```

---

# Technologies Used

- Microsoft Azure
- Azure Virtual Machines
- Azure Virtual Network (VNet)
- Network Security Groups (NSG)
- Azure Backup
- Recovery Services Vault
- Azure Site Recovery (ASR)
- Ubuntu Server 22.04 LTS
- NGINX
- Linux
- Bash
- SSH

---

# Project Workflow

## Phase 1 – Infrastructure Deployment

- Created Azure Resource Group
- Created Virtual Network
- Configured Network Security Group
- Deployed Ubuntu 22.04 Virtual Machine
- Connected using SSH
- Installed and configured NGINX
- Hosted a sample web application

---

## Phase 2 – Azure Backup

- Created Recovery Services Vault
- Configured Daily Backup Policy
- Enabled Virtual Machine Backup
- Performed On-Demand Backup
- Generated Recovery Points
- Verified Backup Health
- Performed File-Level Restore validation

---

## Phase 3 – Azure Site Recovery

- Created Recovery Services Vault in Secondary Region
- Configured Azure Site Recovery
- Enabled Cross-Region Replication
- Completed Initial Replication
- Verified Replication Health
- Performed Test Failover
- Verified Disaster Recovery Virtual Machine
- Completed Cleanup Test Failover

---

# Key Features

- Azure Infrastructure Deployment
- Linux Virtual Machine Administration
- NGINX Web Server Hosting
- Automated Daily VM Backup
- Recovery Point Creation
- File-Level Restore Validation
- Cross-Region Disaster Recovery
- Continuous VM Replication
- Test Failover
- Business Continuity Validation

---

# Validation Performed

✔ Ubuntu VM successfully deployed

✔ NGINX web application accessible

✔ Backup completed successfully

✔ Recovery point created successfully

✔ File-Level Restore validated

✔ Azure Site Recovery configured successfully

✔ Cross-region replication completed

✔ Replication Health verified

✔ Test Failover completed successfully

✔ Cleanup Test Failover completed successfully

---



---

# Skills Demonstrated

- Microsoft Azure Administration
- Azure Virtual Machines
- Azure Networking
- Azure Backup
- Recovery Services Vault
- Azure Site Recovery
- Business Continuity & Disaster Recovery (BCDR)
- Cross-Region Replication
- Linux Administration
- NGINX
- SSH
- GRUB Bootloader
- Linux Kernel Management
- Azure Troubleshooting

---



---

# Learning Outcomes

Through this project, I gained hands-on experience with:

- Azure Infrastructure Deployment
- Virtual Machine Protection
- Backup Strategy Implementation
- Disaster Recovery Planning
- Cross-Region Replication
- Recovery Services Vault
- Azure Site Recovery
- Recovery Point Objective (RPO)
- Recovery Time Objective (RTO)
---

# Author

**Subin T Sasi**



---

## If you found this project helpful, consider giving it a ⭐ on GitHub.
