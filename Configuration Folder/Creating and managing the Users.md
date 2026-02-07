# Creating and managing the Users

## Overview 
---
The writeup includes the creation, configuration and the management of the user in the organization. 

>[!NOTE]
>#### Tasks to be performed 
>- creation of the user
>- adding the user to the group 
>- deleting the users 
>- disabling the users 


### Procedure 
---
#### Creating the admin user 

1. Go to the ADUC ---> Domain User OU and ---> Right click and create a new user ---> Untick the `option of change the password on next logon` and check the option of `password never expires`

![](../Attachments/Pasted%20image%2020260207093105.png)

#### Adding the user to the IT group 

1. Head to the OU containing the IT group ---> Double click ---> In the `members` and `managed by` ---> Add `john colby` user ---> Hit Apply and OK 

![](../Attachments/Pasted%20image%2020260207093907.png)

![](../Attachments/Pasted%20image%2020260207093954.png)


#### Deleting the user account 

1. Create a dummy account  `Test User` ---> Right click on the user ---> Click on the Delete option ---> Click yes on the popup dialogue box 

![](../Attachments/Pasted%20image%2020260207094252.png)

![](../Attachments/Pasted%20image%2020260207094400.png)

![](../Attachments/Pasted%20image%2020260207094415.png)

2. The user gets deleted and is no longer visible in the OU 

![](../Attachments/Pasted%20image%2020260207094511.png)

#### Disabling the user

1. To Disable the user, Right click on the user ---> Click on the `Disable Account` option 

![](../Attachments/Pasted%20image%2020260207094736.png)

>[!TIP]
>It is advisable to create a separate OU for the Disabled Accounts  and move the disabled account to that OU 

2. The account that is disabled will have a downward facing arrow like this 

![](../Attachments/Pasted%20image%2020260207095022.png)


3. To Enable the account --->  Right Click and Enable Account

![](../Attachments/Pasted%20image%2020260207095138.png)

