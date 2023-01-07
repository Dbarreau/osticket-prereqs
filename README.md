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


<h1><Font color="orange"> osTicket </font> - Prerequisites and Installation</h1>
This repository displays the tutorial of the osTicket's installation and its rudiments (prerequisites). The first rudiment begins with composing a virtual machine via Microsoft Azure. After that, there is a series of programs to support osTicket Ticketing System: IIS, Web Platform Installer, and HeidiSQL.<br />


<h2><img src="https://user-images.githubusercontent.com/121436228/209778109-d136551c-80f5-4185-a43b-fd1bab7a2fcb.png">
Video Demonstration<img src="https://user-images.githubusercontent.com/121436228/209778109-d136551c-80f5-4185-a43b-fd1bab7a2fcb.png"></h2> 
  
- ###  [YouTube: How To Create A Virtual Machine: First Prerequisite](https://youtu.be/YGWak28859s)
- ###  [YouTube: How To Install osTicket With Prerequisites](https://www.youtube.com/watch?v=ceEH3uJY5a0)

<h2>👨‍💻Environments and Technologies Used👨‍💻</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2><img src="https://user-images.githubusercontent.com/121436228/211121502-3546a566-3e37-4bb4-b540-d3695714b4f9.png"/>Operating Systems Used<img src="https://user-images.githubusercontent.com/121436228/211121509-f417eb8c-5f03-4808-9a69-97b1ed234783.png"/></h2>

- Windows 10 Pro</b> (21H2)

<h2>📋List of Prerequisites📋</h2>

- Install a __Virtual Machine__ with Microsoft Azure
- Install Web Server: Internet Information Service __(IIS)__
- Install __Web Platform Installer__
- Install Files: __PHP Manager__ and __Microsoft Visual C ++__
- Install the __osTicket__ Installer
- Install __HeidiSQL__
- Eliminate the osTicket's __Setup Directory__

<h2><img src="https://user-images.githubusercontent.com/121436228/210846504-39b1b2f3-9810-47f1-ad7e-05441a4ed097.png"/> First Rudiment: Installing a Virtual Machine<img src="https://user-images.githubusercontent.com/121436228/210846504-39b1b2f3-9810-47f1-ad7e-05441a4ed097.png"/></h2>


<p><img src="https://user-images.githubusercontent.com/121436228/210839261-bdd2b654-c2b0-4388-88f0-cdeccd66f02e.jpg"/>
</p>

1. Search "Virtual Machine" with the Microsoft Azure's account
2. Create a "New Virtual Machine" named "osTicket"
3. Create a "New Resource Group" named "RG"
4. Select a Region: (US) East US
5. Change the Image (Operating System) to __Windows 10 Pro__ (21H2)
6. Select the size of the Virtual Machine (VM) to "2vcpu or 4vcpu" (virtual central processing units)
7. Create a username and password
8. Check off the licensing for Multi-tenant hosting rights
9. Click "Create"
10. Once the VM's installation completes, go to the VM's resource section
11. At the overview tab, copy the VM's Public IP Address
12. Go to the computer's start search button and type "Remote Desktop Connection"
13. Paste the Virtual Machine's public IP address in the Computer section
14. Then click "Connect"
15. Log in with the username and password
16. After the VM finish loading, hit "No" for all the settings
17. __Now The Virtual Machine Installation Complete!__


<h2> <img src="https://user-images.githubusercontent.com/121436228/211121739-d18453e4-9d55-4845-85ec-8a968e614174.png"/>Second Rudiment: Installing the Internet Information Service (IIS) <img src="https://user-images.githubusercontent.com/121436228/211121751-8b7e050b-4db2-495e-9041-d5aea28c2c36.png"/></h2>
  <p><img src="https://user-images.githubusercontent.com/121436228/210849746-ffda9b23-7d47-4cbe-9ee4-32a22c3be9f4.jpg"/>
  </p>
 
  1. In the VM, go to the Search section and type "Windows Features"
  2. Click on "Windows Features"
  3. Check off the "Internet Information Service" box
  4. Then click "OK"
  5. __Internet Information Service Installation Complete!__

<h2><img src="https://user-images.githubusercontent.com/121436228/211121976-14bdacec-1381-4444-a533-988c9ac9054a.png"/> Third Rudiment: Installing Web Platform Installer<img src="https://user-images.githubusercontent.com/121436228/211122006-c5d0fa25-841b-4c6c-8d87-62b4470c96bf.png"></h2>
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

<h2> <img src="https://user-images.githubusercontent.com/121436228/211122366-73a28fe2-5073-48f8-a34a-1d91b1348233.png"/> Fourth Rudiment: Installing the osTicket Installer (Part 1)<img src="https://user-images.githubusercontent.com/121436228/211122366-73a28fe2-5073-48f8-a34a-1d91b1348233.png"/></h2>
<p><img src="https://user-images.githubusercontent.com/121436228/210858079-69bb32c5-93f2-4857-9e4d-5bf23a928386.jpg"/></p>

1. Download the __osTicket v.1.15.8 Installer__
2. Go to "File Explorer" then to "Download"
3. Right click on the "osTicket" folder then click "Extract all"
4. After the installation completes, copy the "Upload" folder
5. Paste the "Upload" folder to C:/inetput/wwwroot
6. Rename "Upload" to "osTicket"
<p><img src="https://user-images.githubusercontent.com/121436228/211037491-9cf9bbff-590d-4f22-887a-a252f1090b3b.jpg"/>
</p>

7. Go to the IIS Manager App to press "Restart"
<p align="center"><img src="https://user-images.githubusercontent.com/121436228/210875414-7ac492d8-457e-4c9e-b1e5-c231e5feba5d.jpg"/></p>



8. On the left side of IIS Manager under "Connections", click on Sites ➪ Default Web Site ➪ osTicket
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
24. "Allow" "Everyone" to have "Full Access" just like below
<p><img src="https://user-images.githubusercontent.com/121436228/211038165-09ab0600-43bf-4622-98b0-4395fb48bc4b.jpg"/>
</p>
25. Go back the osTicket Installer then click "Continue"

26. Fill out the Basic Information

<p><img src="https://user-images.githubusercontent.com/121436228/211041427-52356d64-348d-4fc4-ba48-c45a0fa47a9d.jpg"/>
</p>

27. __The osTicket Installer's process is almost finish because the HeidiSQL is the database's "middle man"__

<h2>Fifth Rudiment: Installing the HeidiSQL Program</h2>
1. Download "HeidiSQL"
<p><img src="https://user-images.githubusercontent.com/121436228/211042600-789912b0-9877-4612-81c2-324cdd78c0b6.jpg"/>
</p>

HeidiSQL is used for directory operation purposes and we are going to connect it to the Port 3306 which is the MySQL's protocol.

2. Log in under the Username: __root__ by putting in your password: __************__

<p><img src="https://user-images.githubusercontent.com/121436228/211044042-9d0588b7-0438-4bdf-8589-e6dc36df1a3b.jpg"/>
</p>

3. Then hit "Open"
4. Right click "__unnamed__"➪Create➪A New Database
5. Make sure you name the new Database "osTicket" correctly
<p><img src="https://user-images.githubusercontent.com/121436228/211044679-052004df-37cf-4114-b658-2990dbcbfbff.jpg"/>
  </p>
  
7. Then hit "OK"
8. __The HeidiSQL's installation is complete!__


<h2><img src="https://user-images.githubusercontent.com/121436228/211122366-73a28fe2-5073-48f8-a34a-1d91b1348233.png"/>Fourth Rudiment: Installing the osTicket Installer (Part 2)<img src="https://user-images.githubusercontent.com/121436228/211122366-73a28fe2-5073-48f8-a34a-1d91b1348233.png"/></h2>

1. Go back to the osTicket Installer's Webpage
2. Under the Database Setting's section fill out the Database name as "osTicket"
3. MySQL's username as "root"
4. Put the password


5. Then hit "Continue"
6.  __🎉CONGRATULATIONS osTICKET'S PROGRAM IS FINALLY RUNNING🎉__
<p><img src="https://user-images.githubusercontent.com/121436228/211047275-640d5fb4-1316-42b8-8ac3-5bf62851a177.jpg">
</p>

<h2>🧹Clean-Up Time🧹</h2>
1. Do you see that warning sign? ⚠️
<p>Let's delete the "Setup Directory" folder for security purposes. 
  </p>

<p><img src="https://user-images.githubusercontent.com/121436228/211050105-10209447-b19b-40c6-b517-35bbf9154be9.jpg"/>
  </p>

2. Go to "File Explorer" then to C:/inetpub/wwwroot/osTicket/Setup
3. Select "all the files"
4. Right click then "delete"
5. Go to C:/inetpub/wwwroot/osTicket then delete the "Setup" folder

<p><img src="https://user-images.githubusercontent.com/121436228/211050284-55db4bb0-c19a-40c3-b4ed-35ef2b0b6d68.jpg"/>
  </p>
  
<h2>osTicket's Post-Installation</h2>
 1.  When we go back to the osTicket's webpage you can see the User and the Admin's URL
 <p><img src="https://user-images.githubusercontent.com/121436228/211053324-633f27f4-7ed5-4908-88cd-f6e29c70d7a9.jpg"/>
  </p>
 
 2. This is how the User fill out a new ticket or check their ticket's status
<p><img src="https://user-images.githubusercontent.com/121436228/211053375-ec170f6d-6738-4262-8504-567e06d7d385.jpg"/>
  </p>
  
3. Here is where the Admin Log in and inside osTicket's operation
<p><img src="https://user-images.githubusercontent.com/121436228/211053390-4503f404-3716-46d5-8fb9-d4aedb463dca.jpg"/>
  </p>
  <p><img src="https://user-images.githubusercontent.com/121436228/211053411-7eb24c1b-866a-448c-bde9-27020b7cfd3b.jpg"/>
  </p>
  
  
 



  
  
 
