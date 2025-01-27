<p align="center">
<img src="https://i.imgur.com/9JmwJSF.png" alt="osTicket logo"/>
</p>

<h1>Active Directory: Environment/Infrastructure Preparation 🪟</h1>
In the first section of this lab we are preparing multiple environments to execute the different functions of the lab. We required a Windows 11 OS Virtual Environment, a Windows Server 22 Datacenter (Domain Controller), a connection between the Domain Controller VM (which will be called Vnet-VM in this lab) and the Windows 11 OS VM (which will be called Client-1-VM). We established this connection by setting the DCs (Domain Controllers) Private IP address to static and pointing the Windows OS Client-1 DNS Server to this Static Private IP of the DC.

(Link Back to Main Project Contents Page is at the Bottom of this Repo)
<h2>Environments and Technologies Used</h2>

- Lenovo Ideapad 5 Pro 16gb AMD Ryzen 7
- Microsoft Azure Resource Group
- Microsoft Azure Windows 10 Pro version 22H2 - x64 Gen2 Virtual Machine
- Microsoft Azure Windows Server 22 Datacenter: Azure Edition - x64 Gen2 Virtual Machine

<h2>Operating Systems Used </h2>

- Local Windows 11 Home Version 21H2</b>
- Windows 10 Pro Version 22H2 Virtual Machine
- Windows Server 22 Datacenter: Azure Edition - x64 Gen2 Virtual Machine
  
<h2>List of Prerequisites</h2>

- Microsoft Azure Subscription
- Microsoft Azure Subscription Credit 

<h2>Installation, Setup, Resource Setup, Executing Functions</h2>
1. Thus far in this Azure project we have only used Windows 11 and Ubuntu Virtual Machines but for this lab we need a Windows Server 22 Virtual Machine which will act as our Domain Controller.
</p>
<br />

<img src="https://i.imgur.com/Ioa3Bzx.png" alt="Disk Sanitization Steps"/>
</p>
<p>
2. There is currently a Private IP address assigned to the DCs Network Interface Controller, we have changed this to static in order to allow a steady connection between the Client-1 OS DNS Servers and the DC.
</p>
<br />

<p>
<img src="https://i.imgur.com/rrfOvap.png" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Here we are pointing the "Client" OS DNS Servers to the Domain Controllers Private IP address to establish a connection between the 2 Machines. 
</p>
<br />

<p>
<img src="https://i.imgur.com/QTDhEsm.png" alt="Disk Sanitization Steps"/>
</p>
<p>
4. To test the connection between the Client and the DC, we used the Ping Command to send an ICMP Echo request to the DC and via the Echo replies we can see that there is a stable connection between the Client and the DC.
</p>
<br />

<p>
<img src="https://i.imgur.com/Acnv18Q.png" alt="Disk Sanitization Steps"/>
</p>
<p>
5. By issuing the ipconfig /all command from our Client VM, we can see clearly the DNS Servers IP Address as 10.0.0.4 which is the Private IP address of our DC.
</p>
<br />

<p>
<img src="https://i.imgur.com/7P1QVjk.png" alt="Disk Sanitization Steps"/>
</p>
<p>
LINK BACK TO THE MAIN PROJECT CONTENTS PAGE - https://github.com/cyberwahid01/Azure-Compute-and-Networking
