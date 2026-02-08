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

>[!TIP]
>#### Active Directory User and Computer Management
> 1. [Organizational Unit and Group Management](Configuration%20Folder/Organizational%20Unit%20and%20Group%20Management.md)
> 2. [Creating and managing the Users](Configuration%20Folder/Creating%20and%20managing%20the%20Users.md)
> 3. [Adding and managing the computers to the Domain](Configuration%20Folder/Adding%20and%20managing%20the%20computers%20to%20the%20Domain.md)

## Phase 3 : Creating , Managing and Configuring the Group Policies 
----
This phase involves the creation, management, and configuration of various Group Policies within the domain. In this section, we will work with the group policies listed below, all of which are managed through the Group Policy Management Console. Group Policy follows the LSDOU hierarchy (Local, Site, Domain, and Organizational Unit) and is applied in a top-down order. In cases where policies conflict, the last policy applied takes precedence, and enforced policies will apply regardless of conflicts.

>[!NOTE]
>#### Group Policy Management Console 
>1. [Configuring the GPO for Task Manager for the Sales OU](Configuration%20Folder/Configuring%20the%20GPO%20for%20Task%20Manager%20for%20the%20Sales%20OU.md)
>2. [Configuring the Screen timeout Policy for the User](Configuration%20Folder/Configuring%20the%20Screen%20timeout%20Policy%20for%20the%20User.md)
>3. [Configuring the Wallpaper Policy for the the Different OU's](Configuration%20Folder/Configuring%20the%20Wallpaper%20Policy%20for%20the%20the%20Different%20OU's.md)
>4. [Configuring the Splash Screen Policy](Configuration%20Folder/Configuring%20the%20Splash%20Screen%20Policy.md)
>5. [Limiting the PowerShell for the people who are not part of the admin Group](Configuration%20Folder/Limiting%20the%20PowerShell%20for%20the%20people%20who%20are%20not%20part%20of%20the%20admin%20Group.md)





