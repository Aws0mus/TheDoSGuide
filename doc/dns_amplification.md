#DNS Amplification

DNS amplification is a Distributed Denial of Service (DDoS) attack in which the attacker exploits vulnerabilities in domain name system (DNS) servers to turn initially small queries into much larger payloads, which are used to bring down the victim’s servers.

DNS amplification is a type of reflection attack which manipulates publically-accessible domain name systems, making them flood a target with large quantities of UDP packets. Using various amplification techniques, perpetrators can “inflate” the size of these UDP packets, making the attack so potent as to bring down even the most robust Internet infrastructure.
Attack Description

DNS amplification, like other amplification attacks, is a type of reflection attack. In this case, the reflection is achieved by eliciting a response from a DNS resolvers to a spoofed IP address.

During a DNS amplification attack, the perpetrator sends out a DNS query with a forged IP address (the victim’s) to an open DNS resolver, prompting it to reply back to that address with a DNS response. With numerous fake queries being sent out, and with several DNS resolvers replying back simultaneously, the victim’s network can easily be overwhelmed by the sheer number of DNS responses.
DNS amplification attack peaking at 100GbpsIncapsula mitigates a DNS amplification attack, peaking at ~100Gbps.

RReflection attacks are even more dangerous when amplified. “Amplification” refers to eliciting a server response that is disproportionate to the original packet request sent.

To amplify a DNS attack, each DNS request can be sent using the EDNS0 DNS protocol extension, which allows for large DNS messages, or using the cryptographic feature of the DNS security extension (DNSSEC) to increase message size. Spoofed queries of the type “ANY,” which returns all known information about a DNS zone in a single request, can also be used.

Through these and other methods, a DNS request message of some 60 bytes can be configured to elicit a response message of over 4000 bytes to the target server – resulting in a 70:1 amplification factor. This markedly increases the volume of traffic the targeted server receives, and accelerates the rate at which the server’s resources will be depleted.

Moreover, DNS amplification attacks generally relay DNS requests through one or more botnets – drastically increasing the volume of traffic directed at the targeted server or servers, and making it much harder to trace the attacker’s identity.
Methods of Mitigation

Common ways to prevent or mitigate the impact of DNS amplification attacks include tightening DNS server security, blocking specific DNS servers or all open recursive relay servers, and rate limiting.

However, these methods do not eliminate attack sources, nor do they reduce the load on networks and switches between name servers and open recursive servers. Also, blocking all traffic from open recursive servers can interfere with legitimate DNS communication attempts. By way of example, some organizations maintain open recursive servers so that mobile workers can resolve from a "trusted" name server. Blocking traffic from these servers can hinder their access.

Incapsula DDoS protection solution leverage Anycast technology to balance the attack load across its global network of high-powered scrubbing servers, where the traffic undergoes a process of Deep Packet Inspection (DIP) that filters out malicious DDoS traffic.

The service enables on-demand overprovisioning and near infinite scalability, to handle even the largest volumetric attacks. Moreover, Incapsula DDoS protection can be instantly deployed on top of any network infrastructure via a BGP announcement, which makes Incapsula the recipient of all incoming traffic.

Once deployed, Incapsula's proxy position ensures that DDoS traffic is filtered outside of the client's network, while all clean traffic is forwarded to its end-destination through a secure GRE tunnel.


<https://www.incapsula.com/ddos/attack-glossary/dns-amplification.html>