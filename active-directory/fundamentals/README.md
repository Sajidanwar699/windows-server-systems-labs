# Active Directory Fundamentals

## Prerequisites

Before installing Active Directory Domain Services, make sure you have:

- An NTFS partition with enough free space
- An Administrator username and password
- A supported operating system (Windows Server 2008 / 2012 / 2016 / 2019)
- A network interface card (NIC) with properly configured TCP/IP (IP address, subnet mask and, optionally, a default gateway)
- A working network connection
- An operational DNS server (it can be installed on the DC itself)
- The domain name you want to use

## Hardware requirements (domain controller)

| Component | Recommendation |
|---|---|
| Storage / database size | 40 KB to 60 KB per user |
| RAM | Base operating system recommendation plus third-party applications |
| Network | 1 Gbps |
| CPU | 1,000 concurrent users per core |

## Lab scenario

| Item | Details |
|---|---|
| Virtualization platform | VMware Workstation Pro 16.0.0 (build 16894299) |
| Server OS | Windows Server 2012 R2 |
| Client OS | Windows 7 and Windows 10 |

## Active Directory

Active Directory is a centralized authentication and directory service based around standards such as the Lightweight Directory Access Protocol (LDAP) and Kerberos. It stores information about user accounts, groups, distribution lists as well as information for directory enabled applications such as Microsoft Exchange Server.

The forest acts as a security boundary for an organization and defines the scope of authority for administrators. By default, a forest contains a single domain, which is known as the forest root domain however additional domains can be created in the forest.

**General Information**

| Setting | Value |
|---|---|
| Server Name | Win-Server2012 |
| Domain Name | Bkteam.com |
| Forest Name | Bkteam.com |
| NetBIOS Name | BKTEAM |
| OS Version | Windows Server 2012 R2 |
| Domain Functional Level | Windows Server 2012 R2 |
| Forest Functional Level | Windows Server 2012 R2 |
| Time Zone | (UTC+05:00) Islamabad, Karachi |

## Recommendations

- Keep AD as simple as possible. It will help in improving efficiency, and it will make the troubleshooting process easier whenever problems arise.

- Use the appropriate site topology.

## Basic terminology

| Term | Definition |
|---|---|
| **Domain Controller** | This is a server that is running the Active Directory Domain Services Role. It is recommended to have multiple domain controllers for failover reasons. |
| **Domain** | The domain is a logical structure of containers and objects within Active Directory. It is a hierarchical structure for users, groups, computers, and other objects. |
| **Domain Tree** | When you add a child domain to a parent domain you create what is called a domain tree. A domain tree is just a series of domains connected together in a hierarchical fashion all using the same DNS namespace. |
| **Functional Levels** | Functional levels determine what capabilities are available in the domain. Higher functional levels allow you to use the latest and greatest technologies in your Active Directory domain. |
| **Forest** | A forest is a collection of domain trees. The domain tree shares a common schema and configuration container. The domain tree is connected together through a transitive trust. When you first install Active Directory and create a domain you are also creating a forest. |
| **Organizational Unit** | An OU is a container object that can contain different objects from the same domain. You will use OUs to store and organize, user accounts, contacts, computers, and groups. You will also link group policy objects to an OU. |
| **Users** | User accounts are assigned to primarily assigned to users to gain access to domain resources. They can also be used to run programs or system services. |
| **Groups** | Groups are used to collect users accounts, computer and contact objects into management units. Creating groups makes it easier to control permissions to resources and assign resources such as printers and folders. There are two types of objects groups, a Security group, and a distribution group. A security group is a grouping of users accounts that can be used to provide access to resources. Distribution groups are used for email distribution lists. |

## Domain and domain controller types

### Domain

Definition: A domain is a logical grouping of computers, users, and resources in a network. It's a boundary within which security policies are applied, and authentication and authorization are managed centrally by domain controllers.

Example: Imagine a company named "Example Corp." They have a domain called "example.com" where all their network resources such as user accounts, computers, printers, and shared files are managed.

### Domain Controller (DC)

Definition: A domain controller is a server that authenticates users, stores security policies, and maintains the Active Directory database for a domain.

Example: In the "example.com" domain of Example Corp., they have a server named "DC1" which acts as the primary domain controller, managing user logins, group policies, and other domain-related tasks.

### Additional Domain Controller (ADC)

Definition: An additional domain controller is a server that replicates the Active Directory database from a primary domain controller, providing redundancy and load distribution for authentication requests.

Example: Example Corp. sets up another server named "ADC1" as a secondary domain controller to support DC1. ADC1 helps handle authentication requests and replicates the Active Directory database from DC1.

### Read-Only Domain Controller (RODC)

Definition: A read-only domain controller is a specialized domain controller that holds a read-only copy of the Active Directory database. It's typically deployed in branch offices or locations with limited physical security.

Example: In "ABC Corp," if there's a branch office with fewer IT resources and lower physical security, an RODC might be deployed there. Employees can still authenticate and access resources, but the RODC ensures that sensitive data isn't compromised if the server is physically accessed.

### Child Domain Controller (CDC)

Definition: A child domain controller is a server that is part of a subdomain (child domain) within a larger domain hierarchy. It has its own Active Directory database but can also replicate data from parent domains.

Example: Example Corp. expands its operations globally and creates a child domain named "asia.example.com" for its offices in Asia. They set up a domain controller named "DC-Asia" within this child domain to manage local resources while still being able to replicate data from the parent domain "example.com".

In summary, a domain is the overall logical structure of a network, while domain controllers such as DCs, ADCs, RODCs, and CDCs are servers responsible for managing authentication, security policies, and directory services within that domain. Each type of domain controller serves specific roles and purposes within the Active Directory infrastructure of an organization.

- Domain is the overall organization.

- DC manages authentication within that organization.

- ADC assists the DC in managing authentication and provides redundancy.

- RODC is a specialized DC that holds a read-only copy of the database.

- CDC is a DC in a sub-domain within the larger domain structure.

## Replication: inbound vs outbound

In a Windows Server environment, replication refers to the process of synchronizing data between domain controllers (DCs) within an Active Directory (AD) forest. There are two main types of replications: inbound replication and outbound replication.

### Inbound replication

Definition: Inbound replication refers to the process by which a domain controller receives updates and changes from other domain controllers within the same domain or forest.

Example: Let's say you have a domain controller (DC1) and a Read-Only Domain Controller (RODC) in a domain. When changes occur on other domain controllers, such as attribute modifications, password changes, or group membership updates, DC1 and RODC receive these changes through inbound replication.

### Outbound replication

Definition: Outbound replication refers to the process by which a domain controller sends updates and changes to other domain controllers within the same domain or forest.

Example: Continuing from the previous example, if DC1 receives updates or changes to the Active Directory database, it will replicate these changes to other domain controllers in the domain, such as the RODC.

## FSMO roles in an ADC vs a CDC

In an Active Directory environment, FSMO (Flexible Single Master Operations) roles are critical operations that must be performed in a distributed environment like Active Directory Domain Services (AD DS). These roles are essential for the proper functioning of the Active Directory infrastructure. There are two types of FSMO roles: domain-wide roles and forest-wide roles. When considering Child Domain Controllers (CDCs) and Additional Domain Controllers (ADCs), the FSMO roles they hold are relevant to their domain's hierarchy and the overall forest.

#### Child Domain Controller (CDC)

FSMO roles held by a CDC are specific to the child domain it belongs to. Each child domain in an Active Directory Forest has its own set of FSMO roles. These roles include:

RID Master: Responsible for allocating RIDs (Relative Identifiers) to domain controllers in the child domain to create objects.

PDC Emulator: Handles password changes within the child domain and time synchronization.

Infrastructure Master: Maintains references to objects in other domains for this domain.

The Schema Master and Domain Naming Master roles, which are forest-wide roles, are not held by any domain controller in a child domain by default. They are typically located at the forest root domain level.

#### Additional Domain Controller (ADC)

FSMO roles held by an ADC can vary. By default, when you add an additional domain controller to an existing domain, it doesn't automatically inherit FSMO roles. These roles are usually assigned to domain controllers during the initial deployment of Active Directory.

If needed, FSMO roles can be transferred or seized onto additional domain controllers based on administrative requirements. The roles held by an ADC could include any of the five FSMO roles, depending on how the Active Directory environment is configured.

In summary, FSMO roles for a Child Domain Controller (CDC) are specific to the child domain it belongs to, while for an Additional Domain Controller (ADC), the roles it holds can vary and depend on administrative decisions regarding role placement and management in the Active Directory Forest.

---
[Active Directory](../README.md) | [Lab 1 →](../lab-01-static-ip-address/)
