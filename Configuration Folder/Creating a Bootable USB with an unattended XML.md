# Creating a Bootable USB with an unattended XML

## Overview 
---
This write-up contains information on the installation of a Windows 11 ISO using an unattended XML file. The ISO is first flashed onto a USB flash drive using the application called Rufus, after which the unattended XML file is mounted to the installer to allow for automated configuration during setup.

>[!NOTE]
>#### Prerequisites 
>- Windows 11 iso file 
>- Rufus 
>- Unattended XML file 
>- VMWare Workstation Pro
### Procedure 
---
1. Create the `unattended.xml` file on the following website. [link](https://schneegans.de/windows/unattend-generator/)

![](../Attachments/Pasted%20image%2020260205110435.png)

2. Go to Rufus ---> Select the ISO ---> Start

![](../Attachments/Pasted%20image%2020260205111643.png)

3. Once the RUFUS has finished ---> The application would look something like this ---> Click on Close 

![](../Attachments/Pasted%20image%2020260205113339.png)


4. Go the VMware Workstation and Create a New Virtual Machine ---> Click Next ---> Select `I will install OS later` Option ---> select the OS which your going to install

![](../Attachments/Pasted%20image%2020260205113513.png)

![](../Attachments/Pasted%20image%2020260205113548.png)

![](../Attachments/Pasted%20image%2020260205113619.png)


5. Select the Name of the VM ---> Enter the encryption password ---> store Virtual disk as a single file ---> Customize Hardware ---> Select the Network Adapter which was created in the AD setup

![](../Attachments/Pasted%20image%2020260205113801.png)

![](../Attachments/Pasted%20image%2020260205113843.png)

![](../Attachments/Pasted%20image%2020260205113919.png)


![](../Attachments/Pasted%20image%2020260205114104.png)

6. Copy and paste the `unattended.xml` file created in the first step to the mounted drive.

![](../Attachments/Pasted%20image%2020260205114402.png)

7. Power on the newly created VM and click F11 tills you see the BIOS screen

![](../Attachments/Pasted%20image%2020260205114607.png)

8. Click on the VM ---> Removable devices ---> Connect the bootable drive

![](../Attachments/Pasted%20image%2020260205114718.png)

9. After a few minutes you will get the LOGO

![](../Attachments/Pasted%20image%2020260205115357.png)


![](../Attachments/Pasted%20image%2020260205120615.png)


10. Once you reach this screen ---> Configure the Default Account

![](../Attachments/Pasted%20image%2020260205121757.png)

>[!TIP]
>#### Configurations
>- name : Paul William Local
>- password : Password1

11. Once the process is complete, the following screen will be displayed.

![](../Attachments/Pasted%20image%2020260205122141.png)

12. Once it is done ---> You should be able to login 

![](../Attachments/Pasted%20image%2020260205124924.png)

