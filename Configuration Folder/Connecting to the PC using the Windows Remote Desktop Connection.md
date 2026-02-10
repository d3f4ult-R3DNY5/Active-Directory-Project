# Connecting to the PC using the Windows Remote Desktop Connection

## Overview 
---
This Phase involves connecting to the remote PC using the windows remote desktop connection . This Works on the RDP protocol which operates on the **TCP Port 3389**

### Procedure 
---
1. Add the Remote Desktop users which in this case is the `IT admins group` who are allowed to access **PC01** via **Settings** ---> **System** ---> **Remote Desktop**

![](../Attachments/Pasted%20image%2020260210093734.png)


![](../Attachments/Pasted%20image%2020260210094432.png)




2. Go to the **Domain Controller** ---> Log in as user `JColby` ---> Open **Remote Desktop Connection** ---> Enter the IP address of the target computer, which in this case is **PC01** (`192.168.20.3`)

![](../Attachments/Pasted%20image%2020260210093310.png)

3. The output will be like the image given below 

#### On the Domain Controller 

![](../Attachments/Pasted%20image%2020260210094607.png)

#### On PC01

![](../Attachments/Pasted%20image%2020260210094712.png)


