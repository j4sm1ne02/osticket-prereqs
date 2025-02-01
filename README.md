<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### YouTube: How To Install osTicket with Prerequisites (https://www.youtube.com](https://youtu.be/fWX1Lj-rOa0?si=1UfaxfmKtDNqbymo)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/99982be6-01f7-4a1d-9563-8d0b8b2d84e5" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/b468cf2e-81f0-4438-a4da-e226051376d8" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: osTicketPassword1!

Log into the VM with Remote Desktop
<br />

<p>
<img width="292" alt="image" src="https://github.com/user-attachments/assets/907da8d5-a993-45c5-85e8-e4fcab1d1329" />
<img <img width="473" alt="image" src="https://github.com/user-attachments/assets/c7703355-59f8-4c0c-b92a-075bb19e3661" />

</p>
<p>
Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto our desktop. The folder should be called “osTicket-Installation-Files
</p>
<br />


<p>
<img <img width="551" alt="image" src="https://github.com/user-attachments/assets/9bf0389e-2c6d-4620-b959-d45d40a7c63f" />

</p>
<p>
Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />

<p>
<img width="551" alt="image" src="https://github.com/user-attachments/assets/58b6236c-556f-4ab4-a720-bb30cb441810" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS 
</p>
<br />

<p>
<img <img width="462" alt="image" src="https://github.com/user-attachments/assets/c5936654-6434-4b43-b11b-810eedd6ad9f" />

</p>
<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module
</p>
<br />

<p>
<img width="482" alt="image" src="https://github.com/user-attachments/assets/8e33a6e8-5a2b-4691-a309-9e7351668dff" />
<img width="485" alt="image" src="https://github.com/user-attachments/assets/be9fe423-cc3a-4f0b-a7f8-89ce5406d8cf" />

</p>
<p>
Create the directory C:\PHP

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 
</p>
<br />

<p>
<img width="412" alt="image" src="https://github.com/user-attachments/assets/98158c7a-2ad4-44fa-ad1c-56f26d8b5f2f" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<br />

<p>
<img width="378" alt="image" src="https://github.com/user-attachments/assets/3b61dc73-c02a-4ef3-bb87-f7151361252f" />
<img width="369" alt="image" src="https://github.com/user-attachments/assets/5ffa9e96-b3a3-40e1-bba3-ae0d274d0036" />
<img width="373" alt="image" src="https://github.com/user-attachments/assets/1ca0a8b8-26ab-4848-b76e-3720fd8a91bb" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->

Launch Configuration Wizard (after install) ->

Standard Configuration ->

Username: root
Password: root
</p>
<br />

<p>
<img width="861" alt="image" src="https://github.com/user-attachments/assets/58005100-dbd0-490a-ba1f-951c0040f128" />

</p>
<p>
Open IIS as an Admin
<br />

<p>
<img width="539" alt="image" src="https://github.com/user-attachments/assets/03a9e516-e6dd-4258-83a2-c137b6880832" />

</p>
<p>
Register PHP from within IIS and then Reload IIS (Open IIS, Stop and Start the server)

</p>
<br />

<p>
<img width="477" alt="image" src="https://github.com/user-attachments/assets/2fb5a81f-6608-4b6d-9e1e-a505bb434f70" />
<img width="475" alt="image" src="https://github.com/user-attachments/assets/83c9ecdd-3036-40f8-80fa-e5fc84fc456e" />
<img width="295" alt="image" src="https://github.com/user-attachments/assets/cf28af4b-b5ce-4d1d-93f4-a1854a9767b7" />

</p>
<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder,unzip “osTicket-v1.15.8.zip” 

and copy the “upload” folder into “c:\inetpub\wwwroot”

Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img width="476" alt="image" src="https://github.com/user-attachments/assets/b8da740f-c1ab-43c7-8d4b-fe0598663e42" />

</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img width="445" alt="image" src="https://github.com/user-attachments/assets/d6983ffc-3e78-4f90-ba11-1856da3bac05" />

</p>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<br />

<p>
<img width="348" alt="image" src="https://github.com/user-attachments/assets/981beda0-eafa-466f-bfb0-33de94a598cd" />
<img width="325" alt="image" src="https://github.com/user-attachments/assets/bfd9141f-c5e7-4243-aed5-ab8748330031" />
</p>
<p>
Note that some extensions are not enabled

Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”

Enable: php_imap.dll

Enable: php_intl.dll

Enable: php_opcache.dll

Refresh the osTicket site in your browser, observe the changes

</p>
<br />

<p>
<img width="153" alt="image" src="https://github.com/user-attachments/assets/547bc863-ef59-45d6-8a1c-27ac96a3baa3" />

</p>
<p>
Rename: ost-config.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img width="578" alt="image" src="https://github.com/user-attachments/assets/66b178f8-210b-482a-a471-952e637e4b61" />
<img width="575" alt="image" src="https://github.com/user-attachments/assets/78708a0a-c95d-49b7-bba5-90897c6d5274" />
</p>
<p>
Assign Permissions: ost-config.php

Disable inheritance -> Remove All

New Permissions -> Everyone -> All

For lab purposes, I put permissions for everyone. In the real world, DO NOT assign everyone perms.
</p>
<br />

<p>
<img width="504" alt="image" src="https://github.com/user-attachments/assets/6f10b1aa-a7c8-48cc-b70a-fe59e199718a" />
<img width="512" alt="image" src="https://github.com/user-attachments/assets/f3e4f15a-53cc-492e-b1c0-00d414a8c1d2" />
<img width="307" alt="image" src="https://github.com/user-attachments/assets/707db4a7-b7f2-4084-9420-e715282c15c6" />


</p>
<p>
Install HeidiSQL
  
Open Heidi SQL

Create a new session, root/root

Connect to the session

Create a database called “osTicket”

</p>
<br />

<p>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/51787611-6da4-41e9-abfa-fe91fb52d47e" />
<img width="550" alt="image" src="https://github.com/user-attachments/assets/8fd0ed09-271d-4bf3-9158-7546f202cee0" />

</p>
<p>
After it's installed, you are able to sign in and view tickets :)
</p>
<br />
