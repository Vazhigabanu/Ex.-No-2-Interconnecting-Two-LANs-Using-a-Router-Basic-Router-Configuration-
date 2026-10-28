# Date :
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
________________________________________

CONFIGURATION 

LAN1

<img width="1903" height="1043" alt="Screenshot 2026-10-28 092111" src="https://github.com/user-attachments/assets/e4bf260b-a818-49d4-b61a-bf116f214abc" />

<img width="1912" height="1037" alt="Screenshot 2026-10-28 092416" src="https://github.com/user-attachments/assets/113090c5-1ac8-423d-8f7d-5e294d6c4cc7" />

<img width="1908" height="1032" alt="image" src="https://github.com/user-attachments/assets/e9f6dec2-567f-4869-b51b-d632b321a603" />

LAN2

<img width="1901" height="1046" alt="Screenshot 2026-10-28 092449" src="https://github.com/user-attachments/assets/22bcec51-4903-46ae-89bc-e25f1d523924" />

<img width="1902" height="1051" alt="Screenshot 2026-10-28 092518" src="https://github.com/user-attachments/assets/aeb8aa60-1ca2-4c0f-aee4-fc6e1f939223" />

<img width="1910" height="1037" alt="Screenshot 2026-10-28 092556" src="https://github.com/user-attachments/assets/3d0ef91a-1075-48f1-9cd4-db7e11858226" />

SWITCH

<img width="1907" height="1041" alt="Screenshot 2026-10-28 095931" src="https://github.com/user-attachments/assets/f31c274b-e10a-4547-9a44-fd5a14c482a6" />

<img width="1905" height="1038" alt="image" src="https://github.com/user-attachments/assets/9fd6ff56-a9a0-4f0b-8545-1ce71ef73bea" />

ROUTER

<img width="1890" height="1078" alt="image" src="https://github.com/user-attachments/assets/e7e2da32-7c32-4d42-9dca-cad2814f8d96" />

PING 

LAN1

<img width="1888" height="1070" alt="image" src="https://github.com/user-attachments/assets/cd0c8928-d292-4a06-b3eb-10d1aa3e611b" />

<img width="1902" height="1077" alt="image" src="https://github.com/user-attachments/assets/6cb3d6ef-66fa-4b14-ac4c-4e381e0cc04e" />

<img width="1907" height="1061" alt="image" src="https://github.com/user-attachments/assets/4a071cc8-5e6d-4411-b6af-faf2cb869059" />

LAN2

<img width="1903" height="1080" alt="image" src="https://github.com/user-attachments/assets/7dd17666-3e13-4d96-83c7-88abd6ef37e1" />

<img width="1903" height="1031" alt="image" src="https://github.com/user-attachments/assets/24eac1a9-4750-4e4e-98cb-760710335aff" />

<img width="1907" height="1033" alt="image" src="https://github.com/user-attachments/assets/247fdd52-2ade-430c-b351-af1fa27cb647" />

SWITCH CONFIG 

SWITCH 0

<img width="1912" height="1067" alt="image" src="https://github.com/user-attachments/assets/1c01eacf-b0f9-4f98-b13f-605baabb148b" />

SWITCH 1

<img width="1917" height="1036" alt="image" src="https://github.com/user-attachments/assets/9c93b855-36f9-43e6-934e-2334302061c3" />

# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

