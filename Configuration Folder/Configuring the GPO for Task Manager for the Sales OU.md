# Configuring the GPO for Task Manager for the Sales OU

## Overview 
---
This writeup contains the information about the configuration of Task Manager Policy For the sales OU 

>[!NOTE]
>#### Prerequisites 
>- Create A sales OU and Assign a user to it
>- Knowledge of the workings of the the Different OU 

### Procedure 
----
#### Creation of the Sales OU and Sales Users 

1. Head to the ADUC and Right click ---> create the OU ---> Sales 

![](../Attachments/Pasted%20image%2020260208092451.png)

2. Go to the OU and again Right Click to Create the Sales Group ---> Right Click Again on the OU and Create a User and Assign IT to the sales Group of the Organization 

![](../Attachments/Pasted%20image%2020260208093003.png)

 
#### Creating the Group Policy 

1. Go to the Domain Controller (DC) ---> Press **Windows + R** ---> Type `gpmc.msc` ---> Right-click **Group Policy Objects** and create a new Group Policy

![](../Attachments/Pasted%20image%2020260208094649.png)

2. Right Click on It ---> Go to the Edit section of It ---> head to the Following Location `User Configuration > Administrative Templates > System > Ctrl+Alt+Del Options`

![](../Attachments/Pasted%20image%2020260208094926.png)

3. Click on Remove Task Manager ---> Enable it 

![](../Attachments/Pasted%20image%2020260208095157.png)

4. Now Head to the gpmc and link the Policy to the sales OU ---> Once done Force the Group Policy to update

![](../Attachments/Pasted%20image%2020260208095701.png)


5. Now if you login on the PC on which the Policy is linked ---> You will see the following 

![](../Attachments/Pasted%20image%2020260208095837.png)