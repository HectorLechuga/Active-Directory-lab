# DHCP Server
I installed and configured Dynamic Host Configuration Protocol (DHCP) on Windows Server 2022 to automatically assigned IP address within a scope to domain joined Win11 clients. Centralized DHCP management ensure reliable network communication, minimizes manuak errors, and automates IP address allocation.

## 1. Creating DHCP Server
Using **Server Manager** I installed the *DHCP Server* role:
  - Opened **Add Roles and Features Wizard**
  - under **Server Roles** I Selected: `DHCP Server`
  - Completed wizard installation steops

🖼️ **Selecting DHCP Server Role**

![Selected DHCP Server Role](https://github.com/user-attachments/assets/d075704c-d1b2-4b79-97dd-8712ca1da12d)

🖼️ **DHCP Role Installation Results**

![Completed Installation](https://github.com/user-attachments/assets/9e2fc871-a993-458d-9768-5686aaf340eb)

## 2. Authorizting DHCP Server in AD
Once installation was completed:
- Selected `Complete DHCP Configuration`
- Selected `Authorize`

🖼️ **Authorized DHCP Server**

![Authorized DHCP Server](https://github.com/user-attachments/assets/b077686a-a930-4bed-b391-2d04fc1237d3)

## 3. Creating DHCP Scope
To allocate IP addresses to Win11 clients in the DHCP Console:
  - Right clicked `IPv4` > `New Scope..`
  - Configured the following:
    - Scope Name: `Workstations`
    - IP Range: `192.168.253.50 - 192.168.253.100`
    - Subnet Mask: `255.255.255.0`
    - DNS Server: `192.168.253.5`
  - Activated the scope

🖼️ **DHCP Scope Name:** `Workstations`

![Created DHCP Scope](https://github.com/user-attachments/assets/46bfc8fc-d9ac-4faa-8720-b14b5e469a6d)

🖼️ **IP Address Range:** `192.168.253.50 - 192.168.253.100`

![IP Addr Range](https://github.com/user-attachments/assets/a0ff3622-66cd-4ebf-a490-03cd7f163d9b)

🖼️ **Lease Duration:** `8 Days`

![Lease Duration](https://github.com/user-attachments/assets/2a10a3a8-ae90-498b-b566-94f70b79fe8a)

🖼️ **Configure DHCP Options:** `Yes, I want to configure these options now`

![Configure DHCP Options](https://github.com/user-attachments/assets/52e923ee-350f-43e3-9691-b3f675376cba)

🖼️ **Default Router:** `192.168.253.2`

![Default Router IP](https://github.com/user-attachments/assets/db94da82-6bb1-46e5-b8cd-3d32d78e0f24)

🖼️ **Domain Name and DNS Server Settings:** `192.168.253.5 and 8.8.8.8`

![Domain Name and DNS Server](https://github.com/user-attachments/assets/57ee76ad-2813-4d13-ba1e-d009239765f1)

🖼️ **Activated Scope Settings:** `Yes, I want to activate the scope now`

![Activate Scope](https://github.com/user-attachments/assets/bcc2325f-70f3-4a08-a6de-af601da586f0)

🖼️ **Complete DHCP Scope Settings**

![Installed DHCP Server](https://github.com/user-attachments/assets/d8b1d3ff-b195-46dc-89e6-c7f653b4cd94)

## 4. Verifying DHCP IP Address Allocation
On Windows 11 Client
- Enabled IP Settings for `DHCP`
- Runned the following commands
  - `ipconfig /release` and `ipconfig /renew`
- Verfified the Win client received IP from DHCP
  - Win client receieved IP addr: `192.168.253.50`

 🖼️ **Ran** `ipconfig /release` **and** `ipconfig /renew`
 
![Verified on Win Client](https://github.com/user-attachments/assets/14cc86a1-64ad-40ad-ae6f-ec021c55818c)

🖼️ **Output of** `ipconfig /all`

![Running Ipconfig all](https://github.com/user-attachments/assets/9c261468-d0a9-4312-b21f-4b09bd91a167)

🖼️ **Confirmed Address Leases on DHCP Console**

![DHCP Verifing Address Lease ](https://github.com/user-attachments/assets/f87f43bc-0f56-47fd-a085-b5955c9325c4)

## 5. Final DHCP Console Look
Completed configuring the DHCP Server:

🖼️ **Configured DHCP Server**

![Confirmed Addr Pool](https://github.com/user-attachments/assets/501c900a-969d-4c9c-ad31-a164a7d65913)
![DHCP Verifing Address Lease ](https://github.com/user-attachments/assets/0285d97d-59f6-47e8-981a-15c7ad742f42)
![Final Scope Options](https://github.com/user-attachments/assets/c6585865-1704-4443-bd61-e73c53bddc11)

