# Active-Directory-lab
Implemented a fully functional Windows Server lab environment using VMware Workstation Pro. This AD lab replicates a real world enterprise network by installing Windows Server 2022, configuring domain services, user management, Group Policy Objects, and file server.

## Project Structure 
- Environment Setup
  - [Windows Server Setup](./Environment%20Setup/Windows-Server-Setup.md)
  - [Windows Client Setup](./Environment%20Setup/Windows-Client-Setup.md)
  - [Organizational Unit Structure](./Environment%20Setup/Organizational-Unit-Structure.md)
  - [DHCP Server](./Environment%20Setup/DHCP-Server.md)
- Group Policy Management
  - Security Policies
    - [Account Lockout](./Group%20Policy%20Management/Security%20Policies/Account-Lockout.md)
    - [Password Policy](./Group%20Policy%20Management/Security%20Policies/Password-Policy.md)
    - [Disable USB Storage](./Group%20Policy%20Management/Security%20Policies/Disable-USB-Storage.md)
  - User Environment
    - [Drive Mapping](./Group%20Policy%20Management/User%20Environment/Drive-Mapping.md)
    - [Desktop Wallpaper](./Group%20Policy%20Management/User%20Environment/Desktop-Wallpaper-Policy.md)
    - [Restrict Control Panel and PC Settings](./Group%20Policy%20Management/User%20Environment/Restrict-Control-Panel-and-Settings.md)
- File Services
  - [File Server](./File%20Services/File-Server.md)
  - [File Server Resource Manager](./File%20Services/File-Server-Resource-Manager.md)
 
# Key Features
## Domain Configuration
  - Deployed and configured a domain controller
  - Created and managed users, groups, and OUs
## Group Policy Management
Created and managed mutiple GPOs to enforce security and user environment:

**Security Policies**
- Password Policy
- Account Lockout Policy
- Disable Removeable Media (USB)

**User Enviroment**
- Drive Mapping
- Desktop Wallpaper
- Restrict Control Panel and Settings Acess
## File Server
- Configured a centralized file server
- Created role-based shared folders (HR, IT, Sales)
- Applied **NTFS** and **share permissions** using security groups
- Configured role-based access control (RBAC)
## Network Drive Mapping
- Automatically mapped drives using GPP
- Configured security group targeting to assign drives based on user roles
## File Server Resource Manager (FSRM)
- Created **quotas** to manage disk usage
- Configured **file screening** to block unauthorized file types
## Verification
- Joined client machines to the domain
- Test GPO using `gpupdate /force` and `gpresult /r`
- Confirmed drive mappings and access permissions based on user roles
