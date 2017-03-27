#DNS Flood

DNS flood is a type of Distributed Denial of Service (DDoS) attack in which the attacker targets one or more Domain Name System (DNS) servers belonging to a given zone, attempting to hamper resolution of resource records of that zone and its sub-zones.

DNS servers are the “roadmap” of the Internet, helping requestors find the servers they seek. A DNS zone is a distinct portion of the domain name space in the Domain Name System (DNS). For each zone, administrative responsibility is delegated to a single server cluster.

In a DNS flood attack the offender tries to overbear a given DNS server (or servers) with apparently valid traffic, overwhelming server resources and impeding the servers’ ability to direct legitimate requests to zone resources.
Attack Description

DNS flood attacks should be clearly differentiated from DNS amplification attacks. DNS amplification is an asymmetrical DDoS attack in which the attacker sends out a small look-up query with spoofed target IP, making the spoofed target the recipient of much larger DNS responses. With these attacks, the attacker’s goal is to saturate the network by continuously exhausting bandwidth capacity.

DNS floods are symmetrical DDoS attacks. These attacks attempt to exhaust server-side assets (e.g., memory or CPU) with a flood of UDP requests, generated by scripts running on several compromised botnet machines.

A DNS flood attack is considered a variant of the UDP flood attack, since DNS servers rely on the UDP protocol for name resolution, and is a Layer 7 attack. With UDP-based queries (unlike TCP queries), a full circuit is never established, and thus spoofing is more easily accomplished.
DNS flood - 25 million packets per second

To attack a DNS server with a DNS flood, the attacker runs a script , generally from multiple servers. These scripts send malformed packets from spoofed IP addresses. Since Layer 7 attacks like DNS flood require no response to be effective, the attacker can send packets that are neither accurate nor even correctly formatted.

The attacker can spoof all packet information, including source IP and make it appear that the attack is coming from multiple sources. Randomized packet data also helps offenders to avoid common DDoS protection mechanisms, while also like IP filtering (e.g., using Linux IPtables) completely useless.

Another common type of DNS flood attack is DNS NXDOMAIN flood attack, in which the attacker floods the DNS server with requests for records that are nonexistent or invalid. The DNS server expends all its resources looking for these records, its cache fills with bad requests, and it eventually has no resources to serve legitimate requests.
DNS flood - 25 million packets per secondIncapsula mitigates a massive DNS flood, peaking at over 25Mpps (million packets per second)

Methods of Mitigation

Large Layer 3 attacks like DNS floods are very difficult for on-premises solutions to mitigate.

Incapsula’s approach to mitigating DNS floods is simple and hassle-free. The solution is enabled by a dedicated anti-DDoS 'DNS Protection' service. Using DNS Protection, clients are able to deploy Incapsula's multi-datacenter network in front of their DNS authoritative server—doing so without making any changes to their existing zone file settings.

With the DNS Protection in place, Incapsula becomes the destination for all incoming DNS queries, which are scrubbed on their way to their origin.

Incapsula users can then continue to set their own custom thresholds, with different values provided for the more likely-to-be-legitimate “safe” queries (e.g. ftp.mydomain.com). In addition, users can also manually enforce DNS freshens by electing to refresh all cached data or by selectively refreshing specific DNS records.

<https://www.incapsula.com/ddos/attack-glossary/dns-flood.html>