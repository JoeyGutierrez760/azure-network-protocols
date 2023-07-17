<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

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

- Step 1 : Create a Windows 10 Virtual Machine VM1 & Create a Linux VM2
- Step 2 : Observe ICMP Traffic
- Step 3 : Observe SSH Traffic
- Step 4 : Observe DHCP Traffic
- Step 5 : Observe RDP Traffic

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/JoeyGutierrez760/azure-network-protocols/assets/41347751/d2e914a5-db23-4f20-815f-3453179a8403" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin setting up Azure Network Security, connect to your Windows 10 Virtual Machine (VM) using Remote Desktop. Install Wireshark within the Windows 10 VM. Open Wireshark and apply a filter to display only ICMP traffic. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM. Observe the ping requests and replies in Wireshark. Additionally, from the Windows 10 VM, use the command line or PowerShell to ping a public website. This sequence of steps allows you to start exploring and monitoring network traffic and connectivity within your Azure environment for network security purposes.
</p>
<br />

<p>
<img src="https://github.com/JoeyGutierrez760/azure-network-protocols/assets/41347751/699a58ea-a2f1-4ee1-9758-036b9f7eb540" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Linux named VM2. During the VM creation process, choose the previously created Resource Group and Virtual Network (Vnet). Utilize Network Watcher to observe your Virtual Network for monitoring purposes. SSH into the Ubuntu VM using its private IP address. Enter commands such as the username and password within the SSH connection and observe the SSH traffic in WireShark. To exit the SSH connection, type 'exit' and press [Enter]. These steps allow you to explore network security aspects within Azure, including VM creation, network monitoring, and SSH traffic analysis.
</p>
<br />

<p>
<img src="https://github.com/JoeyGutierrez760/azure-network-protocols/assets/41347751/418470bb-93b9-435a-99f1-7b6c9cfa520f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This non-stop spam of traffic occurs because RDP is designed to provide a live stream of data from one computer to another. Unlike other protocols that only transmit data when there is an activity or interaction, RDP maintains an ongoing connection and continuously transmits data to ensure a real-time display of the remote desktop. This behavior explains why the RDP traffic appears as constant and continuous in Wireshark, as it is consistently transmitting data to provide a live view of the remote desktop session.
</p>
<br />
