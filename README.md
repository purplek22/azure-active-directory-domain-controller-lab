# azure-active-directory-domain-controller-lab
Deployment of a Windows Server 2022 and a Domain Controller in Microsoft Azure with an Active Directory configuration and basic security hardening.
# Azure Active Directory Domain Controller Lab

## Overview
This project demonstrates the deployment of a Windows Server 2022 virtual machine in Microsoft Azure and the configuration of Active Directory Domain Services (AD DS). The server was promoted to a Domain Controller and configured to manage users, organizational units, and basic Group Policy.

This lab simulates an enterprise environment where centralized identity and access management is required.

---

## Objectives

- Deploy a Windows Server 2022 VM in Azure
- Configure virtual networking
- Install Active Directory Domain Services
- Promote server to Domain Controller
- Create Organizational Units (OUs)
- Create domain users
- Configure basic Group Policy
- Implement basic security hardening

---

## Lab Environment

- Platform: Microsoft Azure
- Server OS: Windows Server 2022
- Region: (Central US)
- VM Size: ("Standard_D2s_v3)
- Virtual Network: Custom VNet
- Remote Access: RDP

---

## Network Configuration

- Created Virtual Network (VNet)
- Assigned static private IP to Domain Controller
- Configured DNS settings for domain functionality
- Restricted RDP access using Network Security Groups (NSG)

---

## Step 1: Deploy Windows Server VM

A Windows Server 2022 virtual machine was deployed in Azure.

![VM Deployment](activedirectory/DomainControllerss.png)

---

## Step 2: Install Active Directory Domain Services

The AD DS role was installed using Server Manager.

![AD DS Installation](activedirectory/adinstall.png)

---

## Step 3: Promote Server to Domain Controller

The server was promoted to a Domain Controller and a new forest was created.

Domain Name: (lab.local)

![Domain Promotion](activedirectory/domainpromo.png)

---

## Step 4: Create Organizational Units and Users

Organizational Units were created to simulate departmental structure. Domain users were added for identity management testing.

![Users Created](activedirectory/users.png)

---

## Step 5: Configure Group Policy

Basic password and account lockout policies were configured.

![Group Policy](activedirectory/grouppolicy.png)

---

## Security Considerations

- Enforced password complexity requirements
- Configured account lockout threshold
- Restricted RDP access via NSG rules
- Disabled unnecessary services
