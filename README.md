<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. <br />

<h2>Prerequisites</h2>

- [Creating a Subscription and Resource Group in Azure](https://github.com/mikeguardiola/create-azure-sub-and-resource)
- [Creating Virtual Machines in Azure and Observing Network Topology](https://github.com/mikeguardiola/azure-vm-and-network)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10 Pro (21H2)

<h2>High-Level Steps</h2>
 
- Create an Azure Virtual Machine Windows 10, 4 vCPUs
- RDP into your Windows 10 VM
- Install / Enable IIS in Windows with CGI
- Download and install PHP Manager for IIS
- Download and install the Rewrite Module
- Create the directory C:\PHP
- Download PHP 7.3.8 and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62
- Open IIS as an Admin and register PHP from within IIS
- Install osTicket v1.15.8
- Download and install HeidiSQL
- Continue setting up osTicket in the browser

<h2>Step-By-Step Instructions:</h2>

<p>
  Step 1:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/f10e93bd-8b3c-4908-ad52-e9cd28cca561)

</p>
<p>
Within the Azure Portal, navigate to the search bar at the top. Within the search bar, type "Resource Group" and select it. Go through the process of setting up your Resource Group.
</p>
<br />

<p>
  Step 2:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/1e751e42-6efd-4372-b5eb-f4704ed3b87d)

</p>
<p>
After you set up your Resource Group, you will now set up a Virtual Machine in Azure. Within the search bar, type "Virtual Machine" and select it. Go through the proper steps of setting up a Virtual Machine, as outlined in previous tutorials.
</p>
<br />

<p>
  Step 3:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/851716f9-236a-4f08-b5a8-3d0e19fc1b2f)


</p>
<p>
Once you've set up your Virtual Machine, you are going to use Remote Desktop to remotely connect to your VM. Copy the IP address for your VM and paste it into the Remote Desktop tool. Enter your username and password for your VM.
</p>
<br />

<p>
  Step 4:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/ae3ab6d7-60bd-4350-8d1a-8beba4a86eb2)

</p>
<p>
Once you are remotely connected to you VM, open a web browser and open the Google Drive folder that contains the download files for osTicket.
</p>
<br />

<p>
  Step 5:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/612bca89-404d-409e-9d81-1042a865cd47)

</p>
<p>
Next, open up the Control Panel in Windows and click on "Program". Then click on "Turn Windows feature on or off".
</p>
<br />

<p>
  Step 6:
  <br />

<img src="https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/8299e93e-12f0-4312-92d7-0870657aa9e4" height="50%" width="50%"/>

</p>
<p>
Install / Enable IIS in Windows with CGI. Make sure every box that is shown in the above image is selected. Then click on "OK".
</p>
<br />

<p>
  Step 7:
<img src="https://i.imgur.com/2UeninD.png"/>
</p>
<p>
Once you are at this screen, click on "+ Container".
</p>
<br />

<p>
  Step 8:
<img src="https://i.imgur.com/6gYK0gP.png"/>
</p>
<p>
A new window will open up on the right side of your screen to edit your container. Give your container a unique name. You can leave the "Public access level" to the default setting of "Private". When you are finished, click on the "Create" button.
</p>

<p>
  Step 9:
<img src="https://i.imgur.com/aoajfg1.png"/>
</p>
<p>
Once your container has been created, go ahead an click on it to enter your container's portal.
</p>
<br />

<p>
  Step 10:
<img src="https://i.imgur.com/A09i2FB.png"/>
</p>
<p>
Now you are going to want to upload a basic text file into your container.
</p>
<br />

<p>
  Step 11:
<img src="https://i.imgur.com/VjKDm35.png"/>
</p>
<p>
First, you will need to create a text document and save it to your desktop. For this tutorial, I will be using Notepad. You can access this program by pressing the Windows Key and typing "Notepad". Once you have it open, add some text to your file and save it to your desktop.
</p>
<br />

<p>
  Step 12:
<img src="https://i.imgur.com/J80CLl7.png"/>
</p>
<p>
Now, head back over to your container. Click on the "Upload" button. You can either drag and drop your file from your desktop, or you can upload from the file explorer. Click on the blue "Upload" button when ready.
</p>
<br />

<p>
  Step 13:
<img src="https://i.imgur.com/OwVZ16r.png"/>
</p>
<p>
Now that the text file has been uploaded, you can edit, download, delete or choose one of the other available options.
</p>
<br />
This will conclude your tutorial on how to create a storage account in Azure. Well done and thank you for following along!
