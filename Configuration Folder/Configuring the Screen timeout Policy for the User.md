# Configuring the Screen timeout  Policy for the User

## Overview 
---
This policy is used to configure the screen timeout settings for users by automatically locking the system after a defined period of inactivity. It helps improve security by preventing unauthorized access when a user is away from their workstation.

### Procedure 
----
1. Go to the Domain Controller (DC) ---> Press **Windows + R** ---> Type `gpmc.msc` ---> Right-click **Group Policy Objects** and create a new Group Policy

![](../Attachments/Pasted%20image%2020260208094649.png)

2. Create a New Policy called the screen timeout Policy 

![](../Attachments/Pasted%20image%2020260208102327.png)

3. Apply this to the Test Solutions OU 

![](../Attachments/Pasted%20image%2020260208102438.png)

4. Now Update the Group Policy using the following command `gpupdate /force`

![](../Attachments/Pasted%20image%2020260208103924.png)









