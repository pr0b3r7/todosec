# Zone-Based Policy Firewall \(also known as Zone-Policy Firewall, or ZFW\)

Interfaces are assigned to zones, and inspection policy is applied to traffic moving between the zones. Inter-zone policies offer considerable flexibility and granularity, so different inspection policies can be applied to multiple host groups connected to the same router interface.

A security zone should be configured for each region of relative security within the network, so that all interfaces that are assigned to the same zone will be protected with a similar level of security. For example, consider an access router with three interfaces:

* One interface connected to the public Internet
* One interface connected to a private LAN that must not be accessible from the public Internet
* One interface connected to an Internet service demilitarized zone \(DMZ\), where a Web server, Domain Name System \(DNS\) server, and e-mail server must be accessible to the public Internet

Each interface in this network will be assigned to its own zone, although you might want to allow varied access from the public Internet to specific hosts in the DMZ and varied application use policies for hosts in the protected LAN. \(See Figure 1.\)

####  **Figure 1: Basic Security Zone Topology**

![](../../.gitbook/assets/image%20%2810%29.png)

In this example, each zone holds only one interface. If an additional interface is added to the private zone, the hosts connected to the new interface in the zone can pass traffic to all hosts on the existing interface in the same zone. Additionally, the hosts’ traffic to hosts in other zones is similarly affected by existing policies.

Typically, the example network will have three main policies:

* Private zone connectivity to the Internet
* Private zone connectivity to DMZ hosts 
* Internet zone connectivity to DMZ hosts

Because the DMZ is exposed to the public Internet, the DMZ hosts might be subjected to undesired activity from malicious individuals who might succeed at compromising one or more DMZ hosts. 

If no access policy is provided for DMZ hosts to reach either private zone hosts or Internet zone hosts, then the individuals who compromised the DMZ hosts cannot use the DMZ hosts to carry out further attack against private or Internet hosts. 

ZFW imposes a prohibitive default security posture. Therefore, unless the DMZ hosts are specifically provided access to other networks, other networks are safeguarded against any connections from the DMZ hosts. Similarly, no access is provided for Internet hosts to access the private zone hosts, so private zone hosts are safe from unwanted access by Internet hosts.

## [SOURCE - Cisco's Documentation](https://www.cisco.com/c/en/us/support/docs/security/ios-firewall/98628-zone-design-guide.html)

