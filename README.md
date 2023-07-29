# Active-Directory-Lab
I completed a lab where I set up active directory on a domain controller then added a windows 10 client to the domain.

<h2>Description</h2>
I utilized virtualbox to set up 2 virtual machines. One, running the DC (domain controller) and the client machine. The DC used a windows 2019 server and the client machine ran on windows 10. An internal network was set up on the Dc that would mainly be used by the client to connect to the domain through the DC’s internet. This was to simulate an enterprise environment, where all the work computers are connected to the same network and domain. The dhcp was set between 172.16.0.100 and 172.16.0.200. After setting up the network and installing Active Directory, I ran a powershell script to add over 1000 users to the Organizational Unit (OU.) 
I now have experience managing an enterprise server (300+ employees) 😉
The script I found initially had syntax errors, naming issues and a few more errors, so I had to debug the code and edit it before it actually started running properly. 
After the users were added, I switched back to the client machine to try and connect it to the DC. At first, I was unsuccessful. For some reason, the client refused to connect. I checked the ipconfig and it seemed to have everything in place, from the Dns suffix to the default gateway, yet it still refused to connect. I figured the best course of action would be to go back to the DC and reinput the dhcp settings then restart the domain server. I also then manually added the domain to the client through the control panel and reinitialized how the virtual box connected to the internet. I changed it to run on my computer’s ethernet, which did allow it to connect to the internet, but unfortunately, not to the domain. After restarting the domain on the DC again and changing the client network adapter back to “internal,” I was finally prompted to make the client discoverable by other PCs on my network, most importantly, the DC! I had successfully set up the DC and connected a client to my domain. Along with managing each individual user in the OU.

<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Virtualbox</b>
- <b>Active Directory</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Windows Server 19</b>

<h2>Project overviewh:</h2>

<p align="center">
Powershell script to add 1000 users: <br/>
<img src="https://i.imgur.com/7xPPMQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Succesfully added the windows 10 client to the domain:  <br/>
<img src="https://i.imgur.com/U5nkMTP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Making sure the DHCP was correctly set up with my ip address: <br/>
<img src="https://i.imgur.com/xPlZquj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirming the windows 10 client could succesfully connect to the domain:  <br/>
(I should probably switch this with the 2nd part)  
<img src="https://i.imgur.com/shhDCq6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1000 added users:  <br/>
<img src=https://i.imgur.com/AIIE4Ft.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
