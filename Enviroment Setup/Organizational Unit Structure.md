# Organizational Unit (OU) Structure 
Domainn enviroment was organzied using Organizational Units (OUs) to support scalability, user management, and Group Policy applications.
## OU Design
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

- Users, Computers,and Servers are placed in different OUs to allow differet policies to be applied correctly
- Users are separated into different departments like HR, IT, and Sales. enabling targeted policies like **drive mapping**
- A dedicated server OU allows tigher control and prevents accidental application of user level policies 
- Security group OU provides a centralized location for managing groups and easier to manage

## Future Scalability 
- Additional sites can be created as separate OUs with their respective users, computers, servers and etc.
- New departments and device types can be easily added 
