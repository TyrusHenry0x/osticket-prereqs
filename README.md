<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket - Prerequisites and Installation</h1>
<p align="center">A step-by-step guide to installing and configuring the open-source help desk ticketing system, osTicket.</p>
<hr/>

<h2>🌐 Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
</ul>

<h2>💻 Operating System</h2>
<ul>
  <li>Windows 10 Pro (21H2)</li>
</ul>

<h2>📝 Prerequisites</h2>
<ul>
  <li>Virtual Machine setup on Azure</li>
  <li>Remote Desktop Connection</li>
  <li>IIS</li>
  <li>osTicket installation files</li>
  <li>PHP and MySQL</li>
</ul>

<hr/>

<h2>🚀 Installation Steps</h2>

<h3>1. Setting Up the Virtual Machine</h3>
<p>
  Begin by creating a virtual machine in Microsoft Azure:
</p>
<ul>
  <li>Create a resource group.</li>
  <li>Assign a name to the virtual machine and select <b>Windows 10 Pro</b> as the operating system.</li>
  <li>Create an administrator account for Remote Desktop access.</li>
  <li>Ensure the licensing option is selected to avoid validation errors.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/4398b003-6d37-45a8-8da7-ddf71c5815d0" alt="Azure VM Setup" width="600"/>
</p>
<hr/>

<h3>2. Connecting to the VM via Remote Desktop</h3>
<p>
  Use the public IP address of your VM to connect via Remote Desktop:
</p>
<ul>
  <li>Open Remote Desktop Connection.</li>
  <li>Enter the public IP address of the VM.</li>
  <li>Optionally, assign a user-friendly name to the connection for better management.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/eb7a4a3f-06fb-4bc9-9e16-9aee60740549" alt="Remote Desktop Connection" width="600"/>
</p>
<hr/>

<h3>3. Downloading and Extracting osTicket Files</h3>
<p>
  Once inside the VM:
</p>
<ul>
  <li>Download the osTicket installation files.</li>
  <li>Extract the files to your desktop or another easily accessible folder.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/7a71765d-c3e8-4708-9f8a-3ec04d021684" alt="osTicket Files" width="600"/>
</p>
<hr/>

<h3>4. Enabling IIS and Setting Up Your Web Server</h3>
<p>
  Enable IIS (Internet Information Services):
</p>
<ul>
  <li>Navigate to Control Panel → Programs and Features → Turn Windows features on or off.</li>
  <li>Check the boxes for <b>Internet Information Services (IIS)</b> and <b>CGI</b>.</li>
</ul>
<p>
  After enabling IIS, test the setup by navigating to <b>127.0.0.1</b> in your browser. You should see the default IIS page.
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/0a0b48e1-3abd-43eb-9848-fe22258cb8a7" alt="IIS Default Page" width="600"/>
</p>
<hr/>

<h3>5. Installing PHP and MySQL</h3>
<p>
  Install the necessary dependencies for osTicket:
</p>
<ul>
  <li>Create a <code>PHP</code> folder in <code>C:\</code>, and extract the PHP files into this folder.</li>
  <li>Install MySQL and set up the username and password as <b>root</b>.</li>
  <li>Optionally, document credentials securely for future reference.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/000a3d21-cac8-4ffe-873d-e403a84de915" alt="MySQL Setup" width="600"/>
</p>
<hr/>

<h3>6. Registering PHP in IIS</h3>
<p>
  Configure IIS to work with PHP:
</p>
<ul>
  <li>Open IIS Manager as an administrator.</li>
  <li>Register the PHP executable in IIS.</li>
  <li>Reload IIS to apply the changes.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/92ae1dfc-ebc6-4e98-ab51-532175041466" alt="Register PHP in IIS" width="600"/>
</p>
<hr/>

<h3>7. Final osTicket Setup</h3>
<p>
  Complete the osTicket configuration:
</p>
<ul>
  <li>Unzip osTicket and move the <code>upload</code> folder to <code>C:\inetpub\wwwroot</code>. Rename it to <code>osTicket</code>.</li>
  <li>Rename <code>ost-sampleconfig.php</code> to <code>ost-config.php</code> and set its permissions to allow full control.</li>
  <li>Enable <b>php_imap.dll</b>, <b>php_intl.dll</b>, and <b>php_opcache.dll</b> in the PHP manager.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/a9a9e76d-7df6-4dae-a688-92aa9c36f487" alt="osTicket Setup" width="600"/>
</p>
<hr/>

<h3>8. Database Configuration with HeidiSQL</h3>
<p>
  Set up the database connection:
</p>
<ul>
  <li>Install and open HeidiSQL.</li>
  <li>Create a new session using the username and password <b>root</b>.</li>
  <li>Verify the connection to the database and observe osTicket traffic.</li>
</ul>
<p align="center">
  <img src="https://github.com/user-attachments/assets/c260b20a-1e50-4591-b28d-9e6e44abbf75" alt="HeidiSQL Configuration" width="600"/>
</p>
<hr/>

<h3>9. Accessing osTicket</h3>
<p>
  Log in to the osTicket user portal and start managing tickets. Customize as needed!
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/76b0d7e2-99e8-460b-bd7a-3c7e3ee753c2" alt="osTicket Portal" width="600"/>
</p>

<hr/>

<h2>🧹 Clean-Up Steps</h2>
<ul>
  <li>Delete: <code>C:\inetpub\wwwroot\osTicket\setup</code></li>
  <li>Set permissions to “Read Only” for: <code>C:\inetpub\wwwroot\osTicket\include\ost-config.php</code></li>
  <li>Log in to the osTicket Admin Panel: <a href="http://localhost/osTicket/scp/login.php">http://localhost/osTicket/scp/login.php</a></li>
</ul>
