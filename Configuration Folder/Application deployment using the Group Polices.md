# Application deployment using the Group Polices

## Overview 
---
This writeup explains the process of deploying applications using the Group Policy Management Console. It covers sharing the folder where the application is stored so that the application can be accessed, and then deploying the policy from that shared location to ensure all designated users can install and use the application.

## Procedure 
---
#### Configuring the Share 

1. Create a folder named `Applications` inside the `Resources` directory, and place the 7-Zip MSI installer in this folder 

![](../Attachments/Pasted%20image%2020260208162811.png)

2.  Next, share the `Applications` folder. Right-click the folder, go to Properties → Sharing tab → Advanced Sharing, and allow access only for authenticated users

![](../Attachments/Pasted%20image%2020260208163204.png)

![](../Attachments/Pasted%20image%2020260208163118.png)

#### Creating a Policy to install the application 

1. Create A new GPO under the domain name named `Software-7z2501-x64`

![](../Attachments/Pasted%20image%2020260208163359.png)

2. Right click to edit the Policy ---> Head to `Computer Configuration\Policies\Software Settings\Software installation` ---> Right Click and Select `New -> Package` ---> Select the package from the share folder created  ---> Select `Assigned`

![](../Attachments/Pasted%20image%2020260208165219.png)

![](../Attachments/Pasted%20image%2020260208165517.png)


