## 📁 Virtualbox Shared Folder Configuration & Troubleshooting

## Objective

Configure a shared folder between Windows 11 and Kali Linux using Oracle VirtualBox.

## Environment

-  Windows 11
-  Kali Linux
-  Oracle VirtualBox

## Initial Configuration

I created the initial **Cybersecurity_Portfolio** folder on the Windows host and began configuring it as a VirtualBox shared folder in Oracle VirtualBox. I enabled the shared folder so it could be accessed from my Kali Linux virtual machine.
This was my first attempt.

![Figure 1. Initial VirtualBox shared folder configuration.](Screenshots/011_operation-error.png)


## Problem
After configuring the shared folder, I attempted to transfer screenshots from Kali Linux to the VirtualBox shared folder. Instead of transferring the files successfully, I received the following error:

**Operation not permitted**

## Troubleshooting

![Figure 2. Initial VirtualBox shared folder configuration.](Screenshots/02_verified-shared-folder.png)


- Verified VirtualBox shared folder mount

-  I verified that the VirtualBox shared folder was mounted and accessible by checking the /media directory and locating the sf_Cybersecurity_Portfolio shared folder. This confirmed that the shared folder was present and could view it's contents.

![Figure 3. Initial VirtualBox shared folder configuration.](Screenshots/03_verified-user-groups.png)

-  The user groups were checked here to determine whether my Linux user had the permissions required to access a VirtualBox shared folder. Specifically I was looking for the vboxsf group, to ensure permissions.

![Figure 4. Initial VirtualBox shared folder configuration.](Screenshots/04_verify_write_access_to_sharedfolder.png)

- I tested write access ti the VirtualBox shared folder by attempting to create a file. The operation failed with an **Operation not permitted** erorr, indicayinh yhat write access was restricted.

-  Checked the shared folder mount

-  Confirmed my user belonged to the 'vboxsf' group

-  Tested write permissions

-  Reconfigured the shared folder

  ## Skills Demonstrated

-  Linux

-  VirtualBox

-  Troubleshooting

-  File Permissions

-  Windows/Linux Inegration

- ## Outcome
- Successfully configured a working shared folder between Windows and Kali Linux.

