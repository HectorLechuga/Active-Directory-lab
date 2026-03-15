# GPO Management
This section outlines the Group Policy Objects (GPOs) implemented in the lab to enforce security policies, manage user enviroments, and simulate real world enterprise configurations.

## 1. Password Policy
Configured a domain password policy to enforce stronger authentication requirements to improve account security and reduce the risk of unauthorized access.

Using the Group Policy Management Console (GPMC) 
- `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`

| Policy                                          | Policy Setting          |
|-------------------------------------------------|-------------------------|
| **Enforce password history**                    | 10 passwords remembered |
| **Maximum password age**                        | 90 days                 |
| **Minimum password age**                        | 30 day                  |
| **Minimum password length**                     | 12 characters           |
| **Password must meet complexity requirements**  | Enabled                 |

🖼️ Creating the Password Policy GPO and defining the policy setting using GPMC

![Password Policy](https://github.com/user-attachments/assets/48609510-09ea-4b81-9396-f9377389b0b1)
![Defined Password Policy](https://github.com/user-attachments/assets/6999bbb9-fa44-4a58-bf88-acedb96e761d)

## 2. Account Lookout Policy
Configured **Account Lockout Policy**
![Defined Account Lockout Policy](https://github.com/user-attachments/assets/fbb70e7e-48b3-4cb6-9250-7bf38097f3d0)

## 3. Restrict Access to Control Panel
## 4. Disable USB Storage
## 5. Drive Mapping
Automatically maps shared network drives for users based on departments upon login  
## 6. Desktop Wallpaper Policy
