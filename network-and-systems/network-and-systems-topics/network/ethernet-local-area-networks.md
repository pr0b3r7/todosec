---
description: 'Fundamentals overview LANs, MAC and Frames'
---

# Ethernet Local Area Networks

In modern environments you will find that, at a general level, computer data networks can be categorized in two types: 

* Local Area Networks - connecting nearby devices, in the same room, building or campus of buildings
* Wide Area Networks - devices are somewhat geographically separated

The aggregate use of these two types of networks covers most of the communication requirements of modern businesses, they  deliver data from one endpoint to another. 

## The Ethernet or Wired LAN

Ethernet is a general reference to any cable that conforms to any of several Ethernet Standards. However, the cables used for the links use copper wires more often than not. 

In contrast to the Wired LAN, the Wireless LAN or WLAN uses radio-frequencies to transmit data between nodes instead of wires for the links. 

[The Institute of Electrical and Electronics Engineers \(IEEE\)](https://www.ieee.org/) define the required elements to build an Ethernet-based Local Area Network. These elements, among others include: 

### Devices

Assuming an Ethernet-only Local Area Network we would need an Ethernet LAN _switch,_ the switch's purpose is to increase the amount of ports that can be used to connect wires terminating into the client machines - this concept is also known as _port density_. These client machines are connected via their network interface card's Ethernet port using an Ethernet cable. 

### Cabling

Ethernet standards from Wikipedia's page on IEEE 802.3:

_"**IEEE 802.3** is a_ [_working group_](https://en.wikipedia.org/wiki/Working_group) _and a collection of_ [_Institute of Electrical and Electronics Engineers_](https://en.wikipedia.org/wiki/Institute_of_Electrical_and_Electronics_Engineers) _\(IEEE\) standards produced by the working group defining the_ [_physical layer_](https://en.wikipedia.org/wiki/Physical_layer) _and_ [_data link layer_](https://en.wikipedia.org/wiki/Data_link_layer)_'s_ [_media access control_](https://en.wikipedia.org/wiki/Media_access_control) _\(MAC\) of wired_ [_Ethernet_](https://en.wikipedia.org/wiki/Ethernet)_. This is generally a_ [_local area network_](https://en.wikipedia.org/wiki/Local_area_network) _\(LAN\) technology with some_ [_wide area network_](https://en.wikipedia.org/wiki/Wide_area_network) _\(WAN\) applications. Physical connections are made between nodes and/or infrastructure devices \(_[_hubs_](https://en.wikipedia.org/wiki/Ethernet_hub)_,_ [_switches_](https://en.wikipedia.org/wiki/Network_switch)_,_ [_routers_](https://en.wikipedia.org/wiki/Router_%28computing%29)_\) by various types of copper or_ [_fiber cable_](https://en.wikipedia.org/wiki/Optical_fiber)_._

_802.3 is a technology that supports the_ [_IEEE 802.1_](https://en.wikipedia.org/wiki/IEEE_802.1) _network architecture._

_802.3 also defines LAN access method using_ [_CSMA/CD_](https://en.wikipedia.org/wiki/CSMA/CD)_."_

| Ethernet standard | Date | Description |
| :--- | :--- | :--- |
| Experimental Ethernet | 1973 | 2.94 [Mbit/s](https://en.wikipedia.org/wiki/Mbit/s) \(367 [kB](https://en.wikipedia.org/wiki/Kilobyte)/s\) over [coaxial cable](https://en.wikipedia.org/wiki/Coaxial_cable) \(coax\) [bus](https://en.wikipedia.org/wiki/Bus_network). Single byte node address unique only to individual network. |
| Ethernet I \(DIX v1.0\) | 1980 | 10 Mbit/s \(1.25 [MB](https://en.wikipedia.org/wiki/Megabyte)/s\) over thick coax. Frames have a Type field. This frame format is used on all forms of Ethernet by protocols in the [Internet protocol suite](https://en.wikipedia.org/wiki/Internet_protocol_suite). Six byte [MAC address](https://en.wikipedia.org/wiki/MAC_address). |
| Ethernet II \(DIX v2.0\) | 1982 |  |
| IEEE 802.3 standard | 1983 | [10BASE5](https://en.wikipedia.org/wiki/10BASE5) 10 Mbit/s \(1.25 MB/s\) over thick coax. Same as Ethernet II \(above\) except Type field is replaced by Length, and an [802.2](https://en.wikipedia.org/wiki/IEEE_802.2) LLC header follows the 802.3 header. Based on the [CSMA/CD](https://en.wikipedia.org/wiki/Carrier_sense_multiple_access_with_collision_detection) Process. |
| [802.3a](https://en.wikipedia.org/wiki/802.3a) | 1985 | [10BASE2](https://en.wikipedia.org/wiki/10BASE2) 10 Mbit/s \(1.25 MB/s\) over thin Coax \(a.k.a. thinnet or cheapernet\) |
| [802.3b](https://en.wikipedia.org/wiki/802.3b) | 1985 | [10BROAD36](https://en.wikipedia.org/wiki/10BROAD36) |
| 802.3c | 1985 | 10 Mbit/s \(1.25 MB/s\) repeater specs |
| 802.3-1985 | 1985 | a revision of the base standard from 1983 |
| [802.3d](https://en.wikipedia.org/wiki/802.3d) | 1987 | [Fiber-optic inter-repeater link](https://en.wikipedia.org/wiki/Fiber-optic_inter-repeater_link) |
| [802.3e](https://en.wikipedia.org/wiki/802.3e) | 1987 | [1BASE5](https://en.wikipedia.org/wiki/1BASE5) or [StarLAN](https://en.wikipedia.org/wiki/StarLAN) |
| [802.3i](https://en.wikipedia.org/wiki/802.3i) | 1990 | [10BASE-T](https://en.wikipedia.org/wiki/10BASE-T) 10 Mbit/s \(1.25 MB/s\) over twisted pair |
| [802.3j](https://en.wikipedia.org/wiki/802.3j) | 1993 | [10BASE-F](https://en.wikipedia.org/wiki/10BASE-F) 10 Mbit/s \(1.25 MB/s\) over Fiber-Optic |
| 802.3q | 1993 | [GDMO](https://en.wikipedia.org/wiki/GDMO) \([ISO 10164-4](https://en.wikipedia.org/wiki/List_of_International_Organization_for_Standardization_standards#ISO_10000_–_ISO_10999)\) format for Layer Managed Objects |
| [802.3u](https://en.wikipedia.org/wiki/802.3u) | 1995 | [100BASE-TX](https://en.wikipedia.org/wiki/100BASE-TX), [100BASE-T4](https://en.wikipedia.org/wiki/100BASE-T4), [100BASE-FX](https://en.wikipedia.org/wiki/100BASE-FX) Fast Ethernet at 100 Mbit/s \(12.5 MB/s\) with [autonegotiation](https://en.wikipedia.org/wiki/Autonegotiation) |
| [802.3x](https://en.wikipedia.org/wiki/IEEE_802.3x) | 1997 | Full Duplex and [flow control](https://en.wikipedia.org/wiki/Ethernet_flow_control); also incorporates DIX framing, so there's no longer a DIX/802.3 split |
| [802.3y](https://en.wikipedia.org/wiki/802.3y) | 1998 | [100BASE-T2](https://en.wikipedia.org/wiki/100BASE-T2) 100 Mbit/s \(12.5 MB/s\) over voice-grade twisted pair |
| [802.3z](https://en.wikipedia.org/wiki/802.3z) | 1998-07 | [1000BASE-X](https://en.wikipedia.org/wiki/1000BASE-X) [Gbit](https://en.wikipedia.org/wiki/Gigabit)/s Ethernet over Fiber-Optic at 1 Gbit/s \(125 MB/s\) |
| 802.3-1998 | 1998-07 | \(802.3aa\) A revision of base standard incorporating the above amendments and errata |
| [802.3ab](https://en.wikipedia.org/wiki/802.3ab) | 1999-06 | [1000BASE-T](https://en.wikipedia.org/wiki/1000BASE-T) Gbit/s Ethernet over twisted pair at 1 Gbit/s \(125 MB/s\) |
| [802.3ac](https://en.wikipedia.org/wiki/802.3ac) | 1998-09 | Max frame size extended to 1522 bytes \(to allow "Q-tag"\) The Q-tag includes [802.1Q](https://en.wikipedia.org/wiki/IEEE_802.1Q) [VLAN](https://en.wikipedia.org/wiki/VLAN) information and [802.1p](https://en.wikipedia.org/wiki/802.1p) priority information. |
| [802.3ad](https://en.wikipedia.org/wiki/802.3ad) | 2000-03 | [Link aggregation](https://en.wikipedia.org/wiki/Link_aggregation) for parallel links, since moved to [IEEE 802.1AX](https://en.wikipedia.org/wiki/IEEE_802.1AX) |
| 802.3-2002 | 2002-01 | \(802.3ag\) A revision of base standard incorporating the three prior amendments and errata |
| [802.3ae](https://en.wikipedia.org/wiki/802.3ae) | 2002-06 | [10 Gigabit Ethernet](https://en.wikipedia.org/wiki/10_Gigabit_Ethernet) over fiber; 10GBASE-SR, 10GBASE-LR, 10GBASE-ER, 10GBASE-SW, 10GBASE-LW, 10GBASE-EW |
| [802.3af](https://en.wikipedia.org/wiki/802.3af) | 2003-06 | [Power over Ethernet](https://en.wikipedia.org/wiki/Power_over_Ethernet) \(15.4 W\) |
| [802.3ah](https://en.wikipedia.org/wiki/802.3ah) | 2004-06 | [Ethernet in the First Mile](https://en.wikipedia.org/wiki/Ethernet_in_the_First_Mile) |
| [802.3ak](https://en.wikipedia.org/wiki/802.3ak) | 2004-02 | [10GBASE-CX4](https://en.wikipedia.org/wiki/10GBASE-CX4) 10 Gbit/s \(1,250 MB/s\) Ethernet over [twinaxial cables](https://en.wikipedia.org/wiki/Twinaxial_cable) |
| 802.3-2005 | 2005-06 | \(802.3am\) A revision of base standard incorporating the four prior amendments and errata. |
| [802.3an](https://en.wikipedia.org/wiki/802.3an) | 2006-06 | [10GBASE-T](https://en.wikipedia.org/wiki/10GBASE-T) 10 Gbit/s \(1,250 MB/s\) Ethernet over unshielded twisted pair \(UTP\) |
| 802.3ap | 2007-03 | [Backplane](https://en.wikipedia.org/wiki/Backplane) Ethernet \(1 and 10 Gbit/s \(125 and 1,250 MB/s\) over [printed circuit boards](https://en.wikipedia.org/wiki/Printed_circuit_board)\) |
| [802.3aq](https://en.wikipedia.org/wiki/802.3aq) | 2006-09 | [10GBASE-LRM](https://en.wikipedia.org/wiki/10GBASE-LRM) 10 Gbit/s \(1,250 MB/s\) Ethernet over multimode fiber |
| P802.3ar | Cancelled | Congestion management \(withdrawn\) |
| 802.3as | 2006-09 | Frame expansion |
| [802.3at](https://en.wikipedia.org/wiki/802.3at) | 2009-09 | [Power over Ethernet](https://en.wikipedia.org/wiki/Power_over_Ethernet) enhancements \(25.5 W\) |
| 802.3au | 2006-06 | Isolation requirements for Power over Ethernet \(802.3-2005/Cor 1\) |
| [802.3av](https://en.wikipedia.org/wiki/802.3av) | 2009-09 | 10 Gbit/s [EPON](https://en.wikipedia.org/wiki/Ethernet_passive_optical_network) |
| 802.3aw | 2007-06 | Fixed an equation in the publication of 10GBASE-T \(released as 802.3-2005/Cor 2\) |
| 802.3ax | 2008-11 | Link aggregation – moved to and approved as [802.1AX](https://en.wikipedia.org/wiki/802.1AX) |
| 802.3-2008 | 2008-12 | \(802.3ay\) A revision of base standard incorporating the 802.3an/ap/aq/as amendments, two corrigenda and errata. |
| [802.3az](https://en.wikipedia.org/wiki/802.3az) | 2010-09 | [Energy-Efficient Ethernet](https://en.wikipedia.org/wiki/Energy-Efficient_Ethernet) |
| [802.3ba](https://en.wikipedia.org/wiki/802.3ba) | 2010-06 | 40 Gbit/s and 100 Gbit/s Ethernet. 40 Gbit/s over 1 m backplane, 10 m Cu cable assembly \(4×25 Gbit or 10×10 Gbit lanes\) and 100 m of [MMF](https://en.wikipedia.org/wiki/Multi-mode_optical_fiber) and 100 Gbit/s up to 10 m of Cu cable assembly, 100 m of [MMF](https://en.wikipedia.org/wiki/Multi-mode_optical_fiber) or 40 km of [SMF](https://en.wikipedia.org/wiki/Single-mode_optical_fiber) respectively |
| 802.3-2008/Cor 1 | 2009 | \(802.3bb\) Increase Pause Reaction Delay timings which are insufficient for 10 Gbit/s \(workgroup name was 802.3bb\) |
| 802.3bc | 2009-09 | Move and update Ethernet related TLVs \(type, length, values\), previously specified in Annex F of [IEEE 802.1AB](https://en.wikipedia.org/wiki/IEEE_802.1AB) \(LLDP\) to 802.3. |
| 802.3bd | 2011-06 | Priority-based Flow Control. An amendment by the [IEEE 802.1](https://en.wikipedia.org/wiki/IEEE_802.1) [Data Center Bridging](https://en.wikipedia.org/wiki/Data_Center_Bridging) Task Group \(802.1Qbb\) to develop an amendment to IEEE Std 802.3 to add a MAC Control Frame to support IEEE 802.1Qbb Priority-based Flow Control. |
| 802.3.1 | 2011-05 | \(802.3be\) MIB definitions for Ethernet. It consolidates the Ethernet related [MIBs](https://en.wikipedia.org/wiki/Management_Information_Base) present in Annex 30A&B, various [IETF](https://en.wikipedia.org/wiki/IETF) [RFCs](https://en.wikipedia.org/wiki/Request_for_Comments), and 802.1AB annex F into one master document with a machine readable extract. \(workgroup name was P802.3be\) |
| 802.3bf | 2011-05 | Provide an accurate indication of the transmission and reception initiation times of certain packets as required to support IEEE P802.1AS. |
| 802.3bg | 2011-03 | Provide a 40 Gbit/s [PMD](https://en.wikipedia.org/wiki/Physical_Medium_Dependent) which is optically compatible with existing carrier [SMF](https://en.wikipedia.org/wiki/Single-mode_optical_fiber) 40 Gbit/s client interfaces \([OTU3](https://en.wikipedia.org/wiki/OTU3)/[STM-256](https://en.wikipedia.org/wiki/STM-256)/[OC-768](https://en.wikipedia.org/wiki/OC-768)/[40G POS](https://en.wikipedia.org/wiki/Packet_over_SONET)\). |
| 802.3-2012 | 2012-08 | \(802.3bh\) A revision of base standard incorporating the 802.3at/av/az/ba/bc/bd/bf/bg amendments, a corrigenda and errata. |
| 802.3bj | 2014-06 | Define a 4-lane 100 Gbit/s backplane PHY for operation over links consistent with copper traces on "improved FR-4" \(as defined by IEEE P802.3ap or better materials to be defined by the Task Force\) with lengths up to at least 1 m and a 4-lane 100 Gbit/s PHY for operation over links consistent with copper [twinaxial cables](https://en.wikipedia.org/wiki/Twinaxial_cable) with lengths up to at least 5 m. |
| 802.3bk | 2013-08 | This amendment to IEEE Std 802.3 defines the physical layer specifications and management parameters for EPON operation on point-to-multipoint passive optical networks supporting extended power budget classes of PX30, PX40, PRX40, and PR40 PMDs. |
| 802.3bm | 2015-02 | [100G/40G Ethernet](https://en.wikipedia.org/wiki/100_Gigabit_Ethernet) for optical fiber |
| 802.3bn | 2016-09 | 10G-[EPON](https://en.wikipedia.org/wiki/Ethernet_passive_optical_network) and 10GPASS-XR, passive optical networks over coax |
| 802.3bp | 2016-06 | 1000BASE-T1 – Gigabit Ethernet over a single twisted pair, automotive & industrial environments |
| 802.3bq | 2016-06 | 25G/[40GBASE-T](https://en.wikipedia.org/wiki/40GBASE-T) for 4-pair balanced twisted-pair cabling with 2 connectors over 30 m distances |
| 802.3br | 2016-06 | Specification and Management Parameters for Interspersing Express Traffic |
| 802.3bs | 2017-12 | [200GbE](https://en.wikipedia.org/wiki/200GbE) \(200 Gbit/s\) over single-mode fiber and [400GbE](https://en.wikipedia.org/wiki/400GbE) \(400 Gbit/s\) over optical physical media |
| [802.3bt](https://en.wikipedia.org/wiki/802.3bt) | 2018-09 | third generation [Power over Ethernet](https://en.wikipedia.org/wiki/Power_over_Ethernet) with up to 100 W using all 4 pairs balanced twisted-pair cabling \(4PPoE\), including 10GBASE-T, lower standby power and specific enhancements to support IoT applications \(e.g. lighting, sensors, building automation\). |
| 802.3bu | 2016-12 | [Power over Data Lines \(PoDL\)](https://en.wikipedia.org/wiki/PoE) for single twisted-pair Ethernet \([100BASE-T1](https://en.wikipedia.org/wiki/Fast_Ethernet#100BASE-T1)\) |
| 802.3bv | 2017-02 | Gigabit Ethernet over [plastic optical fiber \(POF\)](https://en.wikipedia.org/wiki/Plastic_optical_fiber) |
| 802.3bw | 2015-10 | 100BASE-T1 – 100 Mbit/s Ethernet over a single twisted pair for automotive applications |
| 802.3-2015 | 2015-09 | 802.3bx – a new consolidated revision of the 802.3 standard including amendments 802.3bk/bj/bm |
| [802.3by](https://en.wikipedia.org/wiki/802.3by) | 2016-06 | [Optical fiber](https://en.wikipedia.org/wiki/Optical_fiber), twinax and backplane [25 Gigabit Ethernet](https://en.wikipedia.org/wiki/25_Gigabit_Ethernet)[\[6\]](https://en.wikipedia.org/wiki/IEEE_802.3#cite_note-6) |
| 802.3bz | 2016-09 | [2.5GBASE-T and 5GBASE-T](https://en.wikipedia.org/wiki/2.5GBASE-T_and_5GBASE-T) – 2.5 Gigabit and 5 Gigabit Ethernet over [Cat-5](https://en.wikipedia.org/wiki/Category_5_cable)/[Cat-6](https://en.wikipedia.org/wiki/Category_6_cable) twisted pair |
| 802.3ca | 2020-06 | 100G-EPON – 25, 50, and 100 Gbit/s over [Ethernet](https://en.wikipedia.org/wiki/Ethernet) [Passive Optical Networks](https://en.wikipedia.org/wiki/Passive_Optical_Network) |
| 802.3cb | 2018-09 | 2.5 Gbit/s and 5 Gbit/s Operation over Backplane |
| 802.3cc | 2017-12 | 25 Gbit/s over Single Mode Fiber |
| 802.3cd | 2018-12 | Media Access Control Parameters for 50 Gbit/s and Physical Layers and Management Parameters for 50, 100, and 200 Gbit/s Operation |
| 802.3ce | 2017-03 | Multilane Timestamping |
| 802.3cf | 2019-03 | YANG Data Model Definitions |
| [802.3cg](https://en.wikipedia.org/w/index.php?title=802.3cg&action=edit&redlink=1) | 2019-11 | 10 Mbit/s Single Twisted Pair Ethernet |
| [802.3ch](https://en.wikipedia.org/w/index.php?title=802.3ch&action=edit&redlink=1) | 2020-06 | Multi-Gig Automotive Ethernet \(2.5, 5, 10 Gbit/s\) over 15 m with optional PoDL |
| 802.3-2018 | 2018-08 | 802.3cj – 802.3-2015 maintenance, merge recent amendments bn/bp/bq/br/bs/bw/bu/bv/by/bz/cc/ce |
| 802.3ck | \(TBD\) | 100, 200, and 400 Gbit/s Ethernet using 100 Gbit/s lanes – scheduled for fall 2021 |
| 802.3cm | 2020-01 | 400 Gbit/s over multimode fiber \(four and eight pairs, 100 m\) |
| 802.3cn | 2019-11 | 50 Gbit/s \(40 km\), 100 Gbit/s \(80 km\), 200 Gbit/s \(four λ, 40 km\), and 400 Gbit/s \(eight λ, 40 km and single λ, 80 km over [DWDM](https://en.wikipedia.org/wiki/DWDM)\) over Single-Mode Fiber and DWDM |
| 802.3cp | \(TBD\) | 10/25/50 Gbit/s single-strand optical access with at least 10/20/40 km reach – scheduled for summer 2021 |
| 802.3cq | 2020-01 | Power over Ethernet over 2 pairs \(maintenance\) |
| 802.3cr | \(TBD\) | Isolation \(maintenance\) |
| 802.3cs | \(TBD\) | "Super-PON" – increased-reach, 10 Gbit/s optical access with at least 50 km reach and 1:64 split ratio per wavelength pair, 16 wavelength pairs – scheduled for summer 2021 |
| 802.3ct | \(TBD\) | 100 Gbit/s over DWDM systems \(80 km reach using coherent modulation\) – scheduled for fall 2021 |
| 802.3cu | \(TBD\) | 100 Gbit/s and 400 Gbit/s over SMF using 100 Gbit/s lanes – scheduled for early 2021 |
| 802.3cv | \(TBD\) | Power over Ethernet maintenance |
| 802.3cw | \(TBD\) | 400 Gbit/s over DWDM Systems |
| 802.3cx | \(TBD\) | Improved PTP Timestamping Accuracy |
| 802.3cy | \(TBD\) | Greater than 10 Gbit/s Electrical Automotive Ethernet |
| 802.3cz | \(TBD\) | Multi-Gigabit Optical Automotive Ethernet |
| 802.3da | \(TBD\) | 10 Mb/s Operation over Single Balanced Pair Multidrop Segments |
| 802.3db | \(TBD\) | 100 Gbit/s, 200 Gbit/s, and 400 Gbit/s Operation over Optical Fiber using 100 Gbit/s Signaling |

### Connector Terminals or Interfaces

### Protocol Rules

