# Configuring the Roaming Profiles  in the active directory

## Overview 
---
This write-up covers the configuration and use of roaming profiles within an Active Directory environment. Roaming profiles store user profile data on a network server, allowing users to access the same desktop settings and preferences when logging in to different domain-joined computers. This helps provide a consistent user experience while enabling centralized management of user profiles.

>[!NOTE]
>This involves 
>1. creating a romaing user group for the profile
### Procedures
---
#### Creating the User Group for the Roaming Profile

1.  Head to ADUC ---> create a domain groups OU under the `testsolutions OU` ---> Create a Group Named `Roaming Profiles` in `IT\Groups` OU 

![](../Attachments/Pasted%20image%2020260209120349.png)


![](../Attachments/Pasted%20image%2020260209120447.png)
#### Creating and Configuring the Share for the roaming profiles

1. Head to **Server Manager** ---> **File and Storage Services** ---> Right-click and create a **30 GB shared drive**, which will be used for user roaming profiles

![](../Attachments/Pasted%20image%2020260209112641.png)

![](../Attachments/Pasted%20image%2020260209112725.png)

2. The dollar sign is added so that the folder is not easily viewable ---> Do the following Configurations Next by `Enabling Access based Enumerations` and `Encrypting the Data Access`

![](../Attachments/Pasted%20image%2020260209113026.png)

![](../Attachments/Pasted%20image%2020260209113240.png)


3. Configuring The permissions for the share ---> Disable Inheritance  ---> Remove the User Groups ---> Add the `Roaming Profile` Group

![](../Attachments/Pasted%20image%2020260209120547.png)

##### Permissions for the Roaming Users Group
![](../Attachments/Pasted%20image%2020260209121011.png)

##### Permissions for the administrators
![](../Attachments/Pasted%20image%2020260209121054.png)

4. Click on Next and Then create 

![](../Attachments/Pasted%20image%2020260209121215.png)


5. Verify the changes 

![](../Attachments/Pasted%20image%2020260209124721.png)

