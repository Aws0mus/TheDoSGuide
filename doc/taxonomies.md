Diferentes taxonomías
=====================

La clasificación de los ataques de denegación de servicio siempre ha sido un tema muy complejo, debido a la gran variedad de ataques que existen y que pueden afectar a muchos niveles y de muchas formas. Una taxonomía o clasificación nos permite identificar los activos sobre los que puede afectar un ataque de denegación de servicio. Así, nos será más fácil entender cómo funciona un ataque en concreto y qué mecanismos podemos utilizar para mitigarlo.

A lo largo del tiempo se ha intentado recopilar todos los ataques en una única taxonomía, dando lugar a complejos diagramas con decenas de clasificaciones. (Mirkovic & Reiher 2004) (Wun, Cheung & Jacobsen 2007)

**TODO** foto de alguna clasificacion

**TODO** completar

El problema está en que no existe (o no hemos encontrado) una clasificación taxonómica lo suficientemente completa que cubra todos los ataques DoS conocidos hasta la fecha.  Por ello nos apoyamos en la clasificaciones taxonómicas actuales para • Crear una taxonomía genérica que nos ayude a conducir nuestros proyectos. • Sea lo suficientemente simple como para que ayude a  ver a través del bosque  desarrollar un análisis sobre la plataforma existente  valorar las posibles mitigaciones sobre ella**Continua el parrafo** En este apartado se expondrán diferentes taxonomías con las que se podrá definir un ataque de denegación de servicio. Par ello se utilizarán diversas clasificaciones de varios autores.

En primer lugar, se utilizará una simplificación de la taxonomía proporcionada por Gerardo García Peña en su conferencia *DoS: Un enfoque práctico*, en la Rooted CON 2012. Esta clasificacón toma ideas de las otras dos ya mencionadas de 2004 y 2007. (García Peña 2012)

También se utilizará otra taxonomía basada en la pila OSI, que divide los ataques según la capa de protocolos a la que afecte. Esta clasificación ha sido propuesta por el US-CERT, la máxima autoridad en tareas de ciberdefensa nacional en EEUU. https://www.us-cert.gov/sites/default/files/publications/DDoS%20Quick%20Guide.pdf

Forma de ser lanzado
--------------------

**TODO** En cada una, definir, poner los tipos (definir) y ejemplos (con sus referencias)

-	Botnet  
	IRC, P2P, ...  
-	Gusano  
	Formas de expandir el gusano https://www.researchgate.net/publication/277306147_A_Broad_Overview_of_Denial_of_Service_Attack

Impacto
-------

-	Degradar - Crashear

	-	Auto recuperable  
	-	Humano recuperable  
	-	No recuperable

Caracterizable
--------------

-	Filtrable  
-	No filtrable  
-	No caracterizable

Rate
----

-	One shot  
-	Constante  
-	Variable

	-	Fluctante  
	-	Incremental

Forma de explotación
--------------------

-	Saturación  
-	Debilidad semántica  
-	Fallo de implementación

Clasificación OSI
-----------------

-	La que usaremos

Referencias
-----------

Jelena Mirkovic, Peter Reiher, A Taxonomy of DDoS Attack and DDoS Defense Mechanisms, 2004

Alex Wun, Alex Cheung & Hans-Arno Jacobsen, A Taxonomy for Denial of Service Attacks in Content-based Publish/Subscribe Systems, 2007

Gerardo García Peña, DoS: Un enfoque práctico, Rooted CON 2012 https://www.slideshare.net/rootedcon/gerardo-garca-pea-enfoque-prctico-a-la-denegacin-de-servicio-rooted-con-2012

https://www.us-cert.gov/sites/default/files/publications/DDoS%20Quick%20Guide.pdf
