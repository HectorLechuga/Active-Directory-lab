# Account Lockout Policy (GPO)
It is used to protect user accounts from brute-force attacks. It will automatically lock a user account after a defined number of failed login attempts have been reached, this will prevent attackers from repeatdly guessing passwords. The account will remain locked for a specificed period of time. This policy helps improve security by limiting unauthorized access attempts.

## 1. Creating New GPO 
  - Created a new GPO: `Account Lockout Policy`
  - Selected `Computer Configuration > Windows Settings > Security Settings > Account Lockout Policy`

## 2. Defined the Policy

| Setting                                     | Value         |
|---------------------------------------------|---------------|
| **Account lockout duration**                | 30 minutes    |
| **Account lockout threshold**               | 5 attempts    |
| **Reset account lockout counter after**     | 10 minutes    |

🖼️ **Account Lockout Policy**

![Defined Account Lockout Policy](https://github.com/user-attachments/assets/0de4c515-cf1e-46be-bb90-bd90cd8f0353)

## 3. Verifying GPO
  - Inputted 5 incorrect logins for user `csmith`
  - Verified user account was locked
  - Checked Event Viewer logs for lockout entries under: `Event Viewer > Windows Logs > Security`

🖼️ **User Account Locked Out**

![Locked Account](https://github.com/user-attachments/assets/1c80061f-4c57-4086-9f5e-aac7b92ab508)

🖼️ **User Account Management Account Lockout**

![Event Log](https://github.com/user-attachments/assets/7aea0631-04c9-4ea1-a097-47a8dd3ab6ab)


