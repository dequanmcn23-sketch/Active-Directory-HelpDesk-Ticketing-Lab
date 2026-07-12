# Active-Directory-HelpDesk-Ticketing-Lab

## Overview

This project demonstrates the creation of a virtual IT Help Desk environment using VirtualBox. The lab simulates a real-world business network where a Windows Server 2019 Domain Controller manages users through Active Directory, an Ubuntu Server hosts the osTicket help desk platform, and a Windows 11 client joins the domain to simulate an employee workstation.

The purpose of this project was to gain hands-on experience with common IT Support and Help Desk responsibilities including Active Directory administration, user account management, password resets, domain management, ticket handling, and network troubleshooting.

---

## Technologies Used

* VirtualBox
* Windows Server 2019
* Active Directory Domain Services (AD DS)
* DNS
* Windows 11
* Ubuntu Server
* Apache
* MySQL
* PHP
* osTicket
* Git
* GitHub

---

## Skills Demonstrated

* Virtual machine deployment
* Active Directory installation and configuration
* Domain Controller configuration
* Organizational Unit (OU) creation
* User and Security Group management
* Password reset and account unlock procedures
* Windows 11 domain joining
* Ubuntu Server administration
* Apache web server deployment
* MySQL database administration
* PHP configuration
* osTicket installation and configuration
* Network troubleshooting
* DNS troubleshooting
* Help Desk documentation
* Technical documentation using GitHub

---

## Lab Environment

| Machine             | Hostname | Role                    | IP Address     |
| ------------------- | -------- | ----------------------- | -------------- |
| Windows Server 2019 | DC01     | Domain Controller / DNS | 192.168.10.10  |
| Ubuntu Server       | OSTICKET | Web Server / osTicket   | 192.168.10.20  |
| Windows 11          | CLIENT01 | Domain Client           | 192.168.10.100 |

---

## Virtual Network

```text
                     Internet
                         │
                     VirtualBox NAT
                         │
────────────────────────────────────────────
          Internal Network (HelpDeskLab)
────────────────────────────────────────────
          │              │              │
     Windows Server   Ubuntu       Windows 11
         DC01         OSTICKET      CLIENT01
    192.168.10.10   192.168.10.20 192.168.10.100
```

---

## Active Directory Configuration

The Domain Controller was configured with the domain:

```
helpdesk.local
```

Organizational Units:

* Users
* Groups
* Computers
* Sales
* IT
* Managers
* HelpDesk

Security Groups:

* Sales
* Managers
* IT-Admins
* HelpDesk-Team
* Password-Reset-Technicians

Example Users:

| User          | Department |
| ------------- | ---------- |
| John Smith    | Sales      |
| Sarah Jones   | Managers   |
| Mike Brown    | IT         |
| Alex Wilson   | HelpDesk   |
| Robert Taylor | Sales      |

---

## Windows 11 Client

The Windows 11 virtual machine was configured with a static IP address and successfully joined to the **helpdesk.local** domain using Active Directory.

Users were able to authenticate using domain credentials instead of local accounts.

---

## Ubuntu Server

Ubuntu Server was configured with:

* Static IP Address
* Apache Web Server
* MySQL Server
* PHP
* OpenSSH
* osTicket

The osTicket application was connected to a dedicated MySQL database and configured as the organization's internal Help Desk ticketing platform.

---

## Help Desk Scenarios

This lab includes several common Help Desk support scenarios:

* Password Reset
* Account Unlock
* Printer Troubleshooting
* Network Connectivity Issues
* DNS Resolution Problems
* Slow Computer Troubleshooting
* Software Installation
* User Account Creation
* Group Membership Management

Each issue was documented from problem identification through resolution.

---

## Repository Structure

```
home-helpdesk-ticketing-lab/

├── README.md
│
├── docs/
│   ├── setup-guide.md
│   ├── active-directory.md
│   ├── ubuntu-server.md
│   ├── windows11-client.md
│   ├── osticket.md
│   └── troubleshooting-runbook.md
│
├── screenshots/
│   ├── active-directory/
│   ├── ubuntu/
│   ├── windows11/
│   ├── osticket/
│   └── troubleshooting/
│
├── tickets/
│   ├── password-reset.md
│   ├── account-lockout.md
│   ├── network-issue.md
│   ├── printer-issue.md
│   └── slow-computer.md
│
└── build-notes.md
```

---

## Lessons Learned

Building this lab provided practical experience with technologies commonly used in enterprise IT environments. It strengthened my understanding of Active Directory administration, virtualization, Windows and Linux server management, help desk ticket workflows, and technical documentation.

---

## Future Improvements

* Integrate Active Directory authentication with osTicket
* Configure Group Policy Objects (GPOs)
* Deploy a File Server
* Configure Shared Network Drives
* Implement DHCP
* Add WSUS for Windows Updates
* Deploy Microsoft Entra ID (Azure AD)
* Expand the lab into a hybrid cloud environment

---
