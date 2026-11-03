# Active Directory & Windows Server Help Desk Lab

## Project Overview

This project demonstrates hands-on experience configuring and administering a Windows Server Active Directory environment using Oracle VirtualBox.

I built a simulated corporate network consisting of a Windows Server domain controller and a Windows 11 Pro workstation. The lab focuses on Active Directory administration, user account management, security groups, Group Policy, DNS, domain authentication, and common Tier 1 IT Help Desk troubleshooting tasks.

## Technologies Used

- Windows Server 2022
- Windows 11 Pro
- Oracle VirtualBox
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy Management
- Active Directory Users and Computers (ADUC)
- Windows Command Prompt

## Lab Environment

| Component | Configuration |
|---|---|
| Domain | `corp.novatech.com` |
| NetBIOS Domain | `CORP` |
| Domain Controller | `CORP-DC01` |
| Windows Client | `CORP-WIN01` |
| Domain Controller IP | `192.168.100.10` |
| Subnet | `192.168.100.0/24` |
| Network | VirtualBox NAT Network (`CorpLab-NAT`) |
| Client Operating System | Windows 11 Pro |

## Lab Implementation

### 1. Virtual Machine and Server Configuration

Created a Windows Server virtual machine in VirtualBox, configured virtual hardware, established a NAT Network, and installed Windows Server.

Renamed the server `CORP-DC01` and configured a static IPv4 address.

**Server Manager Dashboard**

![Windows Server Dashboard](screenshots/05-Windows-Server-Dashboard.png)

**Static IP Configuration**

![Static IP Configuration](screenshots/07-Static-IP-Configuration.png)

**Network Verification**

![IP Configuration Verification](screenshots/08-IP-Configuration-Verification.png)

### 2. Active Directory Domain Services

Installed Active Directory Domain Services and promoted `CORP-DC01` to a domain controller.

Created the Active Directory forest `corp.novatech.com` and configured DNS and Global Catalog services.

**AD DS Installation**

![AD DS Installation](screenshots/09-ADDS-Installation.png)

**Domain Configuration**

![Active Directory Domain Configuration](screenshots/10-Active-Directory-Domain-Configuration.png)

**Active Directory Domain**

![Active Directory Users and Computers](screenshots/14-Active-Directory-Domain.png)

### 3. Organizational Units and User Administration

Created a Corporate Organizational Unit containing departmental OUs for IT, Human Resources, Finance, Sales, Workstations, and Servers.

Created fictional employee accounts and configured account logon settings.

**Organizational Units**

![Organizational Units](screenshots/15-Organizational-Units.png)

**IT User Accounts**

![IT User Accounts](screenshots/16-IT-User-Accounts.png)

**User Account Properties**

![User Account Properties](screenshots/17-User-Account-Properties.png)

### 4. Security Group Management

Created departmental global security groups and assigned employees to their corresponding groups.

Practiced managing group membership through Active Directory Users and Computers.

**Security Group**

![Security Groups](screenshots/18-AD-Security-Groups.png)

**Group Membership**

![Group Membership](screenshots/19-Security-Group-Membership.png)

### 5. Group Policy Configuration

Created and linked a Group Policy Object named `Workstation Security Policy` to the Workstations OU.

Configured a 900-second (15-minute) inactivity limit for domain-joined workstations.

**Group Policy Object**

![Group Policy Object](screenshots/20-Group-Policy-Object.png)

**Security Policy Configuration**

![Workstation Security Policy](screenshots/21-Workstation-Security-Policy.png)

### 6. Windows Client Domain Integration

Installed Windows 11 Pro on a second VirtualBox VM named
