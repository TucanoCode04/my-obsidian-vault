
2025-10-22 11:12

Status: 

Tags:

# Exercises
##### Question 1: Alice wants to open a communication channel with Bob. Which of the following security properties she must implement in order to check that she is really communicating with Bob?
This is the definition of Peer-Authentication.
##### Question 2: Assume Alice sends a message to Bob. Bob knows that he has to perform data authentication. What does it mean?
Bob must ensure that the message he received was sent by Alice and was not altered during transmission. 
##### Question 3: Assume Alice wants to connect to two systems run by Bob. Alice and Bob must always perform mutual authentication. What does it mean?
Mutual authentication means that both Alice and Bob verify each other's identities before establishing a communication channel. This ensures that Alice is indeed communicating with Bob's systems, and Bob's systems are indeed communicating with Alice.
##### Open Question: Explain the concept of defense-in-depth in the context of cybersecurity and discuss why this approach is considered more effective than relying on a single layer of defense.
Defense-in-depth is a cybersecurity strategy that involves implementing multiple layers of security controls and measures to protect information and systems. The idea is to create a comprehensive security posture that addresses various potential threats and vulnerabilities at different levels, making it more difficult for attackers to penetrate the system. Each layer of defense serves as a barrier that an attacker must overcome, thereby increasing the overall security of the system.
##### Question 13: What is a DDos attack? (justify your answer)
An attacker exploits daemons(zombies and masters) to flood a target system with traffic, overwhelming its resources and causing service disruption. It's distributed because it uses multiple compromised systems to launch the attack, making it harder to mitigate. A zombie is a compromised computer controlled by an attacker, while a master is the command-and-control server that coordinates the attack.
##### Question 14: Bob is an attacker who decides to activate a DNS shadow server to attack Alice? 
A DNS shadow server is a malicious server set up by an attacker to intercept and manipulate DNS queries. When Alice tries to access a legitimate website, her DNS request is redirected to the shadow server controlled by Bob. This allows Bob to provide false IP addresses, redirecting Alice to malicious websites, stealing sensitive information, or launching further attacks. The use of a DNS shadow server can lead to phishing attacks, malware distribution, and other security breaches. It can also allow for a Denial of Service (DoS) attack of Alice's access to legitimate services.
##### Question 21:
![[WhatsApp Image 2025-10-29 at 10.35.54 AM.jpeg]]



## References
