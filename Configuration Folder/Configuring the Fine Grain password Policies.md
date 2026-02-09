# Configuring the Dine grain Password Policies 

## Overview 
---
This write-up involves the creation of Fine-Grained Password Policies using ADSI Edit and assigning these policies to a security group. This is useful in scenarios such as when a local contractor is working for a short period and requires temporary password settings that differ from the default domain policy.

### Procedure 
---
1. Go to ADUC and create a new groups under the `testsolutions\Special groups` OU called `7 Day Password Age`

![](../Attachments/Pasted%20image%2020260209162032.png)

2. Go now to the server manager ---> tools ---> ADSI edit ---> Right Click on ADSI edit and Click on Connect To ---> Leave the Settings as the Default Settings 

![](../Attachments/Pasted%20image%2020260209162150.png)


![](../Attachments/Pasted%20image%2020260209162236.png)

3. Head to this location shown in the below image ---> Right Click and Click New ---> Object 

![](../Attachments/Pasted%20image%2020260209162444.png)


![](../Attachments/Pasted%20image%2020260209162521.png)

4. Create The configurations as shown below 
![](../Attachments/Pasted%20image%2020260209162609.png)

![](../Attachments/Pasted%20image%2020260209162944.png)

![](../Attachments/Pasted%20image%2020260209163002.png)

![](../Attachments/Pasted%20image%2020260209163028.png)

![](../Attachments/Pasted%20image%2020260209163109.png)

![](../Attachments/Pasted%20image%2020260209163130.png)

![](../Attachments/Pasted%20image%2020260209163218.png)

![](../Attachments/Pasted%20image%2020260209163240.png)

![](../Attachments/Pasted%20image%2020260209163308.png)

![](../Attachments/Pasted%20image%2020260209163429.png)

![](../Attachments/Pasted%20image%2020260209163453.png)

5. Go to the Following Option in the Properties and Search for the Option mdDS-PSOAppliesTo the following Security Groups 

![](../Attachments/Pasted%20image%2020260209163817.png)

![](../Attachments/Pasted%20image%2020260209163845.png)

6. The Password policy has been applied to the security Group 




