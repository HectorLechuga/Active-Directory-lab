# 🛠️ Windows Server 2022

## 1. Installation
- Created a new Virtual Machine in VMware Workstation Pro with the following specs:
  - 2GB RAM
  - 2 CPUs
  - 20 GB Virtual Disk
- Mounted the **Windows Server 2022 ISO** file
- Selected **Standard Evaluation (Desktop Experience)**

![OS Setup](https://github.com/user-attachments/assets/0041925d-3f77-4d00-a3be-96e864b7f6e6)

🖼️ ***Sucessful boot after installation***
![Server Menu](https://github.com/user-attachments/assets/a74aff90-92a7-43ef-8081-f70a245d3c80)

## 2. Initial Configuration
After installing the server, I configured the folllowing:
  - Changed the machine name to `WinServer2022`
  - Set Static IP address: `192.168.1.10`
  - Configured DNS to point itself: `192.168.1.10`
  - Default Gateway: `192.168.1.1`

![IP Config](https://github.com/user-attachments/assets/78085184-2773-4f02-86ec-aba71d7f87e8)

## 3. Installing Active Directory
- Opened **Manage**
- Selected **Add Roles and Features**
- Selected **Role-based or featured-based installation**

🖼️ Installed the **Active Directory Services**

![Installing AD DS](https://github.com/user-attachments/assets/3467b6f3-ac87-4cbf-8a71-ea7a2a13d3dd)

## 4. Promoting to Domain Controller
  - Promoted the server to a Domain Controller using the post-installation configuration wizard
  - Created a ***new forest*** named `lechuga.local`
  - Accepted the default NetBIOS name: `LECHUGA`
  - Restarted the server to complete the configuration

🖼️ ***Initial Deployment Configuration***

![Promoting to domain controller](https://github.com/user-attachments/assets/e35e6e57-88e2-4099-a6c4-b84dd48f469e)

🖼️ ***Successful Promotion***

![Successful Promotion](https://github.com/user-attachments/assets/e1376f34-3ff6-41ff-a820-598e0729ce48)
![AD Users and Computers](https://github.com/user-attachments/assets/721b333e-a6fd-43e5-9824-f0c5d9ea2ca6)


## 5. Summary
| Configuration Item         | Value                            |
|----------------------------|----------------------------------|
| **Server Name**            | WinServer2022                    |
| **Static IP**              | 192.168.1.10                     |
| **Domain Name**            | lechuga.local                    |
| **DNS Server**             | 192.168.1.10 (local)             |
| **AD Role Installed**      | Active Directory Domain Services |
| **Domain Controller Type** | New Forest                       |









