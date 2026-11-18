# Lab 5: Adding an Additional Domain Controller (Same Network)

> **Objective:** Add an additional domain controller to the existing domain on the same subnet for redundancy and load balancing.

In this lab we explain, step by step, how to install an additional domain controller in an existing active directory domain. Additional AD domain controller is used to balance the load among existing domain controllers. It also provides fault-tolerance that in case primary AD DC is down, additional AD DC can be used for authentications without any business discontinuity.

> **Important:** confirm the server details below match your environment.


**General Information Windows Server 2012 R2**

| Setting | Value |
|---|---|
| Server Name | Server2012-ADC |
| Domain Name | Bkteam.com |
| Forest Name | Bkteam.com |
| IP Address | 192.168.31.138 |
| DNS Server (Preferred) | 192.168.31.138 |
| DNS Server (Alternative) | 192.168.31.128 |

## Network Topology

![Network Topology – figure 1](images/01-figure.png)

## Installing Active Directory Domain Services

**Step 1.** Open Server Manager dashboard from task bar and click Add roles and features

![Installing Active Directory Domain Services – step 1](images/02-step-1.png)

**Step 2.** Cross check the important notes Before you begin and click Next

![Installing Active Directory Domain Services – step 2](images/03-step-2.png)

**Step 3.** In Select installation type Choose Role-based or feature-based installation and click Next

![Installing Active Directory Domain Services – step 3](images/04-step-3.png)

**Step 4.** Choose a desired destination server (Ex: Server2012-ADC) from server pool you want to configure it as additional domain controller and click Next

![Installing Active Directory Domain Services – step 4](images/05-step-4.png)

**Step 5.** Choose Active Directory Domain Services from roles.

![Installing Active Directory Domain Services – step 5](images/06-step-5.png)

**Step 6.** As soon as you check the box, a small window will pop up prompting you to install other necessary features along with Active Directory Domain Services. Click Add Features

![Installing Active Directory Domain Services – step 6](images/07-step-6.png)

**Step 7.** In Select features wizard, click Next.

![Installing Active Directory Domain Services – step 7](images/08-step-7.png)

**Step 8.** Read related Active Directory Domain Services note and click Next

![Installing Active Directory Domain Services – step 8](images/09-step-8.png)

**Step 9.** Confirm your installation selections and click Install

![Installing Active Directory Domain Services – step 9](images/10-step-9.png)

**Step 10.** It takes a while before an installation completes, click Promote this server to a domain controller.

![Installing Active Directory Domain Services – step 10](images/11-step-10.png)

**Step 11.** Choose Add a domain controller to an existing domain. Provide a domain name and click Select. A security window will pop up, provide user name in the format <domain>\<username> (Ex: Bkteam.com\Administrator) and password. When done, click OK. Choose the domain from forest and click OK. Click Next

![Installing Active Directory Domain Services – step 11](images/12-step-11.png)

**Step 12.** Provide Directory Service Restore Mode (DSRM) password and click Next

**Step 13.** On DNS Options page, Ignore the warning and click Next

![Installing Active Directory Domain Services – step 13](images/13-step-13.png)

**Step 14.** Select your primary DC FQDN name (Ex: Win-Server2012.Bkteam.com) and Click Next

![Installing Active Directory Domain Services – step 14](images/14-step-14.png)

**Step 15.** Verify the location of the AD DS database, log files, and SYSVOL, click Next.

![Installing Active Directory Domain Services – step 15](images/15-step-15.png)

**Step 16.** Review the summary and click Next

![Installing Active Directory Domain Services – step 16](images/16-step-16.png)

**Step 17.** After successfully checking pre-requisite Click Install to begin installation. Installation will begin and take few minutes to complete. After a successful configuration, click Close and server will be rebooted.

![Installing Active Directory Domain Services – step 17](images/17-step-17.png)

## Verification

The additional domain controller (ADC) is now configured and listed in the domain.

![Verification – step 1](images/18-step-1.png)

![Verification – step 1](images/19-step-1.png)

The additional domain controller is ready. You can add more backup domain controllers by repeating the same steps.

---
[← Lab 4](../lab-04-ou-users-groups/) | [Active Directory](../README.md) | [Lab 6 →](../lab-06-additional-dc-different-network/)
