#R-U-Dead-Yet

###HTTP DoS attack via long form field submissions 

RUDY attack targets web applications by starvation of available sessions on the web server.

RUDY keeps sessions at halt using never-ending POST transmissions and sending an arbitrarily large content-length header value.

Herramienta

R-U-Dead-Yet o R-U-D-Y


Fuente 

<https://sourceforge.net/projects/r-u-dead-yet/>  
<http://www.ehacking.net/2011/09/r-u-dead-yet-http-post-denial-of.html>


Named after an album by Finish melodic death metal band Children of Bodom, R.U.D.Y. (short for R-U-Dead-Yet?) is a DoS tool used to execute slow-rate attacks (similar to Slowloris), which is implemented via long form field submissions.

Slow rate, Layer-7 DDoS attacks, also called “low and slow” attacks, attempt to open a relatively few connections to the targeted server or web site over a period of time, and leave the sessions open as long as possible.

Eventually, the number and length of open sessions exhaust the target’s resources, making it unavailable to legitimate traffic. Because low and slow attack traffic appears legitimate, these attacks often fly under the radar of traditional mitigation tools.
Attack Description

R.U.D.Y. is a popular low and slow attack tool that is designed to crash a web server by submitting long form fields.

The attack is executed via a DoS tool which browses the target website and detects embedded web forms. Once the forms have been identified, R.U.D.Y. sends a legitimate HTTP POST request with an abnormally long 'content-length' header field and then t starts injecting the form with information, one byte-sized packet at a time.

![](https://www.incapsula.com/images/illustrations/rudy-script.png)

Excerpt from R.U.D.Y. v2.2 ScriptExcerpt from R.U.D.Y. v2.2 script

The information is sent not only in small chunks but also at a very slow rate, typically with ~10 second intervals between each byte. Still, it should be noted that some variants of R.U.D.Y. will use random time intervals, to prevent detection.

By sending numerous small packets, at a very slow rate, R.U.D.Y. creates a massive backlog of application threads, while the long ‘'Content-Length’ field prevent the server from closing the connection. Ultimately, the attack exhausts the targeted server’s connection table, causing the server to crash.

In addition to automatically detecting web forms most R.U.D.Y. tools also allow the attacker to choose which form fields should be attacked. The latest version of R.U.D.Y. tools also supports SOCKS proxies and cookie-based session persistence, when available.

If undetected or unmitigated, Slowloris attacks can also last for long periods of time. When attacked sockets time out, Slowloris simply reinitiates the connections, continuing to max out the web server until mitigated.
Methods of Mitigation

Low-and-Slow attacks like R.U.D.Y. are relatively difficult to detect, compared to volumetric DDoS attacks which are noticeable due to the abnormally high fluctuation in incoming traffic.
HTTP flood - 690,000,000 DDOS requests from 180,000 botnets IPsjijijaja mitigates a massive HTTP flood: 690,000,000 DDoS requests from 180,000 botnets IPs.

One way to detect a R.U.D.Y. and other low and slow attacks, is by close server resource monitoring is required.

For example, some legacy mitigation solutions would track server memory and CPU usage, connection tables, application threads and more to identify abuse of resources, including long and idle open network connections or stuck application processes.

An additional mitigation method involves behavior analysis of open server connections. These solutions attempt to simulate application stack resource requirements without directly connecting to the server itself. If misuse is identified, it can be traced and mitigated.

jijijaja offers another, less complex and significantly more effective method of mitigating R.U.D.Y. and other low and slow DoS attacks.

jijijaja’s security services, which are are enabled by reverse proxy technology, are used for inspection of all incoming requests on their way to the clients’ servers. This means that jijijaja’s secured proxy will simply not forward any partial connection requests - rendering all R.U.D.Y. DoS attackscompletely useless.