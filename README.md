<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

Part 1 (Create Virtual Machine in Azure)
- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
- When creating the VM, allow it to create a new Virtual Network (Vnet)

Part 2 (Installation)

- Connect to your Virtual Machine with Remote Desktop
- Install / Enable IIS in Windows
- Install Web Platform Installer (download from within lab files: link)
 1. Open after installation
 2. Add MySQL 5.5 (it will ask for credentials to be created later)
    1. Name: root
    2. Password: Password1
 3. Add All simple versions of x86 PHP up until 7.3
 4. Fix any failures if required (download from within lab files: link)
    1. Install PHP Version 7.3.8 (or any other version if necessary, archives)
    2. Install PHP Manager 1.5.0 for IIS 10 (folder you unzipped on the desktop)
    3. Install Microsoft Visual C++ 2009 Redistributable Package

Part 3 

Install osTicket v1.15.8
  1. Download osTicket (download from within lab files: link)
  2. Extract and copy the “upload” folder INTO c:\inetpub\wwwroot
  3. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Part 4 

 Reload IIS (Open IIS, Stop and Start the server)
  1. Go to sites -> Default -> osTicket
  2. On the right, click “Browse *:80”

Part 5 

Enable Extensions in IIS: Note that some extensions are not enabled

  1. Go back to IIS, sites -> Default -> osTicket
  2. Double-click PHP Manager
  3. Click “Enable or disable an extension”
     1. Enable: php_imap.dll
     2. Enable: php_intl.dll
     3. Enable: php_opcache.dll
 
Part 6 

Refresh the osTicket site in your browse, observe the changes
Rename:
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
Part 7 

Assign Permissions: ost-config.php

  1. Disable inheritance -> Remove All
  2. New Permissions -> Everyone -> All

Part 8 

Continue Setting up osTicket in the browser (click Continue)
  1. Name Helpdesk
  2. Default email (receives email from customers)

Part 9 

Download and Install HeidiSQL (download from within lab files: link)

  1. Create a new session, root/Password1
  2. Connect to the session
  3. Create a database called “osTicket”

Part 10 

Continue Setting up osticket in the browser
MySQL Database: osTicket

  1. MySQL Username: root
  2. MySQL Password: Password1

Part 11 

Click “Install Now!”
Congratulations, hopefully it is installed with no errors!
Clean up

  1. Delete: C:\inetpub\wwwroot\osTicket\setup
  2. Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)

Notes:
Browse to your help desk login page: http://localhost/osTicket/scp/login.php  
End Users osTicket URL: http://localhost/osTicket/ 



<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/VtcyxYU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
	
<img src="(https://i.imgur.com/zsiRqhS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
	
</p>
<p>

<h2>Summary of Steps 1</h2>	
	
Step 1 
	
* Connect to your Virtual Machine with Remote Desktop
* Install / Enable IIS in Windows
* Install Web Platform Installer (download from within lab files: link)
1. Open after installation
2. Add MySQL 5.5 (it will ask for credentials to be created later)
    * Name: root
    * Password: Password1
3. Add All simple versions of x86 PHP up until 7.3
4. Fix any failures if required (download from within lab files: link)
    * Install PHP Version 7.3.8 (or any other version if necessary, archives)
    * Install PHP Manager 1.5.0 for IIS 10 (folder you unzipped on the desktop)
    * Install Microsoft Visual C++ 2009 Redistributable Package
	
Step 2
	
Install osTicket v1.15.8
1. Download osTicket (download from within lab files: link)
2. Extract and copy the “upload” folder INTO c:\inetpub\wwwroot
3. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”


</p>
<br />

<p>
<img src="https://i.imgur.com/zsiRqhS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
	
<img src="https://i.imgur.com/zsiRqhS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>	
	
	
</p>
<p>
	
<h2>Summary of Steps 2</h2>	
	
Step 3
	
Reload IIS (Open IIS, Stop and Start the server)
1. Go to sites -> Default -> osTicket
2. On the right, click “Browse *:80”
	
Step 4
	
Enable Extensions in IIS: Note that some extensions are not enabled
1. Go back to IIS, sites -> Default -> osTicket
2. Double-click PHP Manager
3. Click “Enable or disable an extension”
    * Enable: php_imap.dll
    * Enable: php_intl.dll
    * Enable: php_opcache.dll

Step 5

Refresh the osTicket site in your browse, observe the changes Rename: From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/07Q8kYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
	
<h2>Summary of Steps 3</h2>	
	
Step 6

Assign Permissions: ost-config.php
1. Disable inheritance -> Remove All
2. New Permissions -> Everyone -> All

Step 7 

Continue Setting up osTicket in the browser (click Continue)
1. Name Helpdesk
2. Default email (receives email from customers)

Step 8

Download and Install HeidiSQL (download from within lab files: link)
1. Create a new session, root/Password1
2. Connect to the session
3. Create a database called “osTicket”

</p>
<br />

<p>
<img src="https://i.imgur.com/UXUbrhv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>Summary of Steps 4</h2>		
	
Step 9

Continue Setting up osticket in the browser MySQL Database: osTicket
1. MySQL Username: root
2. MySQL Password: Password1

Step 10

Click “Install Now!” Congratulations, hopefully it is installed with no errors! Clean up
1. Delete: C:\inetpub\wwwroot\osTicket\setup
2. Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
Notes: Browse to your help desk login page: http://localhost/osTicket/scp/login.php End Users osTicket URL: http://localhost/osTicket/

</p>
<br />


