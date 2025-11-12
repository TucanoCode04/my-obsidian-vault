
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
So we need to write some authorization rules to define what traffic is allowed or denied:
1. all that is not explicitly allowed is denied (default deny); It is more secure but requires more configuration. This can be implemented through permitlist or allowlist.
2. all that is not explicitly denied is allowed (default allow); It is less secure but requires less configuration. This can be implemented through blocklist or denylist.

## References
