#Ping flood

Ping flood, also known as ICMP flood, is a common Denial of Service (DoS) attack in which an attacker takes down a victim's computer by overwhelming it with ICMP echo requests, also known as pings.

The attack involves flooding the victim's network with request packets, knowing that the network will respond with an equal number of reply packets. Additional methods for bringing down a target with ICMP requests include the use of custom tools or code, such as hping and scapy.

This strains both the incoming and outgoing channels of the network, consuming significant bandwidth and resulting in a denial of service. DoS attack using hping3 with spoofed IP Attack Description

Normally, ping requests are used to test the connectivity of two computers by measuring the round-trip time from when an ICMP echo request is sent to when an ICMP echo reply is received. During an attack, however, they are used to overload a target network with data packets.

Executing a ping flood is dependent on attackers knowing the IP address of their target. Attacks can therefore be broken down into three categories, based on the target and how its IP address is resolved.

```
A targeted local disclosed ping flood targets a single computer on a local network. An attacker needs to have physical access to the computer in order to discover its IP address. A successful attack would result in the target computer being taken down.
A router disclosed ping flood targets routers in order to disrupt communications between computers on a network. It is reliant on the attacker knowing the internal IP address of a local router. A successful attack would result in all computers connected to the router being taken down.
A blind ping flood involves using an external program to uncover the IP address of the target computer or router before executing an attack.
```

There are a number of ping commands that can be used to facilitate an attack, including:

```
The –n command, which is used to specify the number of times a request is sent.
The –l command, which is used to specify the amount of data sent with each packet.
The –t command, which is used to continue pinging until the host times out.
```

Note that in order for a ping flood to be sustained, the attacking computer must have access to more bandwidth than the victim. This limits the ability to carry out a DoS attack, especially against a large network.

Additionally, a Distributed Denial of Service (DDoS) attack executed with a the use of a botnet has a much greater chance of sustaining a ping flood and overwhelming a target's resources. Methods of Mitigation

Reconfiguring your perimeter firewall to disallow pings will block attacks originating from outside your network, albeit not internal attacks. Still, the blanket blocking of ping requests can have unintended consequences, including the inability to diagnose server issues.

The Incapsula DDoS protection provide blanket protection against ICMP floods by limiting the size of ping requests as well as the rate at which they can be accepted.
