
2025-11-12 12:16

Status: 

Tags:

# Security of Network Applications
##### Channel Security
When designing network applications, ensuring the security of data in transit is crucial. This includes implementing:
- authentication(single or mutual) to verify the identities of communicating parties,
- integrity checks to ensure data has not been altered during transmission,
- privacy during transit to protect sensitive information from eavesdropping.
- no possibility of non-repudiation to prevent parties from denying their involvement in a communication.
This practice normally requires no modification of the applications themselves, as security is handled at the transport layer (e.g., using TLS/SSL).
##### Message/data Security
Now, differently from channel security, message/data security focuses on protecting the actual content of the messages being exchanged, not just the transmission channel. This involves:
- authentication(single)  to verify the sender's identity,
- integrity checks to ensure the message has not been altered,
- privacy self-contained within the message to protect sensitive information,
- possibility of non-repudiation to ensure that the sender cannot deny sending the message.
This practice requires modification of the applications to incorporate security features directly into the message structure.
##### Security Internal to Applications
(slide)
##### Security External to Applications
(slide)
##### Secure Channel Protocols
The most widely used secure channel protocol is SSL/TLS, which provides a robust framework for securing communications over networks. 
Another protocol is SSH, which is primarily used for secure remote login and command execution.
Microsoft also developed its own secure channel protocol called PCT (Private Communication Technology), although it was a fiasco and is now largely obsolete.
##### TLS(once SSL- Secure Sockets Layer)
TLS (Transport Layer Security) is the successor to SSL and is the most widely used protocol for securing internet communications. It provides:
- Peer authentication through digital certificates, the server is usually authenticated, while client authentication is optional, because this is used in web browsing where clients are numerous and diverse, but you want to be sure that the server is legitimate.
- Message confidentiality using encryption
- Message authenticity and integrity through MACs (Message Authentication Codes)
- Protection against replay and filtering attacks using sequence numbers and nonces.
It is easily applicable to all protocols that run over TCP, such as HTTP, FTP, SMTP, and IMAP.
Before it was SSL, now it is TLS, the current version is TLS 1.3, everything before TLS 1.2 is considered insecure.
**Authentication and Integrity in TLS**
(slide)
**Confidentiality in TLS**
(slide)
**TLS Handshake Protocol**
![[Pasted image 20251112124016.png]]
1. ...
2. ...





## References
