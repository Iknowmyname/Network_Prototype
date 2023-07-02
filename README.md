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
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Network-Topology.PNG" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h2>IP Addressing Table </h2>

<h4>KL-Site</h4>



| VLAN ID | NAME           | NETWORK ID     | SUBNET MASK   | DEFAULT GATEWAY | IP RANGE                  |
| ------- | -------------- | -------------- | ------------- | --------------- | ------------------------- |
| 10      | KL-Management  | 172.16.50.1/24 | 255.255.255.0 | 172.16.50.1     | 172.16.50.2-172.16.50.254 |
| 20      | KL-HR          | 172.16.1.1/24  | 255.255.255.0 | 172.16.1.1      | 172.16.1.2-172.16.1.254   |
| 30      | KL-Design      | 172.16.2.1/24  | 255.255.255.0 | 172.16.2.1      | 172.16.2.2-172.16.2.254   |
| 40      | KL-Manufacture | 172.16.3.1/24  | 255.255.255.0 | 172.16.3.1      | 172.16.3.2-172.16.3.254   |
| 99      | Native         |                |               |                 |                           |
| 100     | Blackhole      |                |               |                 |                           |

<br />
<br />

<h4>KL-Site-Switch-Virtual-Interfaces</h4>

| NAME           | NETWORK ID      | DEFAULT GATEWAY |
| -------------- | --------------- | --------------- |
| KL-SW1         | 172.16.50.12/24 | 172.16.50.1     |
| KL-SW2         | 172.16.50.13/24 | 172.16.50.1     |
| KL-SW3         | 172.16.50.14/24 | 172.16.50.1     |
| SW-Distributed | 172.16.50.15/24 | 172.16.50.1     |

<br />
<br />

<h4>KL-Router-Sub-Interface</h4>

| Sub-Interface | IP ADDRESS     | SUBNET MASK   |
| ------------- | -------------- | ------------- |
| F0/0.10       | 172.16.50.1/24 | 255.255.255.0 |
| F0/0.20       | 172.16.1.1/24  | 255.255.255.0 |
| F0/0.30       | 172.16.2.1/24  | 255.255.255.0 |
| F0/0.40       | 172.16.3.1/24  | 255.255.255.0 |

<br />
<br />

<h4>KL-Serial-Interface</h4>

| Serial Interface | IP ADDRESS       | SUBNET MASK     |
| ---------------- | ---------------- | --------------- |
| Serial2/0        | 200.100.100.1/30 | 255.255.255.252 |

<br />
<br />

<h4>KL-Server-Farm</h4>

| VLAN ID | NAME            | NETWORK ID      | SUBNET MASK   | DEFAULT GATEWAY | IP RANGE                    |
| ------- | --------------- | --------------- | ------------- | --------------- | --------------------------- |
| 10      | KL -Server Farm | 198.51.100.1/24 | 255.255.255.0 | 198.51.100.1    | 198.51.100.2-198.51.100.254 |
| 999     | Blackhole       |                 |               |                 |                             |

<br />
<br />

<h4>KL-Server-Farm-Switch-Virtual-Interface</h4>

| NAME   | IP ADDRESS       | DEFAULT GATEWAY |
| ------ | ---------------- | --------------- |
| SF-SW1 | 198.51.100.12/24 | 198.51.100.1    |

<br />
<br />

<h4>KL-Server-Farm-Router-Sub-Interface</h4>

| Sub-Interface | IP ADDRESS      | SUBNET MASK   |
| ------------- | --------------- | ------------- |
| F0/0.50       | 198.51.100.1/24 | 255.255.255.0 |

<br />
<br />

<h4>KL-Server-Farm-Router-Serial-Interface</h4>

| Serial Interface | IP ADDRESS       | SUBNET MASK     |
| ---------------- | ---------------- | --------------- |
| Serial2/0        | 200.100.100.2/30 | 255.255.255.252 |
| Serial3/0        | 200.100.100.5/30 | 255.255.255.252 |

<br />
<br />

<h4>Hanoi-Site</h4>

| VLAN ID | NAME         | NETWORK ID       | SUBNET MASK   | DEFAULT GATEWAY | IP RANGE                      |
| ------- | ------------ | ---------------- | ------------- | --------------- | ----------------------------- |
| 10      | R&D          | 192.168.10.1/24  | 255.255.255.0 | 192.168.10.1    | 192.168.10.2-192.168.10.254   |
| 100     | RBManagement | 192.168.100.1/24 | 255.255.255.0 | 192.168.100.1   | 192.168.100.2-192.168.100.254 |
| 999     | Blackhole    |                  |               |                 |                               |

<br />
<br />


<h4>Hanoi-Site-Switch-Virtual-Interface</h4>

| NAME           | IP ADDRESS         | DEFAULT GATEWAY |
| -------------- | ------------------ | --------------- |
| Hanoi-MLayerSW | 192.168.100.100/24 | 192.168.100.1   |

<br />
<br />

<h4>Hanoi-Site-Router-Sub-Interface</h4>

| Sub-Interface | IP ADDRESS       | SUBNET MASK   |
| ------------- | ---------------- | ------------- |
| F0/0.10       | 192.168.10.1/24  | 255.255.255.0 |
| F0/0.100      | 192.168.100.1/24 | 255.255.255.0 |

<br />
<br />

<h4>Hanoi-Site-Router-Serial-Interface</h4>

| Serial Interface | IP ADDRESS        | SUBNET MASK     |
| ---------------- | ----------------- | --------------- |
| Serial2/0        | 200.100.100.14/30 | 255.255.255.252 |

<br />
<br />



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
