
2025-09-27 21:28

Status: 

Tags:

# Introduction to Cybersecurity

The possible consequences of a successful attack might be:
- financial loss: both direct(fund transfer) or indirect(value of share)
- recovery cost: get the system back to normal operations and improve the system to avoid new attacks
- productivity cost: process stopped or delayed
- business disruption: customers may choose alternative suppliers
- reputation damage

Complexity of the Information and Communication Technology(ICT):
- personal devices: laptop, smartphone, smart TV
- communication networks: wired and wireless networks
- distributed services: hosting, cloud, IoT, computation and storage
- programming increasingly complex: stratification, framework
##### Risk Evaluation
To evaluate how risk prone is a service, we first analyze the risks bound to the asset(set of goods, data and people needed for an IT service), then we observe the possible events(vulnerabilities(intrinsic weakness of an asset) that can produce threats(possible action or event that can produce loss of security property by exploiting a vulnerability)) to prevent attacks(threats occurrence: deliberate action) and negative events(threat occurrence: accidental event)
##### Risk Management
To successfully manage the risks you need to keep into account not only the impact but also the available time and budget to solve it. Risk assessment matrices are useful for that.
![[Pasted image 20250929120619.png]]

Basically evaluation analyzes assets, vulnerabilities and threats to evaluate the risks, and then the management selects countermeasures, implements them and the there's an audit.
##### Security in the lifecycle of a system
![[Pasted image 20250929121113.png]]

##### Concepts and relations in cybersecurity
![[Pasted image 20250929121201.png]]

##### Window of exposure
![[Pasted image 20250929121230.png]]

###### State of Art: magnitude of malware for different ops
- Windows: O($10^6$)
- MacOs: O($10^3$)
- Linux: O($10^4$)
- Android: O($10^5$)

##### Weight of Evidence: responsible disclosure
A software house responsible for cybersecurity analysis called Zero Day Initiative sets a 120 days deadline, as part of their responsible disclosure policy, for the vendor to fix the vulnerabilities they found, and then they disclose it to the public. This is done to put pressure on the vendor, inform users and security professionals about the risks and maintain transparency.
##### List of Standardization Bodies
(slides 18-19)

##### What is security?
Security is a process, not a product. Products provide protection, but the only way to effectively do business in an insecure world is to put processes in place that recognize the inherent insecurity in the products. The trick is to reduce your risk of exposure regardless of the products or patches.
##### Some security principles
- Security in Depth: multiple layers of security controls(firewalls + antivirus + encryption + access control)
- Security by Design: built into the system from the start(input validation, secure coding practices)
- Security by Default: secure out of the box(default strong pwds, disabled unnecessary services)
- Separation of Duties: no single person should have control over all aspects of a critical process
- Least Privilege: users and systems should only have the minimum access they need to perform their tasks
- Need-to-Know: access should be granted only if it is necessary for a specific role or task(HR data only visible to HR staff)

##### Security properties and principles
- C.I.A: confidentiality, integrity and availability
- Simple/Mutual Authentication
- Peer Authentication: security process where identities of the single(Single Peer Authentication) or two communicating systems(Mutual Peer Authentication) are verified against each other
- Data/Origin Authentication: a security process to confirm a message's claimed sender and guarantee it has not been altered during transmission
- Authorization, Access Control: the process of determining whether a user or system has the right to access a resource or perform an action
- Integrity: the property that data has not been altered, filtered or destroyed in an unauthorized manner
- Confidentiality, Privacy, Secrecy: the property that information is not made available or disclosed to unauthorized individuals, entities, or processes
- Non-repudiation: formal proof(acceptable by a court of justice) of the origin and integrity of data. We, almost, never have non-repudiation with protocols or procedures that perform automatic actions, because there's no human intervention.
- Availability
- Traceability, Accountability
##### Replay Attack
A replay attack is a a network attack in which a valid data transmission is maliciously or fraudulently repeated or delayed. This or delayed. This is normally done by an adversary who intercepts data and retransmits it. 
##### Data Protection
For each security property, we consider 3 categories of data protection:
- Data in Transit: data transmitted over a communication channel, we need network security(firewalls, VPNs, TLS, IPsec)
- Data at Rest: data stored on stored on a device, we need storage security(encryption, access control)
- Data at Work: data being processed, for example in RAM used by a process, we need processing security(secure coding practices, memory protection)
##### Where is the enemy?
- Outside of organization: boundary, perimeter defence(firewalls, IDS/IPS)
- Outside of organization with exception of partners: extranet security(VPNs, secure APIs)
- Inside of organization: LAN, Intranet security(network segmentation, access control)
- Everywhere: application security(secure coding practices, regular updates), data security(encryption, access control), ZTA(Zero Trust Architecture)

- Position:
	- Man-in-the-Middle(MitM): sitting between two communicating peers A and B
	- Man-at-the-End(MitE): having control over one of the two communicating peers, A or B
	- Man-in-the-Browser(MitB): having control over the web browser of one of the two communicating peers, A or B
- Capability: 
	- Passive: can only eavesdrop the data or the traffic
	- Active: can also modify, inject or delete data or traffic
##### Basic technological problems
The networks are insecure: 
- Most communications are made in clear
- LANs operate in broadcast mode
- Wireless communication is easy to intercept, while wired communication requires physical access.
- Geographical connections are not made through end to end dedicated lines but through shared lines or third party routers

The user authentication is normally password-based, that is weak.
Server authentication is also weak, normally based on certificates that can be forged or stolen.
The softwares already contain bugs and vulnerabilities.
##### Some classes of Attacks
- IP Spoofing(Masquerading): an attacker uses the address of of a trusted host, to take its place as a client or a server. Forging the source IP address(level 3) or the MAC address(level 2). An alternative name is Source Address Spoofing.
	- attacks: data forging, unauthorized access
	- countermeasures: do never use address-based authentication
- Packet Sniffing(Eavesdropping): an attacker intercepts and reads data packets in transit over a network. It's easier to perform in a broadcast network(LAN) or at the switching nodes(routers, switches). 
	- attacks: allows to intercept anything
	- countermeasures: encryption of packet payload(TLS, IPsec), non-broadcast networks
- Connection Hijacking/Data Spoofing: an attacker takes over an active network connection to insert, delete or manipulate the traffic. It can be a logical or physical MitM attack.
	- attacks: reading, insertion of false data and modification of data exchanged between two parties
	- countermeasures: secrecy, authentication, integrity and serialization of each individual network packet
- Shadow Server: an attacker sets up a fake server that mimics a legitimate one to deceive users. It can be accomplished by request sniffing and response spoofing(it's difficult cause the fake server needs to respond faster than the real one) or wrong mapping(DNS manipulation, routing table manipulation)
	- attacks: issue wrong answers and wrong services, capture victims' data
	- countermeasures: server authentication(certificates)
- Denial of Service(DoS): an attacker overwhelms a system with traffic or requests to make it unavailable to legitimate users. It keeps an host busy so that it can't provide its service(mail/log saturation, ping bombing, SYN attack)
	- attacks: block the use of a system/service
	- countermeasures: monitoring and oversizing can mitigate the effects but there are no real solutions
- Distributed Denial of Service(DDoS): an attacker uses multiple compromised systems to launch a coordinated DoS attack. Softwares for DoS are installed on many node(named daemon, zombie or malbot) to create a botnet. Daemons are remotely controlled by a master through a command and control(C&C) infrastructure, with C/S or P2P communications, encrypted or covert channels and auto-update capabilities. The effects are similar to DoS but multiplied by the number of daemons.
- Trojan: a program containing a dangerous payload(hidden inside a useful program, like a keylogger inside a game or a browser extension). This attack can function over a protected network because the user voluntarily installs the trojan. It's often used to create backdoors like MitB and MatE attacks. 
- Virus and Worm: a malicious program that damages the target and replicates itself, the propagation is involuntary done by humans(virus) or is automatic(worm). (Only viruses create damage???). It's used to create backdoors(unauthorized access points), rootkits(hide the presence of certain processes or programs through privilege escalation) or install trojans or PUA( potentially unwanted applications). They require complicity from the user, the sys manager or the producer.
	- countermeasures: user awareness, antivirus, correct configuration/secure software
- Ransomware: a type of malware created to encrypt files on a device or lock the system, then demand a ransom to restore access. It's not only relative to the technology but also to procedures and organizations: encrypted data? How old is the backup? Off-line or network backup? Verified or £trusted backup? When was the attack discovered?  
- Phishing: an attacker impersonates a trusted entity (such as a bank, company, or colleague) to trick users into revealing sensitive information like passwords, credit card numbers, or login credentials. It’s typically carried out through deceptive emails, fake websites, fake kidnapping alarms or instant messages that appear legitimate. Variants include **spear phishing** (targeted attacks against specific individuals or organizations), **whaling** (targeting high-profile figures such as executives), and **smishing/vishing** (using SMS or voice calls instead of email). It's easy to create a fake email, but it's difficult to replicate the right tone, so it's easier to use the original mail with a different(malicious) attachment.
    - **attacks:** credential theft, financial fraud, identity theft, malware installation through malicious links or attachments
    - **countermeasures:** user awareness and training, email filtering, verification of URLs and sender addresses, use of multi-factor authentication, and anti-phishing tools integrated into browsers and mail clients

We can implement all types of securities but it is all subject to human errors. 
##### Malware food chain
![[Pasted image 20250929185422.png]]
##### Non technological problems
There may be some problems related to human nature, for example a poor understanding of the existence of the problem(awareness of the problem), mistakes(leaded by stress or work overloading), the human tendency to trust, complex interfaces or architecture(can mislead the user) or a performance decrease due to the application of security measures

Some other problems related to social engineering techniques and strategies through mail, phone or even paper:
- asking for the user's involuntary participation in the attack
- targeting a naive user(change the password with this password because your pc in under attack)
- targeting more experienced users(copying authentic emails with different attachments or URLs)
- exerting psychological pressure(help, I'm in trouble, do it or I'll report to the boss)
- lowering the targets defenses by showing acquaintance with the company's procedures, habits or personnel
##### Some attacks
- **T.J.Maxx attack**: hackers infiltrated TJX network by exploiting weak wireless encryption (WEP) used in their in-store Wi-Fi. Once inside, the attackers installed sniffer programs that intercepted data from customers’ credit and debit cards as it was transmitted to the company’s servers. Over an 18-month period, they stole information linked to more than 45 million payment cards, leading to widespread financial fraud.
- **Stuxnet:** was a highly sophisticated state-sponsored cyberweapon that specifically targeted Iran’s nuclear enrichment facilities. It spread through USB drives and Windows vulnerabilities using worms and viruses, secretly infiltrating industrial control systems (SCADA) made by Siemens. Once inside, Stuxnet manipulated the centrifuges used to enrich uranium by making them spin at destructive speeds while showing normal readings to operators, causing physical damage without detection. Believed to have been developed jointly by the United States and Israel, Stuxnet marked the first known malware capable of causing real-world physical destruction, ushering in the era of cyberwarfare and critical infrastructure attacks. The attacks and propagation vectors were 2 known zero days vulnerabilities. The first injection was likely via a USB key from a maintenance technician, the attack was disguised as a driver with a digital signature validated by Microsoft and the use of 2 different certificates, then it accesses the back-end DB from the infected node through a shared default password on every node(vulnerability). Lesson learnt: systems protected with physical separation, no unnecessary services active and validation list for software to be installed
- **Fancy Bear/APT 28**: The group is known for cyber-espionage and disinformation campaigns targeting governments, media, and defense organizations, particularly in NATO and Europe. Ukrainian artillery-targeting Android app (an APK named Попр-D30.apk) with its X-Agent for Android implant and posted it on military forums between late 2014 and 2016. The malicious build looked like a legitimate targeting/ballistics tool used by D-30 howitzer crews but secretly exfiltrated device metadata (notably location), allowing the actor to infer the positions and movements of Ukrainian rocket and artillery units
- **Mirai:** The Mirai botnet, first identified in 2016 (Mirai 1), was a massive distributed denial-of-service (DDoS) attack that infected Internet of Things (IoT) devices such as routers, cameras, and DVRs. By exploiting default factory credentials, Mirai turned these devices into a global botnet capable of overwhelming major websites and services—including Twitter, Netflix, and Dyn—with unprecedented traffic volumes. The attack revealed the security weaknesses of IoT ecosystems and how easily they could be hijacked. Later variants, like Mirai 2, expanded on the original code (which was publicly released), leading to multiple derivative botnets used by criminals and hacktivists worldwide. Together, the Mirai attacks highlighted the dangers of insecure connected devices and the urgent need for better default security configurations and firmware updates in consumer electronics.
##### Three(Four) Pillars of Security
- **0 Planning phase:** preliminary phase. It involves defining a security policy, setting goals, identifying assets, and determining the acceptable level of risk. Essentially, it’s about planning how security should be managed before any technical measures are implemented.
- **1 Avoidance**: avoiding security incidents by implementing protective measures, to reduce vulnerabilities and prevent attacks: Firewalls(to block unauthorized access), VPNs(secure communication over untrusted networks), PKI(Public Key Infrastructure, to manage encryption and digital certificates)
- **2 Detection:** some attacks will still happen, so we need to ensure quick awareness of the threats to respond promptly: IDS(Intrusion Detection Systems), Network and System Monitoring(suspicious behavior or breaches)
- **3 Investigation:** after an incident is detected we need to analyze what happened: Forensic Anl




## References
