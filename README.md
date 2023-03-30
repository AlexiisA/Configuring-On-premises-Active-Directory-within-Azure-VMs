<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com/watch?v=54TKBqKCEFc&t=11s)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

<p>
SETUP RESOURCES IN AZURE
<p>
<img src="https://i.imgur.com/VrnWfp0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step I created two Virtual Machines. One VM named DC1 (domain controller) and the other named client1.
</p>
<br />

<p>
CONFIRM CONNECTIVITY BETWEEN BOTH VMs
<p>
<img src="https://i.imgur.com/TCFi4u1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<img src="https://i.imgur.com/JAInfOY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<p>
<img src="https://i.imgur.com/1RtrcPH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
It is very important to make sure both VMs communicate with each other. First, communication was tested with a "ping -t" command and it failed. It sent back a "request timed out" response. Next, I enabled ICMPv4 protocol in the local windows firewall. After doing that, I tested the connection again and the a "ping -t" command and it was a success! A reply was received.
</p>
<br />

<p>
INSTALL ACTIVE DIRECTORY
<p>
<img src="https://i.imgur.com/cl8gdBD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<img src="https://i.imgur.com/1CNKA1K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Active Directory Domain Services. Then setup a new forest as mydomain.com.
</p>
<br />

<p>
CREATE AN ADMIN AND NORMAL USER ACCOUNT IN ACTIVE DIRECTORY
<p>
<img src="https://i.imgur.com/djfY8bV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created a normal user named Jane Doe. Then added her to the ADMINS group.
</p>
