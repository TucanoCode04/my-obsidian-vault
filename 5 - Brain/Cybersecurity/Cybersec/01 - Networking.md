
2025-10-14 15:24

Status: 

Tags:

# Networking
Layered network architecture, where each layer serves the layer above it and is served by the layer below it.

Some notation:
- SAP : Service Access Point
- PAN : Personal Area Network
- LAN : Local Area Network
- MAN  : Metropolitan Area Network
- WAN : Wide Area Network
#### ISO/OSI Model
Open Systems Interconnection model (ISO/OSI) is nowadays only a theoretical model, rarely used in practice. It consists of 7 layers:
![[Pasted image 20260128162517.png]]
##### Layer 1 - Physical Layer
In charge of the physical connection between devices. It sends signals to a peer device through a transmission medium. It offers to Layer 2 the capacity of transmitting bits over a medium. Like electrical signals on cables(wired Ethernet), radio waves(Bluetooth, Wi-Fi), or light signals(fiber optics).
The signals, for every technology, becomes weaker with distance, and are subject to noise and interference, so we use repeaters to regenerate the signal.
##### Transmission Unit (PDU)
Each layer has its own Protocol Data Unit (PDU), which is the unit of data that is transmitted at that layer, it's composed of:
- header: control information added by the layer, like source, destination, type, length, etc..
- payload: the actual data being transmitted, which is the PDU from the layer above. The payload has a maximum size defined by the layer(Maximum Transport Unit).
- trailer(optional): additional control information added by the layer, like error detection codes, end markers, etc..

The PDU of one layer is transported as payload of the next lower layer, which may require fragmentation into more units of that lower layer. This is called encapsulation.
![[Pasted image 20260128164135.png]]
##### Layer 2 - Data Link Layer
It offers Layer 3 the capacity of sending and receiving small data units called frames between two devices connected on the same local network(homogeneous network). It is also called MAC layer (Media Access Control), since it provides access to the physical transmission medium. It uses L1 to transport bits between two peer connected devices.
In 802.3 and 802.11 each peer device has a unique 48-bit MAC address assigned by the manufacturer(the initial bytes identify the manufacturer). The MAC address is used to identify the source and destination of frames on the local network.
The PDU at this layer is called frame, and it is composed of:
- header(14 bytes): 
	- Destination MAC address(6 bytes)
	- Source MAC address(6 bytes)
	- Type/Length(2 bytes)
- payload(46-1500 bytes): data from Layer 3, up to 9000 bytes in jumbo frames
- trailer(4 bytes): Frame Check Sequence(FCS), used for transmission error detection

There exist different types of destination addresses:
- unicast: address of a single device(peer)
- broadcast: address used to send frames to all devices on the local network
- multicast: address used to send frames to all peers that listen to a channel
- anycast: address used to send frames to the peers that provide specific services, it is used as a gateway to reach external networks

The base network device at this layer is the switch, which connects multiple devices on the same local network. It uses MAC addresses to forward frames only to the destination device, reducing collisions and improving performance.
It is composed of multiple ports to connect a node(802.3). Is has a special port, trunk, used from connection with other switches and it learns the port associated with each MAC(location of the nodes) so it can forward frames correctly, either to the specific port or to the switch that manages that MAC address.
![[Pasted image 20260128170556.png]]
##### Layer 3 - Network Layer
It uses L2 to transport bits from one peer to another and it offers L4 the capacity of sending and receiving small data units called IP packets across networks that can have different technologies(heterogeneous networks, really important, every layer above on other basically doesn't depend on the lower layers). It is responsible for routing packets from source to destination across multiple networks, using logical addressing(IP addresses), so each peer is basically identified by either a 32-bit(IPv4) or 128-bit(IPv6) IP address. The packets that do not fit as a payload of L2 frames are fragmented into multiple packets and reassemble only at the destination.
Each node has a unique MAC address assigned to its NIC(Network Interface Card) at L2, useful for communication inside the local network, and an IP address assigned at L3 and knowledge of which address are in its local network(subnet) and the gateway address to reach external networks.
The local network in addressing is identified by the netmask, which indicates which bits of the IP address are used for the network(1s) and which for the host(0s). The lowest address in the subnet is the network address(all host bits 0) and the highest is the broadcast address(all host bits 1).
The basic example for 192.168.1.7 with a netmask 255.255.255.0 (/24):
- 192.168.1.0 - network address
- 192.168.1.1-254 - usable host addresses
##### DHCP
Dynamic Host Configuration Protocol (DHCP) is used to automatically assign IP addresses and other network configuration parameters to devices on a network, allowing them to communicate effectively. When a device connects to the network, it sends a broadcast request for an IP address asking for a valid network configuration (for his own node)(A.MAC > L2.broadcast). The DHCP server responds with a broadcast reply containing the offered network configuration(A.IP, A.netmask, GW.IP and NS.IP).
##### ARP
Address Resolution Protocol (ARP) is used to map IP addresses to MAC addresses within a local network. When a device (node) needs to communicate with another device (peer) on the same local network, it sends a broadcast ARP request asking for the MAC address associated with the target IP address(A.MAC > L2.broadcast, basically saying "I'm address A.IP - A.MAC, who is B.IP?"). The device with the matching IP address responds with an ARP unicast reply containing its MAC address(A.MAC < B.MAC, "B.IP is B.MAC"). 
The result is also cached in an ARP table for future reference. The response could fail if the target IP address is not in the local network.
The base network device at this layer is the router, which connects multiple networks together and routes packets between them. Each network has a border router that connects it to other networks, using routing tables to determine the best path for each packet based on its destination IP address.
![[Pasted image 20260128173016.png]]
Autonomous Systems (AS) are large networks or group of networks under a common administration that share a common routing policy. Each AS is assigned a unique AS number (ASN) for identification in inter-AS routing. Each AS announces its IP address ranges (prefixes) to other ASes using Border Gateway Protocol (BGP) to compute the best paths for routing packets between ASes.
##### Excursus on PDUs 
- L2 uses frames to transport packets from L3
- L3 uses packets to transport segments from L4
- L4 uses segments(TCP) or datagrams(UDP) to transport data from L7
- L7 uses file, messages, requests, responses depending on the application protocol used
##### Layer 4 - Transport Layer














##### Layer 7 - Application Layer
TCP/IP networks typical have a process layer that defines operations o









## References
