<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine with Windows 10
- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- Visual C++ Redistributable
- MySQL 5.5.62
- osTicket v1.15.8
- HeidiSQL

<h2>Installation Steps</h2>

### Step 1: Prepare the Virtual Machine

<p>
<img src="https://s1.ezgif.com/tmp/ezgif-1-08a9d2222c.gif" height="80%" width="80%" alt="Azure VM Configuration"/>
</p>
<p>
Log into your Azure VM using Remote Desktop. Download the `osTicket-Installation-Files.zip` onto the desktop and extract the files.
</p>
<br />

### Step 2: Enable IIS with CGI

<p>
<img src="https://s6.ezgif.com/tmp/ezgif-6-f411406fdc.gif" height="80%" width="80%" alt="Enable IIS with CGI"/>
</p>
<p>
Open **Control Panel** > **Programs** > **Turn Windows features on or off**. Enable Internet Information Services (IIS), including World Wide Web Services > Application Development Features > CGI.
</p>
<br />

### Step 3: Install Required Software

<p>
<img src="https://s6.ezgif.com/tmp/ezgif-6-c8f2b3f762.gif" height="80%" width="80%" alt="Install Prerequisites"/>
</p>
<p>
Install the following software from the extracted `osTicket-Installation-Files`:

1. PHP Manager for IIS
2. Rewrite Module
3. PHP 7.3.8 (unzip into `C:\PHP`)
4. Visual C++ Redistributable
5. MySQL 5.5.62 (set root password to `root`)
</p>
<br />

### Step 4: Configure IIS

<p>
<img src="https://s6.ezgif.com/tmp/ezgif-6-f03c10edf7.gif" height="80%" width="80%" alt="Configure IIS"/>
</p>
<p>
Open IIS as Administrator. Register PHP by selecting `C:\PHP\php-cgi.exe` in PHP Manager. Stop and restart the IIS server.
</p>
<br />

### Step 5: Install osTicket

<p>
<img src="https://s6.ezgif.com/tmp/ezgif-6-9b21e2f6cd.gif" height="80%" width="80%" alt="Install osTicket"/>
</p>
<p>
1. Copy the `upload` folder from `osTicket-v1.15.8.zip` to `C:\inetpub\wwwroot` and rename it to `osTicket`.
2. Browse to `http://localhost/osTicket` in your browser.
3. Enable PHP extensions: `php_imap.dll`, `php_intl.dll`, `php_opcache.dll`.
</p>
<br />

### Step 6: Finalize osTicket Configuration

<p>
<img src="https://s6.ezgif.com/tmp/ezgif-6-cee50efa58.gif" height="80%" width="80%" alt="Finalize Configuration"/>
</p>
<p>
1. Rename `ost-sampleconfig.php` to `ost-config.php` and set its permissions to **Full Control** for `Everyone`.
2. Complete the setup in the browser, providing the helpdesk name and default email.
</p>
<br />

### Step 7: Configure Database

<p>
<img src="https://s1.ezgif.com/tmp/ezgif-1-b7328bcb14.gif" height="80%" width="80%" alt="Configure Database"/>
</p>
<p>
1. Use HeidiSQL to create a new database named `osTicket`.
2. Enter database details during the osTicket setup: Database Name `osTicket`, Username `root`, Password `root`.
3. Click **Install Now!**
</p>
<br />

### Step 8: Post-Installation Cleanup

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Cleanup"/>
</p>
<p>
1. Delete the `setup` directory (`C:\inetpub\wwwroot\osTicket\setup`).
2. Set the `ost-config.php` file to **Read-Only**.
</p>
<br />

<h2>Accessing osTicket</h2>

- Admin Panel: `http://localhost/osTicket/scp/login.php` 🛠️
- End User Portal: `http://localhost/osTicket/` 🌟

<h2>Screenshots</h2>

<p>
Steps Overview:

1. Azure VM creation.
2. IIS configuration window.
3. PHP extension enablement.
4. Database setup in HeidiSQL.
5. osTicket final installation screen.
</p>

<h2>Conclusion 🎉</h2>
<p>
Congratulations! You have successfully installed and configured osTicket. With this powerful help desk tool, you can efficiently manage support tickets and improve customer service workflows. Happy troubleshooting! 🚀
</p>
