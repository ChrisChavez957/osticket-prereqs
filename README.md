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

- Create a virtual machine using Azure 
- Enable internet information services 
- Install web platform installer 
- Install MySQL
- Install C++ Redistributal 
- Configure permissions and install OsTicket 

<h2>Installation Steps</h2>


<p>
</p>
<p>
  
- To begin installation for osTicket, we must first create an Azure virtual machine using Windows 10 and 4 vCPUs. 

</p>
<br />

![image](https://github.com/user-attachments/assets/968c85f7-f138-4911-85c0-d4a002c62c62)


<p>
</p>
<p>
  
- Once our VM (virtual machine) is created, we must get the ip address and open it in the Remote Desktop Connection app on Windows. 

</p>
<br />


![image](https://github.com/user-attachments/assets/41af5327-5730-4207-8712-fe6a6ec1a4fe)



<p>
</p>
<p>
  
- In the Remote Desktop Connection app, we can use our VMs ip address to get logged in. We must use our login credentials when creating the VM to login to our virtual machine. 

</p>
<br />

![image](https://github.com/user-attachments/assets/98fdcea2-e514-4a5e-b0a2-d2a786aecc0f)


<p>
</p>
<p>
  
- Within the virtual machine we will begin the installation for osTicket, to begin, in our downloads folder we will download the ZIP file for osTicket and install and extract the files to the desktop.  

</p>
<br />


![image](https://github.com/user-attachments/assets/2a070c96-e69d-48f5-86a7-376203ea42e2)
![image](https://github.com/user-attachments/assets/a7592ea1-21e1-495b-8b37-6bb162c9ae6b)



<p>
</p>
<p>
- Now we must Install / Enable IIS in Windows WITH CGI

- To do this we open Control Panel -> Programs -> Programs and Features -> Turn Windows features on or off -> Internet Information Systems -> Worldwide Web Services -> Application Development Features -> Enable file [CGI] -> Click OK -> DONE
  
</p>
<br />

![image](https://github.com/user-attachments/assets/6fec5e31-3c4c-4c9f-b777-06e577897147)
![image](https://github.com/user-attachments/assets/1609b67f-999b-4c7e-bdd7-28cf46bc1674)



<p>
</p>
<p>

- From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

</p>
<br />



![image](https://github.com/user-attachments/assets/07136815-5c14-4b95-8f08-8defa7234609)




<p>
</p>
<p>

- From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

</p>
<br />



![image](https://github.com/user-attachments/assets/39b8798e-2e01-4f6a-951f-2707e4138c89)



<p>
</p>
<p>

- Create the directory C:\PHP

</p>
<br />

![image](https://github.com/user-attachments/assets/baabb01e-7c09-4c2b-875a-819c981bb657)



<p>
</p>
<p>

- From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

</p>
<br />


![image](https://github.com/user-attachments/assets/fe8349de-e2db-4099-bf81-5fe9c57c5582)



<p>
</p>
<p>

- From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

</p>
<br />



![image](https://github.com/user-attachments/assets/8aa94218-628a-4d54-923b-501cfcf4a41f)


<p>
</p>
<p>

- From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)


</p>
<br />


![image](https://github.com/user-attachments/assets/10548095-1063-4729-a70b-75c31df8d8f7)



<p>
</p>
<p>

- Typical Setup ->
- Launch Configuration Wizard (after install) ->
- Standard Configuration ->
- Username: root
- Password: root


</p>
<br />

![image](https://github.com/user-attachments/assets/2e6bc968-4630-43a4-94fd-1d988f2d4288)


<p>
</p>
<p>

- Open IIS as an Admin



</p>
<br />

![image](https://github.com/user-attachments/assets/0c8fade1-732d-4efd-b7c5-3d007fe4cab4)

<p>
</p>
<p>

- Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)


</p>
<br />

![image](https://github.com/user-attachments/assets/c9981f1c-0899-4e58-bb84-cc5056fc2ea5)


<p>
</p>
<p>

- Reload IIS (Open IIS, Stop and Start the server)


</p>
<br />

![image](https://github.com/user-attachments/assets/9ab0aade-f2f0-4119-8d54-f6a5b64b0118)

![image](https://github.com/user-attachments/assets/8a077649-ef64-4826-943c-309261df864a)


<p>
</p>
<p>

- Install osTicket v1.15.8
- From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”


</p>
<br />


![image](https://github.com/user-attachments/assets/a4b41c65-64ba-4a35-98d3-59bddfdc520f)



<p>
</p>
<p>

- Reload IIS (Open IIS, Stop and Start the server)

- Go to sites -> Default -> osTicket
- On the right, click “Browse *:80”

</p>
<br />

![image](https://github.com/user-attachments/assets/5ca3ea00-eab1-4cfb-9426-6f9a6fb3b9ae)


<p>
</p>
<p>

- Note that the osTicket site shows up, you will also notice on the bottom that some extensions are not available. We will begin to start enabling some permissions. 

</p>
<br />

![image](https://github.com/user-attachments/assets/71ab8616-9cfa-4303-b1b3-baf590f7b9db)





<p>
</p>
<p>

- Now, go back to ISS and open Sites -> Default Web site -> osTicket -> and then double-click PHP Manager 

</p>
<br />

![image](https://github.com/user-attachments/assets/65d660d1-727b-4f13-bc08-834987c86bc7)





<p>
</p>
<p>

- Now click "Enable or disable an extentions" on the bottom  

</p>
<br />


![image](https://github.com/user-attachments/assets/aaa540f3-f427-45e7-8d11-5b45d91b5d20)






<p>
</p>
<p>

- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browser, observe the changes


</p>
<br />



![image](https://github.com/user-attachments/assets/dd8d15cd-eecb-4313-88c0-ffc9d422557e)





<p>
</p>
<p>

Now, we must 
- Rename: ost-config.php
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php



</p>
<br />




![image](https://github.com/user-attachments/assets/4c26a55a-e562-4d33-9a5f-8fb104161e3f)





<p>
</p>
<p>

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All




</p>
<br />




![image](https://github.com/user-attachments/assets/c6e7c0d0-305b-4b92-b5de-ee4045e52215)




<p>
</p>
<p>

- Now we give access to "Everyone" and then enable the permissions!




</p>
<br />




![image](https://github.com/user-attachments/assets/815787c9-dd27-442e-9df6-df06fe8ab315)









<p>
</p>
<p>

- Now we reload the osticket website and fill in all of our personal information




</p>
<br />








![image](https://github.com/user-attachments/assets/930f07bd-885d-44aa-9ae9-4af439dd3372)





<p>
</p>
<p>


- Next, from the “osTicket-Installation-Files” folder, install HeidiSQL.


</p>
<br />




![image](https://github.com/user-attachments/assets/510707fe-99bc-4e04-b4f9-d55bd2220596)




<p>
</p>
<p>


- Open HeidiSQL, click new on the bottom left, enter the password, the password is "root", and then hit open 


</p>
<br />




![image](https://github.com/user-attachments/assets/e44af0e1-3d6a-469c-9545-ac241f3ae693)






<p>
</p>
<p>


- Right click (Unnamed) -> (Create new) -> click (Database) 


</p>
<br />


![image](https://github.com/user-attachments/assets/7c41b570-1638-4c59-ad11-6f2b66cc92c7)





<p>
</p>
<p>


- In the name section type "osTicket" exactly this way and hit OK 

</p>
<br />





![image](https://github.com/user-attachments/assets/83708af1-5843-4d85-981d-3f21dfbab8d7)




<p>
</p>
<p>


- Now we head back to the osTicket site and input our new login information for the database settings

</p>
<br />



![image](https://github.com/user-attachments/assets/eb9e6864-d26b-4e31-9d71-dd8f9c556e7e)



<p>
</p>
<p>


- Now hit install!!

</p>
<br />




![image](https://github.com/user-attachments/assets/c988f109-9556-4154-b0e1-f4f02a047055)












