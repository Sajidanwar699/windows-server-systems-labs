# Lab 1: Creating a GPO to Restrict Access to Control Panel

> **Objective:** Create and link a Group Policy Object that prevents domain users from opening Control Panel.

**Step 1.** Open run and type gpmc.msc enter OK select the GPO to which you will add the policy.

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 1](images/01-step-1.png)

**Step 2.** Create a new group policy.

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 2](images/02-step-2.png)

**Step 3.** Enter a name for the new group policy (Ex: Prevent Access Control Panel GPO)

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 3](images/03-step-3.png)

**Step 4.** On the Group Policy Management screen, expand the folder named Group Policy Objects and Right-click your new Group Policy Object (Ex: Prevent Access Control Panel GPO) and select the Edit option.

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 4](images/04-step-4.png)

**Step 5.** On the group policy editor screen, expand the User configuration folder and locate the following item and open the GPO named Prohibit access to Control Panel and PC settings. User Configuration > Policies > Administrative Templates > Control Panel

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 5](images/05-step-5.png)

**Step 6.** Enable the item named Prohibit access to Control Panel and PC settings and click on Apply and OK.

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 6](images/06-step-6.png)

**Step 7.** On the Group policy management screen, Right-click the Domain / Organizational Unit desired and select the option to link an existent GPO.

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 7](images/07-step-7.png)

**Step 8.** In our example, we are going to link the group policy named Prevent Access Control Panel GPO to the root of the domain (Bkteam.com).

![Lab 1: Creating a GPO to Restrict Access to Control Panel – step 8](images/08-step-8.png)

After applying the GPO, you need to wait for 10 or 20 minutes or run the command in Run (gpupdate /force) to take effect immediately.

## Verification

**Step 1.** Login On a remote computer via domain user.

![Verification – step 1](images/09-step-1.png)

**Step 2.** Try to access the Control panel you will get a message of restriction.

![Verification – step 2](images/10-step-2.png)

In our example, we have successfully implemented GPO to prevent access to the Control Panel.

---
[Group Policy](../README.md)
