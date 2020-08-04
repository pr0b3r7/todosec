---
description: Dynamic Host Configuration Protocol
---

# DHCP Essentials

DHCP is a protocol that allows us to leverage TCP connections to automatically obtain network configuration parameters automatically through the network.

DHCP is also an open standard defined by [RFC 2131](https://www.ietf.org/rfc/rfc2131.txt) that is based on a client/server paradigm. Meaning that, during client bootup a server contacts is contacted and an IP address is requested an IP address. The server responds offering an IP address that the client accepts and the server acknowledges the assignment before it is completed.

This process can be subsequently divided in 4 steps:

#### DISCOVER - The client is looking for available DHCP servers.

A client boots up for the first time into the initializing state, it transmits a DHCPDISCOVER message on its local physical subnet using 67/UDP \(BootP Server\). Since the client is not aware of which subnet it belongs to, the Discover message is [**broadcasted** ](https://tools.ietf.org/html/rfc919)using 255.255.255.255 as a destination IP address and using a source IP address of 0.0.0.0.

### Client-Server Conversation for Client Obtaining DHCP Address Where Client and DHCP Server Reside on Same Subnet

| Packet Description | Source MAC Addr | Destination MAC Addr | Source IP Addr | Destination IP Addr |
| :--- | :--- | :--- | :--- | :--- |
| DHCPDISCOVER | Client | Broadcast | 0.0.0.0 | 255.255.255.255 |
| DHCPOFFER | DHCP Server | Broadcast | DHCPServer | 255.255.255.255 |
| DHCPREQUEST | Client | Broadcast | 0.0.0.0 | 255.255.255.255 |
| DHCPACK | DHCP Server | Broadcast | DHCPServer | 255.255.255.255 |

At this point, any properly configured DHCP server that exists in the local subnet will receive the DHCPDISCOVER **broadcast** message sent by the client.

#### OFFER - The server response to the client DHCPDISCOVER.

The server responds the DHCPDISCOVER message with a DHCPOFFER message on 68/UDP \(BootP client\). Once the client has received the DHCPOFFER it moves from initialization state to the selecting state.

DHCPOFFER includes initial configuration details about the network such as subnet mask, default gateway. The DHCPOFFER message has several fields such as yiaddr for parameters like the requested IP address, and options field where subnet mask and default gateway are defined. Other options commonly found in the DHCPOFFER fields include IP Address lease time, renewal time, domain name server, and NetBIOS name server \(WINS\).

The DHCP server sends the DHCPOFFER to the [**broadcast** ](https://tools.ietf.org/html/rfc919)address \(255.255.255.255\), the recipient of this message knows that it is intended for them because the DHCP server includes the [physical hardware address \(Media Access Control - MAC\)](https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/macgrp.pdf). If a DHCP server was not in the local subnet of the client, it would send an [**unicast** ](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2003/cc736574%28v=ws.10%29?redirectedfrom=MSDN)DHCPOFFER on port 67/UDP to a [DHCP or BootP Relay Agent](https://www.cisco.com/en/US/docs/ios/12_4t/ip_addr/configuration/guide/htdhcpre.html#wp1085232) that would unicast or broadcast that DHCPOFFER to the destination subnet where the client resides \(i.e **192.168.1.10/24** to **10.10.10.100/8**\) on port 68/UDP, this would be determined by whether or not the broadcast flag is set by the BootP client or not.

#### REQUEST - The client broadcasts to the server, requesting offered parameters from one server specifically, as defined in the packet.

After receiving a DHCPOFFER message, a DHCP client would send a DHCPREQUEST message, this is an accepting acknowledgement of the parameters received in the DHCPOFFER, the client at this point enters the Requesting state. Multiple DHCPOFFER messages may be received if multiple DHCP Servers received the DHCPDISCOVER message originally sent.

The DHCP client makes the decision of choosing one DHCPOFFER and responds to that DHCP Server exclusively accepting its proposed lease.

#### ACKNOWLEDGEMENT - The server-to-client communication with configuration parameters, including committed network address.

DHCP Server then responds to the DHCPREQUEST with a DHCPACK message, at this point its initialization process has been completed. The DHCPACK's source IP address is the DHCP Servers' while the destination is a broadcast address. DHCPACK includes all of the necessary parameters that the client requested in the DHCPREQUEST packets.

At this point we can consider the client to be in the bound state, the IP address that has been leased to it is now effective and it ma use it to communicate over the network with other nodes.

DHCP leases are stored in a database with unique identifiers such as the DHCP Client MAC Address or _chaddr_, as well as its associated IP address. Client and Servers use different combinations of identifiers to refer to the lease. Note that the client identifier is the physical address \(MAC\) of the device plus the media type.

Before DHCP clients can use the address in the lease, the client must calculate the time attributes associated with the DHCP lease:

* Lease Time \(LT\)
* Renewal Time \(T1\)
* Rebind Time \(T2\)

Generally, LT is 72 hours. Shorter lease address may be used to conserve addresses if that is a concern.

Other DHCP Messages include:

* DHCPNAK
* DHCPDECLINE
* DHCPINFORM
* DHCPRELEASE

![Other DHCP messages](../../.gitbook/assets/image%20%2860%29.png)

#### DHCP Packet

DHCP messages are of a variable length and consist of the fields:

#### **Note:** This packet is a modified version of the original BootP packet.

| Field | Bytes | Name | Description |
| :--- | :--- | :--- | :--- |
| op | 1 | OpCode | Identifies the packet as an request or reply: 1=BOOTREQUEST, 2=BOOTREPLY |
| htype | 1 | Hardware Type | Specifies the network hardware address type. |
| hlen | 1 | Hardware Length | Specifies the length hardware address length. |
| hops | 1 | Hops | The client sets the value to zero and the value increments if the request is forwarded across a router. |
| xid | 4 | Transaction ID | A random number that is chosen by the client. All DHCP messages exchanged for a given DHCP transaction use the ID \(xid\). |
| secs | 2 | Seconds | Specifies number of seconds since the DHCP process started. |
| flags | 2 | Flags | Indicates whether the message will be broadcast or unicast. |
| ciaddr | 4 | Client IP address | Only used when client knows its IP address as in the case of the Bound, Renew, or Rebinding states. |
| yiaddr | 4 | Your IP address | If the client IP address is 0.0.0.0, the DHCP server will place the offered client IP address in this field. |
| siaddr | 4 | Server IP address | If the client knows the IP address of the DHCP server, this field will be populated with the DHCP server address. Otherwise, it is used in DHCPOFFER and DHCPACK from DHCP server. |
| giaddr | 4 | Router IP address \(GI ADDR\) | The Gateway IP address, filled in by the DHCP/BootP Relay Agent. |
| chaddr | 16 | Client MAC address | The DHCP client MAC address. |
| sname | 64 | Server name | The optional server host name. |
| file | 128 | Boot file name | The boot file name. |
| options | variable | Option parameters | The optional parameters that can be provided by the DHCP server. RFC 2132 gives all possible options. |

## Why would a DHCP/BootP Relay Agent be needed?

Routers, usually, will not forward broadcast packets.

DHCP client messages use a destination IP address of 255.255.255.255 \(Broadcast\), DHCP clients will not be able to send requests to a DHCP server on a different subnet unless the DHCP/BootP Relay Agent is configured on the router.

The DHCP/BootP Relay Agent will forward DHCP requests on behalf of a DHCP client to the DHCP server. The DHCP/BootP Relay Agent will append its own IP address to the source IP address of the DHCP frames going to the DHCP server. This allows the DHCP server to respond via unicast to the DHCP/BootP Relay Agent.

The DHCP/BootP Relay Agent will also populate the Gateway IP address field with the IP address of the interface on which the DHCP message is received from the client. The DHCP server uses the Gateway IP address field to determine the subnet from which the DHCPDISCOVER, DHCPREQUEST, or DHCPINFORM message originates.

[DHCP info by Cisco ](https://www.cisco.com/c/en/us/support/docs/ip/dynamic-address-allocation-resolution/27470-100.html#understanding)

