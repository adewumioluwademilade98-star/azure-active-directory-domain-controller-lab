# Azure Active Directory Domain Controller lab
Hands-on lab documenting the deployment of a Windows Server domain controller in Azure, including Active Directory Domain Services and DNS.


## Project Overview

This project documents my hands-on experience deploying and configuring a Windows Server domain controller in Microsoft Azure.

The goal was to build a small lab environment to develop practical skills in Windows Server administration, Active Directory, DNS, and remote server management.

## Objectives

- Deploy a Windows Server virtual machine in Azure.
- Configure a stable private IP address through the Azure portal.
- Connect to the server using Remote Desktop Protocol (RDP).
- Install the Active Directory Domain Services (AD DS) role.
- Promote the server to a domain controller.
- Create a new Active Directory forest named `corp.lab.local`.
- Verify that Active Directory and DNS are installed and operational.

## Technologies Used

| Technology | Purpose |
|---|---|
| Microsoft Azure | Cloud infrastructure and virtual machine hosting |
| Windows Server 2022 Datacenter | Server operating system |
| Active Directory Domain Services | Centralized identity and directory management |
| DNS | Name resolution for the domain |
| Remote Desktop Protocol | Remote server administration |
| Azure Virtual Network | Private network connectivity |

## Lab Configuration

- **Virtual machine:** DC01
- **Operating system:** Windows Server 2022 Datacenter
- **Active Directory domain:** `corp.lab.local`
- **NetBIOS domain name:** `CORP`
- **Resource group:** `AD-Lab-RG`
- **Virtual network:** `AD-Lab-VNet`

Sensitive connection details and IP addresses are intentionally excluded.

## Implementation Steps

### 1. Deploy the virtual machine

Created a Windows Server virtual machine in Azure and selected the appropriate resource group, operating system, compute resources, and networking configuration.

### 2. Configure the server's private IP address

Configured the virtual machine's private IP assignment as static through the Azure portal's network interface settings.

This helps other lab devices and services locate the domain controller consistently.

### 3. Connect to the server

Used Remote Desktop Protocol (RDP) to access and administer the Windows Server virtual machine.

### 4. Install Active Directory Domain Services

Used Server Manager to install the AD DS server role and its required supporting features.

### 5. Promote the server to a domain controller

Created a new Active Directory forest using the domain name `corp.lab.local`. Kept DNS enabled during the configuration and completed the promotion process.

The server restarted to apply the domain controller configuration.

### 6. Verify the configuration

Reconnected to the server after the restart and checked the Active Directory and DNS roles.

Opened Active Directory Users and Computers to inspect the new domain structure.

## Key Learning Outcomes

- Understanding the role of a domain controller in a Windows domain.
- Deploying and managing virtual machines in Azure.
- Understanding the relationship between Active Directory and DNS.
- Configuring a stable private IP address for a server.
- Installing Windows Server roles and promoting a server to a domain controller.
- Managing servers remotely using RDP.
- Understanding the importance of protecting administrative credentials and restricting remote access.

## Security Considerations

- No passwords, recovery credentials, or authentication secrets are included in this repository.
- Public IP addresses and sensitive network details are intentionally omitted.
- Remote administration access should be restricted to trusted sources.
- Production environments should use stronger access controls, such as VPN or Azure Bastion, rather than exposing RDP directly to the internet.
- Azure virtual machines should be stopped and deallocated when not in use to help control lab costs.

## Future Improvements

- Create organizational units (OUs) and test user accounts.
- Configure groups and permissions.
- Join a Windows 11 client to the domain.
- Create and test Group Policy Objects (GPOs).
- Practise DNS troubleshooting.
- Document common Active Directory administration tasks.

## Conclusion

This lab provided practical experience deploying a Windows Server domain controller in Azure and establishing an Active Directory domain with DNS.

It is part of my ongoing journey toward Windows administration, IT support, and cybersecurity.
