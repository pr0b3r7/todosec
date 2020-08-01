---
description: 'Here are the next topics you can expect to see content about:'
---

# What is NEXT?!

* PCI-DSS; SOX Act; COBIT; ISO/IEC 27001:2013; HIPAA; FISMA, Patriot Act, Privacy Act of 1974, Cyber Intelligence Sharing and Protection Act \(CISPA\), Consumer Data Security and Notification Act and Computer Security Act of 1987.
* Blackbox/Opaque vs Whitebox/Clear testing vs Gray/_Translucid?_ testing \(limited knowledge about target - privilege escalation from _trusted insider_ scenario\); Phases of Hacking/Pen-testing; What is a Penetration Test?, 3 Main Phases, and Scope.;  Types of Hackers according to their **intent;** Security Policies; CIA Triad
* Annualized Loss Expectancy \(ALE\), Annual Rate of Occurrence \(ARO\) and SLE \(Single Loss Expectancy\). Exposure Factor \(EF\) and how to obtain SLE \(EF x Value of Asset\); Risk Management steps, Control types. Business Impact Analysis, Maximum Tolerable Downtime \(MTD\). Business Continuity Plan \(BCP\), Disaster Recovery Plan \(DRP\).
* Security, Functionality and Usability triangle, zero day attack, payload, exploit, daisy-chaining, bots, doxing, incident response... 
* Social Engineering, email tracking, web spidering and other footprinting such as Google Hacking/Dorks; Business Intelligence/Marketing Tools/Financial Data
* DNS Foot-printing; _name-server, record types_ and possible _operations_
* What is footprinting?
* Vulnerability Research, exploit news, zero-days, [National Vulnerability Database](https://nvd.nist.gov/), [Securitytracker](http://www.securitytracker.com/), [Hackerstorm Vulnerability Database Tool,](http://www.hackerstorm.com/) [Security Focus](http://www.securityfocus.com/) **\(Add More\)**
* **SMTP - Simple Mail Transfer Protocol** - VRFY \(Verify User\), EXPN \(Provides the actual delivery addresses of mailing lists and aliases\), RCPT TO \(which defines recipients\), types of responses to each request from the servers; Lack of encryption; authentication via user ID + password transmitted in plaintext. 
* Network Time Protocol \(123/UDP\) - Queries can reveal internal infrastructure components information. Tools such as NTP Server Scanner, AtomSync, nmap, Wireshark. ntptrace, ntpdc, ntpq. 
* Lightweight Directory Access Protocol \(LDAP\), _made_ to be queried. Sessions are started on 389/TCP connecting to DSA \(Directory System Agent\). Request queries the hierarchical/logical structure in LDAP DB and returns a BER \(Basic Encoding Rules\) answer. usernames, domain info, addresses and phone numbers as well as organizational data. Softerra, JXplorer, Lex, LDAP Admin Tool, AD MS. 
* SNMP - community strings as passwords. Read-only version of the community string allows read over a wide surface of information. Read-write controls access for SNMP SET requests; SNMPv1, NNTP, IMAP and POP3 send their passwd over plaintext as well. 
* NETBIOS - MS Windows - TCP; nbstat provides enumeration vector - code and types
* Banner grabbing - methods
* SIDs, domain/computer indicator, RID. Windows password storage; Linux UID, GID similarities and differences with MS Windows SIDs and RIDs. 
* Vulnerability scanning
* Anonymize your traffic via the use of web proxies - guardster, ultrasurf, Psiphon, and Tails \(Lin Distro\)
* Tor clients, directory servers. Process of random connections and its encryption
* Different proxies and methods to disguise source of traffic. Proxy chains. Proxy Switcher, Workbench, Proxy Chains, Soft-cab's Proxy Chain Builder, and Proxifier.
* Source routing as a method to determine the routing path to a destination \(overriding the routing tables of network infrastructure devices in said path\)
* Spoofing an IP address, packet crafting tools: Hping, Scapy, and Komodia.
* Packet Fragmentation, in hopes of evading an IDS that theoretically would not pick up on other than seemingly disconnected traffic that in reality could be reassembled on the client machine as a malicious payload; nmap can also run scans fragmenting packets. 
*  Hping2,3 - ping sweeping, port scanning, packet-crafting tool \(TCP/IP\)
* Nmap port scanning, vulnerability scanning, nmapAutomator 
* Ping sweeping - how to do it in Python, [Bash](network-and-systems/topics/code/code-bash/ping-sweeping-with-bash.md)
* Definition of Scanning 
* Definition of Sniffing, honeypot,  HTTP tunneling evasion technique; session splicing/fragmentation; types of sniffing; same collision domain sniffing - passive sniffing; definition of a collision domain; method to sniff on a collision domain \(promiscuous mode NIC\); 
* Difference between packet filtering firewalls, stateful multilayer inspection firewalls; purpose of the firewall, methods of work; rule-sets and their role; [Zone-based Firewall](network-and-systems/topics/network/zone-based-policy-firewall-also-known-as-zone-policy-firewall-or-zfw.md); what is a multi-homed device.
* Snort; rules; purpose; method of action; syntax; modes; raw output manipulation \(regex?\); arrows; Snort configuration in Linux and Windows; features; modes of operation.
* False positives, false negatives. Host based IDS; Network based IDS; IDS Definition; methods, signature list; behavior based detection, _lib-whisker_ PERL library for HTTP functions, vuln scanning, exploitation and IDS evasion. 
* Use of Wireshark, filters syntax; how to display HTTP, TCP, follow TCP conversation
* MAC Spoofing; definition, goal, IRDP spoofing = attacker floods ICMP Router Discovery Protocol messages through the network to redirect traffic to a determined gateway; DNS poisoning and similarities with ARP poisoning; ARP poisoning; definition; defenses on modern devices \(DHCP snooping and Dynamic ARP Inspection in the case of IOS\). Tools to prevent it include XArp; OS level mitigation includes static configuration of default gateway MAC address via _arp -s_ command. ARP flooding tools: Cain and Abel; WinArpAttacker; Ufasoft and dnsniff \(linux tools collection including ARPspoof\); ARP exchange steps - ARP\_REQUEST, ARP\_REPLY; How gratuitous ARP messages are offered before the hosts asks for them; MAC flooding; definition; method; effect, filling up content addressable memory \(CAM\) table.
* DHCP starvation; definition; [DHCP Protocol](network-and-systems/topics/network/dhcp.md); DHCP Messages. Yersinia, DHCPstarv; Rogue DHCP servers, + DHCP starvation could allow redirection determined by the attacker. 
* FTP - user ID + passwd authentication --&gt; anonymous accounts, plaintext credentials; TFTP - all data in clear-text - can be sniffed raw. 
* Microsoft Windows - storage of authentication credentials, passwd hashing; SAM file location; method of passwd storage is vulnerable due to low complexity; Windows 2000, NT LAN Manager, to hash passwds. Windows Vista. NTLMv2; Kerberos; KDC, Authentication Service; Ticket Granting Service TGS and Ticket Granting Ticket \(TGT\).
* Web organizations: IEFT, RFCs \(Request for comments and the most important Networking, Security, and Encryption ones.\) [World Wide Web Consortium \(W3C\)](https://www.w3.org); [OWASP](https://www.owasp.org) is a 501\(c\)\(3\) or non-profit, what does it do, its contributions to web security \([Top 10, ](infosec/topics/recon/web/owasp-top-10.md)being one\), WebGoat \(Vulnerable web application\). 
* Web-servers; what are they, what are the most common and relevant ones such as Apache, Microsoft's IIS; How to configure Apache securely; use of http.conf - this file controls aspects regarding who can view the server status page \(containing information related to server status, the hosts that are connected and the requests that the server is handling; files like php.inf contain information for verbose error messaging setting.  its modules; IIS and the role of Privileges within environments using this web-server, spawning shells with IIS ; Modular character of IIS, its core and modules as well as libraries; Common web-server attack vectors such as: misconfigurations, error messages, default passwords and how to change them, SSL Certificates, scripts, implement appropriate controls on remote administrative functions, configuration files, and eliminating services that are not needed on the machine; default accounts and how to change them;
* N-tier architecture - multilayer architecture; distributing roles across several different servers, each tier consisting of a role mapped to one of more \(in the case of clusters\) of machines. Oftentimes 3 layers are employed: Presentation, Logic and Data tiers as a common implementation but not the only one. 



