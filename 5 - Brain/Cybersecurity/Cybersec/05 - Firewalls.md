
2025-11-12 10:17

Status: 

Tags:

# Firewalls
A firewall is used to monitor and control incoming and outgoing network traffic between a network with an higher security level(trusted) and a network with a lower security level(untrusted), based on a set of security rules.
It implements compartmentalization, meaning that it separates different network segments to limit the spread of potential threats.
- Ingress firewalls: control incoming traffic, used to select the services that can be accessed from outside the network. 
- Egress firewalls: control outgoing traffic, used to restrict access to certain external resources from within the network, to monitor the activities of internal users and to prevent data exfiltration.
This division is easily implemented in channel-based services like TCP, where the connection is established before data transmission, but it is more difficult in connectionless, message-based services like UDP.
Three important rules:
- the firewall must be the only communication path between the external and internal networks;
- only the authorized traffic should be allowed to pass through the firewall;
- the firewall must be secure itself and should be minimal to reduce vulnerabilities.
##### Firewall Policies
So we need to write some authorization rules to define what traffic is allowed or denied:
1. all that is not explicitly allowed is denied (default deny); It is more secure but requires more configuration. This can be implemented through permitlist or allowlist.
2. all that is not explicitly denied is allowed (default allow); It is less secure but requires less configuration. This can be implemented through blocklist or denylist.
##### Firewall Basic Components
A firewall is composed of:
- packet filter/scrrening/choke: inspects each packet and accepts or rejects it based on source and destination IP addresses, ports and protocols, so it works at network level
- bastion host: a special-purpose computer on the network that is specifically designed and configured to withstand attacks. It usually runs proxy servers and works at application level.
- application gateway(proxy): a dedicated computer that acts as an intermediary between two networks, with access control rules based on applications or services.
- dual-homed gateway: a computer with with two network interfaces, one connected to the trusted network and the other to the untrusted network, with controlled forwarding of packets between the two networks. The routing is disabled to prevent direct communication.

The controls can be made at different levels, each controlling different aspects of the communication:
- network level: controls IP addresses and protocols; Packet filtering firewalls operate at this level.
- transport level: controls ports and sessions; Circuit gateways operate at this level.
- application level: controls the content of the messages, the application being used and the services requested; Application gateways operate at this level.
The trade-off between security(more secure at higher levels) and performance(more efficient at lower levels) must be considered when choosing the appropriate firewall type.
So the differences in firewall technologies can be summarized as follows:
- controls to be performed (IP addresses, ports, applications); That is detecting malicious activity.
- performance impact (latency, throughput); Higher levels introduce more latency and reduce throughput.
- protection of the firewall itself; Higher levels provide better protection against attacks targeting the firewall.
- keeping or breaking the client-server model; Lower levels maintain the original client-server relationship, while higher levels may require clients to connect to the firewall first.
##### Packet Filter
A packet filter is the most basic type of firewall that inspects each packet and accepts or rejects it based on predefined rules. It operates at the network layer, normally implemented on a router or a dedicated firewall device.
It examines the IP Header and TCP/UDP Header of each packet, looking at:
- source and destination IP addresses;
- source and destination ports;
- protocol type (TCP, UDP, ICMP).
The rules can be based on:
- allow or deny specific IP addresses or ranges;
- allow or deny specific ports or port ranges;
- allow or deny specific protocols.
- allow on the internal DNS server to query external DNS servers, but deny all other DNS traffic.
- typically, there is an implicit deny rule at the end of the rule set, meaning that any traffic not explicitly allowed is denied. 
- so the order of the rules is important, as the first matching rule is applied.
Packet filters are fast, easily scalable(meaning they can handle large amounts of traffic), and they are cost-efficient. However, they have limitations:
(look the slide up)
##### Application Gateway
An application gateway, also known as an application-level firewall or proxy firewall. It is composed of many proxies that inspect the packet payload at the application layer, allowing or denying traffic based on specific application-level protocols and content. It may mask or renumber the internal IP addresses to enhance security and it performs peer authentication, meaning that both the client and server must authenticate themselves to the firewall before communication can occur.
It is secure against buffer overflow attacks and other application-level threats, as it can inspect the content of the messages. However, it introduces higher latency and reduces throughput due to the deep inspection of packets, and it requires more configuration, even modifying the client application, and maintenance.
There are differences between forward and reverse proxies.
- A forward proxy acts on behalf of clients, forwarding their requests to external servers. It is used to control and monitor outbound traffic from the internal network to the internet.
- A reverse proxy acts on behalf of servers, receiving requests from external clients and forwarding them to the appropriate internal servers. It is used to protect and optimize inbound traffic to the internal network from the internet.
The rules are more fine-grained compared to packet filters. 
The cons are that it is higher latency, reduced throughput, since each application needs a specific proxy, it's heavy on resources.
It completely breaks the client-server model, since clients need to connect to the proxy first.
But there are problems with pairing it with application-level security techniques like SSL/TLS, since the firewall cannot inspect encrypted traffic unless it performs SSL/TLS termination, which involves decrypting the traffic at the firewall and re-encrypting it before forwarding it to the destination server. This introduces additional complexity and potential security risks.
**HTTP Forward Proxy**
An HTTP forward proxy is a server that acts as an intermediary for HTTP requests from internal clients to external web servers. It's an egress firewall that filters and controls outbound HTTP traffic. The benefits include, beside the ACL(Access Control List) filtering:
- a shared cache of external web content, reducing bandwidth usage and improving performance for frequently accessed resources, for all internal clients;
- it requires authentication, so only authorized users can access external web resources;
- you can implement content filtering, blocking access to certain websites or categories of content based on organizational policies.
**HTTP Reverse Proxy**
An HTTP reverse proxy is a server that acts as an intermediary for HTTP requests from external clients to internal web servers. It's an ingress firewall that filters and controls inbound HTTP traffic. It implements network ACL and content filtering, but also:
- obfuscates the internal server structure, hiding the details of the internal network from external clients, enhancing security;
- TLS acceleration, offloading the computationally intensive task of SSL/TLS encryption and decryption from the internal web servers, improving their performance;
- load balancing, distributing incoming HTTP requests across multiple internal web servers to optimize resource utilization and improve availability.
- web acceleration, caching frequently accessed web content to reduce latency and improve response times for external clients.
- compression of web content to reduce bandwidth usage and improve load times for external clients.
- spoon feeding, meaning that the reverse proxy can send data to clients at a controlled rate, preventing overwhelming slow clients and improving overall performance.
You can have possible configurations:
- external network -> firewall(-> internal network) ->(DMZ) -> reverse proxy -> internal server
- external network -> firewall(-> internal network) ->(DMZ) -> reverse proxy -> VPN -> internal server - > internal network
##### Web Application Firewall(WAF)
A Web Application Firewall (WAF) is a specialized firewall that protects web applications by filtering and monitoring HTTP/HTTPS traffic between a web application and the internet. It operates at the application layer and is designed to protect against common web application attacks. The WAF is a module that can be integrated into an existing firewall or deployed as a standalone solution. It is typically part of a reverse proxy but it can also be used for forward proxy.
ModSecurity is an open-source WAF that can be deployed as a module for web servers like Apache, Nginx, and IIS. It provides protection against various web application attacks by inspecting HTTP/HTTPS traffic and applying a set of predefined rules.
##### Packet Filter Architecture
It can be implemented between the external and internal networks, but it is insecure since an attacker can bypass it by connecting directly to the internal network.
(slide)
To enhance security, it can be implemented on a dual-homed host, which has two network interfaces, one connected to the external network and the other to the internal network. It is used to check the content of the traffic between the two networks, with routing disabled to prevent direct communication.
It's easy to implement an it masquerades internal IP addresses, but it can become a bottleneck since all traffic must pass through it, more specifically the difference incoming and outgoing traffic.
To improve performance, it can be implemented on a screened host architecture. The packet filter now is both connected to the external and internal networks, so if the traffic is trusted it can pass directly between the the two networks, otherwise it is sent to the dual-homed host for inspection. The problem is that if the packet filter is compromised, the internal network is exposed, creating a single point of failure.
(slide)
To further enhance security, a screened subnet architecture can be used. Here, a demilitarized zone(DMZ) is created between the external and internal networks, with two packet filters: one between the external network and the DMZ, and another between the DMZ and the internal network. The dual-homed host is placed in the DMZ to inspect traffic between the two networks. This setup provides an additional layer of security, as even if the DMZ is compromised, the internal network remains protected.
The two packet filters should have different rulesets to prevent an attacker from exploiting the same vulnerability in both filters or even physically different to prevent the possibility of having the same vulnerability.
You normally put on the DMZ public-facing services like web servers, email servers, DNS servers, FTP servers, etc., so that they can be accessed from the external network while still being isolated from the internal network, to prevent direct access in case they are compromised.
In this architecture, the internal network can can be made unknown to the external network by routing all traffic through the DMZ, enhancing security by obscurity. The only cons is the increased complexity and cost of implementing and maintaining the additional components.
(A VLAN is a logical subdivision of a physical network, allowing multiple virtual networks to coexist on a single physical infrastructure. It provides segmentation and isolation of network traffic, enhancing security and performance. VLANs can be used to create separate network segments for different departments, user groups, or services within an organization, allowing for better control over network access and traffic flow. By using VLANs, organizations can implement security policies that restrict communication between different segments, reducing the risk of unauthorized access and improving overall network security. Additionally, VLANs can help optimize network performance by reducing broadcast traffic and improving bandwidth utilization.)
To reduce the cost and complexity, the packet filters can be implemented as software on the gateway/router that connects the internal network to the external network, instead of using dedicated hardware devices. It is called three-legged firewall, since the gateway/router has three network interfaces: one connected to the external network, one connected to the internal network, and one connected to the DMZ.
##### Local/Personal Firewall
A local or personal firewall is a software application installed on individual computers or devices to monitor and control incoming and outgoing network traffic. It provides an additional layer of security by protecting the device from unauthorized access and potential threats from the internet or other networks.
Differently for a network firewall it may limit the processes and applications permitted to act as network clients or servers, controlling the traffic based on application-level rules.
It's a firewall directly installed at the node to be protected, it is normally just a packet filter.
It's important to limit the diffusion of malwares and trojans or to avoid configuration changes made by malicious software.
In order to be effective, the firewall management must be separate from the system management, to prevent malware from disabling the firewall.
Normally when you install a personal firewall, it asks you to define rules for allowing or denying traffic for specific applications, and it may also provide predefined rules for common applications and services.

## References
