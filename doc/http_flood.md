#HTTP Flood

HTTP flood is a type of Distributed Denial of Service (DDoS) attack in which the attacker exploits seemingly-legitimate HTTP GET or POST requests to attack a web server or application.

HTTP flood attacks are volumetric attacks, often using a botnet “zombie army”—a group of Internet-connected computers, each of which has been maliciously taken over, usually with the assistance of malware like Trojan Horses.

A sophisticated Layer 7 attack, HTTP floods do not use malformed packets, spoofing or reflection techniques, and require less bandwidth than other attacks to bring down the targeted site or server.

As such, they demand more in-depth understanding about the targeted site or application, and each attack must be specially-crafted to be effective. This makes HTTP flood attacks significantly harder to detect and block.
Attack Description

When an HTTP client like a web browser “talks” to an application or server, it sends an HTTP request - generally one of two types of requests: GET or POST. A GET request is used to retrieve standard, static content like images while POST requests are used to access dynamically generated resources.
HTTP flood - 690,000,000 DDOS requests from 180,000 botnets IPsIncapsula mitigates a massive HTTP flood: 690,000,000 DDoS requests from 180,000 botnets IPs.

The attack is most effective when it forces the server or application to allocate the maximum resources possible in response to each single request. Thus, the perpetrator will generally aim to inundate the server or application with multiple requests that are each as processing-intensive as possible.

For this reason HTTP flood attacks using POST requests tend to be the most resource-effective from the attacker’s perspective; as POST requests may include parameters that trigger complex server-side processing. On the other hand, HTTP GET-based attacks are simpler to create, and can more effectively scale in a botnet scenario.
Methods of Mitigation

HTTP flood attacks are very difficult to differentiate from valid traffic because they use standard URL requests. This makes them one of the most advanced non-vulnerability security challenges facing servers and applications today. Traditional rate-based detection is ineffective in detecting HTTP flood attacks, since traffic volume in HTTP floods is often under detection thresholds.

The most highly-effective mitigation mechanism rely on a combination of traffic profiling methods, including identifying IP reputation, keeping track abnormal activity and employing progressive security challenges (e.g., asking to parse JavaScript).

Incapsula’s Web Application Protection solution relies on a unique client classification engine that analyzes and classifies all incoming site traffic. This anti-DDoS solution is specifically designed to transparently identify malicious bot traffic—stopping all HTTP floods and other Application Layer (OSI Layer 7) DDoS attacks.

Moreover, Incapsula solutions leverage unique crowdsourcing and reputation-based techniques, enabling granular control over who can access a given website or application.

<https://www.incapsula.com/ddos/attack-glossary/http-flood.html>


HTTP Flood

An HTTP flood is an attack method used by hackers to attack web servers and applications. It consists of seemingly legitimate session-based sets of HTTP GET or POST requests sent to a target web server. These requests are specifically designed to consume a significant amount of the server’s resources, and therefore can result in a denial-of-service condition (without necessarily requiring a high rate of network traffic). Such requests are often sent en masse by means of a botnet, increasing the attack’s overall power.

HTTP flood attacks may be one of the most advanced non-vulnerability threats facing web servers today. It is very hard for network security devices to distinguish between legitimate HTTP traffic and malicious HTTP traffic, and if not handled correctly, it could cause a high number of false-positive detections. Rate-based detection engines are also not successful at detecting HTTP flood attacks, as the traffic volume of HTTP floods may be under detection thresholds. Because of this, it is necessary to use several parameters detection including rate-based and rate-invariant.

<https://security.radware.com/ddos-knowledge-center/ddospedia/http-flood/>