# File Server Resource Manager (FSRM)
Utilizing FSRM to enforce storage limits and control the file types allowed on shared resources within the Active Directory enviroment.
- Opened Server Manager
- Selected Add Roles and Features
- Installed FSRM

🖼️ **Installing FSRM**

![FSRM Install](https://github.com/user-attachments/assets/efa09281-f9b3-4f53-9bc1-375f8b6f7af5)

🖼️ **FRSM Installed**

![FSRM ](https://github.com/user-attachments/assets/225ac7dd-b654-4b04-9ef8-5463729bf486)

## 1. Quota Management
A **Quota** was configured to limit the amount of storage a user can allocate on shard folders. This prevents excessive disk usage and ensuring fair resource allocation.

I configured the following:
- Quota path: `C:\Sales`
- Limit: `10 GB Limit`
- Hard Quota: `Do not allow users to exceed limit`
  - Warnings: Events logs for 85%, 90%, and 100%

A Quota template was created using the settings listed above and appled to the following paths: `C:\HR` and `C:\IT`

🖼️ Configured the Quota for path `C:\Sales`

![Sales Quota](https://github.com/user-attachments/assets/f5a5c851-3f02-4856-8816-27774f173b31)

🖼️ Created Quota Template with settings listed above

![Template Quota](https://github.com/user-attachments/assets/d3342b1c-9bbd-4af2-8a4a-66bba2f80ce9)

🖼️ Applied the Quota Template to `C:\HR` and `C:\IT`

![Completed Quotas](https://github.com/user-attachments/assets/447c0037-0893-41d7-8046-da424f97104f)

## 2. File Screening
Configured file screening to block specific files types that are commonly restricted in enterprise enviroments, such as executables, media files, and to reduce unnecessary risks.

I configured the following:
- File Screen Path: `C:\Sales`
- Custom Properties: `Active Screening: Do not allow users to save unauthorized files`
- Blocked File Groups:
  - `Audio and Video Files`
  - `Compressed Files`
  - `Executable`
  - `Image Files`
 
The custom settings were saved as `Documents and Text Files Onlyl` and applied to `C:\HR`. `C:\IT` was given only block `Audio and Video Files`
 
🖼️ **Creation of Sales File Screening** 

![Sales File Screening](https://github.com/user-attachments/assets/2db22fcd-612b-4090-870d-01cedf027f88)

🖼️ **Saved Custiom Settings as a Template named `Documents and Text Files Only`**

![File Screen Template](https://github.com/user-attachments/assets/560f0cd6-c88b-4333-89c5-210c944e7bc1)

🖼️ **Completed File Screening**

![Completed File Screening](https://github.com/user-attachments/assets/23b45754-c0a0-4b56-b68a-ac41be4effdb)

## 3. Verification 
- Created a text file on the shared folder `C:\HR`
- Text file was successfully created and allowed on the shared folder
- Downloaded `.mp4` file and moved to the shared folder. Permission was denied 

🖼️ **Allowed Text File**

![Documents Allowed](https://github.com/user-attachments/assets/36be6e70-342e-474e-83e3-bc49e1e4fb0a)

🖼️ **Denied .mp4 File**

![Denied Video File](https://github.com/user-attachments/assets/9e993bca-1593-47e7-bc53-65885676f1bc)

