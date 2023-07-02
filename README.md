# Network_Prototype


<h2>

 </h2>

<h2>Description</h2>
This project consists of a network prototype of an enterprise network. The network contains three separate branches from different locations which are KL, Hanoi and a remote server farm in KL. There are 3 LANs present where the Hanoi branch is  a WLAN as a wireless architecture has been implemented.
<br />
<br />


<h2>Tools Used</h2>

- <b>Cisco Packet Tracer</b> 




<br />
<br />

<h2>Network Topology</h2>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Nmap-Scans-M2/blob/main/Service%20%26%20Version%20Detection%20Scan.PNG" height="65%" width="65%" alt="sV"/>
</p>


<h2>VLAN Management</h2>



<h3>TCP SYN Scan</h3>

```bash
$ nmap -sS 192.168.74.133

```

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Nmap-Scans-M2/blob/main/Service%20%26%20Version%20Detection%20Scan.PNG" height="65%" width="65%" alt="sV"/>
</p>

The TCP SYN Scan is the most widely used scan with Nmap. A TCP SYN packet will be sent to the vulnerable virtual machine's ports and if the port is open it will respond with a SYN-ACK packet back as an acknowledgement to say that the port is open. This scan does not establish a full TCP connection as Nmap will send a RST packet to erase the connection which makes it a quicka and stealthy scan.
Service and Version Detection Scan
