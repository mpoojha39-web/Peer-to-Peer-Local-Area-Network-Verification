# Peer-to-Peer-Local-Area-Network-Verification
Peer-to-Peer Local Area Network Verification
Aim

To create and verify a Peer-to-Peer Local Area Network (LAN) by connecting two PCs through a Layer 2 switch, configuring static IPv4 addresses, and testing connectivity using ping and arp.

Network Topology

The network consists of:

PC0
PC1
Switch0 (2960 Series)
Copper Straight-Through cables
Network Configuration
Device	Interface	IPv4 Address	Subnet Mask	Default Gateway
PC0	FastEthernet0	192.168.10.25	255.255.255.0	192.168.10.1
PC1	FastEthernet0	192.168.10.26	255.255.255.0	192.168.10.1
Switch0	Fa0/1, Fa0/2	Default	—	—
1. Cabling and Link Status

PC0 and PC1 are connected to the 2960 switch using Copper Straight-Through cables.

PC0 → Switch0 Fa0/1
PC1 → Switch0 Fa0/2
The link indicators become green after the ports transition to forwarding state.

2. PC0 IP Configuration

PC0 is configured with the following static IPv4 settings:

IPv4 Address: 192.168.10.25
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.10.1

3. PC1 IP Configuration

PC1 is configured with the following static IPv4 settings:

IPv4 Address: 192.168.10.26
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.10.1

4. Verify PC0 IPv4 Configuration

The ipconfig command is used on PC0 to verify its IPv4 configuration.

ipconfig

PC0 shows the configured IPv4 address:

192.168.10.25

5. Test Connectivity Using Ping

The ping command is used from PC0 to test communication with PC1.

ping 192.168.10.26

Successful replies confirm that PC0 and PC1 can communicate through the switch.

6. Inspect the ARP Table

The ARP table is checked on PC0 using:

arp -a

The ARP table contains an entry for:

192.168.10.26

along with the corresponding MAC address of PC1. This confirms successful Layer 2 address resolution.

Result

The Peer-to-Peer LAN was successfully implemented using two PCs and a Layer 2 switch. Static IPv4 addresses were configured on both PCs, and connectivity was verified using ping. The ARP table also confirmed the MAC address resolution between the two devices.

Technologies Used
Cisco Packet Tracer
IPv4
Ethernet
Layer 2 Switch
Static IP Addressing
Ping
ARP
