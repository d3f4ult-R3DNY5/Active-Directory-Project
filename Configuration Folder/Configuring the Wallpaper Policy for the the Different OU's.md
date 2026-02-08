# Configuring the Wallpaper Policy for the the Different OU's

## Overview 
---
This write-up contains the Group Policy settings used to configure the desktop wallpaper for the Sales organizational unit. It also involves creating a shared folder and configuring the required permissions.

## Procedure 
---
#### Creating the Share 

1. Head to where the folder is located ---> Right Click on the Properties ---> Sharing ---> Advanced Sharing

![](../Attachments/Pasted%20image%2020260208111309.png)


2. Click on the Permissions Tab ---> Remove the User Everyone from IT ---> Add `Authethicated Users` group to it 

![](../Attachments/Pasted%20image%2020260208111527.png)


#### Creating the Base wallpaper for the entire organization

1.  Go to the Domain Controller (DC) ---> Press **Windows + R** ---> Type `gpmc.msc` ---> Right-click **Group Policy Objects** and create a new Group Policy

![](../Attachments/Pasted%20image%2020260208112402.png)

2. Go to the following Path ---> `User Configuration\Administrative Templates\Desktop\Desktop` ---> Click on Desktop Wallpaper

![](../Attachments/Pasted%20image%2020260208113001.png)

![](../Attachments/Pasted%20image%2020260208113212.png)

3. Apply that Policy to the `testsolutions` OU 

![](../Attachments/Pasted%20image%2020260208113937.png)

#### Similarly creating a Wallpaper Policy for the Sales Department 

1. Creating the group Policy 

![](../Attachments/Pasted%20image%2020260208114343.png)


2. Link the GPO to the `Sales` OU 

![](../Attachments/Pasted%20image%2020260208114511.png)

3. Login in `Bill Murphy` who belongs to the sales account 

