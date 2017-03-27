IP fragmentation attacks are a common form of denial of service attack, in which the perpetrator overbears a network by exploiting datagram fragmentation mechanisms.

Understanding the attack starts with understanding the process of IP fragmentation, a communication procedure in which IP datagrams are broken down into small packets, transmitted across a network and then reassembled back into the original datagram.

Fragmentation is necessary for data transmission, as every network has a unique limit for the size of datagrams that it can process. This limit is known as the maximum transmission unit (MTU). If a datagram is being sent that is larger than the receiving server's MTU, it has to be fragmented in order to be transmitted completely

![IP frag image](https://www.incapsula.com/images/illustrations/ddos-mini-site/ip-fragmentation.jpeg)

Example of how an IP datagram is fragmented and reassembled Example of how an IP datagram is fragmented and reassembled

The IP header in every datagram contains flags detailing whether fragmentation is allowed to take place. In cases where a "don't fragment" flag is attached to the IP header, the packet is dropped and the server sends out a message saying that the ICMP datagram is too big to transmit. The offset explains to the recipient device the exact order the fragments should be placed in for reassembly.
Attack Types

IP fragmentation attacks can take several forms. While they all exploit the breakdown of datagrams in order to overbear the target networks, there are some notable differences in how different attack vectors are executed.

    UDP and ICMP fragmentation attacks - These attacks involve the transmission of fraudulent UDP or ICMP packets that are larger than the network's MTU, (usually ~1500 bytes). As these packets are fake, and are unable to be reassembled, the target server's resources are quickly consumed, resulting in server unavailability.

    TCP fragmentation attacks (a.k.a. Teardrop) - Also known as Teardrop attacks, these assaults target TCP/IP reassembly mechanisms, preventing them from putting together fragmented data packets. As a result, the data packets overlap and quickly overwhelm the victim's servers, causing them to fail.

    Teardrop attacks are a result of an OS vulnerability common in older versions of Windows, including 3.1, 95 and NT. While patches were thought to have put a stop to these attacks, a vulnerability resurfaced in Windows 7 and Windows Vista, making Teardrop attacks once again a viable attack vector.

    The vulnerability was re-patched in the latest version of Windows, but operators should keep an eye out to ensure that it stays patched in all future versions.

Methods of Mitigation

IP fragmentation attacks are mitigated in several different ways, depending on the type and severity of the attack. Most mitigation methods ensure that malicious data packets never reach their target destinations. The most common one involves inspecting incoming packets for violations of fragmentation rules (e.g., using a router or a secured proxy).

At Incapsula, these inspections are augmented by dedicated DDoS protection hardware. On top of leveraging our on-edge position to observe fragmentation rules, Incapsula also employs blacklisting/whitelisting mechanisms that filter traffic based on factors such as IP reputation and rate patterns. Using these methods, our platform provides complete immunity from all types of IP fragmentation attacks.

<https://www.incapsula.com/ddos/attack-glossary/ip-fragmentation-attack-teardrop.html>