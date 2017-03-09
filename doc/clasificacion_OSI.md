Tipos ataques clasificados por la capa OSI

https://www.securitycompass.com/dds/?_escaped_fragment_=/layers#!/layers

Layer 7: Application 
Acts as the interface for users and applications allowing them to communicate over a network.

Slow Loris 
Slow POST 
Slow Read 
HTTP/S Flood 
CVE Attack Vectors 
Large payload POST requests 
Database Connection Pool Exhaustion 
Resource Exhaustion 
Mimicked User browsing 
DNS Query/NXDOMAIN floods 
Other protocol floods (SMTP, DNS, SNMP, FTP, SIP) 


Layer 6: Presentation 
Transforms data into a common format that is consumable by the Application Layer.

SSL Exhaustion 

Layer 5: Session 
Establishes a context which encapsulates the messages being exchanged between processes on different machines.

Long lived TCP sessions (Slow Transfer) 
Connection flood/exhaustion 


Layer 4: Transport 
Responsible for providing guarantees on message delivery, arrival order, loss recovery, and error recovery.

SYN Flood 
Other TCP Floods (varying state flags) 
UDP Flood 
IPSec Flood (IKE/ISAKMP association attempts) 


Layer 3: Network 
Allows packets to be routed through a network enabling indirectly connected nodes to exchange data messages.

BGP Hijacking 
ICMP Flood 
IP/ICMP Fragmentation 


Layer 2: Data Link 
Handles detecting and/or correcting errors introduced at layer 1 in order to establish a reliable link between two connected machines.

Attacks at layers 1 and 2 target the base of a network itself. They would require direct physical and internal access to a company's network, making them unlikely to be performed in the wild. 

Layer 1: Physical 
Defines the physical specification for translating digital data into signals to be sent across a physical medium (such as copper or wireless link).

Attacks at layers 1 and 2 target the base of a network itself. They would require direct physical and internal access to a company's network, making them unlikely to be performed in the wild. 
