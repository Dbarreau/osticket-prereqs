reference https://github.com/joshmadakorcc



<p align="center"> 
<img src="https://user-images.githubusercontent.com/121436228/210884823-1be4a783-9e4e-4a3b-944c-7d95681b3756.jpeg"/>
</p>
<p> 
</p>
<p> 
</p>
<p> 
</p>


<h1>osTicket - Prerequisites and Installation</h1>
This repository displays the tutorial of the osTicket's installation and its rudiments (prerequisites). The first rudiment begins with composing a virtual machine via Microsoft Azure. After that, there is a series of programs to support osTicket Ticketing System: IIS, Web Platform Installer, and HeidiSQL.<br />


<h2><img src="https://user-images.githubusercontent.com/121436228/209778109-d136551c-80f5-4185-a43b-fd1bab7a2fcb.png">
Video Demonstration<img src="https://user-images.githubusercontent.com/121436228/209778109-d136551c-80f5-4185-a43b-fd1bab7a2fcb.png"></h2> 
  
- ###  [YouTube: How To Install osTicket With Prerequisites](https://www.youtube.com/watch?v=ceEH3uJY5a0)
- ###  [YouTube: How To Create A Virtual Machine: First Prerequisite](https://youtu.be/YGWak28859s)

<h2>👨‍💻Environments and Technologies Used👨‍💻</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>💻Operating Systems Used💻 </h2>

- Windows 10 Pro</b> (21H2)

<h2>📋List of Prerequisites📋</h2>

- Install a Virtual Machine with Microsoft Azure
- Install Web Server: Internet Information Service (IIS)
- Install Web Platform Installer
- Install Files: PHP Manager and Microsoft Visual C ++
- Install the osTicket Installer
- Install HeidiSQL
- Eliminate the osTicket's "Setup" Directory

<h2><img src="https://user-images.githubusercontent.com/121436228/210846504-39b1b2f3-9810-47f1-ad7e-05441a4ed097.png"/> First Rudiment: Installing a Virtual Machine<img src="https://user-images.githubusercontent.com/121436228/210846504-39b1b2f3-9810-47f1-ad7e-05441a4ed097.png"/></h2>


<p><img src="https://user-images.githubusercontent.com/121436228/210839261-bdd2b654-c2b0-4388-88f0-cdeccd66f02e.jpg"/>
</p>

1. Search "Virtual Machine" with the Microsoft Azure's account
2. Create a "New Virtual Machine" named "osTicket"
3. Create a "New Resource Group" named "RG"
4. Select a Region: (US) East US
5. Change the Image (Operating System) to __Windows 10 Pro__ 21H2
6. Select the size of the Virtual Machine (VM) to "2vcpu or 4vcpu" (virtual central processing units)
7. Create a username and password
8. Check off the licensing for Multi-tenant hosting rights
9. Click "Create"
10. Once the VM's installation completes, go to the VM's resource section
11. At the overview tab, copy the VM's Public IP Address
12. Go to the search button and type "Remote Desktop Connection"
13. Paste the Virtual Machine's public IP address in the Computer section
14. Then click "Connect"
15. Log in with the username and password
16. After the VM finish loading, hit "No" for all the settings
17. __Virtual Machine Installation Complete!__


<h2> Second Rudiment: Installing the Internet Information Service (IIS)</h2>
  <p><img src="https://user-images.githubusercontent.com/121436228/210849746-ffda9b23-7d47-4cbe-9ee4-32a22c3be9f4.jpg"/>
  </p>
 
  1. In the VM, go to the Search section and type "Windows Features"
  2. Click on "Windows Features"
  3. Check off the "Internet Information Service" box
  4. Then click "OK"
  5. __Internet Information Service Installation Complete!__

<h2> Third Rudiment: Installing Web Platform Installer</h2>
<p><img src="https://user-images.githubusercontent.com/121436228/210852054-3986cd61-5e35-4e91-a75d-2053a6680ca2.jpg"/>
</p>

1. Download the "Web Platfrom Installer"
2. Search then add the following programs 
- "MySQL 5.5"
- "PHP 5.6.31"
- "PHP 7.0 (x86)"
- "PHP 7.1 (x86)"
- "PHP 7.2 (x86)"
- "PHP 7.3 (x86)"

3. Download the "PHP Manager"
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210855911-dec394ed-5cf5-4f3e-8c9e-f82a7243070a.png"/></p>

4. Download the "Microsoft Visual C++"
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210855929-cee67635-fe25-46ef-a561-aab059855fb7.png"/></p> 

5. __The Web Platform Installer, PHP Manager and Microsoft Visual C++ Installation Complete!__

<h2> Fourth Rudiment: Installing the osTicket Installer</h2>
<p><img src="https://user-images.githubusercontent.com/121436228/210858079-69bb32c5-93f2-4857-9e4d-5bf23a928386.jpg"/></p>

1. Download the __osTicket v.1.15.8 Installer__
2. Go to "File Explorer" then to "Download"
3. Right click on the "osTicket" folder then click "Extract all"
4. After the installation completes, copy the "Upload" folder
5. Paste the "Upload" folder to C:/inetput/wwwroot
6. Rename "Upload" to "osTicket"
<p><img src="https://user-images.githubusercontent.com/121436228/211037491-9cf9bbff-590d-4f22-887a-a252f1090b3b.jpg"/>
</p>

7. Go to the IIS Manager App to press "restart"
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210875414-7ac492d8-457e-4c9e-b1e5-c231e5feba5d.jpg"/></p>



8. On the left side of IIS Manager under "Connection", click on Sites ➪ Default Web Site ➪ osTicket
9. Then on the right side of IIS manager click "Browse *.80 (http)"
10. The osTicket Installer will open another webpage tab that displays the missing extensions
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210877514-91796dc7-8b6f-4f78-8c7d-71cebe750fa4.jpg"/>
</p>

11. Enable the extensions by going to the IIS App
12. Under the "Connection" section click on Sites ➪ Default Web Site ➪ osTicket
13. Then click on the PHP Manager program
14. Hit the "Enable or disable an extention"
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210877740-254f7cdd-bec9-4cd2-ba30-56f5a678a0f1.jpg"/>
</p>

15. Right click "php_intl.dll" and "php_opcache.dll" to enable the missing extensions
16. Go back to the osTicket Installer Webpage then hit "Continue"
17. Now let's change the __"C:/inetpub/wwwroot/osticket/include/osT-sampleconfig.php"__ to
__"C:/inetpub/wwwroot/osticket/include/osT-config.php"__
<p><img src="https://user-images.githubusercontent.com/121436228/210880130-e54b5cdb-5473-4df8-8936-0fa1be257cf4.jpg"/>
</p>

18. Go to the "File Explorer" and go to "C:/inetpub/wwwroot/osticket/include"
19. Look for the file "osT-sampleconfig" then rename it by erasing the word "sample" in the file name
20. Right click the "osT-config" file
21. Then go to Properties ➪ Security Tab ➪ Advanced ➪ Disabled inheritance ➪ Confirm it
22. Select "A New Principal" 
23. Type in "Everyone" then click on "Check names"
24. "Allow" "Everyone" to have "Full Access" (Select all}
<p><img src="https://user-images.githubusercontent.com/121436228/211038165-09ab0600-43bf-4622-98b0-4395fb48bc4b.jpg"/>
</p>
25. 








  
  
  
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

