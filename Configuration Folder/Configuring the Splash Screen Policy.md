# Configuring the Splash Screen Policy

## Overview 
---
This write-up contains the Group Policy settings used to configure the splash screen for users within the domain. It also involves creating the required files and configuring the appropriate permissions.

### Procedure 
---
1. Go to the Domain Controller (DC) ---> Press **Windows + R** ---> Type `gpmc.msc` ---> Right-click **Group Policy Objects** and create a new Group Policy

![](../Attachments/Pasted%20image%2020260208094649.png)

2. Creating the Policy Object `interactive Logon Policy` ---> Right Click and Edit ---> Head to ---> `Computer Configurations/Windows Settings/Security Settings/Security Options` ---> Modify the Following Policies

![](../Attachments/Pasted%20image%2020260208121338.png)


![](../Attachments/Pasted%20image%2020260208121457.png)

3. Apply this to the Test Solutions OU ---> Check the resultant output

![](../Attachments/Pasted%20image%2020260208122240.png)




