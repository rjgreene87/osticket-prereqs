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
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />
Click on "Virtual Machine" from the search results and then click "Create" on the next screen.
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Follow the prompts to configure your virtual machine, including the subscription, resource group, virtual machine name, region, size, and other settings.
Choose "Windows 10" as the base image for your virtual machine.
Complete the wizard and wait for the virtual machine to be created.
</p>
<br />
<p>
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>



Step 2: Connect to the Azure Virtual Machine

Once the virtual machine is created, click on "Virtual machines" in the Azure portal.

Launch the Remote Desktop Protocol (RDP) file and open it.(In Win go to start menu and type in remote desktop in search bar.)

Enter the credentials for your Azure account when prompted and click "OK."
You will now be connected to your Azure Virtual Machine.
  
  
  
Step 3 : Installing the prerequisites
