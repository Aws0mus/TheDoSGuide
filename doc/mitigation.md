Medidas de mitigación
=====================

empresas como CloudFlare https://en.wikipedia.org/wiki/Anycast

-	Mitigaciones generales  
	https://www.incapsula.com/ddos/how-to-stop-ddos-attacks.html (general)  
	https://www.incapsula.com/web-application-ddos-protection-services.html (layer 7 protection)  
	https://www.incapsula.com/dns-ddos-protection-services.html (dns protection)https://www.incapsula.com/infrastructure-ddos-protection-services.html (infraestructura)  
	Molaria contactar con alguna empresa (Deloitte, Akamai, jijijaja...) para preguntar precios de parar ataques.

Clean Pipe A clean pipe is a partial DDoS mitigation solution for online businesses and mission critical websites that require real-time protection against volumetric DDoS attacks. The primary goal of this anti-DDoS protection solution is to block volumetric attack traffic before it enters an organization's data pipe, enabling web services to remain available for legitimate users. Without such protection, a large volume DDoS attack can clog an organization's Internet pipe, consuming all of its available bandwidth. In order to maintain a clean pipe, all traffic must pass through a cleaning center or "scrubbing center" where malicious traffic is identified and separated allowing only legitimate traffic to get to the server.

https://security.radware.com/ddos-knowledge-center/ddospedia/clean-pipe/

-	Puedo meter también info del documento sobre medidas de seguridad que tiene que hacer cada persona en la empresa (El Workshop)

-	WAF

-	IDS

-	IPS

-	Firewall

-	Honeypots

-	SIEM, logs ...

-	HTTP Challenge

An HTTP challenge is a method used to automatically mitigate HTTP based DDoS attacks . The challenge is intended to be passed by legitimate users and to fail the attackers.

One typical challenge is that after arrival of an HTTP request message, send back to the users a 302 Redirect message. A typical user with a web browser will pass that challenge, while an attacker that does not implement a full HTTP stack will ignore this redirect and send the original request again. A more complicated challenge is to add a cookie - now the client also has to store and resend this cookie. Advantages

```
This protection is considered very accurate, predictable and effective.
```

Disadvantages

```
A Web challenge also blocks's legitimate bots such as web crawlers which the site does not wish to block. This is because they too do not necessarily use a real browser or implement a full HTTP stack. Nevertheless many organizations will be willing to pay this price when under attack.
More sophisticated attack tools and bots can invest in passing the challenge or even using real web browsers so that they will pass the challenge. This however, requires the attacker to invest resources on his side and in most cases will decrease the attack capacity.
```

https://security.radware.com/ddos-knowledge-center/ddospedia/http-challenge/

-	JS cookie challenges

Used to authenticate legitimate sources in modern attack mitigation systems. If HTTP services are under DOS attack; the protection action is triggered. The Attack Mitigation System will authenticate requests by sending a challenge JavaScript response to the suspect client. If the client executes the received challenge JavaScript, generates the cookie, and re-sends the original HTTP request with the JavaScript-generated cookie, it proves that it is a legitimate browser-based client.

https://security.radware.com/ddos-knowledge-center/ddospedia/js-cookie-challenges/

-	Ingress Filtering (InFilter)

This technique checks the validity of incoming network packets’ SRC IPs making sure the IPs are not spoofed, before the packets enter the network and possibly affect it.

https://security.radware.com/ddos-knowledge-center/ddospedia/ingress-filtering-infilter/

-	Scrubbing Center

A centralized data cleansing station where traffic is analyzed and malicious traffic (ddos, known vulnerabilities and exploits) is removed. Scrubbing centers are often used in large enterprises, such as ISP and Cloud providers, as they often prefer to off-ramp traffic to an out of path centralized data cleansing station. When under attack, the traffic is redirected (typically using DNS or BGP) to the scrubbing center where an attack mitigation system mitigates the attack traffic and passes clean traffic back to the network for delivery. The scrubbing center should be equipped to sustain high volumetric floods at the network and application layers, low and slow attacks, RFC Compliance checks, known vulnerabilities and zero day anomalies.

https://security.radware.com/ddos-knowledge-center/ddospedia/scrubbing-center/

-	SYN cookies

SYN cookies is a technical attack mitigation technique whereby the server replies to TCP SYN requests with crafted SYN-ACKs, without inserting a new record to its SYN Queue. Only when the client replies this crafted response a new record is added. This technique is used to protect the server SYN Queue from filling up under TCP SYN floods.

https://security.radware.com/ddos-knowledge-center/ddospedia/syn-cookies/

1.	Install Intrusion Detection System (IDS) such as Advanced Intrusion Detection Environment (AIDE). For installation procedure, consult Linux Gazzette. Perform regular system audits by installing and running RKHUNTER and CHROOTKIT to make sure installed Linux binaries are healthy. You may also install open-source network audit tools like NESSSUS, NMAP, and SAINT and perform regular network audits for vulnerabilities.

2.	Implement Sysctl. Prevent ping attacks (ping of death, ping of flood, and smurf attacks) by disabling ping responses on the network machines. Enable IP Spoofing protection, and TCP SYN Cookie Protection. On Linux variant machines, follow sysctl configuration procedure.

3.	Install advanced firewall and DDoS utilities. To secure your server and protect from DoS attacks, you may want to install APF, BFD, DDoS and Rootkit. To install those utilities, please follow DDoS Prevention: APF, BFD, DDoS and RootKit setup procedure.

APF: Advanced Policy Firewall BFD: Brute Force Detection DDoS: DDoS Deflate Rootkit: Spy and Junkware detection and removal tool

1.	Install Apache mod_evasive and mod_security modules to protect against HTTP DDoS attacks.

https://www.iplocation.net/denial-of-service
