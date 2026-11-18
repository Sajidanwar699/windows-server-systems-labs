# Active Directory

Build and manage the **Bkteam.com** domain: installing the first domain controller, joining clients, managing users and groups, adding domain controllers and recovering FSMO roles.

## Lab environment

| Item | Details |
|------|---------|
| Domain | `Bkteam.com` (NetBIOS name: `BKTEAM`) |
| Server OS | Windows Server 2012 R2 |
| Client OS | Windows 7 / Windows 10 |
| Virtualization | VMware Workstation Pro 16 (GNS3 VM for Lab 6) |
| Primary DC | `Win-Server2012` |
| Additional DC | `Server2012-ADC` |

## Labs

| Lab | Title | Skills demonstrated |
|-----|-------|---------------------|
| – | [Fundamentals](fundamentals/) | Concepts, DC types, replication, FSMO roles |
| 1 | [Assign a static IP address](lab-01-static-ip-address/) | IPv4 and DNS configuration |
| 2 | [Install and configure Active Directory](lab-02-install-active-directory/) | AD DS role, new forest, DC promotion |
| 3 | [Join a client to the domain](lab-03-join-client-to-domain/) | Domain join and verification |
| 4 | [OUs, users and groups](lab-04-ou-users-groups/) | ADUC, account and group management |
| 5 | [Additional domain controller (same network)](lab-05-additional-dc-same-network/) | Redundancy and replication |
| 6 | [Additional domain controller (different network)](lab-06-additional-dc-different-network/) | Multi-subnet design, GNS3, Cisco router |
| 7 | [Seize FSMO roles](lab-07-seize-fsmo-roles/) | Disaster recovery with ntdsutil |

[← Back to the main page](../README.md)
