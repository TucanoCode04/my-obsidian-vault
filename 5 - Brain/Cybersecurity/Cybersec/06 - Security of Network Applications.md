
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
The most widely used secure channel protocol is SSL/TLS, which 



## References
