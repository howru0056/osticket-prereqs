<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/LOzmM5ZjKi0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install / Enable IIS in Windows WITH CGI
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- MySQL 5.5.62
- osTicket v1.15.8
- Same Installation files used in the tutorial, you can use them if you don't want variables in your installation. 
 https://drive.google.com/drive/folders/1jP7oYPvIAqQPyzKEP912DiJ1sSUQJmbb?usp=sharing

<h2>Installation Steps</h2>

<p>
</p>
<p>
Step 1 Create Virtual Machine in Azure
- Create a Resource Group
- Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs with a new Virtual Network (Vnet)
  - Name: Vm-osticket
  - Username: labuser (for example/whatever you chose)
  - Password: osTicketPassword1! (for example/whatever you chose)

</p>
<br />

<p>
<img src="https://i.imgur.com/tVzhLQc.png" height="80%" width="80%" />
<img src="https://i.imgur.com/toKC8xE.png" height="80%" width="80%" />
<img src="https://i.imgur.com/ujDJKZW.png" height="80%" width="80%" />
<img src="https://i.imgur.com/ALh597D.png" height="80%" width="80%" />
</p>
<p>
Step 2 Install / Enable IIS in Windows WITH CGI
- World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/NvK35hU.png" height="80%" width="80%" />
</p>
<p>
Step 3 Create the directory C:\PHP
- Create the directory C:\PHP

</p>
<br />

<p>
<img src="https://i.imgur.com/Z3e5wdX.png" height="80%" width="80%" />
</p>
<p>
Step 4 Download and install
- Download and install (PHPManagerForIIS_V1.5.0.msi) https://drive.google.com/file/d/1VizgW40b2A6ndsOh0RE4sASGbfOa54rg/view?usp=drive_link
</p>
<br />

<p>
<img src="https://i.imgur.com/LmmaKIZ.png" height="80%" width="80%" />
</p>
<p>
Download and install the Rewrite Module (rewrite_amd64_en-US.msi) https://drive.google.com/file/d/1bF7qvZlsmzSpX2ApytklyoU91P8FdXwg/view?usp=drive_link
</p>
<br />

<p>
<img src="https://i.imgur.com/vjVDFcn.png" height="80%" width="80%" />
</p>
<p>
Download and install download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) https://drive.google.com/file/d/1UGPXw3MQ6rU7J7vqVkJIupUo29q-t7ch/view?usp=drive_link
</p>
<br />

<p>
<img src="https://i.imgur.com/Ozdxb1f.png" height="80%" width="80%" />
</p>
<p>
Download and install VC_redist.x86.exe (VC_redist.x86.exe) https://drive.google.com/file/d/1B08-Aqn1RKYaP1D_R_JFJnuF78R-9Y5r/view?usp=drive_link
</p>
<br />

<p>
<img src="https://i.imgur.com/ggUgsY2.png" height="80%" width="80%" />
<img src="https://i.imgur.com/FIU4sGf.png" height="80%" width="80%" />
<img src="https://i.imgur.com/smT3wQg.png" height="80%" width="80%" />
</p>
<p>
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) https://drive.google.com/file/d/1B08-Aqn1RKYaP1D_R_JFJnuF78R-9Y5r/view?usp=drive_link
- Typical Setup -> 
- Launch Configuration Wizard (after install) -> 
- Standard Configuration -> 
- Password1
</p>
<br />

<p>
<img src="https://i.imgur.com/b8lfYNC.png" height="80%" width="80%" />
</p>
<p>
Step 5 Open IIS as an Admin 
</p>
<br />

<p>
<img src="https://i.imgur.com/M6bfZa1.png" height="80%" width="80%" />
<img src="https://i.imgur.com/Kw4uZT2.png" height="80%" width="80%" />
</p>
<p>
Step 6 Register PHP from within IIS 
</p>
<br />

<p>
<img src="https://i.imgur.com/b8lfYNC.png" height="80%" width="80%" />
</p>
<p>
Step 7 Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/PCAWafn.png" height="80%" width="80%" />
<img src="https://i.imgur.com/TTtLiI6.png" height="80%" width="80%" />
<img src="https://i.imgur.com/xZBsvMl.png" height="80%" width="80%" />
<img src="https://i.imgur.com/kcgVgp0.png" height="80%" width="80%" />
</p>
<p>
Step 8 Install osTicket v1.15.8 (osTicket-v1.15.8.zip)
- Download osTicket from the Installation Files Folder https://drive.google.com/file/d/1CY9JJb5o8HJhPGNfjs6XKOckqRI3bF83/view?usp=drive_link
- Extract and copy “upload” folder to c:\inetpub\wwwroot 
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/b8lfYNC.png" height="80%" width="80%" />
</p>
<p>
Step 9 Reload IIS, Again (Open IIS, Stop and Start the server) 

</p>
<br />

<p>
<img src="https://i.imgur.com/R4KfM2k.png" height="80%" width="80%" />
</p>
<p>
Step 10 Go to sites -> Default -> osTicket 
- On the right, click “Browse *:80”
</p>
<br />

<p>
<img src="https://i.imgur.com/ORDaiw1.png" height="80%" width="80%" />
<img src="https://i.imgur.com/CEuxr4t.png" height="80%" width="80%" />
<img src="https://i.imgur.com/V13zEhb.png" height="80%" width="80%" />
<img src="https://i.imgur.com/i27JyEy.png" height="80%" width="80%" />
<img src="https://i.imgur.com/mNRHH3C.png" height="80%" width="80%" />
<img src="https://i.imgur.com/JvXvH1A.png" height="80%" width="80%" />
<img src="https://i.imgur.com/KDBv3F6.png" height="80%" width="80%" />
</p>
<p>
Step 11 Enable this  extensions
- Go back to IIS, sites -> Default -> osTicket 
- Double-click PHP Manager 
- Click “Enable or disable an extension” 
    - Enable: php_imap.dll 
    - Enable: php_intl.dll 
    - Enable: php_opcache.dll 
- Refresh the osTicket site in your browse, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/RIvZRK6.png" height="80%" width="80%" />
</p>
<p>
Step 12 Rename: ost-config.php 
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php 
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php 
</p>
<br />
<p>
<img src="https://i.imgur.com/adouShK.png" height="80%" width="80%" 
<img src="https://i.imgur.com/OFvTeKJ.png" height="80%" width="80%"
<img src="https://i.imgur.com/HR8ygCg.png" height="80%" width="80%"
</p>
<p>
Step 13 Assign Permissions: ost-config.php 
- Disable inheritance -> Remove All 
- New Permissions -> Everyone -> All
</p>
<br />

<p>
<img src="https://i.imgur.com/F8cZTuw.png" height="80%" width="80%" 
</p>
<p>
Step 14 Continue Setting up osTicket in the browser (click Continue) 
- Name Helpdesk 
- Default email (receives email from customers)
</p>
<br />

<p>
<img src="https://i.imgur.com/9w55WkV.png" height="80%" width="80%" 
</p>
<p>
<img src="https://i.imgur.com/3T2C9uF.png" height="80%" width="80%" 
</p>
<img src="https://i.imgur.com/KDBv3F6.png" height="80%" width="80%"
<p>
Step 15 Download and install HeidiSQL
https://drive.google.com/file/d/1RRGvv9V7vnJUFtMhelfk0Gcw38ZgDB1a/view?usp=drive_link
- Open Heidi SQL 
- Create a new session, root/Password1 
- Connect to the session 
- Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/4mQA89F.png" height="80%" width="80%"
</p>
<p>
Step 16 Continue Setting up osticket in the browser 
- MySQL Database: osTicket 
- MySQL Username: root 
- MySQL Password: Password1 
- Click “Install Now!”
</p>
<br />

<p>
<img src="https://i.imgur.com/zD6R6m3.png" height="80%" width="80%" 
</p>
<p>
Congratulations 
- Hopefully it is installed with no errors! 
- Browse to your help desk login page: http://localhost/osTicket/scp/login.php
- End Users osTicket URL: - http://localhost/osTicket/ 
</p>
<br />
