<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

---

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
<p align="center">
<img src="https://via.placeholder.com/436x283.png" alt="Prepare the Virtual Machine" />
</p>
*Click [here](https://www.youtube.com/embed/joWKatENCsM) to watch a video demo.*  
Log into your Azure VM using Remote Desktop. Download the `osTicket-Installation-Files.zip` onto the desktop and extract the files.

---

### Step 2: Enable IIS with CGI
<p align="center">
<img src="https://via.placeholder.com/436x245.png" alt="Enable IIS with CGI" />
</p>
*Click [here](https://www.youtube.com/embed/QGpSbkNHU64) to watch a video demo.*  
Open **Control Panel** > **Programs** > **Turn Windows features on or off**. Enable Internet Information Services (IIS), including World Wide Web Services > Application Development Features > CGI.

---

### Step 3: Install Required Software
<p align="center">
<img src="https://via.placeholder.com/436x272.png" alt="Install Required Software" />
</p>
*Click [here](https://www.youtube.com/embed/XW3_hLmNqw4) to watch a video demo.*  
Install the following software from the extracted `osTicket-Installation-Files`:

1. PHP Manager for IIS
2. Rewrite Module
3. PHP 7.3.8 (unzip into `C:\PHP`)
4. Visual C++ Redistributable
5. MySQL 5.5.62 (set root password to `root`)

---

### Step 4: Configure IIS
<p align="center">
<img src="https://via.placeholder.com/436x245.png" alt="Configure IIS" />
</p>
*Click [here](https://www.youtube.com/embed/8Af_7j-RluA) to watch a video demo.*  
Open IIS as Administrator. Register PHP by selecting `C:\PHP\php-cgi.exe` in PHP Manager. Stop and restart the IIS server.

---

### Step 5: Install osTicket
<p align="center">
<img src="https://via.placeholder.com/436x245.png" alt="Install osTicket" />
</p>
*Click [here](https://www.youtube.com/embed/YOsfQ_rJHeg) to watch a video demo.*  

1. Copy the `upload` folder from `osTicket-v1.15.8.zip` to `C:\inetpub\wwwroot` and rename it to `osTicket`.
2. Browse to `http://localhost/osTicket` in your browser.
3. Enable PHP extensions: `php_imap.dll`, `php_intl.dll`, `php_opcache.dll`.

---

### Step 6: Finalize osTicket Configuration
<p align="center">
<img src="https://via.placeholder.com/436x245.png" alt="Finalize osTicket Configuration" />
</p>
*Click [here](https://www.youtube.com/embed/7MyEU8pb7wk) to watch a video demo.*  

1. Rename `ost-sampleconfig.php` to `ost-config.php` and set its permissions to **Full Control** for `Everyone`.
2. Complete the setup in the browser, providing the helpdesk name and default email.

---

### Step 7: Configure Database
<p align="center">
<img src="https://via.placeholder.com/436x245.png" alt="Configure Database" />
</p>
*Click [here](https://www.youtube.com/embed/17qpEZ-EeKY) to watch a video demo.*  

1. Use HeidiSQL to create a new database named `osTicket`.
2. Enter database details during the osTicket setup: Database Name `osTicket`, Username `root`, Password `root`.
3. Click **Install Now!**

---

<h2>Accessing osTicket</h2>

- Admin Panel: `http://localhost/osTicket/scp/login.php` 🛠️  
- End User Portal: `http://localhost/osTicket/` 🌟  

---

<h2>Screenshots</h2>

Steps Overview:

1. Azure VM creation.
2. IIS configuration window.
3. PHP extension enablement.
4. Database setup in HeidiSQL.
5. osTicket final installation screen.

---

<h2>Conclusion 🎉</h2>
Congratulations! You have successfully installed and configured osTicket. With this powerful help desk tool, you can efficiently manage support tickets and improve customer service workflows. Happy troubleshooting! 🚀
