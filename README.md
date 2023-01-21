<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Preinstallation</h1>
This tutorial walks through installing and configuring the dependencies required for OSTickets.<br />


<!-- <h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

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
1. Create a Windows 10 Virtual Machine in Azure. <br>
</p>
<p>

</p>
<img width="1779" alt="1createvirtualmachine" src="https://user-images.githubusercontent.com/17282458/213870065-92d7a27d-1e24-4db2-a6fd-b2e8c2eb34b6.png">
<br />


<p>
2. Remote into vm-ostickets. <br>
- Use Microsoft Remote Desktop if you have macOS. <br>
- Use Remote Desktop if your are operating on Windows. <br>
- Copy and paste vm-osticket's public IP address into remote desktop prompt.
</p>
<p>
<img width="672" alt="step2_remotetovm" src="https://user-images.githubusercontent.com/17282458/213871340-9e07b4a7-21c2-4bb3-9890-bdbde918d692.png">


</p>
<br />


<p>
3. Install and Enable Internet Information Services. <br>
- Pull up the Control Panel then click on Turn on Windows features <br>
- Select the box next to Internet Information Services. <br>
- Make sure CGI is checked and hit OK. <br>
- Check if ISS is working by browsing 127.0.0.1.
</p>
<p>
 <img width="1166" alt="4clickturnwindowsfeatures" src="https://user-images.githubusercontent.com/17282458/213870117-947792d4-59ed-41ad-b289-c3e3c16ffaa7.png">
<img width="533" alt="5clickIIS" src="https://user-images.githubusercontent.com/17282458/213870131-497bdc94-a8ee-4de5-8bec-ad61dac62a30.png">
<img width="649" alt="6clickwwwservices" src="https://user-images.githubusercontent.com/17282458/213870154-708869fe-159d-4805-a132-509d4914629f.png">
<img width="1740" alt="8checkIISworking" src="https://user-images.githubusercontent.com/17282458/213870218-96a72a9e-5b73-4dba-92be-a397ef4a5e58.png">
</p>
<br />



<p>
4. Download these 5 files. <br>
- <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link">PHP Manager for IIS</a> <br>
- <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link">Rewrite Module</a> <br>
- <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link">PHP 7.3.8 (zipped)</a> <br>
- <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link">Microsoft Visual C++ 2009 Redistributable Package</a> <br>
- <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link">MySQL 5.5.62</a>
 </p>
 <p>
 <img width="1781" alt="9downloadthese5" src="https://user-images.githubusercontent.com/17282458/213870254-7095f9df-c4a3-48dc-ae5e-94c0f64c4bb5.png">
</p>
<br>


<p>
5. Install the Dependencies: <br>
- PHP Manager for IIS<br>
- Rewrite Module <br>
- Microsoft Visual C++ 2009 Redistributable Package <br>
- MySQL 5.5.62 <br>
&emsp;- Select typical and standard setup. <br>
&emsp;- Setup an easy to remember password, i.e. Password1
</p>
<p>
 <img width="1126" alt="10these5downloaded" src="https://user-images.githubusercontent.com/17282458/213870270-7ec29a49-a986-4271-a6ad-75a4f3018333.png">

</p>
<br />


<p>
6. Extracting and moving PHP files.<br>
- create a folder called PHP in C drive (C:/PHP). <br>
- extract all the files in the php.zip contents into C:/PHP
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />



<p>
 7. Right-click on IIS to <strong>open as administrator.</strong>
</p>
<p>
<img width="669" alt="11openIISasadmin" src="https://user-images.githubusercontent.com/17282458/213871072-c243bb4a-3dcc-4afa-82e5-8fef36505263.png">

</p>
<br />

<p>
8. Register PHP from within IIS. <br>
 - Provide path for php-cgi.exe to prompt.
</p>
<p>
 <img width="1350" alt="12registerphp" src="https://user-images.githubusercontent.com/17282458/213870761-288c2a9c-e79c-4747-93f6-f80a0aae6706.png">
<img width="1339" alt="13phpmanager" src="https://user-images.githubusercontent.com/17282458/213870765-8cf600c5-eedc-4b05-a671-5c0ca0ce769d.png">
<img width="759" alt="15providepath" src="https://user-images.githubusercontent.com/17282458/213870769-7d81b8c1-4df9-4aec-b477-6c69dcc7eb03.png">

 
</p>
<br />

<p>
9. Restart IIS (click restart button on IIS panel).
</p>
<p><img width="1524" alt="restartIISpreinstall" src="https://user-images.githubusercontent.com/17282458/213870712-8194873c-7ca1-493a-a1f1-754d4b8b7f17.png">

</p>
<br />

Congrats! Preinstallation is complete!

<a href="https://github.com/aizhuxue007/osticket-installation">Go to Installation</a>
