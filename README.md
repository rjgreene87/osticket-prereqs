# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will explain the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Prerequisites</h2>

- HeidiSQL_12.3.0.6589_Setup.exe
- mysql-5.5.62-win32.msi
- osTicket-v1.15.8
- php-7.3.8-nts-Win32-VC15-x86
- PHPManagerForIIS_V1.5.0.msi
- rewrite_amd64_en-US.msi"
- VC_redist.x86.exe

<h2>Installation Steps</h2>
Step 1: Create an Azure Virtual Machine
<p>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on "Create a resource" in the upper left corner and search for "Virtual Machine.
<p>
  <img src="https://i.imgur.com/R7xUmV5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on "Virtual Machine" from the search results and then click "Create" on the next screen.
<p>
  <img src="https://i.imgur.com/nzJmoAn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Follow the prompts to configure your virtual machine, including the subscription, resource group, virtual machine name, region, size, and other settings.
Choose "Windows 10" as the base image for your virtual machine.
Complete the wizard and wait for the virtual machine to be created.




Step 2: Connect to the Azure Virtual Machine

Once the virtual machine is created, click on "Virtual machines" in the Azure portal.

Launch the Remote Desktop Protocol (RDP) file and open it.(In Win go to start menu and type in remote desktop in search bar.)
<p>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enter the credentials for your Azure account when prompted and click "OK."
You will now be connected to your Azure Virtual Machine.
  
Step 3 : Installing the prerequisites

From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
  (If you get a prompt verify to keep file, choose keep file.)
  
  
  Download and install VC_redist.x86.exe.

Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Password1

  
 
  
  
  Step 4 : Open IIS in windows search bar (right click run as admin)
 <p>
  <img src="https://i.imgur.com/67dq6fQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />
 
Register PHP from within IIS

Reload IIS (Open IIS, Stop and Start the server)

Step 5 : Install osTicket v1.15.8
<p>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”



Reload IIS (Open IIS, Stop and Start the server)


Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Some extensions are not enabled by default
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All


Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)


From the Installation Files, download and install HeidiSQL.
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”



Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”


The installation should is now complete
Browse to your help desk login page: http://localhost/osTicket/scp/login.php
