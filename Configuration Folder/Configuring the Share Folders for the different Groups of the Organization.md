# Configuring the Share Folders for the different Groups of the Organization

## Overview 
---
This write-up contains information on creating different security groups and mapping their respective shared folders to them. It also involves configuring policies so that the shared drives are automatically mapped at login even when a new user is created and assigned to a specific group.

### Procedure 
---
#### Creating the Groups 

1. The **Purchasing** and **Marketing** groups will be created under the `Sales\Groups` organizational unit.

![](../Attachments/Pasted%20image%2020260209141806.png)

2. Creating the Users `Patty Gonzales` and `Pierre Rodriguez` and assigning them to Purchasing and Marketing respectively 

##### Patty Properties

![](../Attachments/Pasted%20image%2020260209142018.png)

##### Pierre Properties 

![](../Attachments/Pasted%20image%2020260209142119.png)


#### Creating the Network Shares 

1. Go to server manager and create the network Share for Purchasing as Follows 

![](../Attachments/Pasted%20image%2020260209142414.png)

![](../Attachments/Pasted%20image%2020260209142525.png)

2. Go to server manager and create the network Share for Marketing as Follows 

![](../Attachments/Pasted%20image%2020260209142759.png)

![](../Attachments/Pasted%20image%2020260209142943.png)

3. Creating the Share folder Objects in ADUC 

![](../Attachments/Pasted%20image%2020260209143339.png)

![](../Attachments/Pasted%20image%2020260209143521.png)


#### Creating a Policy for the Automapping of the drives 

1. Creating a Group Policy to automatically map the Marketing drives using the Group Policy Management Console under the Sales OU

![](../Attachments/Pasted%20image%2020260209143951.png)

2. Now remove the Authenticated users from the security Filtering and add the Marketing Group 

![](../Attachments/Pasted%20image%2020260209144148.png)

3. Now in Delegation pane of the Policy, Add the Authenticated users with Read permissions

![](../Attachments/Pasted%20image%2020260209144328.png)

3. Edit the Policy ---> Head to `User Configurations\Prefernces\Drive Maps\` ---> Right Click `New ---> Mapped Drive` --> Select the drive

![](../Attachments/Pasted%20image%2020260209145504.png)

4. Do the Same for the Marketing Group 

![](../Attachments/Pasted%20image%2020260209150005.png)

#### Account Pierre Rodriguez

![](../Attachments/Pasted%20image%2020260209150317.png)

![](../Attachments/Pasted%20image%2020260209150405.png)

#### Account Patty Gonzales

![](../Attachments/Pasted%20image%2020260209150558.png)

![](../Attachments/Pasted%20image%2020260209150634.png)



