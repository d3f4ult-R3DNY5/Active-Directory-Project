# Performing and AD backup and restore
## Overview 
---
This phase involves backing up the contents of Active Directory to ensure that critical domain data can be restored in the event of a system failure, crash, or corruption. The backup process protects important components such as user accounts, group policies, organizational units, and other domain configurations. By performing regular backups, the domain controller can be recovered to a previous stable state, helping maintain business continuity and minimize downtime.

### Procedure 
---
1. Open **Server Manager** ---> Select **Add Roles and Features** --->Install the **Network Load Balancing** feature ---> Then, Install the **Windows Server Backup** feature

![](../Attachments/Pasted%20image%2020260212095417.png)

2. Create a network share named **Backups** under **File and Storage Services** ---> **Shares** in **Server Manager**

![](../Attachments/Pasted%20image%2020260212104547.png)

3. Under the Tools Section ---> open the Windows Server Backups ---> Click on Backup Once ---> perform the Configuration as per the images below 

![](../Attachments/Pasted%20image%2020260212101711.png)

![](../Attachments/Pasted%20image%2020260212103203.png)

![](../Attachments/Pasted%20image%2020260212103240.png)

![](../Attachments/Pasted%20image%2020260212103303.png)

![](../Attachments/Pasted%20image%2020260212103354.png)

![](../Attachments/Pasted%20image%2020260212103409.png)

![](../Attachments/Pasted%20image%2020260212110603.png)


#### Performing a Restore 
---
1. Go to system config and Perform the following Configurations

![](../Attachments/Pasted%20image%2020260212110905.png)

2. Go to command Prompt and perform the following

![](../Attachments/Pasted%20image%2020260212111229.png)

![](../Attachments/Pasted%20image%2020260212111450.png)

![](../Attachments/Pasted%20image%2020260212111518.png)

![](../Attachments/Pasted%20image%2020260212111603.png)

![](../Attachments/Pasted%20image%2020260212112423.png)







