# Limiting the PowerShell for the people who are not part of the admin Group

## Overview 
---
This write-up contains information on how to restrict non-administrative users from accessing  and PowerShell. To achieve this, an organizational unit will be created for IT users, allowing a separate policy to be applied that permits administrative access while restricting other users.

### Procedure 
---
1. Go to the Domain Controller (DC) ---> Press **Windows + R** ---> Type `gpmc.msc` ---> Right-click **Group Policy Objects** and create a new Group Policy

![](../Attachments/Pasted%20image%2020260208094649.png)

2. Create A new Policy under Group Policy Objects ---> Disable Command Prompt and PowerShell Policy 

![](../Attachments/Pasted%20image%2020260208153002.png)

3. Now Right click and Edit ---> `User Configuration\Administrative Templates\Windows Components\Windows PowerShell` 

>[!TIP]
>- Turn On Module Logging 
>- Turn On script Executions

![](../Attachments/Pasted%20image%2020260208153721.png)

![](../Attachments/Pasted%20image%2020260208154014.png)

4. Go to the AppLocker located in ---> `Computer Config → Windows Settings → Security → AppLocker` ---> Create Default Rules in `Excutable Policies` and `Script Rules` 

![](../Attachments/Pasted%20image%2020260208155301.png)

5. Go to the AppLocker Properties and Enforce the Rules 

![](../Attachments/Pasted%20image%2020260208155919.png)


6. Head to the `Computer Config → Windows Settings → Security → System Services` ---> Set it to Automatic

![](../Attachments/Pasted%20image%2020260208155718.png)

7. Now Link the Policies to the sales Group 

![](../Attachments/Pasted%20image%2020260208160212.png)



