Otros ataques
=============

La lista de ataques DoS y DDoS puede ser interminable, debido a las muchas formas en las que puede darse. Desde saturar la red con paquetes hasta llenar una máquina con logs y así llenar al 100% el disco.

Border Gateway Protocol (BGP) Attack
------------------------------------

The BGP attack is a DDoS attack where attackers take control of a large amount of fast routers to overwhelm their victim. The idea behind it is to take advantage of the ability of routers to exchange router tables. The attackers let the controlled routers know that their target is a router asking for a routing table's exchange, which results in the sending of a big amount of incoming packets to the victim, therefore overwhelming it.

https://security.radware.com/ddos-knowledge-center/ddospedia/border-gateway-protocol/

Buffer Overflow Attack

A Buffer Overflow Attack is an attack that abuses a type of bug called a “buffer overflow”, in which a program overwrites memory adjacent to a buffer that should not have been modified intentionally or unintentionally. Buffer overflows are commonly associated with C-based languages, which do not perform any kind of array bounds checking. As a result, operations such as copying a string from one buffer to another can result in the memory adjacent to the new (shorter) buffer to be overwritten with excess data.

When a buffer overflow occurs in a program, it will often crash or become unstable. An attacker attempting to abuse a buffer overflow for a more specific purpose other than crashing the target system, can purposely overwrite important values in the call stack of the target machine such as the instruction pointer (IP) or base pointer (BP) in order to execute his or her potentially malicious unsigned code. Operating system and software vendors often employ countermeasures in their products to prevent Buffer Overflow Attacks; particularly call stack and virtual memory randomization. Given the existence of such protective measures, Buffer Overflow Attacks have been rendered more difficult, although still possible to carry out.

https://security.radware.com/ddos-knowledge-center/ddospedia/buffer-overflow-attack/

Ransomware

Cyber Ransom A category of information security threat that is growing in scale and sophistication. Its two primary forms are ransomware and ransom denial of service (RDoS) attacks-both of which seek to make digital assets unavailable until a payment is made, typically via a virtual currency.

https://security.radware.com/ddos-knowledge-center/ddospedia/cyber-ransom/

Fragmented ACK Attack

A Fragmented ACK attack is a variation of the ACK & PSH-ACK Flood that uses 1500-byte packets with the goal of hogging the target network’s bandwidth with only a moderate packet rate. If application level filters were applied on network equipment (routers and such), it will have to reassemble the packets, consuming much of its resources. If no filters were applied, these attack packets will be able to pass through many network security devices such as routers, ACLs, and firewalls undetected. These fragmented packets usually contain junk data, as the goal of the attacker is to simply consume all of the target network’s bandwidth.

https://security.radware.com/ddos-knowledge-center/ddospedia/fragmented-ack-attack/

Pull files from webs or ftp para saturar la redirect

https://security.radware.com/ddos-knowledge-center/ddospedia/internet-pipe-saturation/

LAND Attack In a DoS land (Local Area Network Denial) attack, the attacker sends a TCP SYN spoofed packet where source and destination IPs and ports are set to be identical. When the target machine tries to reply, it enters a loop, repeatedly sending replies to itself which eventually causes the victim machine to crash.

https://security.radware.com/ddos-knowledge-center/ddospedia/land-attack/

Naptha attacks Naptha is an availability attack which is conducted remotely. The attack focuses on starving resources and / or exploiting the features inherent to the TCP protocol. It is very efficient with the nature of its attacks and has a great potential to cause significant outages. Its efficiency is gained by using a raw packet handling technique rather than relying on the system’s native TCP/IP stack. Newer recipes are easy to spawn from this technique.

https://security.radware.com/ddos-knowledge-center/ddospedia/naptha-attacks/

Nuke

A Nuke is a type of antiquated denial-of-service (DoS) attack carried out by sending fragmented or corrupted (usually ICMP) packets to a target machine. For any machine running an older more vulnerable operating system, sending such packets to it will slow down and eventually stop it, resulting in a crash or Blue Screen of Death (BSoD) in the case of Windows.

Perhaps the most famous example of a Nuke attack was the 1997 WinNuke, which exploited vulnerability in Windows 95 that allowed for an attacker to cause a target machine to BSoD by sending it a string of invalid data on TCP port 139. The vulnerability used by WinNuke was patched by Microsoft a few weeks after its source code was released. Years later in 2002, a newer version of WinNuke surfaced that affected Windows NT, 2000, and XP, but it was quickly patched by Microsoft. Almost no modern operating systems are vulnerable to such an attack.

https://security.radware.com/ddos-knowledge-center/ddospedia/nuke/

Peer to peer attack

Peer-to-Peer attacks exploit the fabric of peering technology to perform attacks. These attacks distinguish themselves from other types of attacks because of the following:

1.	Attacker doesn't have to communicate with the clients for subversion and

2.	The automated nature of Peer-to-Peer technology can allow for BOT like amplification of an attack with the permission of the victim.

https://security.radware.com/ddos-knowledge-center/ddospedia/peer-to-peer-attack/

SQL Injection (DROP)

SIP Register Flood

Application layer attack on the Session Initiation Protocol- SIP in use in VoIP services, targeted at causing denial of service to SIP servers. A SIP Register flood consists of sending a high volume of SIP REGISTER or INVITE packets to SIP servers (indifferently accepting endpoint requests as first step of an authentication process), therefore exhausting their bandwidth and resource

https://security.radware.com/ddos-knowledge-center/ddospedia/sip-register-flood/

SIP Malformed Attack

Application layer attack on the Session Initiation Protocol- SIP in use in VoIP services, targeted at causing denial of service to SIP servers. A SIP malformed attack consists of sending any kind of non-standard messages (malformed SIP Invite for ex) with an intentionally invalid input, therefore making the system unstable.

https://security.radware.com/ddos-knowledge-center/ddospedia/sip-malformed-attack/

SIP Server Flood

Application layer attack on the Session Initiation Protocol- SIP (in use in VoIP services), targeted denial of service to SIP servers. Common attack vectors include SIP invite and register floods.

https://security.radware.com/ddos-knowledge-center/ddospedia/sip-server-flood/

SSL Garbage Flood

DDoS attack involves sending malformed SSL requests to target SSL servers and attempt to exhaust the servers’ resources, and to deny service from legitimate users. Pushdo botnet is an example tool which sends garbage data toward the target SSL server.

https://security.radware.com/ddos-knowledge-center/ddospedia/ssl-garbage-flood/

SIP brute force

SIP brute force is an adaptation of normal brute force attacks which attack SIP servers and attempt access to servers to make unauthorized outbound calls at another’s expense.

https://security.radware.com/ddos-knowledge-center/ddospedia/sip-brute-force/

SIP Client Call Flood

This is a flood technique focused on SIP application protocol which involves illegitimate call requests. The idea here is to flood the Session Boarder Control (SBC) and / or SIP / VOIP PBX with too many requests to handle and thus making the service unavailable.

https://security.radware.com/ddos-knowledge-center/ddospedia/sip-client-call-flood/

SYN-ACK Flood

A SYN-ACK flood is an attack method that involves sending a target server spoofed SYN-ACK packet at a high rate. Because a server requires significant processing power to understand why it is receiving such packets out-of-order (not in accordance with the normal SYN, SYN-ACK, ACK TCP three-way handshake mechanism), it can become so busy handling the attack traffic, that it cannot handle legitimate traffic and hence the attackers achieve a denial-of-service condition.

https://security.radware.com/ddos-knowledge-center/ddospedia/syn-ack-flood/

Teardrop Attack

A teardrop attack is a denial-of-service (DoS) attack that involves sending fragmented packets to a target machine. Since the machine receiving such packets cannot reassemble them due to a bug in TCP/IP fragmentation reassembly, the packets overlap one another, crashing the target network device. This generally happens on older operating systems such as Windows 3.1x, Windows 95, Windows NT and versions of the Linux kernel prior to 2.1.63.

One of the fields in an IP header is the “fragment offset” field, indicating the starting position, or offset, of the data contained in a fragmented packet relative to the data in the original packet. If the sum of the offset and size of one fragmented packet differs from that of the next fragmented packet, the packets overlap. When this happens, a server vulnerable to teardrop attacks is unable to reassemble the packets - resulting in a denial-of-service condition.

https://security.radware.com/ddos-knowledge-center/ddospedia/teardrop-attack/

HTTP get post grandes

jijijaja

Mail Bomb

This type of DDoS attack either targets a mailbox, or its host server. As the name suggests, a mail bomb attack sends numerous - generally in millions and billions - mass emails to a single email address. This floods the mailbox, and destabilizes the host server. Generally, a single (or multiple) mail addresses are targeted and sent millions of emails from multiple source addresses. Another type of mailbox attack is list linking, where a single email address is signed up to receive multiple subscription emails, thereby flooding the victim's inbox. Another mail bomb attack known as Zip bombing, where the attacker sends a compressed file, which contains an enormous text file, which makes it hard to unzip, thereby flooding the computer system.

https://www.iplocation.net/denial-of-service

Unintentional DDoS attack

This generally happens when a link to a small site is added to a very popular website. It is quite obvious that the website traffic increases significantly resulting in an unintentional overload to the host. Some smaller websites generally can only handle a very limited traffic, but temporary boost in traffic could crash the server causing unintentional DDoS from legitimate traffic.

https://www.iplocation.net/denial-of-service

Al fin y al cabo, cualquier ataque que sea capaz de consumir los recursos de una máquina, CPU, disco, red... puede ser considerado un ataque de denegación de servicio. https://www.cert.org/information-for/denial_of_service.cfm
