# Restricting Control Panel and PC Settings (GPO)
Restricts domain users acess to the Control Panel and system settings to prevent unauthorized configuration changes. This policy helps maintain system integrity and reduce the risk of misconfiguration.

## 1. Configuration
- `User Configuration > Policies > Administrative Templates > Control Panel`
- I enabled the policy `Prohibit access to Control Panel and PC settings`

![Restrict Control Panel](https://github.com/user-attachments/assets/cc14a89c-0b06-4de2-a971-89e09e23b2ab)

## 2. Verifying Policy 
Once the policy was applied to the domain users cannot view the control panel
- Logged in as `csmith` to test policy 
- Attempted to open **Control Panel and Settings**
- Confirmed that both are denied access

![Denied Access](https://github.com/user-attachments/assets/15564a44-8a8a-4182-8f03-9920a634236d)
