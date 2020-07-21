---
description: Dynamic Host Configuration Protocol
---

# DHCP - wip

DHCP is a protocol that allows us to leverage TCP connections to automatically obtain network configuration parameters automatically through the network. 

DHCP is also an open standard defined by [RFC 2131](https://www.ietf.org/rfc/rfc2131.txt) that is based on a client/server paradigm. Meaning that, during client bootup a server contacts is contacted and an IP address is requested an IP address. The server responds offering an IP address that the client accepts and the server acknowledges the assignment before it is completed. 

This process can be subsequently divided in 4 steps:

#### DISCOVER - The client is looking for available DHCP servers.

A client boots up for the first time into the initializing state, it transmits a DHCPDISCOVER message on its local physical subnet using 67/UDP \(BootP Server\). Since the client is not aware of which subnet it belongs to, the Discover message is [**broadcasted** ](https://tools.ietf.org/html/rfc919)using 255.255.255.255 as a destination IP address and using a source IP address of 0.0.0.0.

At this point, any properly configured DHCP server that exists in the local subnet will receive the DHCPDISCOVER **broadcast** message sent by the client. 

#### OFFER - The server response to the client DHCPDISCOVER.

The server responds the DHCPDISCOVER message with a DHCPOFFER message on 68/UDP \(BootP client\). Once the client has received the DHCPOFFER it moves from initialization state to the selecting state.

DHCPOFFER includes initial configuration details about the network such as subnet mask, default gateway. The DHCPOFFER message has several fields such as yiaddr for parameters like the requested IP address, and options field where subnet mask and default gateway are defined. Other options commonly found in the DHCPOFFER fields include IP Address lease time, renewal time, domain name server, and NetBIOS name server \(WINS\). 

The DHCP server sends the DHCPOFFER to the [**broadcast** ](https://tools.ietf.org/html/rfc919)address \(255.255.255.255\), the recipient of this message knows that it is intended for them because the DHCP server includes the [physical hardware address \(Media Access Control - MAC\)](https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/macgrp.pdf). If a DHCP server was not in the local subnet of the client, it would send an [**unicast** ](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc736574%28v=ws.10%29?redirectedfrom=MSDN)DHCPOFFER on port 67/UDP to a [DHCP or BootP Relay Agent](https://www.cisco.com/en/US/docs/ios/12_4t/ip_addr/configuration/guide/htdhcpre.html#wp1085232) that would unicast or broadcast that DHCPOFFER to the destination subnet where the client resides \(i.e **192.168.1.10/24** to **10.10.10.100/8**\) on port 68/UDP, this would be determined by whether or not the broadcast flag is set by the BootP client or not. 

#### REQUEST - The client broadcasts to the server, requesting offered parameters from one server specifically, as defined in the packet.

After receiving a DHCPOFFER message, a DHCP client would send a DHCPREQUEST message, this is an accepting acknowledgement of the parameters received in the DHCPOFFER, the client at this point enters the Requesting state. Multiple DHCPOFFER messages may be received if multiple DHCP Servers received the DHCPDISCOVER message originally sent. 

The DHCP client makes the decision of choosing one DHCPOFFER and responds to that DHCP Server exclusively accepting its proposed lease. 

#### ACKNOWLEDGEMENT - The server-to-client communication with configuration parameters, including committed network address.



[DHCP info ](https://www.cisco.com/c/en/us/support/docs/ip/dynamic-address-allocation-resolution/27470-100.html#understanding)

