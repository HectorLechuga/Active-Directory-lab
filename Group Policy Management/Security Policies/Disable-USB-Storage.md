# Disable USB Storage (GPO)
It is used to prevent users from accessing removeable USB storage devices on domain computers. Reduces the risk of data exfiltration, malware infections, and unathorized file transfers. By restricting all removeable media organizations can better protect sensitive data.

## 1. Creating New GPO 
  - Created a new GPO: `Disable USB Storage`
  - Selected `Computer Configuration > Adminstrative Templates > Removeable Sotrage Access`

## 2. Defined the Policy

| Setting                                     | Value         |
|---------------------------------------------|---------------|
| **All Removeable Storage classes: Deny All access** | Enabled    |


🖼️ **Disable USB Storage**

![Defined USB Device](https://github.com/user-attachments/assets/ac84349e-96ff-4007-814e-7fc909fae2a1)

## 3. Verifying GPO
- Confirm policy was applied using `gpresult /r`
- Inserted a USB storage device into a client machine
- Verified access to device was blocked and attmped to transfer files to media storage 
