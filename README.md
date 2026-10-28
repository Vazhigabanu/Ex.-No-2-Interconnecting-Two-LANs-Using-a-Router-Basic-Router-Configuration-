# Date :28/10/2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
•	Router CLI configuration<br>
•	IP configurations on PCs<br>
•	Successful ping between PC0 and PC1<br>

CONFIGURATION :

LAN1

<img width="1903" height="1043" alt="Screenshot 2026-10-28 092111" src="https://github.com/user-attachments/assets/a6f468a8-3568-4a5b-8d8e-5eb53378fea4" />

<img width="1912" height="1037" alt="Screenshot 2026-10-28 092416" src="https://github.com/user-attachments/assets/09187dbc-fe32-4e0d-8b2b-626213f44298" />

<img width="1901" height="1046" alt="Screenshot 2026-10-28 092449" src="https://github.com/user-attachments/assets/235b7ec7-f4e8-4103-b0f0-c745f9ee8b31" />

<img width="1902" height="1051" alt="Screenshot 2026-10-28 092518" src="https://github.com/user-attachments/assets/af271216-c43a-4046-a5ea-e294f6ad0201" />

<img width="1910" height="1037" alt="Screenshot 2026-10-28 092556" src="https://github.com/user-attachments/assets/a3b449a5-9dac-45a5-8b8f-45feb1bd3930" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

