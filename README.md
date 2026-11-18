# Windows Server Systems Labs

Hands-on Windows Server labs with step-by-step instructions and screenshots, organised by topic.

![Windows Server](https://img.shields.io/badge/Windows%20Server-2012%20R2-0078D6?logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active%20Directory-7%20labs-005A9E)
![Sections](https://img.shields.io/badge/Sections-4-2E9E6B)

> The domain `Bkteam.com` and all names and IP addresses are lab-only examples from a private environment.

## Sections and labs

| Section | Lab | Title | Skills demonstrated |
|---------|-----|-------|---------------------|
| [Active Directory](active-directory/) | 1 | [Assign a static IP address](active-directory/lab-01-static-ip-address/) | IPv4 and DNS configuration |
| [Active Directory](active-directory/) | 2 | [Install and configure Active Directory](active-directory/lab-02-install-active-directory/) | AD DS role, new forest, DC promotion |
| [Active Directory](active-directory/) | 3 | [Join a client to the domain](active-directory/lab-03-join-client-to-domain/) | Domain join and verification |
| [Active Directory](active-directory/) | 4 | [OUs, users and groups](active-directory/lab-04-ou-users-groups/) | ADUC, account and group management |
| [Active Directory](active-directory/) | 5 | [Additional domain controller (same network)](active-directory/lab-05-additional-dc-same-network/) | Redundancy and replication |
| [Active Directory](active-directory/) | 6 | [Additional domain controller (different network)](active-directory/lab-06-additional-dc-different-network/) | Multi-subnet design, GNS3, Cisco router |
| [Active Directory](active-directory/) | 7 | [Seize FSMO roles](active-directory/lab-07-seize-fsmo-roles/) | Disaster recovery with ntdsutil |
| [Backup and Recovery](backup-and-recovery/) | 1 | [Back up Active Directory](backup-and-recovery/lab-01-backup-active-directory/) | Windows Server Backup |
| [Group Policy](group-policy/) | 1 | [Restrict access to Control Panel](group-policy/lab-01-restrict-control-panel/) | GPO creation, linking and testing |
| [Web Server (IIS)](web-server-iis/) | 1 | [IIS and WordPress web server](web-server-iis/lab-01-iis-wordpress/) | IIS 8.5, PHP, MySQL, phpMyAdmin, WordPress |

New to Active Directory? Start with the [fundamentals](active-directory/fundamentals/).

## Repository structure

```
.
├── active-directory/        Fundamentals, Labs 1-7
├── backup-and-recovery/     Lab 1
├── group-policy/            Lab 1
├── web-server-iis/          Lab 1
└── templates/               Template for adding new labs
```

## Lab environment

| Item | Details |
|------|---------|
| Servers | Windows Server 2012 R2 |
| Clients | Windows 7 / Windows 10 |
| Virtualization | VMware Workstation Pro 16 |
| Network simulation | GNS3 with a Cisco c3725 router (Active Directory Lab 6) |

## Certifications

| Certification | Vendor |
|---------------|--------|
| MCSA (2016), MCSE (2021) | Microsoft |
| Azure Administrator Associate (AZ-103) | Microsoft |
| Azure Network Engineer Associate (AZ-700) | Microsoft |
| CCNA, Routing & Switching | Cisco |
| Cisco Certified Specialist, Enterprise Core (350-401 ENCOR) | Cisco |
| Certified Network Security Specialist (CNSS) | ICSI |
