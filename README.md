<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- [Installation Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machine in Azure
- Download and install software
- Configure systems
- Assign permissions
- Setup osTicket in browser


<h2>Installation Steps</h2>

<p>
<img src= "https://github.com/d-mccardell/osticket-prereqs/assets/116754993/7332262d-68d6-42dd-afe9-8823eec750f4"
 height="60%" width="60%" alt="Virtual Machine Installation"/>

</p>
<p>
First we will create a virtual machine in Microsoft Azure. From the image above you can see that we have created a resouce group where the virtual machine will be in. The virtual machine will run on windows 10 and will have 4 vcpus for maximum efficiency. Make sure to make note of your username and password and do not lose this information. Continue with the steps on the bottom of the screen.
</p>
<br />
<br />

<p>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/678668fe-e17c-4bf9-b65b-91800810ae80" height="60%" width="60%"/>
</p>
<p>
On the networking section of creating the virtual machine, it will create a new Virtual Network or Vnet. Review and create your virtual machine.
</p>
<br />
<br />

<p>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/34d5ef67-95de-4b9d-9141-97988001f5d2" height="60%" width="60%"/>
</p>
<p>
Next open remote desktop on your computer and use the VM's public IP address to connect. log in with the credentials used during the creation of the virtual machine. 
</p>
<br />
<br />
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/37d4a3c2-19ec-4f83-a14a-06e379d53ac6"height="60%" width="60%"/>

<p>
Next, copy the link to the installation files and paste it on the web brower inside the vm. 
</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/f0b2801a-5d0e-49fd-a067-9a9497a778b1" height="40%" width="40%"/>
<p>Install and enable IIS with CGI. IIS will allow the virtual machine to serve up the osTicket website. To access IIS, go to control panel--> programs--> turn feautures on or off under program and features. 
<br />
 <img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/81b69169-7b24-4f69-a351-8f302014fd95" height="40%" width="40%"/>

  On the "turn on or off features" page find Internet Information Services or IIS, check box and expand--> expand World Wide Web Services--> Application Development Features--> check CGI. Expand Common HTTP Features and check all boxes. 
</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/a033ac9f-11ca-4dc5-b3f9-45de1339fd8c" height="50%" width="50%"/>
<p>Next, download and install PHP Manager from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/fe0f735e-f82c-4757-94df-23522b4cd937" height="50%" width="50%"/>
<p>Next, download and install Rewrite from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/436728b1-ec54-4d63-bce8-e09c4e1d4d5d" height="50%" width="50%"/>
<p>Create a folder in the C drive of the VM and name it PHP</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/8e7cb62c-9587-40a3-828c-0d9a94bc54d6" height="50%" width="50%"/>
<p>Download PHP 7.3.8 from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/b0f2c1c6-3e21-403a-abb3-971d2ef3cd02" height="50%" width="50%"/>
<p> Then extract all the files into C:\PHP. </p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/31704b90-22af-46ad-a547-eb9bdd6843a0" height="50%" width="50%"/>
 <p>Download and install Rewrite Module form the installation files.</p>
 <br />
 <br />

 <img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/9fe1547e-6bf2-49b8-8205-d0ce6b55c017" height="50%" width="50%"/>
<p>Download and install a typical agreement of MySQL from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/8411cf8e-a0eb-49b2-aece-c9641c899a12" height="50%" width="50%"/>
<p>Setup credentials under a standard configuration. *Note*: Keep track of all usernames and passwords.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/28486613-84b5-43de-9839-04052c453c1a" height="50%" width="50%"/>
<p>Open IIS as an admin and register PHP. Click on PHP Manager--> Register new PHP version--> Browse for php-cgi in the PHP folder thats located inside the C drive.</p>
<br />
<p><Reload IIS></p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/64dc8047-f75f-4508-8c02-448ac9fa6822" height="50%" width="50%"/>
<p>Next download osTicket from the installation files. Once downloaded open osTicket in file explorer and find the upload folder. Open a seperate file explorer tab and navigate to the C drive--> inetpub--> wwroot. Extract upload into wwroot and rename the file to osTicket.</p>
<br />
<p><Reload IIS></p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/68b92b37-b955-44e8-bc08-47d971a254e6" height="50%" width="50%"/>
<p>On IIS expand VM-osTicket--> Sites--> Default Web Site--> osTicket--> then on the right click on Browse*:80. The osTicket website should pop up on another screen.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/2b13c249-3202-49af-aa1a-b025e86ca800" height="50%" width="50%"/>
<p>Notice that some items on osTicket are not enabled. The next steps will demonstarte how to enable these improvements that are recomended by osTicket. </p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/e51ad173-d9a1-4a86-ad0b-46563b5b9681" height="50%" width="50%"/>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/0b61fda1-7547-45f3-9ca7-143f0fa0b7dc" height="50%" width="50%"/>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/6f0e8a54-0e36-4b11-9b79-638eed29bd26" height="50%" width="50%"/>
<p>Go to IISas an admin--> Vm-osTicket--> Sites--> Default Web Site--> osTicket--> PHP manager--> under PHP Extensions click on "enable or disable an extension"</p>
<br />

<li>Enable: php_imap.dll</li>
<li>Enable: php_intl.dll</li>
<li>Enable: php_opcache.dll</li>
<br />
<p>Refresh the osTicket site in your browser and observe the changes</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/808d94a1-f7c4-490e-9a40-058541f46e21"  height="50%" width="50%"/>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/afeeaea8-70b8-4b0c-a4d5-5fa712d40023" height="50%" width="50%"/>
<p>Open file explorer and navigate to C drive--> inetpub--> wwwroot--> osTicket--> include--> then rename ost-sampleconfig.php to ost-config.php</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/2ab06fc1-9103-434a-905b-ec0931bd2645" height="50%" width="50%"/>
<p>Right click ost-config.php--> properties--> security--> advanced--> disable inheritance--> remove all permissions--> add--> select principle--> type everyone--> click ok--> check full control--> click ok and apply. </p>
<br/>
<br/>

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/6ddf7ae4-0823-4b09-afe3-7fb27c47a437" height="50%" width="50%"/>
<br/>
<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/a891c5b6-f646-412b-83c1-a82ee598f031" height="50%" width="50%"/>



<p>Download and install HeidiSQL. Create a new session and log in with the credentials used with MySQL. Connect to the session. 
<br/> Right click unnamed--> create new--> database. Create anew database with the name osTicket</p>
<br/>
<br/>

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/2ac1e3ed-3651-43b1-b080-66929f8890bb" height="50%" width="50%"/>
<p>Continue the osTicket setup in the browser. At the bottom of the page you will use your credentials from MySQL. For the MySQL database type in osTicket. That is the database that was created in HeidiSQL. Click install now.  </p>
<br/>
<br/>

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/5380192f-3338-456e-8a59-fdc3ec3b547b" height="50%" width="50%"/>
<p>Congratulations you have officially installed osTicket.</p>














