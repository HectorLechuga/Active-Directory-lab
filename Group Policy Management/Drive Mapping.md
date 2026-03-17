# Drive Mapping (GPO)
This section outlines how network drives were automatically mapped for users based on their department using Group Policy Preferences in Group Policy

## 1. Creating New GPO 
  - Created a new GPO: `Drive Mapping`
  - Selected `User Configuration > Preferences > Windows Settings > Drive Maps`

## 2. Configuration

| Drive                                     | Path         |
|---------------------------------------------|---------------|
| **IT Drive ( I: )**                | \\WINSERVER2022\IT    |
| **HR Drive ( H: )**               | \\WINSERVER2022\HR    |
| **Sales Drives ( S: )**     | \\WINSERVER2022\SALES     |

- Set the **Action** to `Update`:
  - It will create the drive if it does not exist
  - Updates it if changes are made
  - Does not remove the drive if the policy no longer applies
 
![Finished Drives](https://github.com/user-attachments/assets/960c4172-3afb-4408-97c4-c3b769311107)
## 3. Item-Level Targeting
Each mapped drive was configured with item-level targeting to ensure only users with the correct group receive the appropriate drive
- Targeting Type: **User in group**

| Drive                                     | Group         |
|---------------------------------------------|---------------|
| **IT Drive ( I: )**                | IT_Users    |
| **HR Drive ( H: )**               | HR_Users    |
| **Sales Drives ( S: )**     | Sales_Users     |

🖼️ **IT Config**

![Target IT](https://github.com/user-attachments/assets/8d33691c-9689-41c4-9cca-09a93da02eb4)

🖼️ **HR Config**

![Target HR](https://github.com/user-attachments/assets/de52f710-b719-4990-9c15-8f5e9948f2e1)

🖼️ **Sales Config**

![Target Sales](https://github.com/user-attachments/assets/66e4ec05-f5ba-46ba-bb5c-aea6a2980d31)


## 3. Testing & Verification
  - Logged into a domain user account
  - Ran `gpupdate /force`
  - Verified mapped drives appeared correctly in File Explorer

![HR Verified 2](https://github.com/user-attachments/assets/39582134-064f-4616-81d8-5aebe3c2b3f1)
![IT Verified](https://github.com/user-attachments/assets/0f9e694f-e8c8-48f8-b0dc-9dd631d2c3d3)
![Sales Verified](https://github.com/user-attachments/assets/2b68582e-9178-4cdc-9ae6-afeef902fcc4)


     
