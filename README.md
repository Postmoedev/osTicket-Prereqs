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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create Azure Virtual Machine (Windows 10, 4 vCPUs)
- Install/Enable IIS in Windows
- Install PHP Manager for IIS and Rewrite Module
- Setup PHP and install VC_redist.x86.exe
- Install MySQL 5.5.62
- Configure IIS
- Install osTicket v1.15.8
- Enable PHP Extensions/Rename and Set Permissions
- Continue osTicket Setup and Install HeidiSQL
- Complete osTicket Setup and clean up


<h2>Installation Steps</h2>
<h3>Installation Files:</h3> 
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
<h3>Create Azure Virtual Machine (Windows 10, 4 vCPUs)</h3>
- <b>Name: Vm-osticket</b>
- <b>Username: labuser</b>
- <b>Password: Password of choice</b>
<h3>Install/Enable IIS in Windows</h3>
- <b>Install CGI and Common HTTP Features</b>
- <b>Enable IIS Management Console</b>

<h3>Install PHP Manager for IIS and Rewrite Module</h3>
- <b>Download and install PHPManagerForIIS_V1.5.0.msi</b>
- <b>Download and install rewrite_amd64_en-US.msi.</b>

<h3>Setup PHP and install VC_redist.x86.exe</h3>
- <b>Create directory C:\PHP</b>
- <b>Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip to C:\PHP(If youre having download issues try google chrome)</b>
- <b>Install VC_redist.x86.exe</b>

<h3>Install MySQL 5.5.62</h3>
- <b>Typical Setup with password:Password of choice</b>
- <b>Launch Configuration Wizard after install</b>
<h3>Configure IIS</h3>
- <b>Open IIS as Admin</b>
- <b>Register PHP within IIS</b>
- <b>Reload IIS (Stop and Start server)</b>

<h3>Install osTicket v1.15.8</h3>
- <b>Download osTicket from Installation Files</b>
- <b>Extract and copy "upload" folder to C:\inetpub\wwwroot, rename to "osTicket"</b>
- <b>Reload IIS</b>

<h3>Enable PHP Extensions/Rename and Set Permissions</h3>
- <b>Enable php_imap.dll, php_intl.dll, and php_opcache.dll in PHP Manager</b>
- <b>Refresh osTicket site in browser and notice the changes</b>
- <b>Rename ost-sampleconfig.php to ost-config.php</b>
- <b>Assign permissions to ost-config.php (Disable inheritance, New Permissions: Everyone -> All)</b>

<h3>Install HeidiSQL and Continue osTicket Setup</h3>
- <b>Download and install HeidiSQL from Installation Files</b>
- <b>Create new session (root/Password of choice) and connect</b>
- <b>Create database "osTicket"</b>

<h3>Complete osTicket Setup and Clean Up</h3>
- <b>Enter MySQL details (Database: osTicket, Username: root, Password: Password1)</b>
- <b>Click "Install Now!"</b>
- <b>Delete C:\inetpub\wwwroot\osTicket\setup</b>
- <b>Set Permissions to "Read" only for C:\inetpub\wwwroot\osTicket\include\ost-config.php</b>

<h3>Access osTicket</h3>
- <b> http://localhost/osTicket/scp/login.php</b>

-<b>End Users osTicket URL: http://localhost/osTicket/.</b>
