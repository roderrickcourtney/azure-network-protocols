<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. For this example we will be using two Virtual Machines created in an earlier lab. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create Virtual Machines
- Remote Desktop into VMs
- Install & Run WireShark
- Test Connectivity Between VMs

<h2>Actions and Observations</h2>

<p>
<img src="https://imgur.com/0INwRXw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/tc32g9Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create two Vitrual Machines in Azure: Log into the Microsoft Azure Portal with your Microsoft Account --> search "resource groups" in the search bar --> create resource group --> search "Virtual Machines" in the search bar --> create two Virtual Machines (Windows 10 OS for VM1 & Ubuntu OS for VM2) --> Make sure both VMs are in the same "resource group". *When setting up the VMs remember the username and password that you use. You'll need this information later to remote desktop into the VMs. I recommend using the same login information for both VMs.
</p>
<br />

<p>
<img src="https://imgur.com/Dhd0N4w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/c8UPweu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote Desktop into each "Virtual Machine". Go to --> VM1 settings --> copy "public IP address" --> search "remote desktop connections" in start search bar --> Open "Remote Desktop Connection" & paste copied IP address from VM1 --> click connect --> Use the Username & Password created in step 1 to sign in to the VM. Repeat the same steps to log into VM2.
</p>
<br />

<p>
<img src="https://imgur.com/uDS8XIY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/fv4AE4n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/Bxdbca7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
While into VM1, download WireShark. Search "WireShark" on google --> click Wireshark's official site --> "Windows Installer (64-bit)" download --> Install WireShark and go through installation prompts --> Open WireShark --> click "Ethernet 2" --> next select "shark symbol" in upper left hand corner to start network traffic monitoring --> Filter out irrelevant network traffic via display filter bar (type "icmp" in filter bar to only see ping traffic). 
</p>
<br />

<p>
<img src="https://imgur.com/6cvo6nr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/vBozpzR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/EJCQRcw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to VM2 on Azure Portal --> overview --> copy the "private IP address" --> Go to VM1 --> Search PowerShell in the start menu search bar & open it --> Type "ping" then paste VM2's private IP address into "PowerShell" (WireShark will now show the two VMs pinging back and forth). Pay attention to all of the data being communicated between both VMs on this step
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
