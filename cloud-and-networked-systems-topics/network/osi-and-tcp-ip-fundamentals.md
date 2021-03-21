---
description: Let's describe basic networking concepts
---

# OSI and TCP/IP, IPv6 and Network Protocols at each layer

## OSI Model - Open Systems Interconnection Model

Think of it as an effort to explain how networks work. It sorts functionality in the form of layers. 

If you master it, you may have an understanding of how networks work at each layer and how data is communicated and transferred between layers. 

### There are 7 Layers, you may remember them with the following mnemonic device:

#### _Please Do not throw sausage pizza away_ for:

_\(layer - protocol data unit\*\)_

* **Application** - DATA - End user layer - HTTP, FTP, IRC, SSH and DNS... etc - Application Layer
* **Presentation** - DATA - Syntax Layer - SSL, SSH, IMAP, FTP, MPEG, JPEG, PDF - Data representation and encryption
* **Session** - DATA - Synchronize and send to port - APIs, Sockets, WinSock... Facilitates Inter-host communications
* **Transport** - SEGMENT - End-to-End connections - TCP, UDP... 
* **Network** - PACKET - End-to-End **routing** and **addressing** - IP, ICMP, IPSec, IGMP... IP Addresses live here
* **Data Link** - FRAME - Provides error free transmission and access to the media - ARP, CDP, Ethernet, HDLC, IEEE 802.11 WLAN, LLDP , MPLS , SDN , PPP , UDLD... Physical Addressing of links
* **Physical** - BIT - Physical structure - Coax, Fiber, Wireless, Repeaters... 

![Transport - Layer 4 TLS 1.2 Segment in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2826%29.png)

![Network - Layer 3 Packet in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2816%29.png)

![Data Link - Layer 2 Frame in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2814%29.png)

#### \_\_[_Protocol data unit_](https://en.wikipedia.org/wiki/Protocol_data_unit)_\*\*\*_

## [TCP/IP stack vs OSI Model](https://www.electronicdesign.com/unused/article/21800810/whats-the-difference-between-the-osi-sevenlayer-network-model-and-tcpip)

OSI refers to Open Systems Interconnection whereas TCP/IP refers to Transmission Control Protocol. 

OSI follows a vertical approach whereas TCP/IP follows a horizontal approach. 

OSI model, the transport layer, is only connection-oriented whereas the TCP/IP model is both connection-oriented and connection-less.

In the OSI model, data flows down the transmit layers, over the physical link, and then up through the receive layers.

The seven layers of the OSI model somewhat correspond with the four layers that make up the TCP/IP protocol. 

The header is added and then removed during the encapsulation and de-encapsulation of the packet data at the TCP layer.

The IPv4 header is used during the Internet Protocol process in data transmission. 

Note the 32-bit source and destination addresses.

The new IPv6 header for the Internet Protocol is similar to IPv4 but uses 128-bit source and destination addresses.

TCP/IP is the older of the two approaches to data communications and is well established throughout the world. 

The OSI model, however, is a proven concept that is used in all other data communications protocols. It will continue to be used as a guideline for all other communications applications.

The layers of TCP/IP model are:

* Application
* Transport
* Internet
* Network Access

## Physical Layer

At the bottom layer of the OSI model, concerned with the transmission and reception of the unstructured raw bit stream over a physical medium. 

It describes the electrical/optical, mechanical, and functional interfaces to the physical medium, and it carries the signals for all of the higher layers.

## Data-Link Layer

**Data-link Layer \(Layer 2\)** is the medium provision Layer. 

It encodes and decodes the data in Frames. 

Encoding means adding a header at the source and decoding means removing this header at the destination. 

Layer 2 addresses are used for local transmissions between devices that are directly connected. Layer 3 addresses are used for indirectly connected devices in an inter-network environment. Each network uses addressing to identify and group devices so that transmissions can be sent and received. Ethernet \(802.2, 802.3, Ethernet II, and Sub-network Access Protocol \[SNAP\]\), Token Ring, and Fiber Distributed Data Interface \(FDDI\) use media access control \(MAC\) addresses that are “burned in” to the network interface card \(NIC\). The most commonly used network types are Ethernet II and SNAP.

In order for devices to be able to communicate with each when they are not part of the same network, the 48-bit MAC address must be mapped to an IP address. Some of the Layer 3 protocols used to perform the mapping are:

*  Address Resolution Protocol \(ARP\)
*  Reverse ARP \(RARP\)
*  Serial Line ARP \(SLARP\)
*  Inverse ARP

Data-link Layer has two sub-layers. These layers are:

* Media Access Control \(MAC\) Layer
* Logical Link Control \(LLC\) Layer

The **Media Access Control Layer** determines how nodes on the network obtain access to the data and the considerations required for transmission. Nodes are referred to at this layer via MAC Addresses or Physical Addresses. 

IEEE standard 802.2 defines **Logical Link Control \(LLC\)** as a data link control layer used on 802.3, 802.5, and other networks. 

The LLC layer provides connectionless and connection-oriented data transfer.

Connection-less data transfer is commonly referred to as LLC type 1, or LLC1. Connection-less service does not require you to establish data links or link stations. After a Service Access Point \(SAP\) has been enabled, the SAP can send and receive information to and from a remote SAP that also uses connectionless service. Connection-less service does not have any mode setting commands \(such as SABME\) and does not require that state information is maintained.

Connection-oriented data transfer is referred to as LLC type 2, or LLC2. Connection-oriented service requires the establishment of link stations. When the link station is established, a mode setting command is necessary. Thereafter, each link station is responsible to maintain link state information.

Some of the **Data-Link Layer protocols** are, PPP, HDLC, FDDI, ATM, Frame Relay and IEEE 802.3/802.2.

## Network Layer

Used for the transfer or flow of packets across the network. 

To specify the format of packets and provide an addressing system that enables packets to be routed to the correct destination and a response to be routed back to the source of the communication, two main addressing schemes are in use today, which in reality are two iterations of the same protocol: Internet Protocol - IP:

### [IPv4 Addressing](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)

| IP Addresses in Dotted Decimal | IP Addresses in Binary |
| :--- | :--- |
| 10.34.216.79 | 00001010.00100010.11011000.01001111 |
| 172.16.89.35 | 10101100.00010000.01011001.00100011 |
| 192.168.100.5 | 11000000.10101000.01100100.00000101 |

#### [Subnet Masks](https://subnettingpractice.com/)

Please perform all exercises in the website linked in Subnet Masks title above: [_https://subnettingpractice.com_](https://subnettingpractice.com/)\_\_

Table below from Cisco's documentation should provide a quick reference in binary and dotted decimal notation

| IP Address Ranges by Class with Masks |  |
| :--- | :--- |
| Class | Range |
| A \(range/mask in dotted decimal\) | 0 .0.0.0 to 127.0.0.0/8 \(255.0.0.0\) |
| A \(range in binary\) | 00000000 .00000000.00000000.00000000 to 01111111.00000000.00000000.00000000 |
| A \(mask in binary\) | 11111111.00000000.00000000.00000000/8 |
| B \(range/mask in dotted decimal\) | 128 .0.0.0 to 191.255.0.0/16 \(255.255.0.0\) |
| B \(range in binary\) | 10000000 .00000000.00000000.00000000 to 10111111.11111111.00000000.00000000 |
| B \(mask in binary\) | 11111111 .11111111.00000000.00000000/16 |
| C \(range/mask in dotted decimal\) | 192 .0.0.0 to 223.255.255.0/24 \(255.255.255.0\) |
| C \(range in binary\) | 11000000 .00000000.00000000.00000000 to 11011111.11111111.11111111.00000000 |
| C \(mask in binary\) | 11111111.11111111.11111111.0000000/24 |
| D[1](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipaddr_ipv4/configuration/xe-3s/ipv4-xe-3s-book/configuring_ipv4_addresses.html#fntarg_1) \(range/mask in dotted decimal\) | 224 .0.0.0 to 239.255.255.255/32 \(255.255.255.255\) |
| D \(range in binary\) | 11100000 .00000000.00000000.00000000 to 11101111.11111111.11111111.11111111 |
| D \(mask in binary\) | 11111111.11111111.11111111.11111111/32 |
| E[2](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipaddr_ipv4/configuration/xe-3s/ipv4-xe-3s-book/configuring_ipv4_addresses.html#fntarg_2) \(range/mask in dotted decimal\) | 240 .0.0.0 to 255.255.255.255/32 \(255.255.255.255\) |
| E \(range in binary\) | 11110000 .00000000.00000000.00000000 to 11111111.11111111.11111111.11111111 |
| E \(mask in binary\) | 11111111.11111111.11111111.11111111/32 |

### IPv4 Packet Header

Many different fields are defined in the packet header of an IPv4 packet. These binary values are referenced as the packet is forwarded across the network. 

* IP Source Address of the packet
* IP Destination Address of the packet
* Time-to-live \(TTL\) - 8-bit value indicating the remaining life of the packet
* Type-of-Service \(ToS\) - 8-bit binary value used to determine the priority of a packet
* Protocol - 8-bit value indicating the data payload type that the packet is carrying

![IP Packet Header](../../.gitbook/assets/image%20%2829%29.png)

Contains Source and Destination IP addresses in the packet as well as flags and Differentiated Services Field codes for Quality of Service purposes.

### [IPv6 Addressing](https://en.wikipedia.org/wiki/IPv6)

"IPv6 addresses are represented as eight groups, separated by colons, of four hexadecimal digits. The full representation may be simplified by several methods of notation; for example, _2001:0db8:0000:0000:0000:8a2e:0370:7334 becomes 2001:db8::8a2e:370:7334." \(Wikipedia\)_

Some [statistics ](https://www.google.com/intl/en/ipv6/statistics.html)by google on its world-wide adoption, up to you is to decide when the [well announced ](https://csrc.nist.gov/publications/detail/journal-article/2008/internet-protocol-version-6-ipv6)final cut over is happening.

![](../../.gitbook/assets/image%20%288%29.png)

## Transport Layer

Facilitates end-to-end connections that transmit data between hosts via the use of protocols like TCP and UDP

Every machine has ports open as means to provide services to other machines in the network. 

The Transmission Control Protocol \(TCP\) and the User Datagram Protocol \(UDP\) are two Transport Layer protocols that use port numbers that corresponding to services or applications communicating in said ports. These are two common but not the only Layer 4 \(transport\) protocols. 

 [Internet Assigned Numbers Authority](https://en.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority) \(IANA\) maintains [port assignments.](top-1000-well-known-ports.md) 

### TCP Header

![TCP Header in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2822%29.png)

Contains Source Port, Destination Port, TCP Flags and options as well as sequence and timestamp information used for TCP reliable transmission features as well as information regarding the size of the TCP payload.

![Reliable transmission features use sequence numbers to maintain accountability of all the data sent](../../.gitbook/assets/image%20%2830%29.png)

#### TCP Header Flags

Responsible for the transmission and flow of packets across the network. Port scanning methods involve techniques that employ packets with specially selected TCP flags to determine the targets OS, service versions and alert about the presence of a firewall or packet filtering methods. 

![TCP Header Flags](../../.gitbook/assets/image%20%2821%29.png)

## Transmission Control Protocol - TCP

### TCP _"3-way"_ handshake

Describes an interaction between two systems, often performing the roles of client and server in which the following exchange occurs: \(diagram from [Medium](https://cdn-images-1.medium.com/max/1600/1*n22QJMww4vGw_MrlZbysLg.png)\)

![](../../.gitbook/assets/image%20%289%29.png)

1. Client starts connection by sending packet with a SYN flag. This indicates to the server that the client wishes to start a connection
2. Server responds with another packet that has both the SYN and ACK flags activated indicating to the client that it accepts the invitation to establish a connection. The sequence and acknowledge numbers increase and expected next numbers are included in packets.

### User Datagram Protocol - UDP

Connection-less protocol used to transmit data in an unordered manner. Examples of appropriate use include low latency data transmission in audio & video calls.

![UDP Header in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2819%29.png)

#### UDP Header

Includes Source and Destination Port since this is a much simpler protocol that lacks many of the reliable transmission features TCP offers. Since there is no sequencing of data it is appropriate for applications like voice over IP, video conference... etc. 

Low-Latency applications are called as such because of their nature, the speed of the transmission and delivery of data is more important than its reliable transmission or even complete arrival. Think of when the video glitches/freezes green and the image in a video call comes back pixelated until it recovers and you can see your significant other clearly again. 

## Application Layer

Interfaces between the programs and the network - most popular applications on the Internet today \(2021\) are web browsers.

A client machine **requests** via HTTP the contents of a website. This request is destined to the hostname of a web-server "website.com". This request is formatted in HTTP. Furthermore, when the client software sends this request, the hostname will be translated to an IP address using [Domain Name System](domain-name-system-wip.md). 

After, the web server receives and processes the request, it determines the appropriate **response** which is sent in HTTP protocol again back to the client's source IP address, this time the Source IP address will be placed in the Destination field of the TCP/IP packet. 

Please note that the full expression of a web address or Uniform Resource Identifiers \(URI\) or Universal Resource Locators \(URL\) - begin with either HTTP or HTTPS, this denotes the protocol used to transfer the web page files. The S in HTTPS refers to [Transport Layer Encryption \(TLS\) or Secure Socket Layer \(SSL\)](https://kinsta.com/knowledgebase/tls-vs-ssl/#what) to authenticate the connection and encrypt the contents transmitted. _on the link a comparison between both protocols courtesy of Kinsta. - **not paid.**_

### Hypertext Transfer Protocol - HTTP

The Hypertext Transfer Protocol \(HTTP\) is an application-level protocol for distributed, collaborative, hypermedia information systems. It is a generic, stateless, protocol which can be used for many tasks beyond its use for hypertext, such as name servers and distributed object management systems, through extension of its request methods, error codes and headers. A feature of HTTP is the typing and negotiation of data representation, allowing systems to be built independently of the data being transferred. [\(RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1\)](https://tools.ietf.org/html/rfc2616)

Further reading on [Cisco](https://www.cisco.com/E-Learning/bulk/public/tac/cim/cib/using_cisco_ios_software/linked/tcpip.htm#xtocid291429)'s knowledge base.



