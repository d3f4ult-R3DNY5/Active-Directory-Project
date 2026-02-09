# Configuration of the Printer In the Active Directory

## Overview 
---
This step involves installing and configuring the required server roles and features to support printer services within the Active Directory environment. Once the necessary roles and features are added, the printer can be centrally managed through Active Directory, allowing controlled access for users and groups.

>[!NOTE]
>In this setup, the printer configuration is adapted based on the available hardware, without requiring a separate network cable or dedicated printer network.

## Network Diagram 
---

![](../Attachments/Pasted%20image%2020260209201645.png)


### Procedure 
---
1. Go to the Server manger ---> Add Roles and features ---> Add the Print and Document Services 

![](../Attachments/Pasted%20image%2020260209201837.png)

![](../Attachments/Pasted%20image%2020260209201946.png)

2. Now Go to Tools ---> Print Management 

![](../Attachments/Pasted%20image%2020260209202123.png)

3. Under **Print Servers** ---> **TestSolutions** ---> **Printers** ---> Right-click and select **Add Printer** ---> Perform the following configurations as shown in the images

![](../Attachments/Pasted%20image%2020260209204817.png)

![](../Attachments/Pasted%20image%2020260209205124.png)

![](../Attachments/Pasted%20image%2020260209205142.png)

![](../Attachments/Pasted%20image%2020260209205332.png)

![](../Attachments/Pasted%20image%2020260209205349.png)

4. Go to **Active Directory Users and Computers (ADUC)** ---> Enable **Users, Contacts, Groups, and Computers as containers** ---> Add the printer to the **Printers OU** under the **Sales** department

![](../Attachments/Pasted%20image%2020260209210855.png)

5. Add the **Sales** group to the printer permissions.

![](../Attachments/Pasted%20image%2020260209210947.png)

6. You can now log in as **User Patty** on **PC01** and confirm that the printer is listed in the **Settings** app.

![](../Attachments/Pasted%20image%2020260209211331.png)



