<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
  >**Note**: Be sure to check the box recognizing 'I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights.' or else you will receive a validation error message when you choose to 'Review + Create'.
<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Connect Virtual Machine to Remote Desktop
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
I began by setting up a virtual machine in Azure, starting with the configuration of key settings. This included creating a resource group, assigning a name to the virtual machine, and selecting Windows 10 Pro as the operating system image.
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/4398b003-6d37-45a8-8da7-ddf71c5815d0" height="65%" width="65%"/>
</p>
<br />

<p>
Next, I created an administrator account for remote desktop access, and ensured that the licensing option was selected to avoid a validation error when continuing.

</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/89b898db-3c37-4c13-aea7-195e187d36db" height="65%" width="65%"/>
</p>
<br />

<p>
Moving forward, I added the virtual machine to Remote Desktop using its public IP address. To simplify management in complex environments, I recommend assigning a user-friendly name, as shown in the example below, to easily distinguish between machines..
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/eb7a4a3f-06fb-4bc9-9e16-9aee60740549" height="80%" width="80%"/>
</p>
<br />
<p>
At this Point I'm inside my Virtual Machine.
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/a31ecdf4-353a-4586-a814-3eb31bbdce06" height="80%" width="80%"/>
</p>
<br />
<p>
  
After that I downloaded the files neccessary to setup osTicket within my virtual machine, after that ill extract my zip file onto my desktop for easy access.
</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/7a71765d-c3e8-4708-9f8a-3ec04d021684" height="80%" width="80%"/>
</p>
<br />

<p>The next step is to enable IIS(Internet Information Services) as well as enabling CGI. completing this will allow my machine to act as a web server.</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/0a0b48e1-3abd-43eb-9848-fe22258cb8a7" height="80%" width="80%"/>
</p>
<br />

<p>Once that is finished I'm able to load the IIS default page located at 127.0.0.1</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/b4caa0bf-8a96-44e0-a46e-231346f10aed" height="80%" width="80%"/>
</p>
<br />
<!--
<p></p>
<p align="center">
<img src="" height="80%" width="80%"/>
</p>
<br />
-->
<p>Moving forward I need a few dependencys installed, I'll start by creating a PHP folder inside my windows(C:) drive, from there I'll extract my PHP manager file in the folder.</p>
<p align="center">
<img src="https://github.com/user-attachments/assets/a17fb94a-1e90-4bb5-9bbb-ddb2efc63814" height="80%" width="80%"/>
</p>
<br />

<p>After that I'll install my VC_redist file, and MySQL, these wil be used to store Tickets within a database. From there I'll laumch the Configuration Wizard and set both Username and Password to 'Root'</p>
💡: Even though I have my User and Password set as something fairly simple, I like to keep documentation of all of my logins in a sticky note.
<p align="center">
<img src="https://github.com/user-attachments/assets/000a3d21-cac8-4ffe-873d-e403a84de915" height="80%" width="80%"/>
</p>
<br />

<p>After that step is complete I'll open IIS as an Admin and register PHP from within IIS, then I'll reload to save the change I made.</p>

<p></p>
<p align="center">
<img src="https://github.com/user-attachments/assets/92ae1dfc-ebc6-4e98-ab51-532175041466" height="80%" width="80%"/>
</p>
<br />
