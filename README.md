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

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/xywYSqv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Pinging a Non-Existent Hostname
I open a command prompt on Client One.
I type ping Mainframe and press Enter.
I observe that the ping fails because there is no DNS record for "Mainframe".
</p>
<br />

<p>
<img src="https://imgur.com/zkgqXtb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Creating an A Record
Creating an A Record
On DC One (the DNS Server), I open Server Manager.
I go to Tools > DNS.
I expand the server name (DC One).
I expand Forward Lookup Zones and then my domain name.
</p>
<br />

<p>
<img src="https://imgur.com/b8C22YN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. I right-click and select New Host (A or AAAA)....
I enter "Mainframe" for the name and DC One's IP address for the IP address.
I click Add Host.
</p>
<br />

</p>
<p>
<img src="https://imgur.com/UsqRQ3Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

4.  Pinging the Newly Created A Record Back on Client One, I type ping Mainframe in the command prompt and press Enter. I observe that the ping succeeds, and the IP address matches DC One's IP address.

</p>
<br />

</p>
<p>

<img src="https://i.imgur.com/ND2ylVi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 Viewing the DNS Cache
On Client One, I use the command ipconfig /displaydns to view the DNS cache.
I observe an entry for "Mainframe" and its corresponding IP address.
</p>
<br />
<p>
<img src="https://imgur.com/Xhoczmo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
</p>
<br />
<p>
6. Pinging a Non-Existent CNAME

On Client One, I type ping search in the command prompt and press Enter.
I observe that the ping fails because there is no record for "search".
</p>
<br />

<p>
<img src="https://imgur.com/RZt3aih.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://imgur.com/zkgqXtb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />




<p>
<img src="https://imgur.com/o1n2NOz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://imgur.com/VrcO588.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://imgur.com/8BtH394.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://imgur.com/xyxqHJB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://imgur.com/f7zbNKT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://imgur.com/ypsK5Tf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

