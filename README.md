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

- <a href="#Install_Internet_Information_Services">Internet Information Services</a>
- <a href="#Install_PHP_Manager">Install PHP Manager</a>
- <a href="#Rewrite_Module_Install">Rewrite Module Install</a>
- <a href="#Create_PHP_Directory">Create PHP Directory</a>
- <a href="#Install_Visual_C++">Install Visual C++</a>
- <a href="#Install_MySQL">Install MySQL</a>
- <a href="#Register_PHP_within_IIS">Register PHP within IIS</a>
- <a href="#Install_osTicket">Install osTicket</a>
- <a href="#Install_MySQL">Install MySQL</a>
- <a href="Register_PHP_within_IIS">Register PHP within IIS</a>
- <a href="Install_osTicket">Install osTicket</a>
- <a href="Load_osTicket_Site">Load osTicket Site</a>
- <a href="Enable_PHP_Extensions">Enable PHP Extensions</a>
- <a href="Reassign_Permissions">Reassign Permissions</a>
- <a href="Install_HeidiSQL">Install HeidiSQL</a>
- <a href="osTicket_Installed">osTicket Installed</a>
- <a href="Help_Desk_Ticket_Page">Help Desk Ticket Page</a>




<h2>Installation Steps</h2>

<h3><a id="Install_Internet_Information_Services">Install Internet Information Services</a></h3>
<p>
<img src="https://imgur.com/7rfQAMy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Beginning the installation of osTicket, a prerequsite is the enabling of Intenet Information Services (IIS). This is done by loading the Control Panel from the Windows Start Up Key. Within the Control Panel, clicking on Programs then Programs and Features gets you to a new window where IIS can be turned on. CGI must also be alllowed. From the IIS drop down, click World Web Management, click Application Development Features, this is where CGI can be enabled.
</p>
<br />

<h3><a id="Install_PHP_Manager">Install PHP Manager</a></h3>
<p>
<img src="https://imgur.com/8BFdHAE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
PHP Manager is a tool to set up and mangage PHP, which is a programming langauge. PHP Manager allows specific extensions from the configuration to be enabled or disabled, making it easy to add or remove features. Installing PHP Manager now allows for future access when registering from inside IIS to ensure optimal running of the server. 
</p>
<br />

<h3><a id="Rewrite_Module_Install">Rewrite Module Install</a></h3>
<p>
<img src="https://imgur.com/PJ002kO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When you install the URL Rewrite Module on IIS, it allows you to create clear and easy-to-read URLs for your website. This makes it simpler to manage redirects, which helps ensure visitors are sent to the correct pages, even if the URLs change. As well, the module helps organize the structure of your URLs, reducing the risk of broken links or confusion for both users and search engines.
</p>
<br />

<h3><a id="Create_PHP_Directory">Create PHP Directory</a></h3>
<p>
<img src="https://imgur.com/wjwAhlW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Install_Visual_C++">Install Visual C++</a></h3>
<p>
<img src="https://imgur.com/kccrQOz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Install_MySQL">Install MySQL</a></h3>
<p>
<img src="https://imgur.com/HvicKTg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Register_PHP_within_IIS">Register PHP within IIS</a></h3>
<p>
<img src="https://imgur.com/f4GzaFH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Install_osTicket">Install osTicket</a></h3>
<p>
<img src="https://imgur.com/uEfA8pX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Load_osTicket_Site">Load osTicket Site</a></h3>
<p>
<img src="https://imgur.com/R0gulKz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Enable_PHP_Extensions">Enable PHP Extensions</a></h3>
<p>
<img src="https://imgur.com/yASbzid.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Reassign_Permissions">Reassign Permissions</a></h3>
<p>
<img src="https://imgur.com/lRs0y2G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Install_HeidiSQL">Install HeidiSQL</a></h3>
<p>
<img src="https://imgur.com/BSoM9eB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="osTicket_Installed">osTicket Installed</a></h3>
<p>
<img src="https://imgur.com/LmekkHM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h3><a id="Help_Desk_Ticket_Page">Help Desk Ticket Page</a></h3>
<p>
<img src="https://imgur.com/mKB9bH6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
