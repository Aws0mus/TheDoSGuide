Herramientas
============

-	FloodNet

https://oddletters.com/2012/07/15/hope9-talk-activist-ddos-when-similes-and-metaphors-fail/ https://www.thing.net/~rdom/ecd/ZapTact.html

-	ByteDos

ByteDos is a windows desktop DoS application. It is a simple, standalone executable file which does not require any special installation on the attacker's PC.

ByteDoS is equipped with embedded IP resolver capabilities that allow this attack tool to resolve IPs from domain names. This DoS tool supports two attack vectors: SYN flood and ICMP flood , allowing the user to choose which vector to use during the attack.

ByteDos also supports attacks behind Proxy, which enables the attackers to hide their source and identity.

This tool is very common among Hacktivists and Anonymous supporters, and it becomes very effective when used by many attackers in a well-coordinated DDoS attack.https://security.radware.com/ddos-knowledge-center/ddospedia/bytedos/

-	Low Orbit Ion Cannon (LOIC)

Low Orbit Ion Cannon (LOIC) was originally developed by Praetox Technologies as an open-source network stress testing tool. It allowed developers to subject their servers to heavy network traffic loads for diagnostic purposes, but it has since been modified in the public domain through various updates and been widely used by Anonymous as a DDoS tool.

LOIC (which runs on both Microsoft Windows and Mac OS X) is a flooding tool used to generate a massive amount of network traffic in order to utilize network or application resources. Such a high rate of traffic results in performance degradation and potentially a loss of service. A user armed with LOIC can perform a denial-of-service (DoS) attack on a target site by flooding its server with illegitimate TCP, UDP, or HTTP packets. On its own, one computer running Low Orbit Ion Cannon cannot generate enough TCP, UDP, or HTTP requests at once to overwhelm the average web server. It takes thousands of computers all targeting a single server to have any real impact.

The IRC-based "Hive Mind" mode enables a LOIC user to connect his or her copy of LOIC to an IRC channel in order to receive a target and other attack parameters via an IRC topic message. Using many copies of Low Orbit Ion Cannon running in Hive Mind mode across many computers, a third party such as the "hacktivist" group Anonymous can take control of each copy of LOIC simultaneously. With thousands of copies of LOIC attacking a single target, the effect on network performance can be much more significant than that of a "normal" coordinated Low Orbit Ion Cannon attack. Hive Mind mode effectively lets anyone with a computer participate in a distributed denial-of-service attack, as LOIC requires very little computer literacy to operate.

LOIC has been used in several well-known attacks against large organizations including but not limited to Anonymous' Project Chanology, Operation Payback, and OpSony. Over 30,000 downloads of LOIC were recorded between the 8th and 10th of December 2010 when Anonymous organized attacks on the websites of companies and organizations that opposed Wikileaks. Since Low Orbit Ion Cannon was utilized by a vast number of attackers in conjunction with a few advanced users employing their large botnets to launch additional DDoS attacks, many of the targeted sites suffered outages.

While LOIC is simple and effective, it does not make any attempt to spoof its users' IP addresses, and most volunteers running LOIC are unaware of this lack of anonymity. If any form of non-anonymous attack is not routed through an anonymizer such as Tor, I2P, or some form of proxy server, the attacker's IP address can be logged by his or her target. An ISP can then use a list of logged attacking IP addresses to identify the individuals participating in an attack, allowing for the proper law enforcement actions to be taken against them.

Several countries including the United States have taken legal actions against Low Orbit Ion Cannon attackers based on the IP information. On January 27, 2011, five people were arrested in the UK in connection with the Operation Payback attacks, while in June 2011 another three LOIC users were arrested in Spain for their involvement in other attacks. On June 14 2011, Turkish police arrested 32 individuals who allegedly attacked government websites in protest against the introduction of state level web filtering; these individuals are thought to be members of Anonymous that used the LOIC tool as a means of protest. As a result of various arrests, LOIC's popularity began to decline towards the end of 2011.

https://security.radware.com/ddos-knowledge-center/ddospedia/loic-low-orbit-ion-cannon/

https://github.com/NewEraCracker/LOIC/

-	HOIC (High Orbit Ion Cannon)

“High Orbit Ion Cannon” or HOIC for short is a network stress testing tool related to LOIC; the use of both for launching DDoS attacks was popularized in recent years by the “hacktivist” group Anonymous. Unlike its “low-orbiting” cousin, HOIC is able to cause DoS through the use of HTTP floods. Additionally, HOIC has a built-in scripting system that accepts .hoic files called “boosters”, allowing a user to implement some anti-DDoS randomization counter measures as well as increase the magnitude of his or her attack.

While HOIC (similarly to LOIC) still has no significant obfuscation or anonymization techniques to protect the user, the use of .hoic “booster” scripts allows the user to specify a list of rotating target URLs, referrers, user agents, and headers in order to more effectively cause a DoS condition by attacking multiple pages on the same site, as well as make it seem like attacks are coming from a number of different users.

https://security.radware.com/ddos-knowledge-center/ddospedia/hoic-high-orbit-ion-cannon/

-	Mobile LOIC

Mobile LOIC is the online web version of LOIC. It is a Javascript-based HTTP DoS tool that is delivered within an HTML page, has very few options and is limited to conducting HTTP floods. Unlike its PC counterpart, Mobile LOIC does not support more complex options, like randomization of URLs and remote control by IRC botnets (“the Hive”).

Mobile LOIC is flexible because it can run on various browsers and be accessed remotely. Typically, attack organizers post a URL for the website hosting the page and invite others to use the tool to attack the specified target. Since only a web browser is required, an attacker can use a smartphone to generate an attack.

Offering extremely simple operation, Mobile LOIC has only three configuration parameters:

```
Target URL - the URL of the attacked target. Must start with http://
Requests per second - the number of desired requests to be sent per second
Append message - the content for the message parameter to be sent within the URL of HTTP requests
Consisting of simple 100 lines of code that execute web requests in a loop. It is possible to append text with an appropriately revolutionary message.
```

Recently, a new variant of the Mobile LOIC was detected, which incorporates several techniques to bypass detection and provide greater redundancy. These include:

```
A JavaScript method that prevents left mouse click in order to prevent users from viewing the page source code.
Obfuscating all JavaScript methods contained and referenced on page, which may slow down security researchers from fully investigating this tool and its capabilities.
Removal of a message field that existed in the original version and had its value included in the attack packets themselves. This is most likely in order to try and avoid signature based protections.
Links from each attack page to up to 4 mirror attack pages hosted on other servers in order to quickly reference users and allow the attack campaign to continue even if one or more of the mobile LOIC nodes are taken down.
Additionally, several “cosmetic” functionalities were also added such as listing the number of current attackers using the tool, and reflecting the current client IP detected by the tool which may prove useful when trying to avoid attacks using an attackers real IP address.
```

https://security.radware.com/ddos-knowledge-center/ddospedia/mobile-loic/

-	Dosis

-	Darkness (Optima)

The Darkness (Optima) bot software is an advanced commercially available piece of malware developed by cyber criminals in Russia for the purpose of forming botnets to perform distributed denial-of-service (DDoS) attacks, steal passwords, and use infected machines for traffic tunneling (as proxy servers) among other functions. Anyone can purchase a copy of Darkness (Optima) from various underground online forums for as low as $450 and as high as $999, depending on the number of add-ons, updates, and rebuilds the user desires.

The original bot, “Darkness” was released in 2009. After being very well-received by the underground cyber crime community, its command and control interface was revamped and dubbed “Optima”. The bot, now referred to by the double name Darkness (Optima), released its tenth iteration at the end of 2011. Its most common use is to perform various types of DDoS attacks using amassed botnets of infected hosts: HTTP floods, ICMP floods, SYN floods, and UDP floods.

https://security.radware.com/ddos-knowledge-center/ddospedia/darkness-optima/

-	hping

Hping is a free TCP/IP packet generator and analyzer created by Salvatore Sanfilippo (also known as Antirez) that is similar to the ping utility; however, it has more functionality than the sending of a simple ICMP echo request that ping is usually used for. Hping can be used to send large volumes of TCP traffic at a target while spoofing the source IP address, making it appear random or even originating from a specific user-defined source.

https://security.radware.com/ddos-knowledge-center/ddospedia/hping/

-	itsoknoproblembro

The 'itsoknoproblembro' tool was designed and implemented as a general purpose PHP script injected into a victim’s machine allowing the attacker to upload and execute arbitrary Perl scripts on the target’s machine.

The 'itsoknoproblembro' script injects an encrypted payload, in order to bypass IPS and Malware gateways into the website main file index.php, allowing the attacker to upload new Perl scripts at any time.

Initial server infection is usually done by using the well-known Remote File Inclusion (RFI) technique. By uploading Perl scripts that run different DOS flood vectors, the server might act as a Bot in a DDOS Botnet army.

Although originally designed for general purpose, some variants of this tool found in the wild were customized to act as a proprietary DDOS tool, implementing the flood vector logics inside without the need to upload additional scripts.

https://security.radware.com/ddos-knowledge-center/ddospedia/itsoknoproblembro/

-	Pyloris

Pyloris is a slow HTTP DoS tool which enables the attacker to craft its own HTTP request headers. These include the packet header, cookies, packet size, timeout and CRLF option.

Pyloris objective is to keep TCP connections open for as long as possible between the attacker and the victims servers. This results in exhausting the server's connection table resources. Once the connection table of the server is exhausted, it will not be able to handle new connections from legitimate users, resulting in a denial-of-service.

https://security.radware.com/ddos-knowledge-center/ddospedia/pyloris/

-	Sockstress

Sockstress is an attack tool that exploits vulnerabilities in the TCP stack allowing an attacker to create a denial-of-service condition for a target server. In the normal TCP three-way handshake, a client sends a SYN packet to the server, the server responds with a SYN-ACK packet, and the client responds to the SYN-ACK with an ACK, establishing a connection. Attackers using Sockstress establish a normal TCP connection with the target server but they send a “window size 0” packet to the server inside the last ACK, instructing it to set the size of the TCP window to 0 bytes.

The TCP Window is a buffer that stores the received data before it uploads it up to the application layer. The Widow Size field indicates how much more room is in the buffer in each point of time. Window size set to zero means that there is no more space whatsoever and that the other side should stop sending more data until further notice. In this case the server will send window size probe packets to the client continually to see when it can accept new information, but because the attacker does not change the window size, the connection is kept open indefinitely.

By opening many connections of this nature to a server, the attacker consumes all of the space in the server’s TCP connection table (as well as other tables), preventing legitimate users from establishing a connection. Alternately, the attacker can open many connections with a very small (around 4-byte) window size, forcing the server to break up information into a massive number of tiny 4-byte chunks. Many connections of this type will consume a server’s available memory, also causing a denial-of-service.

https://security.radware.com/ddos-knowledge-center/ddospedia/sockstress/

Tor‘s Hammer

Tor's Hammer is a slow-rate HTTP POST (Layer 7) DoS tool created by phiral.net. The first public occurrence of this tool dates back to early 2011.

Tor’s Hammer executes a DoS attack by using a classic slow POST attack, where HTML POST fields are transmitted in slow rates under the same session (actual rates are randomly chosen within the limit of 0.5-3 seconds).

Similar to the former R.U.D.Y. (R-U-Dead-Yet) tool, the slow POST attack causes the web server application threads to await the end of boundless posts in order to process them. This causes the exhaustion of the web server resources and causes it to enter a denial-of-service state for any legitimate traffic.

A new functionality added to Tor's Hammer is a traffic anonym capability. DoS a ttacks can be carried out through the Tor Network by using a native socks proxy integrated in Tor clients. This enables launching the attack from random source IP addresses, which makes tracking the attacker almost impossible

Though difficult to track, Radware is able to nullify a Tor's Hammer based attack and many other forms of DoS attacks. Learn more about protecting your site here.

https://security.radware.com/ddos-knowledge-center/ddospedia/tors-hammer/

Trin00 o Tribe Flood Network?

Trinoo is a botted network which has been attributed to numerous DDoS-type attacks. Although it's been around for a while and illustrated via a CERT advisory 99-04, the nature of the compromised network appears to have changed over the years. The Trinoo attacks are an example of latent compromised networks available for quick leverage when amplification networks are desired.

https://security.radware.com/ddos-knowledge-center/ddospedia/trin00/

Topera (IPv6)

Topera is a new security tool for IPv6, built with the intention to bypass Snort signature checks.

Snort is the most known IDS/IPS and is widely used in many different critical environments and some commercial tools (Juniper or Checkpoint) use it as detection engine as well. Topera is the first known tool out there to challenge IDS/IPS security with slow HTTP header attacks with IPv6.

It is written with Python and supports 3rd party plugins. It's primary intention is to promote awareness of the security implications of IPv6.

Topera version 0.0.2 is currently supporting TCP scan and SlowLoris attacks over IPv6.

https://security.radware.com/ddos-knowledge-center/ddospedia/topera/

XerSeS

https://security.radware.com/ddos-knowledge-center/ddospedia/xerxes/

Wireshark
