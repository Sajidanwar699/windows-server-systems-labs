# Lab 2: Installing and Configuring Active Directory

> **Objective:** Install the Active Directory Domain Services role and promote the server to the first domain controller of a new forest, `Bkteam.com`.

**Step 1.** Log in as Administrator to the Workgroup Computer.

**Step 2.** Assign IP Address and preferred DNS Server Address.

**Step 3.** Click Server Manager.

![Lab 2: Installing and Configuring Active Directory – step 3](images/01-step-3.png)

**Step 4.** In Server Manager Dashboard, Click Add roles and features.

![Lab 2: Installing and Configuring Active Directory – step 4](images/02-step-4.png)

**Step 5.** In Before you begin page, click Next.

![Lab 2: Installing and Configuring Active Directory – step 5](images/03-step-5.png)

**Step 6.** In Select installation type, select Role-based or feature-based installation, click Next.

![Lab 2: Installing and Configuring Active Directory – step 6](images/04-step-6.png)

**Step 7.** In Select destination server from Server Pool select Win-Server 2012, click Next.

![Lab 2: Installing and Configuring Active Directory – step 7](images/05-step-7.png)

**Step 8.** In Roles, check the box Active Directory Domain Services.

![Lab 2: Installing and Configuring Active Directory – step 8](images/06-step-8.png)

**Step 9.** Click Add Features, to install the required features for Active Directory Domain Services. Click Next.

![Lab 2: Installing and Configuring Active Directory – step 9](images/07-step-9.png)

**Step 10.** In Select features wizard, click Next.

![Lab 2: Installing and Configuring Active Directory – step 10](images/08-step-10.png)

**Step 11.** In Active Directory Domain Services wizard, click Next.

![Lab 2: Installing and Configuring Active Directory – step 11](images/09-step-11.png)

**Step 12.** Check the box Restart the destination server automatically if required. Click Install.

![Lab 2: Installing and Configuring Active Directory – step 12](images/10-step-12.png)

**Step 13.** Click Promote this server to a domain controller.

![Lab 2: Installing and Configuring Active Directory – step 13](images/11-step-13.png)

**Step 14.** In Deployment Configuration wizard, select Add a new forest, enter the Root domain name (Ex: Bkteam.com) and click Next

![Lab 2: Installing and Configuring Active Directory – step 14](images/12-step-14.png)

**Step 15.** In Domain Controller Options, change Forest and Domain functional level to Windows Server 2012 R2, and Domain Name System server. Type the Directory Services Restore Mode Password and Confirm password and click Next.

![Lab 2: Installing and Configuring Active Directory – step 15](images/13-step-15.png)

**Step 16.** On DNS Options page, click Next.

![Lab 2: Installing and Configuring Active Directory – step 16](images/14-step-16.png)

**Step 17.** Verify the NetBIOS domain name (Ex: BKTEAM), click Next.

![Lab 2: Installing and Configuring Active Directory – step 17](images/15-step-17.png)

**Step 18.** Verify the location of the AD DS database, log files, and SYSVOL, click Next.

![Lab 2: Installing and Configuring Active Directory – step 18](images/16-step-18.png)

**Step 19.** Review the Summary and click Next.

![Lab 2: Installing and Configuring Active Directory – step 19](images/17-step-19.png)

**Step 20.** After successfully checking pre-requisite Click Install to begin installation.

![Lab 2: Installing and Configuring Active Directory – step 20](images/18-step-20.png)

## Verification of Active Directory Domain Controller

**Step 1.** Click Server Manager.

![Verification of Active Directory Domain Controller – step 1](images/19-step-1.png)

**Step 2.** In Server Manager, select Local Server, verify for Domain Bkteam.com

![Verification of Active Directory Domain Controller – step 2](images/20-step-2.png)

---
[← Lab 1](../lab-01-static-ip-address/) | [Active Directory](../README.md) | [Lab 3 →](../lab-03-join-client-to-domain/)
