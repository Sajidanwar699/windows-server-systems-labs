# Lab 1: Backing Up Active Directory with Windows Server Backup

> **Objective:** Install Windows Server Backup and schedule a daily full-server backup of the domain controller.

**Step 1.** Click Server Manager.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 1](images/01-step-1.png)

**Step 2.** In Server Manager Dashboard, Click Add roles and features.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 2](images/02-step-2.png)

**Step 3.** In Before you begin page, click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 3](images/03-step-3.png)

**Step 4.** In Select installation type, select Role-based or feature-based installation, click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 4](images/04-step-4.png)

**Step 5.** In Select destination server from Server Pool select Win-Server 2012, click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 5](images/05-step-5.png)

**Step 6.** Then go next to Features. check the Windows Server Backup box and then click on Next

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 6](images/06-step-6.png)

**Step 7.** Click Install and then wait for the process to Finish.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 7](images/07-step-7.png)

**Step 8.** Wait for the installation of Windows Server Backup to complete and click Close.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 8](images/08-step-8.png)

**Step 9.** Now go to Server Manager select Tools > Windows Server Backup.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 9](images/09-step-9.png)

**Step 10.** Right click on Local Backup item in the left pane and select Backup Schedule.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 10](images/10-step-10.png)

**Step 11.** On Getting Started window, Click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 11](images/11-step-11.png)

**Step 12.** If you want to backup a file or a folder, you can click on custom file, but in this case, we want to take full backup of the server. So, we should click on the first option Full server (recommended) and then click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 12](images/12-step-12.png)

**Step 13.** We should do backup once in a day, so we will choose the first option and the appropriate time, and click Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 13](images/13-step-13.png)

**Step 14.** We can back up our DC to a dedicated backup volume, or a shared network folder. We are using a back up to a volume, and click next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 14](images/14-step-14.png)

**Step 15.** Add your volume where you want to take Back up.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 15](images/15-step-15.png)

**Step 16.** Select your Destination Volume (Ex: Backup E) and click OK.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 16](images/16-step-16.png)

**Step 17.** After select your destination volume for back up, Click on Next.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 17](images/17-step-17.png)

**Step 18.** Review the confirmation Press Finish to create a backup task.

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 18](images/18-step-18.png)

![Lab 1: Backing Up Active Directory with Windows Server Backup – step 18](images/19-step-18.png)

**Step 19.** Now you will get a window showing the status if the backup was created successfully.

## Verification

**Step 1.** Backup successfully Saved in Destination Volume.

![Verification – step 1](images/20-step-1.png)

---
[Backup and Recovery](../README.md)
