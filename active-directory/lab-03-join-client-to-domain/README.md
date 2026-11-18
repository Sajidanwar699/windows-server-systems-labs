# Lab 3: Joining a Windows Client to the Domain

> **Objective:** Join a Windows 7 client to the `Bkteam.com` domain and verify the membership.

## Prerequisites

Before starting, you need:

- A computer running windows 2012 server Domain Controller.

- A computer running windows 2012 server or windows 7.

In this lab, Windows Server 2012 R2 runs the domain controller for the `Bkteam.com` domain, and a Windows 7 client joins it.

## Environment

**General Information Windows Server 2012 R2**

| Setting | Value |
|---|---|
| Server Name | Win-Server2012 |
| Domain Name | Bkteam.com |
| Forest Name | Bkteam.com |
| IP Address | 192.168.31.128 |
| DNS Server (Preferred) | 192.168.31.128 |
| DNS Server of ADC (Alternative) | 192.168.31.138 |

**General Information Client Windows 7**

| Setting | Value |
|---|---|
| Computer Name | Win-7 |
| IP Address | 192.168.31.129 |
| DNS Server (Preferred) | 192.168.31.128 |
| DNS Server (Alternative) | 192.168.31.138 |

## Procedure

**Step 1.** Log in as Administrator to Workgroup Computer.

**Step 2.** Right click Computer Icon and click Properties and click Change settings.

![Procedure – step 2](images/01-step-2.png)

![Procedure – step 2](images/02-step-2.png)

**Step 3.** In the System properties dialog box click Change.

![Procedure – step 3](images/03-step-3.png)

**Step 4.** Select the Member of Domain and enter the Domain Name (Ex: Bkteam.com).

![Procedure – step 4](images/04-step-4.png)

**Step 5.** Enter the user’s name Administrator and Password, click OK.

![Procedure – step 5](images/05-step-5.png)

**Step 6.** Welcome Message appears indicating that the computer was successful in joining the Domain, click OK and OK, it will ask for restart, click Restart Now.

![Procedure – step 6](images/06-step-6.png)

![Procedure – step 6](images/07-step-6.png)

## Verification:

**Step 1.** Right click Computer Icon → Properties.

![Verification: – step 1](images/08-step-1.png)

**Step 2.** Click Computer Name, domain, and workgroup settings and verify for the Domain Name Bkteam.com.

![Verification: – step 2](images/09-step-2.png)

---
[← Lab 2](../lab-02-install-active-directory/) | [Active Directory](../README.md) | [Lab 4 →](../lab-04-ou-users-groups/)
