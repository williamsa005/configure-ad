<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/NORz5eA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside of Microsoft Azure I create a Virtual Machine (VM) using Windows Server 2022. I will be duplicating this process to create another VM (Windows 10) named Client-1.
</p>
<br />

<p>
<img src="https://i.imgur.com/fTGijiK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ensuring connectivity between the client VM and the Domain Controller. I utilized a perpetual ping along with the disabling of firewall restrictions.
</p>
<br />

<p>
<img src="https://i.imgur.com/8OTGV2k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Wrapping up the installation process but my created server is not fully established as a Domain Controller. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Insert text here
