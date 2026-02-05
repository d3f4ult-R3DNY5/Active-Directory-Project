# Active-Directory-Project

## Overview of the project 
---
This Project contains the processes and steps taken to configure the active directory Homelab and Getting it up and running 

>[!NOTE]
>#### **Prerequisites** 
>- Having Virtualization Enabled 
>- Minimum hardware specifications : 16 GB RAM, Octa Core, Virtualisation Enabled
>
>#### **Software and Package Installations**
>- VMware Workstation Pro 17.6.4 or above
>- Windows 11. iso (Disk Image)
>- Windows Server 2022 (Disk Image)
>


## Phase 1 : Installation of the Disk Images and Configuring the Server
---
This phase involves the installation and configuration of the ISO images and the server. We will be creating a local domain and a domain administrator account, as well as installing the Windows 11 ISO and configuring a local user account. The Windows 11 installation will use an `unattended XML` file  to allow for easier and more consistent configuration. 

>[!TIP]
>#### Configurations
>- Step 1 : [Installing the Server 2022 on VMware workstation](Configuration%20Folder/Installing%20the%20Server%202022%20on%20VMware%20workstation.md)
>- Step 2 : [Configuring the server 2022](Configuration%20Folder/Configuring%20the%20server%202022.md)
>- Step 3 : [Adding the Domain services role to the Server 2022](Configuration%20Folder/Adding%20the%20Domain%20services%20role%20to%20the%20Server%202022.md)
>- Step 4 : Creating the Windows 11 VM 
>	- Option 2 : [Creating a Bootable USB with an unattended XML](Configuration%20Folder/Creating%20a%20Bootable%20USB%20with%20an%20unattended%20XML.md) (Fast)
>	- Option 3 : Manually installing the OS (Slow)

## Phase 2 : Creating and Managing the Organizational Units, Computers and Users 
---
This phase focuses on common helpdesk-related tasks involving the management of organizational units, users, computers, and groups. It includes creating organizational units, user accounts, and groups, assigning users to groups, and moving users between organizational units. Additional tasks involve managing user accounts by copying existing accounts, resetting and changing passwords, enabling or disabling user accounts, and deleting users or organizational units as required. This phase also covers adding PCs to the network and configuring basic settings on systems joined to the domain.

