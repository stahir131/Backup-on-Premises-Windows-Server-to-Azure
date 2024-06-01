<h3><p align="center"><b>Backup on-Premises Windows Server to Azure</b></p></h3>h3>
This tutorial describes how to backup an on-premises Windows server to Azure using Microsoft Azure Recovery Services(MARS).<br />
<b>Step1: Login to Azure</b>
<br />
<b>Step2: Create a Recovery Services vault</b>
<br />
Recovery services vault is a management entity that stores recovery points that are created over time and provides an interface to perform backup-related operations.
Search for <b>Backup and Site Recovery</b> and create Service vault<br />

<b>Step3: Download Recovery Services Agent</b>
Go to the created Vault -> Backup -> select On-Premises
<br />
What do you want to backup -> Files and Folders & system state

Click on <b>Prepare Infrastructure
</b>
<br />
Click on Download Agent for Windows server or WIndows client to download MARS
Before running the MARS, download the Vault credentials to register the server to the vault.
![bk1](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/3919dc0b-b1b2-4a10-b7f0-07f726787dfc)

![bk2](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/50d875aa-236e-4530-af0f-2cece8eae3ff)
![bk3](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/add63189-293f-4b10-9850-4aa1beaf606d)
Proceed to Registration
![bk4](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/e43f51df-af47-4b7f-a81a-867c9685fdb4)

Browse to the downloaded Vault credential<br />
Create passphrase and save on azure vault or local to pc
<br />
Click Finish.
![bk5](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/decb2428-ec4f-4033-b6f2-54912f371c40)

![bk6](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/a8c45742-8e40-4d05-aa33-88d1890cbfb4)

![bk7](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/915aeaff-567d-43db-941b-abcdb547780d)

Open the Microsoft Azure backup from the server
<br />
Click Schedule Backup
<br />
Select items to backup > Add items and Next
<br />
Specify backup schedule for system state
<br />
Select retention policy for system state
<br />
Specify backup schedule for Files and folders
<br />
Select retention policy for files and folders
<br />
Choose initial backup type > Online, offline
<br />
Confirmation
<br />
Run a backup from the program

![bk8](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/453fdec7-1a83-45dc-9eb7-afaf41fafb21)

<b>Recovering data</b>
<br />
Deleting all the files and folders from the local server and restoring it back
<br />
Click on Recover data
<br />
- Select Recovery location > Primary region</br>
- Select recovery mode > Individual files and folders
<br />
- Select volume and date > Backups are available for the bolded date
<br />
- Click Mount
<br />
Browse to the Mounted volume
<br />
Unmount when done.

![bk9](https://github.com/stahir131/Backup-on-Premises-Windows-Server-to-Azure/assets/64047385/bd80b3e1-10b9-47d8-a201-ab63b37c5672)

To stop using an existing backup schedules and delete all of the stored backups
-  Click on Schedule backup wizard
-  Stop backup schedules and delete all of the stored backups


