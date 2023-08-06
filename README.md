<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This quick guide outlines the implementation of Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>Accelerated Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/NORz5eA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside of Microsoft Azure I create a Virtual Machine (VM) using Windows Server 2022. I will be duplicating this process to create another VM (Windows 10) named Client-1.
  
Setup resources in Azure:
1. Create the Domain Controller VM (Windows Server 2022) named “DC-1". Note: the Resource Group and Virtual Network (Vnet) will be created at this time.
2. DO NOT FORGET THIS STEP: Set Domain Controller’s NIC Private IP address to be static. 
3. Create the Client VM (Windows 10) named “Client-1”. Be sure to use the same Resource Group and Vnet that was initially created in Step 1.
4. Ensure both VMs are in the same Vnet (you can check the topology within Network Watcher) 

</p>
<br />

<p>
<img src="https://i.imgur.com/fTGijiK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Ensuring connectivity between the client VM and the Domain Controller. I utilized a perpetual ping along with the disabling of firewall restrictions.

Ensure connectivity between the client VM and Domain Controller: 

5. Login to Client-1 with Remote Desktop and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping)
6. Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall
7. Check back at Client-1 to see the ping succeed


</p>
<br />

<p>
<img src="https://i.imgur.com/8OTGV2k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Wrapping up the installation process but my created server is not fully established as a Domain Controller. 

Install Active Directory:

8. Login to DC-1 and install Active Directory Domain Services
9. Promote as a DC: Setup a new forest as mydomain.com (can be anything, just remember what it is)
10. Since we now have a functioning DC we need to restart and then log back into DC-1 as user: mydomain.com\labuser
</p>
<br />

<p>
<img src="https://i.imgur.com/AeHLg1y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Active Directory has successfully been installed and is ready to be customized for a wide range of tasks. 
