# Windows 11 Enterprise Setup

## 1. Virtual Machine Configuration

I created a Windows 11 Enterprise VM with the following specifications:
- OS: `Windows 11 Enterprise`
- RAM: `4 GB`
- CPU: `2 cores`
- Disk: `20 GB`
- Network Adapter: `NAT`

🖼️  **VMware Virtual Machine Settings**

![Win11 Specs](https://github.com/user-attachments/assets/62aac9a3-08ce-4e2a-a049-587099a5b1f7)

## 2. Network & Hostname Setup

Once the OS was installed, I configured the following:
- Changed system name as: `Comp01`
- IP Address: `192.168.253.130 (DHCP)` 
- Set Preferred DNS Server: `192.168.253.5`
  - Alternate DNS Server: `8.8.8.8 (Google DNS Server)`

🖼️  **Network Settings with DHCP and DNS for `Comp01`**

![Network Configuration](https://github.com/user-attachments/assets/ef95ffee-af80-4af1-ac14-d0b769ab34a2)

## 3. Joining the Domain
  1. Opened `System > About > System Properties > Change...`
  2. Selected Domain Join, entered  `lechuga.local`
  3. Entered the domain admin creditentials account
  4. Restarted the machine 

🖼️ **Changed System Name and Joined Domain**

![System Name and Joining Domain](https://github.com/user-attachments/assets/4d4867bd-abaf-474b-91c0-005d028c9263)

🖼️ **Successfully Joined the Domain**

![Successfully Joined Domain](https://github.com/user-attachments/assets/97568684-1e7e-4aae-9c5d-60fa29c75727)

## 4. Verification
Once machine was back online, I:
  - Logged in as `hlechuga` using domain credentials
  - Verified domain membership in System Properties
  - Confirmed connectivity to the Domain Controller using `ping` and `nslookup`

🖼️ **Login Screen with Domain Name Shown**

![Sign in to domain](https://github.com/user-attachments/assets/e2c77cee-6046-4ecb-837a-d65646808dbe)

🖼️ **System Properties Showing Domain Joined**

![systeminfo ](https://github.com/user-attachments/assets/02bfbfce-5acb-4773-b7c0-9de69be1cf4a)

🖼️ Successfull `ping` and `nslookup` 

![Ping and Nslookup](https://github.com/user-attachments/assets/3ba47ba4-a920-49a7-a9f6-b81f61ba2d13)
