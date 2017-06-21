#Smurf attack o ICMP amplification

Smurf is a network layer distributed denial of service (DDoS) attack, named after the DDoS.Smurf malware that enables it execution.

Smurf attacks are somewhat similar to ping floods, as both are carried out by sending a slews of ICMP Echo request packets.

Unlike the regular ping flood, however, Smurf is an amplification attack vector that boosts its damage potential by exploiting characteristics of broadcast networks.
Attack Description

In a standard scenario, host A sends an ICMP Echo (ping) request to host B, triggering an automatic response. The time it takes for a response to arrive is used as a measure of the virtual distance between the two hosts.

In an IP broadcast network, an ping request is sent to every host, prompting a response from each of the recipients. With Smurf attacks, perpetrators take advantage of this function to amplify their attack traffic.DNS flood - 25 million packets per second

A Smurf attack scenario can be broken down as follows:

    Smurf malware is used to generate a fake Echo request containing a spoofed source IP, which is actually the target server address.
    The request is sent to an intermediate IP broadcast network.
    The request is transmitted to all of the network hosts on the network.
    Each host sends an ICMP response to the spoofed source address.
    With enough ICMP responses forwarded, the target server is brought down.

The amplification factor of the Smurf attack correlates to the number of the hosts on the intermediate network. For example, an IP broadcast network with 500 hosts will produce 500 responses for each fake Echo requests. Typically, each of the relies is of the same size as the original ping request.

It should be noted that, during the attack, the service on the intermediate network is likely to be degraded.

In addition to showing good internet citizenship, this should incentivize operators to prevent their networks from being unwitting Smurf attack participants.

To accomplish this you can:

    Disable IP-directed broadcasts on your router.
    Reconfigure your operating system to disallow ICMP responses to IP broadcast requests.
    Reconfigure the perimeter firewall to disallow pings originating from outside your network.

Mitigation Methods

Smurf attack mitigation relies on a combination of capacity overprovisioning (CO) and an existence of filtering services to identify and block illegal ICMP responses.

Infrastructure Protection, one of jijijaja DDoS mitigation solutions, uses BGP routing to direct all incoming traffic through a worldwide network of scrubbing centers.
Through inspection of incoming traffic, all illegal packets—including unsolicited ICMP responses—are identified and blocked outside of your network.

<https://www.incapsula.com/ddos/attack-glossary/smurf-attack-ddos.html>