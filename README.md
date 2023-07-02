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
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Network_Topology.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h2>IP Addressing Table </h2>

```bash

VLAN ID	      NAME	                   NETWORK ID	         SUBNET MASK	       DEFAULT GATEWAY	     IP RANGE
10	           KL-Management	          172.16.50.1/24	     255.255.255.0	     172.16.50.1	         172.16.50.2-172.16.50.254
20	           KL-HR	                  172.16.1.1/24	      255.255.255.0	     172.16.1.1	          172.16.1.2-172.16.1.254
30	           KL-Design              	172.16.2.1/24	      255.255.255.0	     172.16.2.1	          172.16.2.2-172.16.2.254
40          	 KL-Manufacture	         172.16.3.1/24	      255.255.255.0	     172.16.3.1	          172.16.3.2-172.16.3.254
99	           Native
100	          Blackhole				


```


<h2>VLAN Management</h2>

<h3>KL-Distributed-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Distributed.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-Distributed-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Distributed.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-Distributed-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Distributed.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-Distributed-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Distributed.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />




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
