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

- Enable internet information services 
- Install web platform installer 
- Install MySQL
- Install C++ Redistributal 
- Configure permissions and install OsTicket 

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/968c85f7-f138-4911-85c0-d4a002c62c62)

<p>
</p>
<p>
To begin installation for osTicket, we must first create an Azure virtual machine using Windows 10 and 4 vCPUs. 
</p>
<br />


![image](https://github.com/user-attachments/assets/41af5327-5730-4207-8712-fe6a6ec1a4fe)


<p>
</p>
<p>
Once our VM (virtual machine) is created, we must get the ip address and open it in the Remote Desktop Connection app on Windows. 
</p>
<br />


![image](https://github.com/user-attachments/assets/98fdcea2-e514-4a5e-b0a2-d2a786aecc0f)


<p>
</p>
<p>
In the Remote Desktop Connection app, we can use our VMs ip address to get logged in. We must use our login credentials when creating the VM to login to our virtual machine. 
</p>
<br />


![image](https://github.com/user-attachments/assets/2a070c96-e69d-48f5-86a7-376203ea42e2)
![image](https://github.com/user-attachments/assets/a7592ea1-21e1-495b-8b37-6bb162c9ae6b)


<p>
</p>
<p>
Within the virtual machine we will begin the installation for osTicket, to begin, in our downloads folder we will download the ZIP file for osTicket and install and extract the files to the desktop.  
</p>
<br />


![image](https://github.com/user-attachments/assets/6fec5e31-3c4c-4c9f-b777-06e577897147)
![image](https://github.com/user-attachments/assets/1609b67f-999b-4c7e-bdd7-28cf46bc1674)



<p>
</p>
<p>
Now we must Install / Enable IIS in Windows WITH CGI

To do this we open Control Panel -> 
  
</p>
<br />
