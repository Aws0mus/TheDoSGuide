ICMP flood
==========

La inundación ICMP o también conocida como inundación ping, es un ataque de denegación de servicio en el que el atacante tumba la máquina de una víctima saturándola a través de peticiones ICMP, *ICMP echo requests*, también conocidas como paquetes ping.

Los ataques involucran inundar la red de la víctima con paquetes de petición que serán respondidos generando un número igual de paquetes de respuesta, aumentando más aun el tráfico en la red. Es posible combinar este ataque con otras técnicas de manipulación de paquetes, como en el caso del ping de la muerte, para hacer que a la víctima le cueste más trabajo procesar la solicitud. El objetivo final acaba siendo saturar el ancho de banda de la red o consumir los recursos de CPU de la víctima.

Descripción del Ataque
----------------------

**TODO**

Normally, ping requests are used to test the connectivity of two computers by measuring the round-trip time from when an ICMP echo request is sent to when an ICMP echo reply is received. During an attack, however, they are used to overload a target network with data packets.

Executing a ping flood is dependent on attackers knowing the IP address of their target. Attacks can therefore be broken down into three categories, based on the target and how its IP address is resolved.

A targeted local disclosed ping flood targets a single computer on a local network. An attacker needs to have physical access to the computer in order to discover its IP address. A successful attack would result in the target computer being taken down. A router disclosed ping flood targets routers in order to disrupt communications between computers on a network. It is reliant on the attacker knowing the internal IP address of a local router. A successful attack would result in all computers connected to the router being taken down. A blind ping flood involves using an external program to uncover the IP address of the target computer or router before executing an attack.

There are a number of ping commands that can be used to facilitate an attack, including:

```
The –n command, which is used to specify the number of times a request is sent.
The –l command, which is used to specify the amount of data sent with each packet.
The –t command, which is used to continue pinging until the host times out.
```

Note that in order for a ping flood to be sustained, the attacking computer must have access to more bandwidth than the victim. This limits the ability to carry out a DoS attack, especially against a large network.

Additionally, a Distributed Denial of Service (DDoS) attack executed with a the use of a botnet has a much greater chance of sustaining a ping flood and overwhelming a target's resources.

Mitigación
----------

Reconfiguring your perimeter firewall to disallow pings will block attacks originating from outside your network, albeit not internal attacks. Still, the blanket blocking of ping requests can have unintended consequences, including the inability to diagnose server issues.

The jijijaja DDoS protection provide blanket protection against ICMP floods by limiting the size of ping requests as well as the rate at which they can be accepted.

Referencias
-----------

https://www.incapsula.com/ddos/attack-glossary/ping-icmp-flood.html
