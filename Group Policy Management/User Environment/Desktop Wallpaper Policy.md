# Desktop Wallpaper Policy
A standardized Windows desktop wallpaper was enforced across all domain users to maintain a consistent desktop backgrounds for branding and professionalism. 

## 1. GPO Overview
Navigated through 
  - `User Configuration > Policies > Adminstrative Templates > Desktop`
Enabled the **Desktop Wallpaper** policy
Stored the wallpaper image on a shared network location where all users have read access to the shard folder. File path is accessible from all domain users.
  - Set the wallpaper path `\\WINSERVER\Wallpapers\Window.jpg`
  - Selected wallpaper style to **Fit**

![Desktop Wallpaper](https://github.com/user-attachments/assets/1f85ea67-97d8-4170-b2e0-c8898ac975de)

## 2. Verification
- Verified the image was placed in the correct shared folder
- All domain users had **read acess** to both the share and the NTFS file
- Logged in as `csmith` to verify wallpaper

![Windows Wallpaper Applied](https://github.com/user-attachments/assets/c2f30a67-c5a1-4e60-982c-5298a56b7d6b)
