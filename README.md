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

- Microsoft Azure
- Basic Knowledge of IIS (Information Internet Services)
- Remote Desktop Access
- osTicket Installalation Files
- HeidiSQL

<h2>Index of Procedures</h2>

- <a href="#Create_a_Virtual_Machine">Create a Virtual Machine</a>
- <a href="#Accessing_the_Virtual_Machine">Accessing the Virtual Machine</a>
- <a href="#Download_and_Prepare_Installation_Files">Download and Prepare Installation Files</a>
- <a href="#Install_Internet_Information_Services">Internet Information Services</a>
- <a href="#Install_Required_Files">Install Required Files</a>
- <a href="#Set_Up_PHP">Set Up PHP</a>
- <a href="#Install_MySQL">Install MySQL</a>
- <a href="#Configure_IIS">Configure IIS</a>
- <a href="#Install_osTicket">Install osTicket</a>
- <a href="#Configure_osTicket">Configure osTicket</a>
- <a href="#Reassign_Permissions">Reassign Permissions</a>
- <a href="#Complete_osTicket_Setup">Complete osTicket Setup</a> 
- <a href="#Install_HeidiSQL">Install HeidiSQL</a>
- <a href="#Finalize_osTicket_Installation">Finalize osTicket Installation</a>
- <a href="#Help_Desk_Ticket_Page">Help Desk Ticket Page</a>




<h2>Installation Steps</h2>
<h3><a id="Create_a_Virtual_Machine">1.) Create a Virtual Machine</a></h3> 

- In Microsoft Azure, we will create a Virtual Machine and make a new resource group, "osTicket".

- **VM Name:** osTicket-vm
- **Image:** Windows 10 Pro, version 22H2 - 64x Gen 2
- **Size:** 2 vCPUs, 8 Gig Memory Minimum 


<p>
<img src="https://imgur.com/thkBVC0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Check the licensing box and review & create the VM. No changes are needed for management, disks, or networking sections.

<p>
<img src="https://imgur.com/i51NX2S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Accessing_the_Virtual_Machine">2.) Accessing the Virtual Machine</a></h3>

- Log in to the VM using **Remote Desktop** with the credentials created during the VM setup.

  
<p>
<img src="https://imgur.com/Z3oafg3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3><a id="Download_and_Prepare_Installation_Files">3.) Download and Prepare Installation Files</a></h3>

- Within the VM, download the `osTicket-Installation-Files.zip` and unzip it to your desktop. The folder should be named `osTicket-Installation-Files`.

<p>
<img src="https://imgur.com/WdoV5ro.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Install_Internet_Information_Services">4.) Install Internet Information Services</a></h3>

- Open **Control Panel** -> **Programs** -> **Turn Windows features on or off**.
- Install/enable **IIS** with the following features:
  - **World Wide Web Services** -> **Application Development Features** -> [X] CGI
    
<p>
<img src="https://imgur.com/7rfQAMy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Install_Required_Files">5.) Install Required Files</a></h3>

  - From the `osTicket-Installation-Files` folder:
  - Install **PHP Manager for IIS**: `PHPManagerForIIS_V1.5.0.msi`.
 
<p>
<img src="https://imgur.com/8BFdHAE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

 - Install **Rewrite Module**: `rewrite_amd64_en-US.msi`.

<p>
<img src="https://imgur.com/PJ002kO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Set_Up_PHP">6.) Set Up PHP</a></h3>

- Create the directory `C:\PHP`.

<p>
<img src="https://imgur.com/wjwAhlW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Unzip `PHP 7.3.8` (`php-7.3.8-nts-Win32-VC15-x86.zip`) into the `C:\PHP` folder.
  
<p>
<img src="https://imgur.com/DOp8eDG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Install `VC_redist.x86.exe`.
  
<p>
<img src="https://imgur.com/kccrQOz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Install_MySQL">7.) Install MySQL</a></h3>

- From the `osTicket-Installation-Files` folder, install MySQL 5.5.62 (`mysql-5.5.62-win32.msi`).
  - Select **Typical Setup**.
  - Launch the Configuration Wizard:
    - **Standard Configuration**
    - Input a username and password, take note of this!
      
<p>
<img src="https://imgur.com/HvicKTg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://imgur.com/BijVEdY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Configure_IIS">8.) Configure IIS</a></h3>

- Open IIS as an administrator.
- Register PHP:
  - Go to **PHP Manager** -> Register PHP path -> `C:\PHP\php-cgi.exe`.
- Reload IIS (Stop and Start the server).

<p>
<img src="https://imgur.com/f4GzaFH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Install_osTicket">9.) Install osTicket</a></h3>

- From the `osTicket-Installation-Files` folder:
  - Unzip `osTicket-v1.15.8.zip`.
  - Copy the `upload` folder into `C:\inetpub\wwwroot`.
  - Rename the `upload` folder to `osTicket`.
- Reload IIS (Stop and Start the server).
  
<p>
<img src="https://imgur.com/uEfA8pX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Configure_osTicket">10.) Configure osTicket</a></h3>

- Open IIS:
  - Navigate to **Sites** -> **Default** -> **osTicket**.
  - On the right, click **Browse *:80**.
    
<p>
<img src="https://imgur.com/R0gulKz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Some extensions that are not enabled. Return to IIS:
  - Navigate to **Sites** -> **Default** -> **osTicket**.
  - Double-click **PHP Manager** -> Click **Enable or disable an extension**.
  - Enable the following extensions:
    - `php_imap.dll`
    - `php_intl.dll`
    - `php_opcache.dll`
      
<p>
<img src="https://imgur.com/yASbzid.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Reassign_Permissions">11.) Reassign Permissions</a></h3>

- Rename `ost-config.php`:
  - From: `C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php`
  - To: `C:\inetpub\wwwroot\osTicket\include\ost-config.php`.

<p>
<img src="https://imgur.com/d79Eowd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Assign Permissions:
  - Disable inheritance -> Remove all permissions.
  - Add new permissions -> **Everyone** -> **Full control**.
    
<p>
<img src="https://imgur.com/lRs0y2G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Complete_osTicket_Setup">12.) Complete osTicket Setup</a></h3>

- In the browser, continue the osTicket setup:
  - Set **Helpdesk Name**.
  - Set **Default email** (receives emails from customers).

<p>
<img src="https://imgur.com/ESTjfKy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h3><a id="Install_HeidiSQL">13.) Install HeidiSQL</a></h3>

- From the `osTicket-Installation-Files` folder, install **HeidiSQL**.
- Open HeidiSQL:
  - Create a new session: Enter previously used username and password
  - Connect to the session.
  - Create a database named `osTicket`.
    
<p>
<img src="https://imgur.com/BSoM9eB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://imgur.com/BfQLaku.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>



<h3><a id="Help_Desk_Ticket_Page">14.) Verify Completion</a></h3>

- Access your help desk login page: `http://localhost/osTicket/scp/login.php`.
  
<p>
<img src="https://imgur.com/mKB9bH6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Conclusion</h2>

In summary, you have installed and configured osTicket on your virtual machine. Your help desk system is now ready to use.

<br />
