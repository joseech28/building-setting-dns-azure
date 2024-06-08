<p align="center">
<img src="https://i.imgur.com/kJhEm5a.png" alt="Traffic Examination"/>
</p>

<h1>Understanding Root Hints and DNS Resolution Azure Virtual Machines</h1>
In this tutorial,  This source explains and demonstrates the basics of DNS, including A records, CNAME records, and the DNS cache. <br />






<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools



<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>




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
7. Creating a CNAME Record

On DC One, in the DNS Manager, I right-click in the same zone where I created the A record.
I select New Alias (CNAME)....
I enter "search" for the alias name and "www.google.com" for the fully qualified domain name.
I click OK.
</p>
<br />

<p>
<img src="https://imgur.com/zkgqXtb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Exploring Root Hints
On DC One, I right-click on the server name (DC One) and select Properties.
I go to the Root Hints tab.
I observe a list of root hint servers that DC One can use to resolve queries for domains not in its local records.

</p>
<br />




