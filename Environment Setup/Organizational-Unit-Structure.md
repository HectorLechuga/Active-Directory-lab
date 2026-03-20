# Organizational Unit (OU) Structure 
Domainn enviroment was organzied using Organizational Units (OUs) to support scalability, user management, and Group Policy applications.
## 1. OU Design
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
- Security group OU provides a centralized location for managing groups 
## 2. User Account Creation
I created the following domain user accounts with passwords set to expire and required to change on first login

| Username            | Full Name        | Department       |
|---------------------|------------------|------------------|
| **hlechuga**        | Hector Lechuga   | IT           |
| **csmith**          | Cody Smith       | IT           | 
| **lporres**         | Luis Porres      | HR               | 
| **jpalacio**        | Jose Palacio     | Sales               | 

## 3. Group Creation
The following security groups were created to manage access to shared resources such as network drives and folders.

| Group Name        | Scope    | Type     |
|-------------------|----------|----------|
| **IT_Users**      | Global   | Security |
| **Sales_Users**   | Global   | Security | 
| **HR_Users**      | Global   | Security | 

Distribution groups were created for email based communication across departments.
| Group Name        | Scope    | Type     |
|-------------------|----------|----------|
| **DL_IT**      | Global   | Distribution |
| **DL_Sales**   | Global   | Distribution | 
| **DL_HR**      | Global   | Distribution | 

🖼️ **List of Groups**

![Security Groups](https://github.com/user-attachments/assets/ce0b343a-cc2f-436a-a8cc-2e75da542bf6)

## Future Scalability 
- Additional sites can be created as separate OUs with their respective users, computers, servers and etc.
- New departments and device types can be easily added 
