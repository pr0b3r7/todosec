---
description: 'https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers'
---

# Top 1000 Well Known Ports



| Well-known ports |  |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Port | TCP | UDP | IANA status | Description | SCTP |
| 0 | Reserved | Reserved | Official |  |  |
| N/A | N/A | Unofficial | In programming [APIs ](https://www.youtube.com/watch?v=s7wmiS2mSXY)\(not in communication between hosts\), requests a system-allocated \(dynamic\) port |  |  |
| 1 | Yes | Assigned | Official | [TCP Port Service Multiplexer](https://en.wikipedia.org/wiki/TCP_Port_Service_Multiplexer) \(TCPMUX\). Historic. Both TCP and UDP have been assigned to TCPMUX by IANA, but by design only TCP is specified. |  |
| 5 | Assigned | Assigned | Official | [Remote Job Entry](https://en.wikipedia.org/wiki/Remote_Job_Entry) was historically using socket 5 in its [old socket form](https://en.wikipedia.org/wiki/Network_socket#History), while MIB PIM has identified it as TCP/5 and IANA has assigned both TCP and UDP 5 to it. |  |
| 7 | Yes | Yes | Official | [Echo Protocol](https://en.wikipedia.org/wiki/Echo_Protocol) |  |
| 9 | Yes | Yes | Official | [Discard Protocol](https://en.wikipedia.org/wiki/Discard_Protocol) | Yes  |
| No | Yes | Unofficial | [Wake-on-LAN](https://en.wikipedia.org/wiki/Wake-on-LAN) |  |  |
| 11 | Yes | Yes | Official | Active Users \([systat](https://en.wikipedia.org/wiki/Systat_%28protocol%29) service\) |  |
| 13 | Yes | Yes | Official | [Daytime Protocol](https://en.wikipedia.org/wiki/Daytime_Protocol) |  |
| 15 | Yes | No | Unofficial | Previously [netstat](https://en.wikipedia.org/wiki/Netstat) servic |  |
| 17 | Yes | Yes | Official | [Quote of the Day](https://en.wikipedia.org/wiki/QOTD) \(QOTD\) |  |
| 18 | Yes | Yes | Official | [Message Send Protocol](https://en.wikipedia.org/wiki/Message_Send_Protocol) |  |
| 19 | Yes | Yes | Official | [Character Generator Protocol](https://en.wikipedia.org/wiki/Character_Generator_Protocol) \(CHARGEN\) |  |
| 20 | Yes | Assigned | Official | [File Transfer Protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol) \(FTP\) data transfer | Yes  |
| 21 | Yes | Assigned | Official | [File Transfer Protocol](https://en.wikipedia.org/wiki/File_Transfer_Protocol) \(FTP\) control \(command\) | Yes |
| 22 | Yes | Assigned | Official | [Secure Shell](https://en.wikipedia.org/wiki/Secure_Shell) \(SSH\), secure logins, [file transfers](https://en.wikipedia.org/wiki/File_transfer) \([scp](https://en.wikipedia.org/wiki/Secure_copy), [sftp](https://en.wikipedia.org/wiki/SSH_file_transfer_protocol)\) and port forwarding | Yes  |
| 23 | Yes | Assigned | Official | [Telnet](https://en.wikipedia.org/wiki/Telnet) protocol—unencrypted text communications |  |
| 25 | Yes | Assigned | Official | [Simple Mail Transfer Protocol](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) \(SMTP\), used for email routing between mail servers |  |
| 37 | Yes | Yes | Official | [Time Protocol](https://en.wikipedia.org/wiki/Time_Protocol) |  |
| 42 | Assigned | Yes | Official | [Host Name Server Protocol](https://en.wikipedia.org/wiki/ARPA_Host_Name_Server_Protocol) |  |
| 43 | Yes | Assigned | Official | [WHOIS](https://en.wikipedia.org/wiki/WHOIS) protocol |  |
| 47 | Reserved | Reserved | Official |  |  |
| 49 | Yes | Yes | Official | [TACACS](https://en.wikipedia.org/wiki/TACACS) Login Host protocol. [TACACS+](https://en.wikipedia.org/wiki/TACACS%2B), still in draft which is an improved but distinct version of TACACS, only uses TCP 49. |  |
| 51 | Reserved | Reserved | Official | Historically used for [Interface Message Processor](https://en.wikipedia.org/wiki/Interface_Message_Processor) logical address management, entry has been removed by IANA on 2013-05-25 |  |
| 52 | Assigned | Assigned | Official | [Xerox Network Systems](https://en.wikipedia.org/wiki/Xerox_Network_Systems) \(XNS\) Time Protocol. Despite this port being assigned by IANA, the service is meant to work on [SPP](https://en.wikipedia.org/wiki/Sequenced_Packet_Protocol) \(ancestor of [IPX/SPX](https://en.wikipedia.org/wiki/IPX/SPX)\), instead of TCP/IP. |  |
| 53 | Yes | Yes | Official | [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) \(DNS\) |  |
| 54 | Assigned | Assigned | Official | Xerox Network Systems \(XNS\) Clearinghouse \(Name Server\). Despite this port being assigned by IANA, the service is meant to work on [SPP](https://en.wikipedia.org/wiki/Sequenced_Packet_Protocol) \(ancestor of [IPX/SPX](https://en.wikipedia.org/wiki/IPX/SPX)\), instead of TCP/IP. |  |
| 56 | Assigned | Assigned | Official | Xerox Network Systems \(XNS\) Authentication Protocol. Despite this port being assigned by IANA, the service is meant to work on [SPP](https://en.wikipedia.org/wiki/Sequenced_Packet_Protocol) \(ancestor of [IPX/SPX](https://en.wikipedia.org/wiki/IPX/SPX)\), instead of TCP/IP. |  |
| 58 | Assigned | Assigned | Official | Xerox Network Systems \(XNS\) Mail. Despite this port being assigned by IANA, the service is meant to work on [SPP](https://en.wikipedia.org/wiki/Sequenced_Packet_Protocol) \(ancestor of [IPX/SPX](https://en.wikipedia.org/wiki/IPX/SPX)\), instead of TCP/IP. |  |
| 61 | Reserved | Reserved | Official | Historically assigned to the [NIFTP-Based Mail](https://en.wikipedia.org/w/index.php?title=NIFTP-Based_Mail&action=edit&redlink=1) protocol,  but was never documented in the related [IEN](https://en.wikipedia.org/wiki/Internet_Experiment_Note). The port number entry was removed from IANA's registry on 2017-05-18. |  |
| 67 | Assigned | Yes | Official | [Bootstrap Protocol](https://en.wikipedia.org/wiki/Bootstrap_Protocol) \(BOOTP\) server; also used by [Dynamic Host Configuration Protocol](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) \(DHCP\) |  |
| 68 | Assigned | Yes | Official | Bootstrap Protocol \(BOOTP\) client; also used by Dynamic Host Configuration Protocol \(DHCP\) |  |
| 69 | Assigned | Yes | Official | [Trivial File Transfer Protocol](https://en.wikipedia.org/wiki/Trivial_File_Transfer_Protocol) \(TFTP\) |  |
| 70 | Yes | Assigned | Official | [Gopher](https://en.wikipedia.org/wiki/Gopher_%28protocol%29) protocol |  |
| 71–74 | Yes | Yes | Official | [NETRJS](https://en.wikipedia.org/wiki/NETRJS) protocol |  |
| 79 | Yes | Assigned | Official | [Finger protocol](https://en.wikipedia.org/wiki/Finger_protocol) |  |
| 80 | Yes | Assigned | Official | [Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) \(HTTP\) | Yes |
| No | Yes | Unofficial | [QUIC](https://en.wikipedia.org/wiki/QUIC), a transport protocol over UDP \(still in draft as of April 2020\), using stream [multiplexing](https://en.wikipedia.org/wiki/Multiplexing), encryption by default with [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security), and currently supporting [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2). QUIC has been renamed to [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3), which is currently an [Internet Draft](https://en.wikipedia.org/wiki/Internet_Draft). |  |  |
| 82 |  | Yes | Unofficial | [TorPark](https://en.wikipedia.org/wiki/TorPark) control |  |
| 83 | Yes | Assigned | Official | MIT ML Device, networking file system  |  |
| 88 | Yes | Assigned | Official | [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) authentication system |  |
| 90 | Yes | Yes | Unofficial | [PointCast \(dotcom\)](https://en.wikipedia.org/wiki/PointCast_%28dotcom%29) |  |
| 95 | Yes | Assigned | Official | SUPDUP, terminal-independent remote login  |  |
| 101 | Yes | Assigned | Official | [NIC](https://en.wikipedia.org/wiki/History_of_the_Internet#NIC,_InterNIC,_IANA_and_ICANN) [host name](https://en.wikipedia.org/wiki/Hostname) |  |
| 102 | Yes | Assigned | Official | [ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization) Transport Service Access Point \([TSAP](https://en.wikipedia.org/wiki/TSAP)\) Class 0 protocol |  |
| 104 | Yes | Yes | Official | [Digital Imaging and Communications in Medicine](https://en.wikipedia.org/wiki/Digital_Imaging_and_Communications_in_Medicine) \(DICOM; also port 11112\) |  |
| 105 | Yes | Yes | Official | [CCSO Nameserver](https://en.wikipedia.org/wiki/CCSO_Nameserver) |  |
| 107 | Yes | Yes | Official | [Remote User Telnet Service](https://en.wikipedia.org/wiki/Rtelnet) \(RTelnet\) |  |
| 108 | Yes | Yes | Official | IBM [Systems Network Architecture](https://en.wikipedia.org/wiki/Systems_Network_Architecture) \(SNA\) gateway access server |  |
| 109 | Yes | Assigned | Official | [Post Office Protocol](https://en.wikipedia.org/wiki/Post_Office_Protocol), version 2 \(POP2\) |  |
| 110 | Yes | Assigned | Official | Post Office Protocol, version 3 \(POP3\) |  |
| 111 | Yes | Yes | Official | [Open Network Computing Remote Procedure Call](https://en.wikipedia.org/wiki/Open_Network_Computing_Remote_Procedure_Call) \(**ONC RPC**, sometimes referred to as **Sun RPC**\) |  |
| 113 | Yes | No | Official | [Ident](https://en.wikipedia.org/wiki/Ident_protocol), authentication service/identification protocol, used by [IRC](https://en.wikipedia.org/wiki/Internet_Relay_Chat) servers to identify users |  |
| Yes | Assigned | Official | Authentication Service \(auth\), the predecessor to identification protocol. Used to determine a user's identity of a particular TCP connection. |  |  |
| 115 | Yes | Assigned | Official | [Simple File Transfer Protocol](https://en.wikipedia.org/wiki/Simple_File_Transfer_Protocol) |  |
| 117 | Yes | Yes | Official | [UUCP Mapping Project](https://en.wikipedia.org/wiki/UUCP_Mapping_Project) \(path service\) |  |
| 118 | Yes | Yes | Official | Structured Query Language \([SQL](https://en.wikipedia.org/wiki/SQL)\) Services |  |
| 119 | Yes | Assigned | Official | [Network News Transfer Protocol](https://en.wikipedia.org/wiki/Network_News_Transfer_Protocol) \(NNTP\), retrieval of newsgroup messages |  |
| 123 | Assigned | Yes | Official | [Network Time Protocol](https://en.wikipedia.org/wiki/Network_Time_Protocol) \(NTP\), used for time synchronization |  |
| 126 | Yes | Yes | Official | Formerly [Unisys](https://en.wikipedia.org/wiki/Unisys) Unitary Login, renamed by Unisys to NXEdit. Used by Unisys Programmer's Workbench for Clearpath MCP, an IDE for [Unisys MCP software development](https://en.wikipedia.org/wiki/Unisys_MCP_programming_languages) |  |
| 135 | Yes | Yes | Official | [DCE](https://en.wikipedia.org/wiki/Distributed_Computing_Environment) [endpoint](https://en.wikipedia.org/wiki/Communication_endpoint) resolution |  |
| Yes | Yes | Official | [Microsoft](https://en.wikipedia.org/wiki/Microsoft) EPMAP \(End Point Mapper\), also known as DCE/[RPC](https://en.wikipedia.org/wiki/Remote_procedure_call) Locator service,[\[67\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-67) used to remotely manage services including [DHCP server](https://en.wikipedia.org/wiki/DHCP_server), [DNS](https://en.wikipedia.org/wiki/Domain_Name_System) server and [WINS](https://en.wikipedia.org/wiki/Windows_Internet_Name_Service). Also used by [DCOM](https://en.wikipedia.org/wiki/Distributed_Component_Object_Model) |  |  |
| 137 | Yes | Yes | Official | [NetBIOS](https://en.wikipedia.org/wiki/NetBIOS) Name Service, used for name registration and [resolution](https://en.wikipedia.org/wiki/Name_resolution_%28computer_systems%29) |  |
| 138 | Assigned | Yes | Official | NetBIOS Datagram Service |  |
| 139 | Yes | Assigned | Official | NetBIOS Session Service |  |
| 143 | Yes | Assigned | Official | [Internet Message Access Protocol](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol) \(IMAP\),management of [electronic mail](https://en.wikipedia.org/wiki/Email) messages on a server |  |
| 152 | Yes | Yes | Official | [Background File Transfer Program](https://en.wikipedia.org/w/index.php?title=Background_File_Transfer_Program&action=edit&redlink=1) \(BFTP\) |  |
| 153 | Yes | Yes | Official | [Simple Gateway Monitoring Protocol](https://en.wikipedia.org/wiki/Simple_Gateway_Monitoring_Protocol) \(SGMP\), a protocol for remote inspection and alteration of gateway management information |  |
| 156 | Yes | Yes | Official | Structured Query Language \([SQL](https://en.wikipedia.org/wiki/SQL)\) Service |  |
| 158 | Yes | Yes | Official | [Distributed Mail System Protocol](https://en.wikipedia.org/w/index.php?title=Distributed_Mail_System_Protocol&action=edit&redlink=1) \(**DMSP**, sometimes referred to as **Pcmail**\) |  |
| 161 | Assigned | Yes | Official | [Simple Network Management Protocol](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol) \(SNMP\) |  |
| 162 | Yes | Yes | Official | [Simple Network Management Protocol](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol) Trap \(SNMPTRAP\) |  |
| 170 | Yes | Yes | Official | Network [PostScript](https://en.wikipedia.org/wiki/PostScript) [print server](https://en.wikipedia.org/wiki/Print_server) |  |
| 177 | Yes | Yes | Official | [X Display Manager Control Protocol](https://en.wikipedia.org/wiki/X_Display_Manager_Control_Protocol) \(XDMCP\), used for remote logins to an [X Display Manager](https://en.wikipedia.org/wiki/X_display_manager_%28program_type%29) server |  |
| 179 | Yes | Assigned | Official | [Border Gateway Protocol](https://en.wikipedia.org/wiki/Border_Gateway_Protocol) \(BGP\),[\[77\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-rfc4271-77) used to exchange routing and reachability information among [autonomous systems](https://en.wikipedia.org/wiki/Autonomous_system_%28Internet%29) \(AS\) on the [Internet](https://en.wikipedia.org/wiki/Internet) | Yes  |
| 194 | Yes | Yes | Official | [Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat) \(IRC\) |  |
| 199 | Yes | Yes | Official | [SNMP](https://en.wikipedia.org/wiki/SNMP) Unix Multiplexer \(SMUX\) |  |
| 201 | Yes | Yes | Official | [AppleTalk](https://en.wikipedia.org/wiki/AppleTalk) Routing Maintenance |  |
| 209 | Yes | Assigned | Official | [Quick Mail Transfer Protocol](https://en.wikipedia.org/wiki/Quick_Mail_Transfer_Protocol) |  |
| 210 | Yes | Yes | Official | [ANSI](https://en.wikipedia.org/wiki/ANSI) [Z39.50](https://en.wikipedia.org/wiki/Z39.50) |  |
| 213 | Yes | Yes | Official | [Internetwork Packet Exchange](https://en.wikipedia.org/wiki/Internetwork_Packet_Exchange) \(IPX\) |  |
| 218 | Yes | Yes | Official | Message posting protocol \(MPP\) |  |
| 220 | Yes | Yes | Official | [Internet Message Access Protocol](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol) \(IMAP\), version 3 |  |
| 225–241 | Reserved | Reserved | Official |  |  |
| 249–255 | Reserved | Reserved | Official |  |  |
| 259 | Yes | Yes | Official | Efficient Short Remote Operations \(ESRO\) |  |
| 262 | Yes | Yes | Official | Arcisdms |  |
| 264 | Yes | Yes | Official | [Border Gateway Multicast Protocol](https://en.wikipedia.org/wiki/Border_Gateway_Multicast_Protocol) \(BGMP\) |  |
| 280 | Yes | Yes | Official | http-mgmt |  |
| 300 | Yes |  | Unofficial | [ThinLinc](https://en.wikipedia.org/wiki/ThinLinc) Web Access |  |
| 308 | Yes |  | Official | Novastor Online Backup |  |
| 311 | Yes | Assigned | Official | [Mac OS X Server](https://en.wikipedia.org/wiki/Mac_OS_X_Server) Admin \(officially [AppleShare](https://en.wikipedia.org/wiki/AppleShare) IP Web administration\) |  |
| 318 | Yes | Yes | Official | PKIX [Time Stamp Protocol](https://en.wikipedia.org/wiki/Time_Stamp_Protocol) \(TSP\) |  |
| 319 |  | Yes | Official | [Precision Time Protocol](https://en.wikipedia.org/wiki/Precision_Time_Protocol) \(PTP\) event messages |  |
| 320 |  | Yes | Official | [Precision Time Protocol](https://en.wikipedia.org/wiki/Precision_Time_Protocol) \(PTP\) general messages |  |
| 350 | Yes | Yes | Official | [Mapping of Airline Traffic over Internet Protocol](https://en.wikipedia.org/wiki/Mapping_of_Airline_Traffic_over_Internet_Protocol) \(MATIP\) type A |  |
| 351 | Yes | Yes | Official | MATIP type B |  |
| 356 | Yes | Yes | Official | cloanto-net-1 \(used by Cloanto Amiga Explorer and VMs\) |  |
| 366 | Yes | Yes | Official | On-Demand Mail Relay \(ODMR\) |  |
| 369 | Yes | Yes | Official | Rpc2portmap |  |
| 370 | Yes | Yes | Official | codaauth2, Coda authentication server |  |
|  | Yes | Official | securecast1, outgoing packets to [NAI](https://en.wikipedia.org/wiki/McAfee)'s SecureCast servers. As of 2000 |  |  |
| 371 | Yes | Yes | Official | ClearCase albd |  |
| 383 | Yes | Yes | Official | HP data alarm manager |  |
| 384 | Yes | Yes | Official | A Remote Network Server System |  |
| 387 | Yes | Yes | Official | AURP \([AppleTalk](https://en.wikipedia.org/wiki/AppleTalk) Update-based Routing Protocol\) |  |
| 388 | Yes | Assigned | Official | [Unidata LDM](https://en.wikipedia.org/wiki/Local_Data_Manager) near real-time data distribution protocol |  |
| 389 | Yes | Assigned | Official | [Lightweight Directory Access Protocol](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol) \(LDAP\) |  |
| 399 | Yes | Yes | Official | [Digital Equipment Corporation](https://en.wikipedia.org/wiki/Digital_Equipment_Corporation) [DECnet+](https://en.wikipedia.org/w/index.php?title=DECnet%2B&action=edit&redlink=1) \(Phase V\) over TCP/IP \(RFC1859\) |  |
| 401 | Yes | Yes | Official | [Uninterruptible power supply](https://en.wikipedia.org/wiki/Uninterruptible_power_supply) \(UPS\) |  |
| 427 | Yes | Yes | Official | [Service Location Protocol](https://en.wikipedia.org/wiki/Service_Location_Protocol) \(SLP\)[\[10\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-apple-kb-HT202944-10) |  |
| 433 | Yes | Yes | Official | NNSP, part of [Network News Transfer Protocol](https://en.wikipedia.org/wiki/Network_News_Transfer_Protocol) |  |
| 434 | Yes | Yes | Official | [Mobile IP](https://en.wikipedia.org/wiki/Mobile_IP) Agent \([RFC 5944](https://tools.ietf.org/html/rfc5944)\) |  |
| 443 | Yes | Assigned | Official | [Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \([HTTPS](https://en.wikipedia.org/wiki/HTTPS)\) | Yes |
| No | Yes | Unofficial | [Quick UDP Internet Connections](https://en.wikipedia.org/wiki/QUIC) \(QUIC\), a transport protocol over UDP \(still in draft as of July 2018\), using stream [multiplexing](https://en.wikipedia.org/wiki/Multiplexing), encryption by default with [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security), and currently supporting [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2). |  |  |
| 444 | Yes | Yes | Official | [Simple Network Paging Protocol](https://en.wikipedia.org/wiki/Simple_Network_Paging_Protocol) \(SNPP\), [RFC 1568](https://tools.ietf.org/html/rfc1568) |  |
| 445 | Yes | Yes | Official | Microsoft-DS \(Directory Services\) [Active Directory](https://en.wikipedia.org/wiki/Active_Directory), Windows shares |  |
| Yes | Assigned | Official | Microsoft-DS \(Directory Services\) [SMB](https://en.wikipedia.org/wiki/Server_Message_Block) file sharing |  |  |
| 464 | Yes | Yes | Official | [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) Change/Set password |  |
| 465 | Yes | No | Official | URL Rendezvous Directory for SSM \(Cisco protocol\)\[[importance?](https://en.wikipedia.org/wiki/Wikipedia:What_Wikipedia_is_not#Encyclopedic_content)\] |  |
| Yes | No | Official | Authenticated [SMTP](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \([SMTPS](https://en.wikipedia.org/wiki/SMTPS)\) |  |  |
| 475 | Yes | Yes | Official | tcpnethaspsrv, [Aladdin Knowledge Systems](https://en.wikipedia.org/wiki/Aladdin_Knowledge_Systems) Hasp services |  |
| 491 | Yes |  | Unofficial | [GO-Global remote access and application publishing software](https://en.wikipedia.org/wiki/GO-Global) |  |
| 497 | Yes | Yes | Official | [Retrospect](https://en.wikipedia.org/wiki/Retrospect_%28software%29) |  |
| 500 | Assigned | Yes | Official | [Internet Security Association and Key Management Protocol](https://en.wikipedia.org/wiki/Internet_Security_Association_and_Key_Management_Protocol) \(ISAKMP\) / [Internet Key Exchange](https://en.wikipedia.org/wiki/Internet_Key_Exchange) \(IKE\) |  |
| 502 | Yes | Yes | Official | [Modbus](https://en.wikipedia.org/wiki/Modbus) Protocol |  |
| 504 | Yes | Yes | Official | [Citadel](https://en.wikipedia.org/wiki/Citadel/UX), multiservice protocol for dedicated clients for the Citadel groupware system |  |
| 510 | Yes | Yes | Official | FirstClass Protocol \(FCP\), used by [FirstClass](https://en.wikipedia.org/wiki/FirstClass) client/server groupware system |  |
| 512 | Yes |  | Official | [Rexec](https://en.wikipedia.org/wiki/Remote_Process_Execution), Remote Process Execution |  |
|  | Yes | Official | comsat, together with [biff](https://en.wikipedia.org/wiki/Biff_%28Unix%29) |  |  |
| 513 | Yes |  | Official | [rlogin](https://en.wikipedia.org/wiki/Rlogin) |  |
|  | Yes | Official | Who |  |  |
| 514 | Yes |  | Unofficial | [Remote Shell](https://en.wikipedia.org/wiki/Remote_Shell), used to execute non-interactive commands on a remote system \(Remote Shell, rsh, remsh\) |  |
| No | Yes | Official | [Syslog](https://en.wikipedia.org/wiki/Syslog), used for system logging |  |  |
| 515 | Yes | Assigned | Official | [Line Printer Daemon](https://en.wikipedia.org/wiki/Line_Printer_Daemon_protocol) \(LPD\),[\[10\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-apple-kb-HT202944-10) print service |  |
| 517 |  | Yes | Official | Talk |  |
| 518 |  | Yes | Official | NTalk |  |
| 520 | Yes |  | Official | efs, extended file name server |  |
|  | Yes | Official | [Routing Information Protocol](https://en.wikipedia.org/wiki/Routing_Information_Protocol) \(RIP\) |  |  |
| 521 |  | Yes | Official | [Routing Information Protocol Next Generation](https://en.wikipedia.org/wiki/RIPng) \(RIPng\) |  |
| 524 | Yes | Yes | Official | [NetWare Core Protocol](https://en.wikipedia.org/wiki/NetWare_Core_Protocol) \(NCP\) is used for a variety things such as access to primary NetWare server resources, Time Synchronization, etc. |  |
| 525 |  | Yes | Official | Timed, [Timeserver](https://en.wikipedia.org/wiki/Timeserver) |  |
| 530 | Yes | Yes | Official | [Remote procedure call](https://en.wikipedia.org/wiki/Remote_procedure_call) \(RPC\) |  |
| 532 | Yes | Assigned | Official | netnews |  |
| 533 |  | Yes | Official | netwall, For Emergency Broadcasts |  |
| 540 | Yes |  | Official | Unix-to-Unix Copy Protocol \([UUCP](https://en.wikipedia.org/wiki/UUCP)\) |  |
| 542 | Yes | Yes | Official | [commerce](https://en.wikipedia.org/wiki/Commerce) \(Commerce Applications\) |  |
| 543 | Yes |  | Official | klogin, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) login |  |
| 544 | Yes |  | Official | kshell, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) Remote shell |  |
| 546 | Yes | Yes | Official | [DHCPv6](https://en.wikipedia.org/wiki/DHCPv6) client |  |
| 547 | Yes | Yes | Official | [DHCPv6](https://en.wikipedia.org/wiki/DHCPv6) server |  |
| 548 | Yes | Assigned | Official | [Apple Filing Protocol](https://en.wikipedia.org/wiki/Apple_Filing_Protocol) \(AFP\) over [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) |  |
| 550 | Yes | Yes | Official | new-rwho, new-who |  |
| 554 | Yes | Yes | Official | [Real Time Streaming Protocol](https://en.wikipedia.org/wiki/Real_Time_Streaming_Protocol) \(RTSP\) |  |
| 556 | Yes |  | Official | Remotefs, [RFS](https://en.wikipedia.org/wiki/Remote_File_System), rfs\_server |  |
| 560 |  | Yes | Official | rmonitor, Remote Monitor |  |
| 561 |  | Yes | Official | monitor |  |
| 563 | Yes | Yes | Official | [NNTP](https://en.wikipedia.org/wiki/NNTP) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(NNTPS\) |  |
| 564 | Yes |  | Unofficial | [9P](https://en.wikipedia.org/wiki/9P_%28protocol%29) \([Plan 9](https://en.wikipedia.org/wiki/Plan_9_from_Bell_Labs)\) |  |
| 585 | Port 993 | ? | Unofficial | Legacy use of [Internet Message Access Protocol](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(IMAPS\), now in use at port 993. |  |
| 587 | Yes | Assigned | Official | [email message submission](https://en.wikipedia.org/wiki/Mail_submission_agent) \([SMTP](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol)\) |  |
| 591 | Yes |  | Official | [FileMaker](https://en.wikipedia.org/wiki/FileMaker) 6.0 \(and later\) Web Sharing \(HTTP Alternate, also see port 80\) |  |
| 593 | Yes | Yes | Official | HTTP RPC Ep Map, [Remote procedure call](https://en.wikipedia.org/wiki/Remote_procedure_call) over [Hypertext Transfer Protocol](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol), often used by [Distributed Component Object Model](https://en.wikipedia.org/wiki/Distributed_Component_Object_Model) services and [Microsoft Exchange Server](https://en.wikipedia.org/wiki/Microsoft_Exchange_Server) |  |
| 601 | Yes |  | Official | Reliable [Syslog](https://en.wikipedia.org/wiki/Syslog) Service — used for system logging |  |
| 604 | Yes |  | Official | TUNNEL profile, a protocol for [BEEP](https://en.wikipedia.org/wiki/BEEP) [peers](https://en.wikipedia.org/wiki/Peer-to-peer) to form an [application layer](https://en.wikipedia.org/wiki/Application_layer) [tunnel](https://en.wikipedia.org/wiki/Tunneling_protocol) |  |
| 623 |  | Yes | Official | ASF Remote Management and Control Protocol \(ASF-RMCP\) & IPMI Remote Management Protocol |  |
| 625 | Yes | No | Unofficial | Open Directory Proxy \(ODProxy\) |  |
| 631 | Yes | Yes | Official | [Internet Printing Protocol](https://en.wikipedia.org/wiki/Internet_Printing_Protocol) \(IPP\) |  |
| Yes | Yes | Unofficial | [Common Unix Printing System](https://en.wikipedia.org/wiki/Common_Unix_Printing_System) \(CUPS\) administration console \(extension to IPP\) |  |  |
| 635 | Yes | Yes | Official | RLZ DBase |  |
| 636 | Yes | Assigned | Official | [Lightweight Directory Access Protocol](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(LDAPS\) |  |
| 639 | Yes | Yes | Official | MSDP, [Multicast Source Discovery Protocol](https://en.wikipedia.org/wiki/Multicast_Source_Discovery_Protocol) |  |
| 641 | Yes | Yes | Official | SupportSoft Nexus Remote Command \(control/listening\), a proxy gateway connecting remote control traffic |  |
| 643 | Yes | Yes | Official | SANity |  |
| 646 | Yes | Yes | Official | [Label Distribution Protocol](https://en.wikipedia.org/wiki/Label_Distribution_Protocol) \(LDP\), a routing protocol used in [MPLS](https://en.wikipedia.org/wiki/Multiprotocol_Label_Switching) networks |  |
| 647 | Yes |  | Official | [DHCP Failover](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol#Reliability) protocol |  |
| 648 | Yes |  | Official | Registry Registrar Protocol \(RRP\) |  |
| 651 | Yes | Yes | Official | IEEE-MMS |  |
| 653 | Yes | Yes | Official | SupportSoft Nexus Remote Command \(data\), a proxy gateway connecting remote control traffic |  |
| 654 | Yes |  | Official | Media Management System \(MMS\) Media Management Protocol \(MMP\) |  |
| 655 | Yes | Yes | Official | [Tinc](https://en.wikipedia.org/wiki/Tinc_%28protocol%29) VPN daemon |  |
| 657 | Yes | Yes | Official | [IBM](https://en.wikipedia.org/wiki/IBM) RMC \(Remote monitoring and Control\) protocol, used by [System p5](https://en.wikipedia.org/wiki/IBM_System_p) [AIX](https://en.wikipedia.org/wiki/IBM_AIX) Integrated Virtualization Manager \(IVM\) and [Hardware Management Console](https://en.wikipedia.org/wiki/IBM_Hardware_Management_Console) to connect managed [logical partitions \(LPAR\)](https://en.wikipedia.org/wiki/LPAR) to enable dynamic partition reconfiguration |  |
| 660 | Yes | Assigned | Official | [Mac OS X Server](https://en.wikipedia.org/wiki/Mac_OS_X_Server) administration, version 10.4 and earlier |  |
| [666](https://en.wikipedia.org/wiki/Number_of_the_Beast) | Yes | Yes | Official | [Doom](https://en.wikipedia.org/wiki/Doom_%28game%29), first online [first-person shooter](https://en.wikipedia.org/wiki/First-person_shooter) |  |
| Yes |  | Unofficial | [airserv-ng](http://www.aircrack-ng.org/doku.php?id=airserv-ng), [aircrack-ng](https://en.wikipedia.org/wiki/Aircrack-ng)'s server for remote-controlling wireless devices |  |  |
| 674 | Yes |  | Official | [Application Configuration Access Protocol](https://en.wikipedia.org/wiki/Application_Configuration_Access_Protocol) \(ACAP\) |  |
| 688 | Yes | Yes | Official | REALM-RUSD \(ApplianceWare Server Appliance Management Protocol\) |  |
| 690 | Yes | Yes | Official | Velneo Application Transfer Protocol \(VATP\) |  |
| 691 | Yes |  | Official | [MS](https://en.wikipedia.org/wiki/Microsoft) [Exchange](https://en.wikipedia.org/wiki/Microsoft_Exchange_Server) Routing |  |
| 694 | Yes | Yes | Official | [Linux-HA](https://en.wikipedia.org/wiki/Linux-HA) high-availability heartbeat |  |
| 695 | Yes |  | Official | [IEEE](https://en.wikipedia.org/wiki/IEEE) Media Management System over [SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(IEEE-MMS-SSL\) |  |
| 698 |  | Yes | Official | [Optimized Link State Routing](https://en.wikipedia.org/wiki/Optimized_Link_State_Routing_protocol) \(OLSR\) |  |
| 700 | Yes |  | Official | [Extensible Provisioning Protocol](https://en.wikipedia.org/wiki/Extensible_Provisioning_Protocol) \(EPP\), a protocol for communication between [domain name registries](https://en.wikipedia.org/wiki/Domain_name_registry) and [registrars](https://en.wikipedia.org/wiki/Domain_name_registrar) \([RFC 5734](https://tools.ietf.org/html/rfc5734)\) |  |
| 701 | Yes |  | Official | Link Management Protocol \(LMP\), a protocol that runs between a pair of [nodes](https://en.wikipedia.org/wiki/Node_%28networking%29) and is used to manage [traffic engineering](https://en.wikipedia.org/wiki/Teletraffic_engineering) \(TE\) [links](https://en.wikipedia.org/wiki/Telecommunications_link) |  |
| 702 | Yes |  | Official | IRIS \(Internet Registry Information Service\) over [BEEP](https://en.wikipedia.org/wiki/BEEP) \(Blocks Extensible Exchange Protocol\)[\[99\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-99) \([RFC 3983](https://tools.ietf.org/html/rfc3983)\) |  |
| 706 | Yes |  | Official | [Secure Internet Live Conferencing](https://en.wikipedia.org/wiki/SILC_%28protocol%29) \(SILC\) |  |
| 711 | Yes |  | Official | [Cisco](https://en.wikipedia.org/wiki/Cisco) Tag Distribution Protocol being replaced by the MPLS [Label Distribution Protocol](https://en.wikipedia.org/wiki/Label_Distribution_Protocol) |  |
| 712 | Yes |  | Official | [Topology Broadcast based on Reverse-Path Forwarding routing protocol](https://en.wikipedia.org/wiki/Topology_Broadcast_based_on_Reverse-Path_Forwarding_routing_protocol) \(TBRPF; [RFC 3684](https://tools.ietf.org/html/rfc3684)\) |  |
| 749 | Yes | Yes | Official | [Kerberos \(protocol\)](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) administration |  |
| 750 |  | Yes | Official | kerberos-iv, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) version IV |  |
| 751 | Yes | Yes | Unofficial | kerberos\_master, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) authentication |  |
| 752 |  | Yes | Unofficial | passwd\_server, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) password \(kpasswd\) server |  |
| 753 | Yes | Yes | Official | Reverse Routing Header \(RRH\)[\[104\]](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers#cite_note-104) |  |
|  | Yes | Unofficial | userreg\_server, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) userreg server |  |  |
| 754 | Yes | Yes | Official | tell send |  |
| Yes |  | Unofficial | krb5\_prop, [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) v5 slave propagation |  |  |
| 760 | Yes | Yes | Unofficial | krbupdate \[kreg\], [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29) registration |  |
| 782 | Yes |  | Unofficial | [Conserver](https://en.wikipedia.org/wiki/Conserver) serial-console management server |  |
| 783 | Yes |  | Unofficial | [SpamAssassin](https://en.wikipedia.org/wiki/SpamAssassin) spamd daemon |  |
| 800 | Yes | Yes | Official | mdbs-daemon |  |
| 802 | Yes | Yes | Official | [MODBUS](https://en.wikipedia.org/wiki/Modbus)/TCP Security |  |
| 808 | Yes |  | Unofficial | Microsoft Net.TCP Port Sharing Service |  |
| 829 | Yes | Assigned | Official | [Certificate Management Protocol](https://en.wikipedia.org/wiki/Certificate_Management_Protocol) |  |
| 830 | Yes | Yes | Official | [NETCONF](https://en.wikipedia.org/wiki/NETCONF) over [SSH](https://en.wikipedia.org/wiki/Secure_Shell) |  |
| 831 | Yes | Yes | Official | NETCONF over [BEEP](https://en.wikipedia.org/wiki/BEEP) |  |
| 832 | Yes | Yes | Official | NETCONF for [SOAP](https://en.wikipedia.org/wiki/SOAP) over [HTTPS](https://en.wikipedia.org/wiki/HTTPS) |  |
| 833 | Yes | Yes | Official | NETCONF for SOAP over [BEEP](https://en.wikipedia.org/wiki/BEEP) |  |
| 843 | Yes |  | Unofficial | [Adobe Flash](https://en.wikipedia.org/wiki/Adobe_Flash) |  |
| 847 | Yes |  | Official | [DHCP Failover](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol#Reliability) protocol |  |
| 848 | Yes | Yes | Official | Group Domain Of Interpretation \(GDOI\) protocol |  |
| 853 | Yes | Yes | Official | [DNS](https://en.wikipedia.org/wiki/Domain_Name_System) over [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) \([RFC 7858](https://tools.ietf.org/html/rfc7858)\) |  |
| 860 | Yes |  | Official | [iSCSI](https://en.wikipedia.org/wiki/ISCSI) \([RFC 3720](https://tools.ietf.org/html/rfc3720)\) |  |
| 861 | Yes | Yes | Official | OWAMP control \([RFC 4656](https://tools.ietf.org/html/rfc4656)\) |  |
| 862 | Yes | Yes | Official | TWAMP control \([RFC 5357](https://tools.ietf.org/html/rfc5357)\) |  |
| 873 | Yes |  | Official | [rsync](https://en.wikipedia.org/wiki/Rsync) file synchronization protocol |  |
| 888 | Yes |  | Unofficial | cddbp, [CD DataBase](https://en.wikipedia.org/wiki/CD_database) \([CDDB](https://en.wikipedia.org/wiki/CDDB)\) protocol \(CDDBP\) |  |
| Yes |  | Unofficial | IBM Endpoint Manager Remote Control |  |  |
| 897 | Yes | Yes | Unofficial | [Brocade](https://en.wikipedia.org/wiki/Brocade_Communications_Systems) SMI-S RPC |  |
| 898 | Yes | Yes | Unofficial | Brocade SMI-S RPC SSL |  |
| 902 | Yes | Yes | Unofficial | [VMware ESXi](https://en.wikipedia.org/wiki/VMware_ESXi) |  |
| 903 | Yes |  | Unofficial | VMware ESXi |  |
| 953 | Yes | Reserved | Official | [BIND](https://en.wikipedia.org/wiki/BIND) remote name daemon control \(RNDC\) |  |
| 981 | Yes |  | Unofficial | Remote HTTPS management for firewall devices running embedded [Check Point VPN-1](https://en.wikipedia.org/wiki/Check_Point_VPN-1) software |  |
| 987 | Yes |  | Unofficial | [Microsoft Remote Web Workplace](https://en.wikipedia.org/wiki/Microsoft_Remote_Web_Workplace), a feature of [Windows Small Business Server](https://en.wikipedia.org/wiki/Windows_Small_Business_Server) |  |
| 989 | Yes | Yes | Official | [FTPS](https://en.wikipedia.org/wiki/FTPS) Protocol \(data\), [FTP](https://en.wikipedia.org/wiki/FTP) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) |  |
| 990 | Yes | Yes | Official | [FTPS](https://en.wikipedia.org/wiki/FTPS) Protocol \(control\), [FTP](https://en.wikipedia.org/wiki/FTP) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) |  |
| 991 | Yes | Yes | Official | [Netnews](https://en.wikipedia.org/wiki/Netnews) Administration System \(NAS\) |  |
| 992 | Yes | Yes | Official | [Telnet](https://en.wikipedia.org/wiki/Telnet) protocol over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) |  |
| 993 | Yes | Assigned | Official | [Internet Message Access Protocol](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(IMAPS\) |  |
| 994 | Reserved | Reserved | Official |  |  |
| Maybe | Maybe | Unofficial | [Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat) over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(IRCS\). Previously assigned, but not used in common practice. |  |  |
| 995 | Yes | Yes | Official | [Post Office Protocol](https://en.wikipedia.org/wiki/Post_Office_Protocol) 3 over [TLS/SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) \(POP3S\) |  |
| 1010 | Yes |  | Unofficial | [ThinLinc](https://en.wikipedia.org/wiki/ThinLinc) web-based administration interface |  |
| 1011–1020 | Reserved | Reserved | Official |  |  |
| 1023 | Reserved | Reserved | Official |  |  |
| Yes | Yes | Unofficial | [z/OS](https://en.wikipedia.org/wiki/Z/OS) Network File System \(NFS\) \(potentially ports 991–1023\) |  |  |

