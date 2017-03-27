#Apache Killer

"Apache Killer" is a severe vulnerability (discovered in August 2011) affecting the widely used Apache web server. Despite the fact that the vulnerability had been previously described in January 2007 by Google security researcher Michal Zalewski, it was only patched in Apache version 2.2.20 (released a week after knowledge of the vulnerability was public in August 2011), and version 2.2.21 which presented a more effective fix.

The vulnerability allowed an attacker to send a request to an Apache server to retrieve URL content in a large number of overlapping "byte ranges" or chunks, effectively causing the server to run out of useable memory - resulting in a denial-of-service condition.

According to a June 2012 survey conducted by Netcraft, nearly two thirds of all Internet domains use Apache. Given how widespread the use of Apache is, such a critical vulnerability left unpatched would prove a serious threat to the majority of Internet domains; this is especially true if the Apache Killer vulnerability was integrated into the DDoS software running on large botnets. It's likely that many Apache servers have not been updated and are therefore still vulnerable to this exploit.

<https://security.radware.com/ddos-knowledge-center/ddospedia/apache-killer/>