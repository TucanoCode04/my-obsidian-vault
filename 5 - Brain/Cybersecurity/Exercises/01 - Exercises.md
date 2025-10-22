
2025-10-22 10:13

Status: 

Tags:

# Exercises
##### Question 1: Which layer is responsible for converting "raw" data bits from the physical layer into frames?
Data link layer.
##### Question 2: At which layer for MAC addresses operate in the OSI model?
Data link layer, the addresses are of size 48 bits. To not be confused with IP addresses which operate at the Network layer and are of size 32 bits (IPv4) or 128 bits (IPv6).
##### Question 3: Which OSI layer is primarily responsible for end-to-end communication and reliability through error correction and flow control?
Transport layer, which includes protocols like TCP that ensure reliable data transfer. UDP operates at the same layer but does not provide reliability. 
##### Question 4: Transport Control Protocol:
Provides reliable data transmission through error detection, retransmission of lost packets, and flow control. Implements error checking mechanisms like checksums to ensure data integrity. It adopts different ports to distinguish between multiple applications on the same device, this is called multiplexing and it works at the Transport layer. We have 2^16 = 65536 ports available, ranging from 0 to 65535. Well-known ports (0-1023) are assigned to common services like HTTP (port 80) and HTTPS (port 443). Ports are logical constructs and do not correspond to physical ports on a device.
##### Question 5: User Datagram Protocol: 
UDP is a connectionless protocol that provides low-latency communication without the overhead of error correction and flow control. It is suitable for applications that require speed over reliability, such as video streaming and online gaming, real-time applications. Like TCP, UDP also uses ports to differentiate between multiple applications on the same device.
##### Question 6: Which layer handles routing of data across wide area network ...?
Network layer is responsible for routing data across wide area networks (WANs). It manages logical addressing (IP addresses) and determines the best path for data packets to travel from the source to the destination across interconnected networks.
##### Question 7: What is the primary function of the Session Layer in the OSI model?
Session layer is responsible for establishing, managing, and terminating sessions between applications. It provides mechanisms for dialog control, synchronization, and checkpointing to ensure that data exchange is organized and can be resumed in case of interruptions.
This layer is deprecated in the TCP/IP model, where its functions are often handled by the Transport layer or Application layer protocols.
##### Question 8: Which of the following are DNS record types?
- A (Address) Record: Maps a domain name to an IPv4 address.
- AAAA (IPv6 Address) Record: Maps a domain name to an IPv6 address.
- MX (Mail Exchange) Record: Specifies the mail server responsible for receiving email on behalf of a domain.
FQDN (Fully Qualified Domain Name): Not a DNS record type, but refers to the complete domain name for a specific host within the DNS hierarchy.
A record type is a specific format used to store information in the DNS system.
The difference between FQDN and CNAME is that FQDN is the complete domain name for a specific host, while CNAME (Canonical Name) is a type of DNS record that maps an alias name to the true or canonical domain name.
##### Question 9: Which of the following are types of DNS servers in the DNS hierarchy?
- Root DNS Servers: The top-level DNS servers that respond to queries for records in the root zone and direct requests to appropriate TLD servers.
- TLD (Top-Level Domain) DNS Servers: These servers manage the top-level domains (like .com, .org, .net) and direct queries to the authoritative DNS servers for specific domains.
- Authoritative DNS Servers: These servers hold the actual DNS records for domains and respond to queries with the requested information.
- Forwarding DNS Servers: These servers forward DNS queries to other DNS servers, often used to cache responses for improved performance.
ICMP (Internet Control Message Protocol) Servers: Not a type of DNS server; ICMP is a network layer protocol used for error messages and operational information.
##### Question 10: 





## References
