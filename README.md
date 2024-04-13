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
<h3>Create Azure Virtual Machine (Windows 10, 4 vCPUs)</h3>
- <b>Name: Vm-osticket</b>

- <b>Username: labuser</b>

- <b>Password: Password of choice</b>

<h3>Install/Enable IIS in Windows</h3>
- <b>Install CGI and Common HTTP Features</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/8695a34a-2173-4a47-a82d-bdac3c597048)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/4b022c66-76fa-4975-a0bd-39e361f7d6f2)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/724e368a-4e23-4900-88d2-3a1586ef72f7)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/453270a3-631a-4681-8cb9-356e1a76d526)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/8b653bef-c306-4787-a1dc-0d380b6d577a)

- <b>Enable IIS Management Console</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/bdcb09ed-cd64-4294-852d-c7403d6e6381)

<h3>Install PHP Manager for IIS and Rewrite Module</h3>
- <b>Download and install PHPManagerForIIS_V1.5.0.msi</b>

- <b>Download and install rewrite_amd64_en-US.msi.</b>

<h3>Setup PHP and install VC_redist.x86.exe</h3>
- <b>Create directory C:\PHP</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/c367ec0a-a0ed-43a8-aa07-748cbdfae8a4)

- <b>Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip to C:\PHP(If youre having download issues try google chrome)</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/e4bcb7b3-b671-468b-a2c2-6ca2d9814624)

- <b>Install VC_redist.x86.exe</b>

<h3>Install MySQL 5.5.62</h3>
- <b>Typical Setup</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/0f27014c-9b02-48db-84b9-990ac330f450)

- <b>Launch Configuration Wizard after install</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/f8e9c103-87d3-4356-b9c9-3c748fe57274)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/1d6b622b-e536-44bd-8cd6-4ce1e354f80a)


<h3>Configure IIS</h3>
- <b>Open IIS as Admin</b>
- <b>Register PHP within IIS</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/0d5e01f4-d669-49e2-9df1-f23f9d95d777)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/ada9b849-1982-4c60-af64-9a96cd8ed4af)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/e5b437cd-7607-48d6-8745-4a26d68536fa)

- <b>Reload IIS (or Stop and Start server)</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/3102a16f-25e8-42f0-b7d2-a2b3eff8d3a6)

<h3>Install osTicket v1.15.8</h3>
- <b>Download osTicket-v.1.15.8.zip</b>
- <b>Extract and copy "upload" folder to C:\inetpub\wwwroot, rename to "osTicket"</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/856124c1-6928-49b6-9914-cc1a543a8de9)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/fe70d4cd-4f4d-4375-a131-ae345c6a1fea)

- <b>Reload IIS and Open osTicket site</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/57389668-57d6-427f-b525-b154ca3dd277)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/dce0f065-efd9-4326-9bd4-e34b338f57a9)

<h3>Enable PHP Extensions/Rename and Set Permissions</h3>
- <b>Enable php_imap.dll, php_intl.dll, and php_opcache.dll in PHP Manager</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/bf082b11-682f-4348-a9d8-6327c15446f1)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/cf0b47f1-acb7-4b80-ab0b-36e0a6c93b2c)

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/e89f4e3c-b996-40aa-9f8c-dcfb9093ef7b)

- <b>Refresh osTicket site in browser and notice the changes</b>

![image](https://github.com/Postmoedev/osTicket-Prereqs/assets/150564271/2f91e580-0df2-4328-839d-92b7ba27953a)


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
