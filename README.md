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

- Create an Azure Virtual Machine Windows 10

<p>Within the Azure envirnoment, create a Virtual Machine(VM) with at least 8GB of RAM to house as the location for the osTicket installation process.  </p>
  
  ![(1) Create a VM](https://github.com/user-attachments/assets/a108536f-d5b8-4825-899f-5310d920a38e)

- Log into the VM with Remote Desktop
  <p>Use the Remote Desktop Protoccal </p>
  
  ![VM IP ADDRESS](https://github.com/user-attachments/assets/281ffd5f-79dc-4c83-b048-4ca738fc1353)
![RDP Login](https://github.com/user-attachments/assets/ec17df63-df47-4d51-a2e4-a1cd1f9815f7)

  
- Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
  We will use the files in this folder to install osTicket and some of the dependencies. Make sure to actually unzip the folders contents onto your Virtual Machine, otherwise you may run into issues later.
  https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD


<h2>Installation Steps</h2>
- Step One, Install / Enable IIS in Windows WITH CGI
<p>We're going to install/enable ISS within windows with CGI enabled. To get to the ISS settings you need to navigate to the windows control panel and select programs. After selecting programs you need to select the 'Turn Windows features on or off' option, which will pull up the window which includes ISS and many other options.
  
![control panel, programs](https://github.com/user-attachments/assets/c15137ca-e54d-4e4e-af91-451b64cdd339)![Windows Features Breakdown](https://github.com/user-attachments/assets/f545e435-5f3e-424b-ad3e-22d39f01c354)


Within that window find ISS, and check the box. Once it's expanded go ahead and go into the World Wide Web Services folder, and finally into the Application Development Features folder to find CGI. Make sure to select CGI before hitting Ok. That's the end of step one.</p>

- Step Two, From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
![PHP manager](https://github.com/user-attachments/assets/bf0071ab-e1c9-4c7b-8d1e-94af2e751d7b)

This step is pretty straightforward, you just need to go into the folder and select 'PHPManagerForIIS_V1.5.0.msi'. The installation for this program is very simple, you just click 'Next, select 'I Agree', and select 'Next' before closing out the window.

- Step Three, From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Installing these modules is what is going to allow us to run and use osTicket, the installation for many of them is similar, and might feel a bit repetitive. But I assure you it is very necessary to have osTicket functioning properly within our Virtual Machine. Next is the Rewrite Module, within the same 'osTicket-Installation-Files' folder select the 'rewrite_amd64_en-US.msi' option.

![ReWriteModle](https://github.com/user-attachments/assets/7009612d-5a83-4f74-8b31-bb120b748b10)

Once It's opened checked the box agreeing to the terms in the Licesnse Agreement, and click install. It will take a second before prompting you with the option to 'Finish', concluding the installation process.

- Step Four, Create the directory C:\PHP

This step gives us a place to store our files in the upcoming step. You'll want to open up file explorer and navigate to 'This PC' then on to the local C drive 'Windows(C:)'. Here you'll want to create a new folder and name it 'PHP'.

![PHP --](https://github.com/user-attachments/assets/1eb84b17-e6da-48ed-b2dd-2e8d342a4a2a)


<br />
