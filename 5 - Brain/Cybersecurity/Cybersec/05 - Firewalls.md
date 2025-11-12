
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
The rules are more fine-grained compared to packet filters, as they can be based on:


## References
