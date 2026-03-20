# 1. Password Policy
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

