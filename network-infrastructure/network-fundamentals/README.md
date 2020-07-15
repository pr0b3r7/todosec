---
description: >-
  Let's aim to describe the basic components of modern computer networking and
  outline some topics to structure/guide our study with
---

# Network Fundamentals

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

![Transport - Layer 4 TLS 1.2 Segment in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2815%29.png)

![Network - Layer 3 Packet in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2813%29.png)

![Data Link - Layer 2 Frame in Wireshark Packet Analyzer](../../.gitbook/assets/image%20%2812%29.png)

#### \_\_[_Protocol data unit_](https://en.wikipedia.org/wiki/Protocol_data_unit)_\*\*\*_

## TCP/IP stack

* Application
* Transport
* Internet
* Network Access

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

### [IPv6 Addressing](https://en.wikipedia.org/wiki/IPv6)

"IPv6 addresses are represented as eight groups, separated by colons, of four hexadecimal digits. The full representation may be simplified by several methods of notation; for example, _2001:0db8:0000:0000:0000:8a2e:0370:7334 becomes 2001:db8::8a2e:370:7334." \(Wikipedia\)_

Some [statistics ](https://www.google.com/intl/en/ipv6/statistics.html)by google on its world-wide adoption, up to you is to decide when the [well announced ](https://csrc.nist.gov/publications/detail/journal-article/2008/internet-protocol-version-6-ipv6)final cut over is happening.

![](../../.gitbook/assets/image%20%288%29.png)

## Transport Layer

Facilitates end-to-end connections that transmit data between hosts via the use of protocols like TCP and UDP

Every machine has ports open as means to provide services to other machines in the network. 

The Transmission Control Protocol \(TCP\) and the User Datagram Protocol \(UDP\) are two Transport Layer protocols that use port numbers that corresponding to services or applications communicating in said ports. These are two common but not the only Layer 4 \(transport\) protocols. 

 [Internet Assigned Numbers Authority](https://en.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority) \(IANA\) maintains [port assignments.](top-1000-well-known-ports.md) 

## TCP _"3-way"_ handshake

Describes an interaction between two systems, often performing the roles of client and server in which the following exchange occurs: \(diagram from [Medium](https://cdn-images-1.medium.com/max/1600/1*n22QJMww4vGw_MrlZbysLg.png)\)

![](../../.gitbook/assets/image%20%289%29.png)

1. SYN - hey, are you available and willing to communicate? 
2. SYN/ACK - yes, I am and would like to establish said communication.
3. ACK - Very well, let's consider this communication channel established, from now on, we will keep communicating this way

_Synchronize, Acknowledge\*\*\*_ 

