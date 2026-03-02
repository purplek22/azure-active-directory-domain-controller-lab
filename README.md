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

[VM Deployment]<img width="1124" height="1172" alt="vmdeployment" src="https://github.com/user-attachments/assets/669986a1-73e7-40cf-8ce4-ce51ad41bf55" />
ss.png)

---

## Step 2: Install Active Directory Domain Services

The AD DS role was installed using Server Manager.

![AD DS Installation]<img width="1295" height="1017" alt="adinstall" src="https://github.com/user-attachments/assets/a62656b2-6cfe-4106-9ec4-8a312c1074dd" />


---

## Step 3: Promote Server to Domain Controller

The server was promoted to a Domain Controller and a new forest was created.

Domain Name: (lab.local)

[Domain Promotion]
<img width="762" height="558" alt="domainpromo" src="https://github.com/user-attachments/assets/57a6275b-7fb5-41c7-8a0a-eec585750fb4" />

---

## Step 4: Create Organizational Units and Users

Organizational Units were created to simulate departmental structure. Domain users were added for identity management testing.

[Users Created]<img width="643" height="400" alt="users" src="https://github.com/user-attachments/assets/f255bba9-51c3-4283-84de-204713cad596" />


---

## Step 5: Configure Group Policy

Basic password and account lockout policies were configured.

[Group Policy]<img width="565" height="117" alt="grouppolicy" src="https://github.com/user-attachments/assets/b6c01fce-d12c-41ac-afe6-5bec49c0a3b5" />


---

## Security Considerations

- Enforced password complexity requirements
- Configured account lockout threshold
- Restricted RDP access via NSG rules
- Disabled unnecessary services
