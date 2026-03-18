# Organizational Unit (OU) Structure 
Domainn enviroment was organzied using Organizational Units (OUs) to support scalability, user management, and Group Policy applications.
## OU Design
````
  lechuga.local
  │
  CA
  │
  ├── Users
  │   ├── HR
  │   ├── IT
  │   └── Sales
  │
  ├── Computers
  │   ├── Workstations
  │   └── Laptops
  │
  ├── Servers
  │   └── File Server 
  │
  └── Security Groups
````

![OU Structure](https://github.com/user-attachments/assets/38f14e82-5f42-43a8-a49f-88e19f2afe73)

- Users, Computers,and Servers are placed in different OUs to allow differet policies to be applied correctly
- Users are separated into different departments like HR, IT, and Sales. enabling targeted policies like **drive mapping**
- A dedicated server OU allows tigher control and prevents accidental application of user level policies 
- Security group OU provides a centralized location for managing groups and easier to manage
## User Account Creation

## Future Scalability 
- Additional sites can be created as separate OUs with their respective users, computers, servers and etc.
- New departments and device types can be easily added 
