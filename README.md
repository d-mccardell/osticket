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
- Item 2
- Item 3
- Item 4
- Item 5

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
<p>Install and enable IIS with CGI. IIS will allow the virtual machine to serve up the osTicket website. To access IIS, go to control panel> programs> turn feautures on or off under program and features. 
<br />
 <img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/81b69169-7b24-4f69-a351-8f302014fd95" height="40%" width="40%"/>

  On the "turn on or off features" page find Internet Information Services or IIS, check box and expand> expand World Wide Web Services> Application Development Features> check CGI. Expand Common HTTP Features and check all boxes. 
</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/a033ac9f-11ca-4dc5-b3f9-45de1339fd8c" height="40%" width="40%"/>
<p>Next, install PHP Manager from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/fe0f735e-f82c-4757-94df-23522b4cd937" height="40%" width="40%"/>
<p>Next, install Rewrite from the installation files.</p>
<br />
<br />

<img src="https://github.com/d-mccardell/osticket-prereqs/assets/116754993/436728b1-ec54-4d63-bce8-e09c4e1d4d5d" height="40%" width="40%"/>
<p>Create a folder in the C drive of the VM and name it PHP</p>

