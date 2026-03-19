# File Server 
I configured a file server to provide centralized storage and the use of **Group Policy** to automatically map network drives for different departments

## 1. Creating Shared Folders
On the file server I created shared folders for each departments:
````
C:\WINSERVER2022
 ├── HR
 ├── Sales
 └── IT
````
## 2. Share Permissions Configured
Used to control access to shared folders over the network.
Each folder was shared over the network with the following paths:

`\\WINSERVER2022\HR`
- Assigned Permissions:
  - **Domain Admins** -> Full Control
  - **HR_Users** -> Change + Read

![HR Share Permissions](https://github.com/user-attachments/assets/2507883f-2a73-4ccb-a30c-7364f8190f7a)

`\\WINSERVER2022\Sales`
- Assigned Permissions:
  - **Domain Admins** -> Full Control
  - **Sales_Users** -> Change + Read

![Sales Share Permissions](https://github.com/user-attachments/assets/49016445-bce5-4208-a199-8aab3c40ddad)

`\\WINSERVER2022\HR`
- Assigned Permissions:
  - **Domain Admins** -> Full Control
  - **IT_Users** -> Change + Read

 ![IT Share Permissions](https://github.com/user-attachments/assets/579e4f43-1b06-4e24-8a41-7168c876aade)

## 3. New Technology File System (NTFS) Permissions Configuration
Used to enforce detailed access control at the file system level
Configured the following:
- Path: `C:\HR`
- Assigned Permissions
  - HR_Users -> Modify, Read & Execute, List, Write
  - Domain Admins -> Full Control

![NTFS HR Permission](https://github.com/user-attachments/assets/35138b3a-4ecc-46bb-b15b-1d9179c124fd)

- Path: `C:\Sales`
- Assigned Permissions
  - Sales_Users -> Modify, Read & Execute, List, Write
  - Domain Admins -> Full Control
 
![NTFS Sales Permission](https://github.com/user-attachments/assets/63d12bc2-2539-4905-bc50-7e3ea121bf62)

- Path: `C:\IT`
- Assigned Permissions
  - IT_Users -> Modify, Read & Execute, List, Write
  - Domain Admins -> Full Control
![NTFS IT Permissions](https://github.com/user-attachments/assets/4e79d572-d3af-4b83-9d16-f5613ffa98c0)

## 4. Verification
- Logged in as users in different departments
- Verified:
  - Access to their respective \\WINSERVER2022\
  - Ability to create / edit files within folder
  - Unable to view other department folders
- [Implemented Drive Mapping](Group%20Policy%20Management/Drive-Mapping.md)

🖼️ **Verifying HR Drive** 

![HR Verified 2](https://github.com/user-attachments/assets/bcfea2b3-9f4e-4066-8cbe-85acb189ca68)

🖼️ **Verifying Sales Drive** 

![Sales Verified](https://github.com/user-attachments/assets/2b189268-1847-4036-bcf6-b4bed2023510)

🖼️ **Verifying IT Drive** 

![IT Verified](https://github.com/user-attachments/assets/536c4bcb-746b-45d7-bfe3-f91bea1970f0)

