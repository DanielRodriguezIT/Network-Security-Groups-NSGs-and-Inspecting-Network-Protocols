<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>Actions and Observations</h2>

<p>
</p>
<p>
Welcome to my tutorial on Network Security Groups and Inspecting Network Protocols. First you will need to create two VMs on Azure. One machine will be a Linux machine and the other will be a Windows 10 machine. Both will have two cpus and they must be on the same VNET. Once that is done go on the Windows machine and download Wireshark. I will attatch a link to the wireshark download. https://www.wireshark.org/download.html Once installed open Wireshark and filter for ICMP Traffic only. ICMP is a network layer protocol that relays messages concerning network connection issues. Ping uses this protocol, ping tests connectivity between hosts. When we filter wirehsark to only capture ICMP packets and ping the private IP address of our linux machine we can visually see the packets on wireshark. 
</p>
<br />
<p>
<img src="https://i.imgur.com/IIUShxp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can inspect each individual packet and see the actual data that is being sent in each ping. the picture below demonstrates just that. 
</p>
<br />
<p>
<img src="https://i.imgur.com/GLxSIG3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the next portion of the lab we will perpetually ping the Linux machine with the command ping -t. This will continually ping the machine until we decide to stop it, while the Windows machine is pinging the Linux machine we will go to the Linux machine and block inbound ICMP traffic on it's firewall. Once we do that we will stop recieving echo replys from the Linux machine. We will block ICMP by creating a new Network Security Group on the Linux machine that will be set to block ICMP.
</p>
<br />
<img src="https://i.imgur.com/5vXO75R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/GLxSIG3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/GLxSIG3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
<img src="https://i.imgur.com/GLxSIG3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
