# Adding the computers to the Domain

## Overview 
---
In this write-up, we will add a Windows 11 Pro PC to the domain. Before joining the domain, the system will be configured with the required IP settings. Once added to the domain, we will manage the computer account by disabling and re-enabling the system, and observe the different outputs produced when the account or the system is disabled.

### Procedure 
---
#### Configuring the IP address on PC01

1. Go to the network and sharing Center in the control panel ---> Select Etherenet 0 ---> Go toproperties ---> Internet Protocol Version 4 ---> Select the options `use the following IP address`  and `use the following DNS server Addresses`

![](../Attachments/Pasted%20image%2020260207174646.png)




#### Joining the PC to the domain

1. Go to the settings ---> System ----> About ----> Domain or workgroup ---> Click on Change ---> 

![](../Attachments/Pasted%20image%2020260207105551.png)

![](../Attachments/Pasted%20image%2020260207105740.png)

2. Enter the following details ---> once that is done ---> Enter the account information

![](../Attachments/Pasted%20image%2020260207110207.png)

![](../Attachments/Pasted%20image%2020260207174953.png)

3. Once you Enter the account name you will have to restart the computer 

#### Disabling the Computer from the network

1. To Disable the computer  from the network we will right click on the computer and disable the computer 

![](../Attachments/Pasted%20image%2020260207191752.png)

![](../Attachments/Pasted%20image%2020260207191819.png)


### O/P screens on the various issues

1. Disabled Workstation `PC01`

![](../Attachments/Pasted%20image%2020260207192213.png)

2. Disabled user screen 

![](../Attachments/Pasted%20image%2020260207192457.png)


3. Password Locked due to incorrect attempts screen 

![](../Attachments/Pasted%20image%2020260207203431.png)




