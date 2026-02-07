# Organizational Unit and Group Management

## Overview 
---
This document explains how to manage Active Directory. It covers creating and managing users, setting up and organizing Organizational Units (OUs), creating and deleting groups. 

>[!NOTE]
>It is important to create organizational units because the **group polices objects** cannot be applied to container

### Procedure 
---

#### Creating an OU

1. Go the the Search ---> Type ` Active Directory Users and Computers` ---> domain name `testsolutions.com`

![](../Attachments/Pasted%20image%2020260205165940.png)

2. To create a new organizational unit (OU) you right click on domain ---> New ---> organizational unit ---> Name it ---> Click OK 

![](../Attachments/Pasted%20image%2020260205170222.png)

![](../Attachments/Pasted%20image%2020260205170329.png)

3. I have created the Additional OU which are `Domain Users` and `Domain Computers` Respectively under `testsolutions` OU 

#### Deleting an OU 

1. Create a dummy OU known as `TestOU`, You can delete the OU by going into `View ---> Clicking on Advanced features` 

![](../Attachments/Pasted%20image%2020260205173559.png)

![](../Attachments/Pasted%20image%2020260205173609.png)

2. once you have done, `Right Click on the OU ---> Properties ---> Select the Object pane ---> Uncheck protect the object from accidental deletion` ---> Apply & OK

![](../Attachments/Pasted%20image%2020260205173922.png)

3. Right click again on the OU ---> Delete ---> Click yes on the dialogue box which sould be similar to this 

![](../Attachments/Pasted%20image%2020260205174059.png)

>[!NOTE]
>Additionally by enabling the **advanced features** you can see the built-in security groups and computers 

#### Creating a Security Group and Configuring it 
---
1. Head to the `Domain Users` OU and Right click and create a new group 

![](../Attachments/Pasted%20image%2020260205174605.png)

>[!TIP]
>#### Configurations
>- Name : IT Group 
>- Group type : Security 
>- Group Scope : Global 


2. Again Right Click on the security Group ---> Go to the properties ---> Create the following configurations 

![](../Attachments/Pasted%20image%2020260205174926.png)

![](../Attachments/Pasted%20image%2020260205175331.png)

>[!TIP]
>#### General tab 
>- Description : Contains the users who are able to Perform the admin tasks 
>#### Members of Tab 
>- Added Domain Admins





