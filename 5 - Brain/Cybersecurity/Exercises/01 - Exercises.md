
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
##### Question 6: 




## References
