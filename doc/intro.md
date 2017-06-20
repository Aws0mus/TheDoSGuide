Introducción
============

Hoy en día son muy comunes los ataques de denegación de servicio (DoS) y los ataques de denegación distribuidos (DDoS) en el mundo empresarial. El informe del tercer trimestre de 2016 realizado por la empresa Kaspersky muestra algunos datos alarmantes, por ejemplo, el tráfico generado por los ataques en dicho trimestre fue de más de 277 millones de segundos, el equivalente a casi 9 años de tráfico legítimo (https://securelist.com/kaspersky-ddos-intelligence-report-for-q3-2016/76464/).

Este tipo de ataques consiste en no permitir el funcionamiento correcto de los servicios que proporciona o recibe una empresa, organización o particular; de ahí su nombre, denegación de servicio.

También, el informe sobre el estado de Internet en materia de seguridad del tercer trimestre de 2016 (https://www.akamai.com/us/en/multimedia/documents/state-of-the-internet/q3-2016-state-of-the-internet-security-report.pdf), realizado por la empresa de seguridad Akamai, destaca el aumento interanual del 138% en ataques DDoS totales de más de 100 Gbps, con dos ataques DDoS record desencadenados por la botnet Mirai.

Este ataque DDoS de la botnet Mirai, ocurrido en este último trimestre de 2016, tuvo fuera de servicio a Dyn, uno de los proveedores DNS más importantes, provocando que muchas páginas web, entre ellas Twitter o Reddit, fuesen inaccesibles.

A diario las empresas sufren estos ataques contra sus servidores y tienen que contratar a compañías de seguridad para que reduzcan su efecto.

Estos ataques se pueden basar en diversas técnicas: saturar de tráfico los servidores, saturar los cables que llevan a esos servidores, explotar vulnerabilidades, etc. (Ramanauskaite y Cenys 2011).

Este trabajo de fin de grado consiste en la investigación sobre técnicas de denegación de servicio (DoS) y técnicas de denegación de servicio distribuidos (DDoS), así como de las medidas de prevención, protección y fortificación frente a estos ataques.

**TODO** revisar desde aqui

El objetivo final del trabajo será el diseño y la elaboración de una herramienta capaz de integrar los dos tipos de ataques, cuya finalidad sea la realización de test de estrés controlados. También se creará una guía de protecciones y buenas prácticas para poder evitar o paliar en cierta medida este tipo de ataques . Este proyecto pretende contribuir a generar conocimiento sobre el amplio tema de la Denegación de Servicio. Esto permitirá tan to a las personas del sector público, ya sean universidades o gobiernos, como a las personas del sector privado tener una fuente de información de la cual poder partir para realizar futuras investigaciones sobre esta temática.

Los objetivos finales del trabajo son realizar una herramienta para realizar pruebas de estrés y una guía de protecciones y buenas prácticas contra los ataques de denegación de servicio. La herramienta incluirá diversos ataques para realizar estas pruebas de estrés. Estos ataques se podrán clasificar según ataque in dividual o ataque distribuido, por el tipo de servicio afectado, por la capa de la pila OSI sobre la que actúe...

Para la herramienta se utilizará el lenguaje de programación Python. Esto permitirá el uso de la herramienta Scapy ( http://secdev.org/projects/scapy/ ), que permite manipular paquetes en cualquiera de las capas de la pila OSI. A través de esta herramienta se desarrollarán todos o al menos gra n parte de los ataques . También se valora la existencia de una gran variedad de sistemas distribuidos diseñados con Python, con los que se dará soporte a ataques de mayor envergadura, como son zeroMQ ( http://zeromq.org/ ) o RabbitMQ ( http://www.rabbitmq.com ). Algunos de los ataques previstos para la herramienta son:  TCP/UDP flood. Cuyo objetivo es saturar la red a base de paquetes TCP/UDP.  ICMP flood. En este caso utilizando paquetes ICMP.  Long TCP session . Cuyo objetivo consiste en alargar lo máximo posible una sesión TCP para que un servidor no pueda dar servicio a clientes legítimos. También un objetivo secundario es investigar sobre los ataques de servicio geolocalizados, es decir, en lugar de atacar una máquina, ser capaces de atacar cierto rango para realizar un ataque de denegación de servicio focalizado en una zona determinada. No se quiere partir de una herramienta como base, sino que se quiere desarrollar de cero. Aun así, se tomará como referencia la herramienta DoS:IS ( https://github.com/killabytenow/dosis ) presentada en la Rooted2012 por Gerardo García Peña escrita en lenguaje C

La guía incluirá una lista de protecciones , en forma de hardware o software, y una lista de buenas prácticas a tomar para combatir los ataques de denegación de servicio. Para realizar estos objetivos será necesario un estudio teórico sobre los diferentes ataques. Las fuentes del estudio estarán ba sadas en diversos artículos versados sobre el tema e información publicada en Internet. Se intentará ser lo más riguroso posible y analizar de forma crítica todos los ataques, para así comprobar su efectividad, limitaciones y contramedidas.

El proyecto se dividirá en 3 fases.  La primera fase consistirá en un estudio teórico sobre los diversos tipos de ataques de denegación de servicio . Tipos de técnicas, consecuencias directas e indirectas de un ataque, servicios vulnerables, clasificación, etc . La duración de esta parte será aproximadamente de un mes.  La segunda fase consistirá en la elaboración de una herramienta para realizar prueb as de estrés . Esta herramienta permitirá al investigador realizar ataques de forma controlada en cualquiera de las capas de la pila OSI. Dada la magnitud de la herramienta , tendrá una alta complejidad y una difícil configuración, para así evitar que sea us ada con fines maliciosos por parte de personas con escasos o nulos conocimientos de seguridad informática cuya ética pueda ser cuestionable. Como p or ejemplo , el caso de la herramienta LOIC , utilizada por hacktivistas , personas que utilizan ordenadores y r edes para expresar protesta social o promover ideologías políticas, para realizar ataques contra gobiernos o empresas privadas . Esta fase tendrá una duración de dos meses.  La tercera fase consistirá en un estudio teórico y práctico sobre diversas medid as de seguridad para evitar o reducir las causas de estos ataques . Con los resultados de diversos ataques se hará una pequeña investigación sobre contramedidas o formas de reducir el impacto de un ataque. Esta última fase tendrá una duración de un mes.

**TODO** revisar hasta aqui ^

DoS, DDoS y alcance del trabajo
-------------------------------

Antes de llegar más lejos en el trabajo debemos considerar la definiciones: ataque de denegación de servicio y ataque de denegación de servicio distribuido; ya que son los pilares sobre los que se basará el resto del proyecto.

**TODO** definiciones

dos (cualquier cosa que pueda no funcionar)

Se ha demostrado la existencia de ataques de denegación de servicio sobre tecnologías ajenas a Internet, como redes de sensores inalámbricas (WSN), las cuales tienen menos recursos hardware que muchos ordenadores de la actualidad y necesitan comunicarse unas con otras para transmitir la información recopilada en los diferentes nodos (Ghildiyal 2015), o sistemas industriales, los cuales ... **TODO** articulo aqui y rellenar

El alcance del trabajo se ha limitado exclusivamente a la pila OSI y, más en concreto, a su implementación sobre TCP/IP. Se incluirá información sobre IPv6, aunque tampoco se ha considerado de forma principal debido a que aun no se ha implantado de forma tan masiva como IPv4.

Actualidad
----------

-	Estado actual y previsiones de futuro http://cso.computerworld.es/cibercrimen/los-ataques-ddos-aumentan-un-138-segun-un-informe-de-akamai  
	<https://securelist.com/analysis/quarterly-malware- reports/76464/kaspersky-ddos-intelligence-report-for-q3-2016/)>

-	Negocio de DoS (parte de ataque y parte defensiva)

-	Lo facil que es pillar botnets y el mercado de los DoShttps://www.incapsula.com/ddos/booters-stressers-ddosers.html

-	Anonymous y hacktivismo

Consecuencias de los ataques de denegación de servicio
------------------------------------------------------

-	Consecuencias  
	https://www.incapsula.com/ddos/how-to-stop-ddos-attacks.html

	-	Economicas (ejemplo amazon) y meter datos de cifras y tal  
		https://www.incapsula.com/ddos/ddos-mitigation-services.html(para algunas cifras)
	-	Imagen de la empresa

-	Hablar sobre tráfico normal, datos sobre tráfico diario en Internet y picos de tráfico en un ataque

-	Hablar sobre en qué consiste estabilizar el tráfico (Sacar de la charla de la rooted)

-	Rate Limit

Rate limit is the ability of the server or application to restrict a certain traffic flow characteristic such as connections-per-second, packets-per-second, number-of-queries, type-of-queries, etc. The idea here is to be able to restrict network and application transmission characteristics in order to maintain overall business availability. One major drawback to this technique is that by definition it does not discriminate between legitimate or illegitimate traffic blocking. https://security.radware.com/ddos-knowledge-center/ddospedia/rate-limit/

-	Low (Slow) rate attack, high rate attack  

https://security.radware.com/ddos-knowledge-center/ddospedia/slow-rate-attack/

-	Local y remoto (bomba de forks, kill de users para local)

-	Reflector - Reflective DoS attacks https://security.radware.com/ddos-knowledge-center/DDoSPedia/reflector-reflective-dos-attacks/

Referencias
-----------

-	Ramanauskaite, Simona, y Antanas Cenys. 2011. «Taxonomy of DoS attacks and their countermeasures». Central European Journal of Computer Science 1 (3): 355.doi:10.2478/s13537\-011\-0024\-y.

-	US\-CERT. 2016. «Alert (TA16\- 288A) Heightened DDoS Threat Posed by Mirai and Other Botnets». https://www.us-cert.gov/ncas/alerts/TA16-288A.

-	Sunil Ghildiyal et al. Int. Journal of Engineering Research and Applications ISSN: 2248\-9622, Vol. 5, Issue 11, (Part\-1) November 2015, pp. 86\-89 http://ijera.com/papers/Vol5_issue11/Part%20-%201/O511018689.pdf
