<p align="center">

<img src="https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/9ba47fd6-2434-483d-a4e6-86e9d99b46f3" height="65%" width="65%"/>
 
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
Within the Azure Portal, navigate to the search bar at the top. Within the search bar, type "Resource Group" and select it. Go through the process of setting up your Resource Group. You can name your resource group "resource-group-osticket". Select the region that most closely matches where you live.
</p>
<br />

<p>
  Step 2:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/1e751e42-6efd-4372-b5eb-f4704ed3b87d)

</p>
<p>
After you set up your Resource Group, you will need to set up a Virtual Machine in Azure. Within the search bar, type "Virtual Machine" and select it. Go through the proper steps of setting up a Virtual Machine, as outlined in previous tutorials. Set up your Virtual Machine with the following details:
 <br />
 
- Resource group: resource-group-osticket
- Virtual machine name: vm-osticket
- Region: select the correct region for your location
- Image: Windows 10 Pro, version 22H2 - x64 Gen2
- Size: Standard_D4s_v3 - 4 vcpus, 16 GiB memory
  
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
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/86d8e001-eefb-47db-9985-6b86efe1d0be)

</p>
<p>
Now you are going to test the web server to make sure IIS was installed correctly. Open up a web broswer tab in your VM, type "127.0.0.1" and press Enter. If this screen pops up then you know that IIS was installed correctly.
</p>
<br />

<p>
  Step 8:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/6b958b69-5f5e-4236-8863-7ebca7877b5e)

</p>
<p>
Next, open up your Google Drive folder containing the download files. Click on "PHP Manager for IIS" and download the files.
</p>
<br />

<p>
  Step 9:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/492e7a1a-7988-4f2e-8480-a000a0e96a71)

</p>
<p>
Once the files download, open up the File Explorer and go to Downloads. Double click on the download files and go through the installation steps.
</p>
<br />

<p>
  Step 10:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/4dead6e0-9ef1-4874-ba04-c7e8f9a28408)

</p>
<p>
Now go back to the Google Drive folder. Click on "Rewrite Module" and download the files.
</p>
<br />

<p>
  Step 11:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/ad70ab3c-d9e8-4844-9ca5-c6b1e0a8ee67)

</p>
<p>
Once the files download, open up your File Explorer again and go to Downloads. Click on the download files and go through the installation steps.
</p>
<br />

<p>
  Step 12:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/18bdef96-4316-4f1a-96c0-5bf1b8f5a319)

</p>
<p>
Next, you need to create a new folder in the (C:) Drive of your VM. Open up your File Explorer. Click on "This PC". Then click on the "Windows (C:)". Once there, right click on the empty space and create a new folder. Name the new folder "PHP".
</p>
<br />

<p>
  Step 13:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/26bfbb4e-2d39-41e4-bda6-c862cae79ba0)

</p>
<p>
Next, head back to the Google Drive folder. Download the file named "php-7.3.8-nts-Win32-VC15-x86". Once the files download, open your File Explorer and go to Downloads. Right click on the file and click "Extract All...". Make sure to then select the correct destination folder. You will be using the PHP folder that you previously created in the (C:) drive. Then click on "Extract".
</p>
<br />

<p>
  Step 14:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/3d241c2a-ac5f-48fd-9348-05a8f9d4e71b)

</p>
<p>
Next, you are going to download and install the file named "VC_redist.x86.exe". Go back to your Google Drive folder again. Download the file and go through the installation steps.
</p>
<br />

<p>
  Step 15:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/8d3c3a5d-c2ae-4cfe-a36c-9fcefb0e3fe2)

</p>
<p>
Next, you are going to download and install the file named "MySQL_5.5.6". Open the Google Drive folder. Download the file and go through the installation steps.
</p>
<br />

<p>
  Step 16:
 
![image](https://github.com/mikeguardiola/osticket-prereqs/assets/126979089/8c04f1f6-d721-47b2-908f-fb002f4c098e)

</p>
<p>
Once everything is installed, you will need to set up some credentials for MySQL. Follow these steps:
 <br />
 
- Select "Standard Configuration" -> Next
- Select "Install as a Windows Service" -> Next
- Create a username and password -> Next
- Click on "Execute" -> Finish
 
</p>
<br />

<p>
  Step 17:
<img src="https://i.imgur.com/J80CLl7.png"/>
</p>
<p>
Now, head back over to your container. Click on the "Upload" button. You can either drag and drop your file from your desktop, or you can upload from the file explorer. Click on the blue "Upload" button when ready.
</p>
<br />

<p>
  Step 18:
<img src="https://i.imgur.com/J80CLl7.png"/>
</p>
<p>
Now, head back over to your container. Click on the "Upload" button. You can either drag and drop your file from your desktop, or you can upload from the file explorer. Click on the blue "Upload" button when ready.
</p>
<br />

<p>
  Step 19:
<img src="https://i.imgur.com/J80CLl7.png"/>
</p>
<p>
Now, head back over to your container. Click on the "Upload" button. You can either drag and drop your file from your desktop, or you can upload from the file explorer. Click on the blue "Upload" button when ready.
</p>
<br />
