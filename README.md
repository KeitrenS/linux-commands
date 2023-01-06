<p align="center">
<img src="https://i.imgur.com/StEBVLU.png" alt="Traffic Examination"/>
</p>

<h1>Linux Command Analyzation using VPN</h1>
In this tutorial, we check for connectivity to and from with our Azure Virtual Machines while hooked up to a Virtual Private Network, as well as experiment using multiple Linux commands. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Mircosft Remote Desktop
- Proton Virtual Private Network
- Powershell
- Windows Command Prompt

<h2>Operating Systems Used </h2>

- Ubuntu Server 20.04
- Windows 10 (21H2)

<h2>High-Level Steps</h2>

- Remote Desktop into VM
- Download and Install Proton VPN
- Ping Linux VM using Powershell
- Connect to Linux VM via SSH 
- Using Command Prompt type mulitple Linux commands

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/x6DvRKY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After setting up your Virtual Machines in Azure login to VM1 (Windows 10) with the Public IP Address given by Azure. Once logged in open up Microsft Edge and head to https://protonvpn.com create a free account and then download the software for Windows. Afer the downloading open up the Software and login again with your user information. Once inside the software connect to any of the 3 regions (Japan, United States and Netherlands) associated with the free account and connect to any of the selected regions VPN servers.
</p>
<br />

<p>
<img src="https://i.imgur.com/zkFZ7Ak.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this demonstration the region of choice connected to is the Netherlands. After connecting to a VPN server in the Netherlands open up Powershell, go back into the Azure portal on your actual computer then copy the private IP address of VM2, go back into Remote Desktop and on the Powershell command line ping VM2 (Linux) with the private IP address to check for connectivity. In this demonstration the protocol 'ping (Ip Address) -t' is used to send and recieve infinite data packets between VM1 and VM2 which is a sign that the connection has been established.
</p>
<br />

<p>
<img src="https://i.imgur.com/c1OIKj5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that the connection between the two VMs have been established, using the Command Prompt in the Windows VM1 connect into VM2 via SSH Protocol. In this demonstration 'ssh labuser@10.0.0.5' is typed in on the command line to connect to VM2 with SSH. Once connected you can utilize various of Linux commands (ls -lasth, pwd, uname -a, etc)  and observe the feedback generated once punched in.
</p>
<br />
