
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


## References
