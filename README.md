<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Preinstallation</h1>
This tutorial walks through installing and configuring the dependencies required for OSTickets.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 VM (2 vCPUs)

<h2>List of Dependencies for osTicket</h2>

- [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
- [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
- [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
- [Microsoft Visual C++ 2009 Redistributable Package](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)

<h2>Pre-installation Walkthrough</h2>


<p>
1. Create a Windows 10 Virtual Machine in Azure <br>
</p>
<p>
<a href="https://ibb.co/KhfwTF7"><img src="https://i.ibb.co/3djzgBW/1createvirtualmachine.png" alt="createvirtualmachine" border="0"></a>
 <img src="https://imgur.com/a/vAZMBWh" alt="deployedvm" border="0">
</p>

<br />


<p>
2. Remote into vm-ostickets <br>
- Use Microsoft Remote Desktop if you have macOS. <br>
- Use Remote Desktop if your are operating on Windows. <br>
- Copy and paste vm-osticket's public IP address and enter into remote desktop prompt.
</p>
<p>
<a href="https://ibb.co/jr4b3V0"><img src="https://i.ibb.co/5RcGsYp/3remoteintovm.png" alt="3remoteintovm" border="0"></a>
</p>
<br />


<p>
3. Install and Enable Internet Information Services <br>
- Pull up the Control Panel then click on Turn on Windows features <br>
- Select the box next to Internet Information Services. <br>
- Make sure CGI is checked.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
4. Download these 5 files <br>
- <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link">PHP Manager for IIS</a> <br>
- <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link">Rewrite Module</a> <br>
- <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link">PHP 7.3.8</a> <br>
- <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link">Microsoft Visual C++ 2009 Redistributable Package</a> <br>
- <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link">MySQL 5.5.62</a>
 </p>
 <p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br>


<p>
5. Install These Dependencies in This Order: <br>
- PHP Manager for IIS<br>
- Rewrite Module <br>
- Microsoft Visual C++ 2009 Redistributable Package <br>
- MySQL 5.5.62 <br>
    - Select typical and standard setup. <br>
    - Setup an easy to remember password, i.e. Password1
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
6. Extracting and moving PHP files<br>
- create a folder called PHP in C drive (C:/PHP). <br>
- extract all the files in the php.zip contents into C:/PHP
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
7. Right-click on IIS to open as administrator.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
8. Register PHP from within IIS
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
9. Restart IIS (click restart button on IIS panel)
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<a href="https://github.com/aizhuxue007/osticket-installation">Go to Installation</a>
