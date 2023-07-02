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
| 99      | Native         |       -        |       -       |        -        |              -            |
| 100     | Blackhole      |       -        |       -       |        -        |              -            |

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
| 999     | Blackhole       |         -       |        -      |        -        |               -             |

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
| 999     | Blackhole    |         -        |        -      |         -       |               -               |

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


<h2> KL Site LAN</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Kl-Site-LAN.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<p align="justify">The LAN in the KL site has a total of 4 switches where 3 of the switches are designated to each department which are HR, Design and Manufacture. There fourth switch acts as a distribution where the access layer is connected to the core layer. Four VLANs are created for each department and also one as the management VLAN. The ports which are a switch-to-switch connection are configured as trunk ports in order to carry multiple VLANSs in a single interface whereas the switch-to-end devices connections are configured as access ports to only access the respective VLAN.  InterVLAN routing is configured in the KL-Router to enable end devices from different departments to communicate with each other.</p>




<h2>VLAN Management</h2>

<h3>KL-Distributed-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Distributed.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-HR-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-HR.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-Design-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Design.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h3>KL-Manufacture-Switch</h3>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN-KL-Manufature.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h2>KL Site InterVLAN Routing</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL-Site-InterVLAN-Routing.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>The router on a stick configuration method is implemented in the KL Site in order to enable communications between multiple VLANs. Four sub-interfaces are created in the KL-Router to enable the end devices in each VLAN to communicate with one another. The sub-interfaces are configured with the IP addresses of the VLAN default gateways based on each department.</p>


<h2>KL Server Farm LAN</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL-Server-Farm-LAN.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>The KL Server Farm consists of three servers which are the DNS , web and FTP server. This server are grouped into one VLAN which has the VLAN ID of 50 and is named KL-ServerFarm. There is a centralized switch which acts as a access layer and also distributor layer switch. The switch-to-server connections are configured as access points to VLAN 50 whereas the switch-to-router connection is configured as a trunk port.</p>


<h2>Server Configurations</h2>

<p>The servers in KL Server Farm are configured statically to allow the management to customize the Ips of the servers manually.</p>

<h4>KL-WEB-SERVER</h4>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL-WebServer.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h4>KL-DNS-SERVER</h4>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL-DNS.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<h4>KL-FTP-SERVER</h4>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL-FT.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h2>VLAN Management-KL SERVER FARM</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/VLAN%20Management%20KL-Server%20Farm.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h2>KL Sever Farm Trunking Port Configuration in Switch</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL%20Sever%20Farm%20Trunking%20Port%20Configuration%20in%20Switch.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>The interface which connects to the router is configured as a trunk port with the 801.1q encapsulation mode.</p>


<h2>KL Server Farm InterVLAN Routing Configuration</h2>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL%20Server%20Farm%20InterVLAN%20Routing%20Configuration.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />



<h2>Hanoi Site WLAN</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi%20Site%20WLAN.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>The Hanoi remote branch has a distributed switch in the center which connects the access layers to the core layer. Three access points are configured in the Hanoi LAN to facilitate a wireless architecture in the remote branch to ease the wireless communication and connections. Three VLANs are created in this LAN which are the management VLAN which is the native VLAN with the VLAN ID of 100, the R&D VLAN with the VLAN ID of 10 and also the Blackhole VLAN for unused ports. The DHCP server is configured in the Hanoi-Router which enables DHCP for the end devices in the network to obtain their IP addresses dynamically. This is done to improve the scalability of the network. The end devices in R&D Floor 1,2 and 3 access the VLAN 10 which is the R&D VLAN for communications whereas the Radius server and the admin PC is accessing the management VLAN. The radius server is configured with authorized usernames and password to authenticate the remote connection to network devices.</p>


<h2>VLAN Management-Hanoi Site</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi-Site%20VLAN%20Management.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h2>Trunking Port Configuration in Hanoi Multilayered Switch</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi%20Trunking%20Port%20Configuration.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h2>Hanoi Site InterVLAN Routing Configuration</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi%20Site%20InterVLAN%20Routing%20Configuration.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>2 sub-interfaces are configured in the Hanoi-Router for the management VLAN and also the R&D VLAN. Both interfaces are configured with the IP address of the default-gateway of both VLANs to enable connections with multiple VLANs.</p>

<h2>AAA Radius Server Configuration in Hanoi</h2>

<p>The radius server is configured with a AAA service where multiple authorized user credentials are stored for accessing the networking devices in the Hanoi LAN via SSH.</p>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi%20Radius%20Server.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h2>WAN Configurations</h2>

<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/WAN%20Configurations.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />

<p>The WAN of this network consists of 3 routers and also a core ISP network which is a cluster of two ISP routers. The serial ports of the routers are configured with IP addresses in order to communicate with each other. The serial DCE ports are configured with the clock rate of 64000 to ensure a stable and fast connection to route packets.</p>


<h2>OSPF Protocol Configuration in Routers</h2>

<p> OSPF has been chosen as it does not have a limit to the hop count as the RIP routing protocol and also provides better load balancing than other routing protocol. OSPF is also adaptive to scalable networks which is suitable for enterprise level networks as they are constantly making changes to scale and improve their network.</p>


<h4>Hanoi-Router</h4>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Hanoi%20Router%20OSPF.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />


<h4>KL-Router</h4>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/KL%20Router%20OSPF.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />



<h4>KL-Server-Farm-Router</h4>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/Server%20Farm%20Router%20OSPF.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />



<h4>ISP1-Router</h4>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/ISP1%20Router%20OSPF.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />



<h4>ISP2-Router</h4>


<br />
<br />
<p align="center">
<img src="https://github.com/Iknowmyname/Network_Prototype/blob/main/Images_NP/ISP2%20Router%20OSPF.png" height="65%" width="65%" alt="sV"/>
</p>
<br />
<br />
 <!--
<h2>Security Implementations</h2>
-->
<!--
- <b>[SSH & Port Security Configuration](https://github.com/Iknowmyname/)</b> 
- <b>[ACL Configuration](https://github.com/Iknowmyname/)</b>
- 
-->
