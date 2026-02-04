# Installing the Server 2022 on VMware workstation

## Overview 
---
This Readme contains the steps of installation of the Windows 2022 Server on the VMware workstation

### Procedure 
---

1. Install the iso file for the server from the [Microsoft Website](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022) from your default web browser 
2. Once the files is installed ---> Open the VMware Workstation ---> Create A new Virtual Machine 

![](../Attachments/Pasted%20image%2020260204161414.png)

3. Click on Next ---> installer disc image file ---> Click on `Browse` ---> Select the server iso file ---> Click Next 

![](../Attachments/Pasted%20image%2020260204161630.png)

4. Now Create the name and password for the default windows account ---> Click Next ---> Select  `yes` on the dialogue box

![](../Attachments/Pasted%20image%2020260204162212.png)

>[!TIP]
>#### Credentials 
>- Fullname : PJones
>- Password : password1

![](../Attachments/Pasted%20image%2020260204162429.png)

5. Click next (or change the storage location or VM name) ---> Select the Size ---> Click on `Store Virtual Disk as a single File` or leave it as it is ---> Click Next

![](../Attachments/Pasted%20image%2020260204162607.png)

7. Now open virtual network editor on the Host machine  and create the following configurations ---> Apply ---> OK

![](../Attachments/Pasted%20image%2020260204163853.png)

![](../Attachments/Pasted%20image%2020260204163838.png)

![](../Attachments/Pasted%20image%2020260204164039.png)


8. Go to Customized Hardware ---->  Network Adapter ---> Select the newly created Virtual Network ---> Close ---> Finish

![](../Attachments/Pasted%20image%2020260204164445.png)

9. Power on the virtual machine ---> You will get the following error

![](../Attachments/Pasted%20image%2020260204164659.png)

10. Go to VM ----> Virtual machine Settings ---> Floppy ---> Uncheck  ` Connect at Power on`

![](../Attachments/Pasted%20image%2020260204165231.png)

11. Once you uncheck ---> Power on the Machine ----> You will get the following screen 

![](../Attachments/Pasted%20image%2020260204165407.png)


