Tipos ataques clasificados por la capa OSI
==========================================

Podemos clasificar los diferentes ataques de denegación de servicio según el modelo de interconexión de sistemas abiertos o modelo OSI (Open System Interconnection). Este esquema clasifica los diferentes protocolos en siete capas o fases por las que deben pasar los datos para transmitirse de un dispositivo a otro a través de una red de comunicaciones.

Consiste en una normativa estandarizada que ayuda a situar las tecnologías de diferentes fabricantes y compañías dentro del mundo de las telecomunicaciones.

![Modelo OSI](../static/images/modelo_osi.png)

Este modelo forma una pila de capas en las que se basará la clasificación de ataques comprendidos en este trabajo. Se utilizará un enfoque Top-Down, de forma similar al libro *Computer Networking: A Top-Down Approach* de James F. Kurose y Keith W. Ross.

**Capa de aplicación**
----------------------

Esta capa, comprendida en la cima de la pila OSI, permite a las aplicaciones acceder a los datos y servicios de las demás capas. Define los protocolos que deben utilizar las aplicaciones para poder intercambiar datos, como el correo electrónico (POP3 y SMTP), servidores de fichero (FTP), acceso a páginas web (HTTP y HTTPS), en otros. Hay gran variedad de protocolos en esta capa, tantos como aplicaciones diferentes, y debido al continuo crecimiento de aplicaciones también aumenta el número de protocolos.

Es importante destacar que el usuario no interactua directamente con el nivel de aplicación, sino que interactua con programas que internamente realizan esta tarea, ocultando su complejidad.

En esta capa encontramos los ataques:

**TODO** Completar ataques y traducir

-	Slow Loris
-	Slow POST
-	Slow Read
-	HTTP/S Flood
-	CVE Attack Vectors
-	Large payload POST requests
-	Database Connection Pool Exhaustion
-	Resource Exhaustion
-	Mimicked User browsing
-	DNS Query/NXDOMAIN floods
-	Other protocol floods (SMTP, DNS, SNMP, FTP, SIP)

**Capa de presentación**
------------------------

Layer 6: Presentation Transforms data into a common format that is consumable by the Application Layer.

-	SSL Exhaustion

**Capa de sesión**
------------------

Layer 5: Session Establishes a context which encapsulates the messages being exchanged between processes on different machines.

-	Long lived TCP sessions (Slow Transfer)
-	Connection flood/exhaustion

**Capa de transporte**
----------------------

Layer 4: Transport Responsible for providing guarantees on message delivery, arrival order, loss recovery, and error recovery.

-	SYN Flood
-	Other TCP Floods (varying state flags)
-	UDP Flood
-	IPSec Flood (IKE/ISAKMP association attempts)

**Capa de red**
---------------

Layer 3: Network Allows packets to be routed through a network enabling indirectly connected nodes to exchange data messages.

-	BGP Hijacking
-	ICMP Flood
-	IP/ICMP Fragmentation

**Capa de enlace**
------------------

Layer 2: Data Link Handles detecting and/or correcting errors introduced at layer 1 in order to establish a reliable link between two connected machines.

Attacks at layers 1 and 2 target the base of a network itself. They would require direct physical and internal access to a company's network, making them unlikely to be performed in the wild.

**Capa física**
---------------

Layer 1: Physical Defines the physical specification for translating digital data into signals to be sent across a physical medium (such as copper or wireless link).

Attacks at layers 1 and 2 target the base of a network itself. They would require direct physical and internal access to a company's network, making them unlikely to be performed in the wild.

Referencias
-----------

https://www.securitycompass.com/dds/?_escaped_fragment_=/layers#!/layers

https://es.wikipedia.org/wiki/Modelo_OSI

Computer Networking: A Top-Down Approach, 6th Edition, James F. Kurose, Keith W. Ross.
