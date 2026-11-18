# Lab 1: Assigning a Static IP Address to a Server

> **Objective:** Assign a static IPv4 address and preferred DNS server to a Windows Server 2012 R2 machine before promoting it to a domain controller.

**Step 1.** Click Server Manager.

![Lab 1: Assigning a Static IP Address to a Server – step 1](images/01-step-1.png)

**Step 2.** In Server Manager Dashboard, Click Configure this local server.

![Lab 1: Assigning a Static IP Address to a Server – step 2](images/02-step-2.png)

**Step 3.** In Local Server, select Ethernet IPv4 address assigned by DHCP.

![Lab 1: Assigning a Static IP Address to a Server – step 3](images/03-step-3.png)

**Step 4.** Right click Ethernet, select Properties.

![Lab 1: Assigning a Static IP Address to a Server – step 4](images/04-step-4.png)

**Step 5.** Select Internet Protocol Version 6 (TCP/IPv6) and uncheck the box.

**Step 6.** Select Internet Protocol Version 4 (TCP/IPv4) and click Properties.

![Lab 1: Assigning a Static IP Address to a Server – step 6](images/05-step-6.png)

**Step 7.** Select Use the following IP address and enter the IP address and click Subnet mask, it will be entered automatically and select Use the DNS Server addresses and enter the Preferred DNS Server address and Click OK and OK.

![Lab 1: Assigning a Static IP Address to a Server – step 7](images/06-step-7.png)

---
[← Fundamentals](../fundamentals/) | [Active Directory](../README.md) | [Lab 2 →](../lab-02-install-active-directory/)
