# Adding the Domain services role to the Server 2022

## Overview 
---
This write-up outlines the procedure for adding Active Directory Domain Services to the Windows Server 2022 virtual machine.

>[!note]
>#### Process
>- Configure the server’s network settings by assigning a static IP address and changing the PC name
>- Install Active Directory Domain Services
>- Configure the domain controller account and complete post-deployment configurations



### Procedure 
---

1. Changing the IP address ---> Control Panel ---> large icons ---> network and sharing center ---> Ethernet0 ---> properties ---> Internet Protocol Version 4 ---> Select the options `use the following IP address`  and `use the following DNS server Addresses`

![](../Attachments/Pasted%20image%2020260204201329.png)

![](../Attachments/Pasted%20image%2020260204201430.png)

![](../Attachments/Pasted%20image%2020260204201533.png)


![](../Attachments/Pasted%20image%2020260204201957.png)

2. Changing the workstation name ---> Settings -> System -> about -> Rename This PC

![](../Attachments/Pasted%20image%2020260204202457.png)

3. Go to the server manager ---> Manage Add Roles and features ---> Click Next for the Next 3 pages

![](../Attachments/Pasted%20image%2020260204200347.png)

![](../Attachments/Pasted%20image%2020260204200358.png)

![](../Attachments/Pasted%20image%2020260204200457.png)

![](../Attachments/Pasted%20image%2020260204200545.png)


3. Select the `Active Directory Domain Services` ---> Click Add features on the Popup Box ---> Select the DNS Server ---> Click Add features on the Popup Box ---> Click Next 4 Times ---> Click Install

![](../Attachments/Pasted%20image%2020260204203023.png)

![](../Attachments/Pasted%20image%2020260204203100.png)


![](../Attachments/Pasted%20image%2020260204203422.png)

![](../Attachments/Pasted%20image%2020260204203444.png)


![](../Attachments/Pasted%20image%2020260204203523.png)

4. Once the installation is complete ---> Click Close 

![](../Attachments/Pasted%20image%2020260204203734.png)

7. Now the Post deployment Configuration , proceed to click on the Flag icon ---> Click on Promote this server to a Domain Controller

![](../Attachments/Pasted%20image%2020260204203901.png)

8. Click on Add a new forest and add a root domain name ---> Click next 

![](../Attachments/Pasted%20image%2020260204204048.png)

7. Add the DSRM password which is used when the AD service is no longer running or Failed 

![](../Attachments/Pasted%20image%2020260204211940.png)


8. Uncheck create DNS Delegation ---> proceed to Verify the NETBIOSNAME

![](../Attachments/Pasted%20image%2020260204212829.png)

![](../Attachments/Pasted%20image%2020260204212907.png)


9. Verify the Paths and review Changes 

![](../Attachments/Pasted%20image%2020260204213126.png)

10. Click install to apply the changes 

![](../Attachments/Pasted%20image%2020260204213336.png)


