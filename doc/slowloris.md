#Slow Loris

El ataque Slowloris, desarrollado por Robert “RSnake” Hansen, permite a una sola máquina realizar un ataque de denegación de servicio sobre un servidor web. 

Coge su nombre del Loris Perezoso (Slow Loris en inglés), debido a que puede funcionar de forma lenta y continua.

![Slow loris image](../static/images/slowloris.jpeg)

Durante las protestas por las elecciones presidenciales de Irán, en 2009, se utilizó este ataque de denegación de servicio contra diversos sitios que pertenecían al gobierno iraní. Se eligió este ataque, sobre otros basados en saturar la red, debido a que estos segundos podían afectar tanto a las webs del gobierno como a las webs de los manifestantes. Al elegir este ataque el impacto fue más focalizado e implicaba un menor consumo de ancho de banda. (<https://web.archive.org/web/20090629152805/http://iran.whyweprotest.net/general-discussion/2156-list-anti-protester-sites-2.html>) (<https://web.archive.org/web/20090811013813/http://iran.whyweprotest.net/help-iran-online/6194-condensed-list-sites-w-pictures-part-1-a.html>)

##Descripción general del ataque

Slowloris se basa en abrir múltiples conexiones en el servidor web objetivo y manteniéndolas durante el máximo tiempo posible. Esto se consigue enviando peticiones HTTP parciales, las cuales jamás se completarán.

Los servidores víctima abrirán cada vez más conexiones, esperando por cada una de ellas a que llegue una petición completada.

Al final, el pool de conexiones del servidor alcanzará el máximo posible de sesiones simultáneas provocando que cualquier conexión adicional (legítima) sea rechazada.

Debido a que los paquetes no estarán malformados, sino que serán parciales, este ataque puede evitar fácilmente los IDS tradicionales que actuan sobre la capa 4 (capa de transporte) de la pila OSI.

Lo más característico del ataque es que no requiere muchos recursos para poder efectuarse. Similar al Loris Perezoso <https://es.wikipedia.org/wiki/Nycticebus> (Slow Loris en inglés, del cuál obtiene su nombre), este ataque puede funcionar de forma lenta y continua, esperando que los sockets del servidor se liberen de una conexión legítima para entonces poder acapararlos.

El ataque también puede ser efectivo en servidores web diseñados para altos volúmenes de tráfico o que reinicien las conexiones legítimas. En ambos casos el ataque será más lento pero, si no es mitigado, efectivo.

##Descripción técnica

**TODO**

##Características principales

- Consume muy poco ancho de banda.
- Es posible realizarlo con una única máquina.
- Afecta únicamente al servicio web atacado, con casi ningún efecto lateral en otros servicios y puertos.

##Mitigación

**TODO**

Methods of Mitigation
Incapsula’s security services are enabled by reverse proxy technology, used for inspection of all incoming requests on their way to the clients’ servers.
Incapsula’s secured proxy will not forward any partial connection requests—rendering all Slowloris DDoS attack attempts completely and utterly useless.

But this attack is easily defensible using popular load balancers and DDoS protection solutions, such as HaltDos and Cisco, reverse proxies and certain Apache modules.

While there are no reliable configurations of the affected web servers that will prevent the Slowloris attack, there are ways to mitigate or reduce the impact of such an attack. In general these involve increasing the maximum number of clients the server will allow, limiting the number of connections a single IP address is allowed to make, imposing restrictions on the minimum transfer speed a connection is allowed to have, and restricting the length of time a client is allowed to stay connected.

In the Apache web server, a number of modules can be used to limit the damage caused by the Slowloris attack; the Apache modules mod_limitipconn, mod_qos, mod_evasive, mod security, mod_noloris, and mod_antiloris have all been suggested as means of reducing the likelihood of a successful Slowloris attack.[1][5] Since Apache 2.2.15, Apache ships the module mod_reqtimeout as the official solution supported by the developers.[6]

Other mitigating techniques involve setting up reverse proxies, firewalls, load balancers or content switches.[7] Administrators could also change the affected web server to software that is unaffected by this form of attack. For example, lighttpd and nginx do not succumb to this specific attack.[1]

Referencias

* **Funcionamiento general**  
<https://www.incapsula.com/ddos/attack-glossary/slowloris.html>
* **Funcionamiento técnico**  
<https://isc.sans.edu/forums/diary/Apache+HTTP+DoS+tool+released/6601/>
<http://security.stackexchange.com/questions/86298/rsnakes-slow-loris-tool>
* **Medidas de mitigación**  
<https://isc.sans.edu/forums/diary/Apache+HTTP+DoS+tool+mitigation/6613/>
<http://www.techrepublic.com/blog/smb-technologist/secure-your-apache-server-from-ddos-slowloris-and-dns-injection-attacks/>
* **Herramienta**  
<https://github.com/gkbrk/slowloris/blob/master/slowloris.py>
* **Un poco de todo**  
<https://en.wikipedia.org/wiki/Slowloris_(software)>