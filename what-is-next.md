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
* Lightweight Directory Access Protocol \(LDAP\), _made_ to be queried. Sessions are started on 389/TCP connecting to DSA \(Directory System Agent\). Request queries the hierarchical/logical structure in LDAP DB and returns a BER \(Basic Encoding Rules\) answer. usernames, domain info, addresses and phone numbers as well as organizational data. Softerra, JXplorer, Lex, LDAP Admin Tool, AD MS.; LDAP Injection attack, exploiting applications that use LDAP statements based on user input - done via adding characters \)\(&\) after the username + any passwd provided. 
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
* Web-servers; what are they, what are the most common and relevant ones such as Apache, Microsoft's IIS; How to configure Apache securely; use of http.conf - this file controls aspects regarding who can view the server status page \(containing information related to server status, the hosts that are connected and the requests that the server is handling; files like php.inf contain information for verbose error messaging setting.  its modules; IIS and the role of Privileges within environments using this web-server, spawning shells with IIS ; Modular character of IIS, its core and modules as well as libraries; Common web-server attack vectors such as: misconfigurations attacks, error messages, default passwords and how to change them, SSL Certificates, scripts, implement appropriate controls on remote administrative functions, configuration files, and eliminating services that are not needed on the machine; default accounts and how to change them; Most common attack vectors: Password attacks, Denial of Service DDoS, Man In the Middle \(MiTM or Sniffing\), DNS poisoning \(hijacking\), and phishing. DNS amplification \(how to manipulate recursive DNS to DoS the target.\); Use of a botnet, possible DNS attacks with it.
* N-tier architecture - multilayer architecture; distributing roles across several different servers, each tier consisting of a role mapped to one of more \(in the case of clusters\) of machines. Oftentimes 3 layers are employed: Presentation, Logic and Data tiers as a common implementation but not the only one. 
* HTML entity instructs the browser to display certain characters i.e **&nbsp;** and **&lt;.** HTTP request methods such as GET, HEAD, POST, PUT, DELETE, TRACE, and CONNECT; Proxies ability to modify POST, GET requests; Where can we find each method's traffic \(GET displayed by the browser, POST visible with packet capture\); HTTP HEAD, headers and metadata; Differences with HTTP GET \(does not display body information within the browser\); GET can be used to send data, HOW? What is the downside? \(Data gets added to the URL\); Does POST do this? 
* Directory Traversal, common on older machines \(unauthorized access of restricted directories and execution of commands in directories other than the web-server's; ../ attack or non-validated input attack.; Unicode, what is it? use cases and risks, relationship between HTTP GET and non-validated input - command execution, brute-force of administrative access passwds, etc.; URL Tampering/unauthorized manipulation of parameters within the URL, the goal is to modify settings and achieve escalation of privileges, credentials and potentially business data; Password and SSH brute-forcing; Web defacing/vandalism - unauthorized

  changing appearances of websites

* Use of Metasploit; pre-loaded with Telnet, SSH, and HTTP modules to automatically take advantage of previously published CVEs, perform passwd attacks as well as configure custom payloads; create custom modules \(\), plug-ins and interfaces \(Armitage\); Additionally, Post-exploitation tools such as **multi/handler** are specially useful. 
* Web 1.0 vs Web 2.0 differences - static vs dynamic web page content. \(Better suited for social media\) - Since there are more capabilities built in the websites, more attack surface is also a downside of this evolution. 
* Web Application attacks include: arbitrary command execution via injecting them into the input string, this is possible due to poor input validation in the application; Methods include _file injection \(_attacker injects a pointer in form input to an exploit hosted elsewhere_\)_, _command injection \(_attacker injects commands into the form fields instead of expected test entry_\), shell injection \(_attacker attempts to gain shell access by executing OS commands on the server running the web-app_\)._
* **SOAP injection -** Simple Object Access Protocol \(SOAP\) - Goal is to exchange structured information in web services, uses XML as formatting to present the information. Injection of malicious query strings \(Similar to SQL injection\) - allows authentication bypass and database access in the back-end, compatibility with HTTP and SMTP are usually 1-way.; **Stack smashing, Buffer Overflows attack** - the goal is to overwrite the application's pre-determined memory buffer area, replace what's supposed to be in there and execute arbitrary code or make an application crash; **Cross-site scripting \(XSS\)** - the goal is injection of a script in a form field that had a storage purpose. XSS classic attack vector involves access to "document.cookie" and sending it to the remote hosts; **Cross-site request forgery \(CSRF\)** - attack vector that forces the end user to execute unwanted actions on a web application in which they are authenticated. CSRF makes the target inadvertently submitting a malicious request; **Session fixation attacks**, similar to CSRF, attacker fetches a "session ID" that is sent in a Phishing email to target, when the victim clicks and logs in to the site, the attacker is now able to use the same "session ID" to log in and use the user's access.; _**Cookies**:_ small text file stored on client machine for use by the web server. Contains information such as authentication details, site preferences, shopping cart, in general session details, they can contain _some_ of this data or all. Sent in Header of HTTP response from a web server, may or may not have an expiration date. Goal: provide a stable web view for customers and speed up access for repeated visitors; **HTTP response splitting -** works adding header response data to an input field so the server splits the response in a couple directions. If successful, attacker controls the content of the second header, versatile—i.e redirecting the user to a malicious site the attacker runs.; **SQL \(Structured Query Language\) injection** common and successful injection attack. SQL's goal is: management of data in relational database systems. RDBS are collections of tables \(rows, hold individual fields of data\) tied using a common key, may be updated and queried; Tables have a name, referenced in queries or updates. SQL provides a method to add, delete, move, update, or view the data these tables and fields; SQL queries often begin with SELECT. **SELECT** chooses the data to perform an action on. i.e, **DROP TABLE** _**tablename**_ will delete the table _tablename_. There's also INSERT and UPDATE; SQL injection occurs when attacker injects SQL queries into the input form. The goal is for the SQL command to bypass the front end and the command is executed on the database. To check if a system is vulnerable against SQL injection, check target for login page, instead of entering what’s asked for, try a single quote \(**'**\) and see what kind of error message, if any, it returns. If that doesn’t work, try entering _**anything**_**'or 1=1-** and see what you get. Attack names and definitions for SQL such as union query, tautology, blind SQL injection, and error-based SQL injection; security testing \(hacking\) a web application _sometimes_ is to try using it in a way it wasn’t intended; **Countermeasures for web server and application attacks:** server perimeter and strong patch management; disabling unnecessary services, ports, and protocols; removing outdated, unused accounts and properly configuring default accounts; appropriate file-system permissions and disabling directory listing; ensuring monitoring and incident response are in place; Automated scanners for injection vulnerabilities: Sqlmap, Havij, and sqlninja . SQLBrute \(predefined SQL injection queries\) against a target. Others tools include Pangolin, SQLExec, Absinthe, and BobCat.
* Wireless:  802.11 **standards**... 802.11a - up to 54 Mbps, uses 5 GHz range; 802.11b - 11 Mbps, 2.4 GHz; 802.11g - 54 Mbps, 2.4 GHz;  802.11n  + 100 Mbps, variety of ranges in **MIMO format** 2.4 and 5 GHz; 802.11i \(amendment to 802.11, specifies security mechanisms for the WLAN\); 802.16 \(WiMAX\); 802.11an and 802.11ax are soon to be seen; **Modulation**—manipulating a waveform—encoding in wireless. Orthogonal frequency-division multiplexing \(**OFDM**\) and direct-sequence spread spectrum \(**DSSS**\) use pieces of a waveform to carry a signal. OFDM uses several waveforms: the transmission media is divided into a series of frequency bands that don’t overlap each other, and each of them can then be used to carry a separate signal. DSSS works differently by _combining_ all the available waveforms into a single purpose; the entire frequency bandwidth can be used at once for the delivery of a message; **Wireless Modes**: Ad Hoc Mode, wireless systems connect directly to other systems, as if a cable were strung between the two. Infrastructure mode uses an access point **\(AP\)** to funnel all wireless connections through, and clients associate and authenticate to it. Wireless networks can consist of a single access point or multiple ones, thus creating overlapping cells and allowing a user to roam freely without losing connectivity. The client needs to associate with an access point first and then disassociate when it moves to the next one; When there is a **single access point**, its footprint is called a **basic service area \(BSA\).** Communication between this single AP and its clients is known as a basic service set \(BSS\). If you extend the range of your network by adding multiple access points, the setup is known as an extended service set \(ESS\). As a client moves from one AP in your subnet to another, so long as everything is configured correctly, it’ll disassociate from one AP and \(re\)associate with another seamlessly. This movement across multiple APs within a single ESS is known as **“roaming.”**
* **Type of antennas** used \(omnidirectional antenna - 360 degrees from the source, 

  Directional antennas allow you to focus the signal in a specific direction, which greatly increases signal strength and distance. Other antennas you can use are dipole and parabolic grid. Dipole antennas have, quite obviously, two signal “towers” and work omnidirectionally. Parabolic grid antennas work a lot like satellite dishes and can have phenomenal range \(up to 10 miles\) but aren’t in use much.\), **where** to place them and how to **contain or corral** the signal; Avoid **spillage** and **loss** of **power** of the **signal;** Service set identifier **\(SSID\) identifies** the network. \(text word - 32 characters or less\). Can be hidden through “SSID cloaking” though ineffective since the SSID is part of the header on every packet; WLAN **Authentication**: **Open** System Authentication \(client can simply send an 802.11 authentication frame with the appropriate SSID to an AP and have it answer with a verification frame.\), **Shared Key** Authentication \(the client would participate in a challenge/request scenario, with the AP verifying a decrypted “key” for authentication\), and **Centralized** Authentication \(i.e, RADIUS - An authentication server provides centralized authentication services in the Domain/Network\).  . . _**Association**_ ****is the action of a client connecting to an AP, whereas _**authentication**_ ****identifies the client before it accesses the network.; **WEP,** Wired Equivalent Privacy, weak 40 to 232-bit keys in RC4 encryption, reuses initialization vectors \(IVs\) - sent in clear text as part of the header, are small and, reused, these can be abused to, with enough captured packets, decode the WEP shared key IV; WEP, Aircrack can use a **dictionary** technique, or algorithmic processes called **PTW, FMS**, and the **Korek** technique, **only dictionary** against WPA/WPA2; Cain and Abel and Aircrack \(both use Korek, but Aircrack is faster\) as well as KisMAC, WEPCrack, and Elcomsoft’s Wireless Security Auditor tool; **Wi-Fi Protected Access \(WPA\)** or **WPA2 \(government and the enterprise\)** uses **Temporal Key Integrity Protocol \(TKIP\)**, a **128-bit** key, client’s MAC address much stronger encryption. WPA changes the key out \(“_temporal_ key integrity protocol tkip”\). Keys are exchanged with **Extensible Authentication Protocol \(EAP\)** authentication session, four-step handshake process proving client belongs to AP; **WPA2** _**Enterprise**,_ EAP or a RADIUS server into authentication \(AES for encryption, FIPS 140-2. Integrity, uses the Cipher Block Chaining Message Authentication Code Protocol \(CCMP\), with message integrity codes \(MICs\), process called cipher block chaining message authentication code \(CBC-MAC\), allows use of Kerberos tickets. 

* [AirPcap dongle ](https://www.riverbed.com/document/fpo/AirPcap-Frequently-Asked-Questions.pdf)USB wireless. [WIGLE](http://wigle.net) identifying locations of wireless networks; teams have mapped wireless locations using GPS and a tool called NetStumbler. [NetStumbler](www.netstumbler.com) \(identifying poor coverage locations within an ESS, detecting interference causes, finding any rogue APs. Windows, compatible with 802.11a, b, and g.; **Kismet** - wireless discovery, works on Linux, unlike NetStumbler, works passively, detects APs and clients without sending packets. Can detect default configurations on access points \(out-of-the-box admin password\) will determine encryption on target. “Channel Hops”, has the ability to sniff packets and generate pcaps; NetSurveyor similar to NetStumbler and Kismet —other tools for wireless sniffing include NetStumbler, Kismet, OmniPeek, AirMagnet WiFi Analyzer Pro, and WiFi Pilot; **Wireless Attacks** such as**: rogue AP** \(attacker sets up an access point near legitimate APs and tricks users into associating and authenticating with it - aka - “Evil twin” - aka-  “mis-association attack."\) Faking a well-known hotspot on a rogue AP \(McDonald’s or Starbucks free Wi-Fi spots\) is “honeyspot attack.”; **Denial-of-service;** **Wireless Signal jamming**, using jamming device and, high-gain antenna/amplifier. All wireless devices are susceptible to jamming/interference. 
* [\(OWASP\) - mobile security ](https://www.owasp.org/index.php/OWASP_Mobile_Security_Project)and [Top 10 mobile risks](https://www.owasp.org/index.php/Mobile_Top_10_2016-Top_10).: M1 – Improper Platform Usage, M2 – Insecure Data Storage, M3 – Insecure Communication, M4 – Insecure Authentication, M5 – Insufficient Cryptography, M6 – Insecure Authorization, M7 – Client Code Quality, M8 – Code Tampering, M9 – Reverse Engineering, and M10 – Extraneous Functionality.  ; [Android ](https://www.android.com/)and [iOS](www.apple.com/ios/). By Google for mobile devices, OS + middleware + mobile applications. iOS = Apple’s for mobile \(iPhone and iPad , Apple TV and iPods\). mobile apps + AI voice assistant \(Siri\); Android or iOS system access = rooting/ jailbreaking. Android rooting KingoRoot, [TunesGo](https://tunesgo.wondershare.com), [OneClickRoot,](https://oneclickroot.com) and [MTK Droid.](https://androidmtk.com)  ; jailbreaking tools include: evasi0n7, GeekSn0w, Pangu, Redsn0w, Absinthe, and Cydia. There are three basic techniques and three different types, regardless which tool you want to try. Techniques include **untethered** \(**kernel will remain patched**—jailbroken—after reboot, with or without system connection\), semi-tethered \(reboot no longer retains the patched kernel but the software has already been added to the device; therefore, if admin privileges are required, the installed jailbreaking tool can be used\), and tethered \(reboot removes jailbreak, phone may loop on startup requiring USB, to repair\). **3 types of jailbreak**: Userland \(user access, not admin\), iBoot, and BootROM \(admin access\); Mobile attack vector comes from the apps. Others include social engineering, phishing, and physical security. [Android Device Administration API ](https://developer.android.com/guide/topics/admin/device-admin)system device administration allowing development of security apps.; **BYOD**—Bring Your Own Device—users bring own smartphones, tablets to the network. **Problem is security and control**. Mobile Device Management \(MDM\), like Group Policy, some control to enterprise mobile devices. MDM pushes security policies, application deployment, and monitoring of mobile. MDM offer: passcodes for unlocking, remote locking, remote wipe, root or jailbreak detection, policy enforcement, inventory, and reporting. Some solutions are **XenMobile, IBM MaaS360, AirWatch, and MobiControl.  ; 3G, 4G**, and **Bluetooth** connectivity means to know. Third- and Fourth-gen mobile telecom, broadband-type speeds. Bluetooth open wireless data exchange, short range \(10m &gt;\). **2 modes**: discovery mode and pairing mode. Discovery mode determines device reacts to inquiries, and it has **three actions**. The **discoverable action** obviously has the device answer to all inquiries, **limited discoverable** restricts that action, and **non discoverable** device ignore all inquiries.;  **Discovery** mode device it’s available, **pairing** details how device will react when asked to pair. two versions: yes, and no. **Non Pairable** rejects connection, **pairable** accepts all.; **Attacks** on mobile: **phishing , social engineering**. **SMS phishing -** text messaging; **Trojans,** Android Trojans: Obad, Fakedefender, TRAMP.A, and ZitMo. **Spyware**: Mobile Spy and Spyera, listen or even watch the target. AndroidLost, Find My Phone, and Where’s My Droid designed **find lost phones**, but can be used to track users; Mobile also attack platform. Network Spoofer control how websites appear on a desktop/laptop. DroidSheep perform sidejacking listening to wireless packets and pulling session IDs. Nmap works on mobile device. Kali Linux Nethunter. [NetCut ](www.arcai.com/netcut/)able to identify and drop Wi-Fi for a target  ; **Bluetooth attacks:** Bluesmacking \(denial-of-service\), **Bluejacking** \(unsolicited messages to, and from, mobile devices\), **Bluesniffing** \(discover Bluetooth-like war driving\), **Bluebugging** \(accessing a Bluetooth device remotely\), **Bluesnarfing** \(theft of data from a mobile device due to an open connection—such as remaining in discovery mode\), and **Blueprinting** \(footprinting\).; **IoT architecture \(**three components\)—things using sensing technology, IoT gateways, and the cloud \(or put another way, data storage availability\). A **thing** inside IoT is any device somewhere with ability and purpose of communicating. IoT devices can communicate and interact over the Internet, and can be remotely monitored and controlled. **Sensors** are embedded in the device to measure and forward data.   **IoT OS** include RIOT OS, ARM mbed OS, RealSense OS X, Nucleus RTOS, Brillo, Contiki, Zephyr, Ubuntu Core, Integrity RTOS, and Apache Mynewt. **Four IoT communication models**—**device to device**, **device to gateway** \(adds a collective before sending to cloud, which can be used to offer some security controls\), **device to cloud**, and **back-end data sharing**, is like **device to cloud**; adds third parties to collect and use data.; Once **thing** sensed and collected, forwards data to the IoT gateway. Designed to send collected data from devices to the user or to the third component, data storage or cloud, for use later. Cloud stores and analyzes data, information for future queries. **The Vehicle Ad Hoc Network \(VANET\)** communications used by vehicles. Spontaneous creation of a wireless network for vehicle-to-vehicle \(V2V\) data exchange; **Architecture layers** inside IoT: Edge Technology Layer, Access Gateway Layer, Internet Layer, Middleware Layer, and Application Layer. [IEEE maintains journal IoT](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=6488907), and [ITU - news articles about current IoT efforts.](https://www.itu.int/en/ITU-T/ssc/resources/Pages/topic-001.aspx);   [OWASP Top 10 for IoT](https://www.owasp.org/index.php/Top_IoT_Vulnerabilities); Attacks include: DDoS \(distributed denial of service\), Sybil attack, multiple forged identities create the illusion of traffic congestion in the local network. HVAC attacks in IoT attacks. Hack IoT to shut down air conditioning.

  **"rolling code" and BlueBorne**. key fob unlock code is = rolling/hopping. Attacks sniff for the code by jamming and sniffing it. BlueBorne attack is techniques and attacks against Bluetooth vulnerabilities; [HackRF One](https://greatscottgadgets.com). Mirai malware \(botnets—purpose of DDoS attacks\).   IoT hacking phases: **information gathering, vulnerability scanning, launching attacks, gaining access, and maintaining access**. [Shodan](https://www.shodan.io/). [Censys](https://censys.io) and [Thingful](www.thingful.net); **vulnerability scanning**, \(Nmap, [Beyond Trust, RIoT](https://www.beyondtrust.com/resources/data-sheet/retina-iot-riot-scanner/). [beSTORM](https://www.beyondsecurity.com/bestorm.html), [IoTsploit ](https://iotsploit.com)and [IoT Inspector](www.iot-inspector.com).  ; **launching attacks phase**, [Firmalyzer](https://firmalyzer.com), KillerBee,  [JTAGulator](www.grandideastudio.com), [Attify Zigbee Framework](https://www.attify.com).; Sniffers for IoT traffic include [Foren6](http://cetic.github.io/foren6/), [Z-Wave](www.suphammer.com) and [CloudShark](https://www.cloudshark.org). 

* Virtualization \(started back in the 1960s by companies like General Electric, Bell Labs, and IBM\) is a practice whereby the physical aspects of the hardware are virtually presented to operating systems in a way that allows more than one virtual machine \(with their own operating systems\) to run simultaneously on the same physical box. Cloud computing provides user and enterprise subscribers on-demand delivery of various IT services as a metered service over a network. Cloud computing offers everything from on-demand self-service, storage, and resource pooling to elasticity, automation in management, and broad network access. To further define what exactly it is, we need to consider the three major types of cloud computing—IaaS, PaaS, and SaaS. Cloud computing can be thought of as the ultimate in separation of duties. It moves system services that would otherwise be hosted internally to an external provider. It also separates the role of data owner from the role of data custodian.



  Infrastructure as a Service \(IaaS\) basically provides virtualized computing resources over the Internet. A third-party provider hosts infrastructure components, applications, and services on behalf of its subscribers, with a hypervisor \(such as VMware, Oracle VirtualBox, Xen, or KVM\) running the virtual machines as guests. IaaS is a good choice not just for day-to-day infrastructure service, but also for temporary or experimental workloads that may change unexpectedly. IaaS subscribers typically pay on a per-use basis \(within a certain timeframe, for instance, or sometimes by the amount of virtual machine space used\).



  Platform as a Service \(PaaS\) is geared toward software development, as it provides a development platform that allows subscribers to develop applications without building the infrastructure it would normally take to develop and launch software. Hardware and software are hosted by the provider on its own infrastructure so customers do not have to install or build homegrown hardware and software for development work. PaaS doesn’t usually replace an organization’s actual infrastructure; instead, it just offers key services the organization may not have onsite.



  Software as a Service \(SaaS\) is simply a software distribution model—the provider offers on-demand applications to subscribers over the Internet. SaaS benefits include easier administration, automated patch management, compatibility, and version control.



  Along with the types of cloud, there are four main deployment models: public, private, community, and hybrid. A public cloud model is one where services are provided over a network that is open for public use \(like the Internet\). A private cloud model is, not surprisingly, private in nature. The cloud is operated solely for a single organization \(a.k.a. single-tenant environment\) and is usually not a pay-as-you-go operation. A community cloud model is one where the infrastructure is shared by several organizations, usually with the same policy and compliance considerations. A hybrid cloud model is exactly what it sounds like—a composition of two or more cloud deployment models.



  NIST \(National Institutes of Standards and Technology\) released Special Publication 500-292: NIST Cloud Computing Reference Architecture to provide a “fundamental reference point to describe an overall framework that can be used government wide.” This publication defined five major roles within a cloud architecture: cloud carrier \(the organization that has the responsibility of transferring the data; that is, the intermediary for connectivity and transport between subscriber and provider\), cloud consumer \(the individual or organization that acquires and uses cloud products and services\), cloud provider \(the purveyor of products and services\), cloud broker \(acts to manage use, performance, and delivery of cloud services, as well as the relationships between providers and subscribers\), and cloud auditor \(an independent assessor of cloud service and security controls\).



  FedRAMP is probably the most recognized and referenced regulatory effort regarding cloud computing. The Federal Risk and Authorization Management Program \(FedRAMP\) is a government-wide program that provides a standardized approach to security assessment, authorization, and continuous monitoring for cloud products and services. FedRAMP not only provides an auditable framework for ensuring basic security controls for any government cloud effort, but also offers weekly tips for security and configuration and even has free training available on the site. PCI Data Security Standard \(PCI DSS\) Cloud Special Interest Group’s Cloud Computing Guidelines also provides notables assistance and information for the cloud.



  The Cloud Security Alliance \(CSA\) is the leading professional organization devoted to promoting cloud security best practices and organizing cloud security professionals. In addition to providing a certification on cloud security and offering an array of cloud-centric training, they published a general cloud enterprise architecture model to help professionals conceptualize the components of a successful cloud implementation. They also publish documentation on everything from privacy concerns to security controls, focus, and implementation.



  Cloud security is really talking about two sides of the same coin—you must be concerned with the security of the provider as well as that of the subscriber. Both the provider and subscriber are responsible for security. Using virtualization introduces a hypervisor layer between the physical hardware and subscribed servers. Therefore, if you comprise the hypervisor, you compromise them all.



  The Trusted Computing Model refers to an attempt to resolve computer security problems through hardware enhancements and associated software modifications. The Trusted Computing Group \(TCG\) is made up of a bunch of hardware and software providers who cooperate to come up with specific plans. Roots of Trust \(RoT\) is a set of functions within the Trusted Computing Model that are always trusted by the computer’s operating system \(OS\).



  Tools to assist in cloud security include CloudInspect and CloudPassage Halo. Core’s CloudInspect is “a tool that profits from the Core Impact & Core Insight technologies to offer penetration-testing as a service from Amazon Web Services for EC2 users.” It’s designed for AWS cloud subscribers and runs as an automated, all-in-one testing suite specifically for your cloud subscription. CloudPassage’s Halo “provides instant visibility and continuous protection for servers in any combination of data centers, private clouds and public clouds. The Halo platform is delivered as a service, so it deploys in minutes and scales on-demand. Halo uses minimal system resources, so layered security can be deployed where it counts, right at every workload—servers, instances and containers.” Other cloud-specific tools and toolsets mentioned include Dell Cloud Manager, Qualys Cloud Suite, Trend Micro’s Instant-On Cloud Security, and Panda Cloud Office Protection.



  Cloud Security Alliance released a publication titled “The Dirty Dozen: 12 Top Cloud Security Threats” \(also referred to as “The Treacherous 12”\) and EC-Council has its own list of top threats. Important ones to remember include:



  •   Data breach or loss   The malicious theft, erasure, or modification of almost anything in the cloud you can think of. While cloud providers deploy their own tools, methods, and controls to protect their overall environment, it’s generally and ultimately up to the subscribers themselves to protect their own data in the cloud. CSA recommends multifactor authentication and encryption as protection against data breaches.



  •   Abuse of cloud resources   If attackers can create anonymous access to cloud services, they could then leverage the tremendous resources to do whatever they want. Typically this threat isn’t necessarily a specific concern of cloud subscribers, but it’s a very valid concern for the provider. The provider should perform active monitoring to detect any abuse instances as well as have a means to protect/recover from them. Generally speaking, threats of abuse of cloud services apply to the IaaS and PaaS models.



  •   Insecure interfaces and APIs   Cloud services rely heavily on APIs and web services to function and operate, and without them, functions like auto-scaling, authentication, authorization, and sometimes the operations of cloud applications themselves will fail. Insecure interfaces and APIs can circumvent user-defined policies and really mess around with input data verification efforts. Both provider and subscriber should ensure strong security controls are in place, such as strong encryption and authorization access to APIs and connectivity. This threat applies to all models of cloud.



  Other threats mentioned that warrant inclusion in our discussion are insufficient due diligence \(for example, moving an application from one cloud environment to another and not knowing the security differences between the two\), shared technology issues \(multitenant environments may not provide proper isolation between systems and applications\), and unknown risk profiles \(subscribers simply do not know exactly what security provisions are made in the background of and by the provider\). Many others, such as malicious insiders, inadequate design, and DDoS are valid for both cloud services and traditional data centers.



  SOAP \(Simple Object Access Protocol\) is an API that makes it easier for application components to cooperate and exchange information on systems connected over a network. A wrapping attack occurs when a SOAP message is intercepted and the data in the envelope is changed and then sent/replayed.



  In addition to every other attack mentioned previously in this book, two that ECC mentions explicitly are session riding and side channel attacks. Session riding is simply CSRF under a different name and deals with cloud services instead of traditional data centers. Side channel attacks, also known as a cross-guest VM breach, deal with the virtualization itself: if an attacker can somehow gain control of an existing VM \(or place his own\) on the same physical host as the target, he may be able to attempt a litany of attacks and efforts.

* Malware is generally defined as software designed to harm or secretly access a computer system without the owner’s informed consent. Some states also define malware as computer contaminant. Malvertising involves embedding malware into ad networks in an effort to throw malware across many legitimate sites. Other definition terms of note include overt channels \(legitimate communication channels used by programs across a system or a network\) and covert channels \(used to transport data in unintended ways\).



  Most malware is simply downloaded from the Internet with or without the user’s knowledge. Sometimes legitimate sites get compromised, leading to infections on visiting systems. Other times drive-by downloading infects the system, usually via some weird Java vulnerability delivered through an ad stream or something like it. Peer-to-peer applications or web application “features” are often hijacked to distribute malware, and an IRC channel is always a great way to distribute malware. Sending malware \(usually a Trojan\) via e-mail, file sharing, or a browser is also a good distribution method.



  Wrappers are programs that allow you to bind an executable of your choice \(Trojan\) to an innocent file your target won’t mind opening. EliteWrap is an example. Crypters are software tools that use a combination of encryption, obfuscation, and code manipulation to render malware as undetectable to AV and other security-monitoring products. Exploit kit examples include Infinity, Bleeding Life, Crimepack, and Blackhole Exploit Kit.



  A Trojan is software that appears to perform a desirable function for the user prior to running or installing it but instead performs a function, usually without the user’s knowledge, that steals information or otherwise harms the system \(or data\). Although a backdoor isn’t a Trojan, and a Trojan isn’t a backdoor, they’re tied together in this discussion and on your exam: the Trojan is the means of delivery, and the backdoor provides the open access.



  Trojan types include defacement Trojans, proxy server Trojans, botnet Trojans \(Tor-based Chewbacca and Skynet\), remote access Trojans \(RAT, MoSucker, Optix Pro, and Blackhole\), and e-banking Trojans \(Zeus and Spyeye\). Covert Channel Tunneling Trojan \(CCTT\) is one form of remote access Trojan that uses a variety of exploitation techniques to create data transfer channels in previously authorized data streams. It’s designed to provide an external shell from within the internal environment.



  A command shell Trojan is intended to provide a backdoor to the system that you connect to via command-line access. Netcat is known as the “Swiss Army knife” of TCP/IP hacking and provides all sorts of control over a remote shell on a target. Netcat can be used for outbound or inbound connections, over TCP or UDP, to or from any port on the machine. It offers DNS forwarding, port mapping and forwarding, and proxying. You can even use it as a port scanner if you’re really in a bind.



  Port numbers in use by Trojans should be memorized for your exam:



  Images



  Netstat will show all connections in one of several states—everything from SYN\_SEND \(indicating active open\) to CLOSED \(the server has received an ACK from the client and closed the connection\). Fport is a free tool from McAfee that reports all open TCP/IP and UDP ports and maps them to the owning applications. Process Explorer is a free tool from Microsoft \(formerly from SysInternals\) that can tell you almost anything you’d want to know about a running process. Some of the options for monitoring the registry are SysAnalyzer, Tiny Watcher, Active Registry Monitor, and Regshot.



  Windows will automatically run everything located in Run, RunServices, RunOnce, and RunServicesOnce, and you’ll find that most questions on the exam are centered around or show you settings from HKEY\_LOCAL\_MACHINE.



  A virus is a self-replicating program that reproduces its code by attaching copies into other executable codes. In other words, viruses create copies of themselves in other programs, then activate on some sort of trigger event \(such as a specific user task, a particular time, or an event of some sort\). One method for getting viruses onto a system is known as a virus hoax or fake antivirus. The process involves letting a target know about a terrible virus running rampant through the world, then providing them an antivirus program \(or signature file\) to protect themselves with.



  Here are the virus types for exam memorization:



  •   Ransomware   This malware locks you out of your own system resources and demands an online payment of some sort in order to release them back to you. The ransomware “family” includes examples such as Cryptorbit, CryptoLocker, CryptoDefense, and police-themed. Specific versions to know include WannaCry and Petya.



  •   Boot sector virus   Also known as a system virus, this virus type actually moves the boot sector to another location on the hard drive, forcing the virus code to be executed first.



  •   Shell virus   Working just like the boot sector virus, this virus type wraps itself around an application’s code, inserting its own code before the application’s. Every time the application is run, the virus code is run first.



  •   Cluster virus   This virus modifies directory table entries so that user or system processes are pointed to the virus code itself instead of the application or action intended.



  •   Multipartite virus   Attempts to infect both files and the boot sector at the same time. This generally refers to a virus with multiple infection vectors.



  •   Macro virus   Usually written with Visual Basic for Applications \(VBA\), this virus type infects template files created by Microsoft Office, normally Word and Excel.



  •   Polymorphic code virus   This virus type mutates its code using a built-in polymorphic engine. These viruses are difficult to find and remove because their signatures constantly change. No part of the virus stays the same from infection to infection.



  •   Encryption virus   Shockingly, these viruses use encryption to hide the code from antivirus scanners.



  •   Metamorphic virus   This virus type rewrites itself every time it infects a new file.



  •   Stealth virus   Also known as a “tunneling virus,” this one attempts to evade antivirus \(AV\) applications by intercepting the AV’s requests to the operating system \(OS\) and returning them to itself instead of OS.



  •   Cavity virus   Cavity viruses overwrite portions of host files so as not to increase the actual size of the file. This is done using the null content sections of the file and leaves the file’s actual functionality intact.



  •   Sparse infector virus   This virus type only infects occasionally.



  •   File extension virus   These viruses change the file extensions of files to take advantage of most people having file extension view turned off.



  A worm is a self-replicating malware computer program that uses a computer network to send copies of itself to other systems without human intervention. Usually it doesn’t alter files, but it resides in active memory and duplicates itself, eating up resources and wreaking havoc along the way. The most common use for a worm in the hacking world is the creation of botnets. “Ghost Eye Worm” is a hacking tool that uses random messaging on Facebook and other sites to perform malicious actions. Other worms include the following:



  •   Code Red   Exploited indexing software on IIS servers in 2001.



  •   Darlloz   The worm for the “Internet of Things,” darlloz is a Linux-based worm that targets running ARM, MIPS, and PowerPC architectures.



  •   Slammer   Also known as SQL Slammer, this was a denial-of-service worm attacking buffer overflow weaknesses in Microsoft SQL Services.



  •   Nimda   A successful file infection virus that modified and touched nearly all web content on a machine.



  •   Bug Bear   Propagating over open network shares and e-mail, Bug Bear terminated AV applications and set up a backdoor for later use.



  •   Pretty Park   Pretty Park spread via e-mail \(attempting a send every 30 minutes\) and took advantage of IRC to propagate stolen passwords and the like.



  Tools like binText and UPX can help in malware analysis. Others that can help are IDA Pro \(www.hex-rays.com\), VirusTotal \(www.virustotal.com\), Anubis \(Anubis.iseclab.org\), and Threat Analyzer \(www.threattracksecurity.com\).



  The standard DoS attack seeks to accomplish nothing more than taking down a resource or denying access to it by authorized users. The distributed denial-of-service \(DDoS\) attack comes not from one system but many, and they’re usually part of a botnet. The botnet is a network of zombie computers the hacker can use to start a distributed attack from \(examples of botnet software/Trojans are Shark and Poison Ivy\). For study purposes, the preferred communications channel used to signal the bots is IRC or Internet Chat Query \(ICQ\). Another way of saying “botnet” may be the distributed reflection denial of service \(DRDoS\) attack, also known as a spoof attack. It uses multiple intermediary machines to pull off the denial of service, by having the secondary machine send the attack at the behest of the attacker. The attacker remains hidden because the attack appears to originate from the secondary machine.



  ECC lists four basic categories of Dos/DDoS as well as several examples of DoS/DDoS attacks. The categories are as follows:



  •   Fragmentation attacks   These attacks take advantage of the system’s ability \(or lack thereof\) to reconstruct fragmented packets.



  •   Volumetric attacks   Also known as bandwidth attacks, these consume all available bandwidth for the system or service.



  •   Application attacks   These attacks consume resources necessary for the application to run, effectively making it unavailable to others.



  •   TCP state-exhaustion attacks   These attacks go after load balancers, firewalls, and application servers by attempting to consume their connection state tables.



  Here’s a short list of attacks, with all the salient information you’ll need:



  •   SYN attack   The hacker will send thousands upon thousands of SYN packets to the machine with a false source IP address. The machine will attempt to respond with a SYN/ACK but will be unsuccessful \(because the address is false\). Eventually, all the machine’s resources are engaged, and it becomes a giant paperweight.



  •   SYN flood   In this attack, the hacker sends thousands of SYN packets to the target but never responds to any of the return SYN/ACK packets. Because there is a certain amount of time the target must wait to receive an answer to the SYN/ACK, it will eventually bog down and run out of available connections.



  •   ICMP flood   Here, the attacker sends ICMP Echo packets to the target with a spoofed \(fake\) source address. The target continues to respond to an address that doesn’t exist and eventually reaches a limit of packets per second sent.



  •   Smurf   The attacker sends a large number of pings to the broadcast address of the subnet, with the source IP spoofed to that of the target. The entire subnet will then begin sending ping responses to the target, exhausting the resources there. A fraggle attack is similar but uses UDP for the same purpose.



  •   Ping of death   \(This isn’t a valid attack with modern systems, but is still a definition you may need to know.\) In the ping of death, an attacker fragments an ICMP message to send to a target. When the fragments are reassembled, the resultant ICMP packet is larger than the maximum size and crashes the system.



  •   Teardrop   In a teardrop attack, a large number of garbled IP fragments with overlapping, oversized payloads are sent to the target machine. On older operating systems \(such as Windows 3.1x, Windows 95, and Windows NT operating systems\), this takes advantage of weaknesses in the fragment reassembly functionality of their TCP/IP stack, causing the system to crash or reboot.



  •   Peer to peer   In this attack, clients of a peer-to-peer file-sharing hub are disconnected and directed to connect with the target system.



  •   Permanent   Phlashing refers to a DoS attack that causes permanent damage to a system. Usually this includes damage to the hardware and can also be known as bricking a system.



  The real answer to a true DDoS is the involvement of your ISP up channel. It will be next to impossible for you, at an endpoint locale, to keep up with attacks from a sophisticated global, or even geographically close, botnet. The ISP may wind up blocking a lot of legitimate traffic too, but it may be all you can do until the storm passes.



  In session hijacking, an attacker waits for a session to begin and, after all the pesky authentication gets done, jumps in to steal the session for himself. The server isn’t even aware of what happened, and the client simply connects again in a different session. The following more completely describes the session hijack steps \(per EC-Council\):



  1.   Sniff the traffic between the client and the server.



  2.   Monitor the traffic and predict the sequence numbering.



  3.   Desynchronize the session with the client.



  4.   Predict the session token and take over the session.



  5.   Inject packets to the target server.



  You’ll need to remember that the sequence numbers increment on acknowledgment. Additionally, you’ll almost certainly get asked a scenario version of sequence numbering. You’ll need to know, given an acknowledgment number and a window size, what sequence number would be acceptable to the system. For example, an acknowledgment of 105 with a window size of 200 means you could expect sequence numbering from 105 through 305.



  IPSec is used to secure IP communication by providing encryption and authentication services to each packet, and it has several architectural components you’ll need to know. First, IPSec works in two modes. In transport mode, the payload and ESP trailer are encrypted; however, the IP header of the original packet is not. Transport can be used in network address translation \(NAT\) because the original packet is still routed in exactly the same manner as it would have been without IPSec. Tunnel mode, however, encrypts the whole thing, encapsulating the entire original packet in a new IPSec shell. This makes it incompatible with NAT. The rest of IPSec architecture includes the following protocols:



  •   Authentication Header   AH is a protocol within IPSec that guarantees the integrity and authentication of the IP packet sender.



  •   Encapsulating Security Payload   ESP is a protocol that also provides origin authenticity and integrity, but it can take care of confidentiality \(through encryption\) too. ESP does not provide integrity and authentication for the entire IP packet in transport mode, but in tunnel mode protection is provided to the entire IP packet.



  •   Internet Key Exchange   IKE is the protocol that produces the keys for the encryption process.



  •   Oakley   A protocol that uses Diffie-Hellman to create master and session keys.



  •   Internet Security Association Key Management Protocol Software that facilitates encrypted communication between two endpoints

* Cryptography is the science or study of protecting information, whether in transit or at rest, by using techniques to render the information unusable to anyone who does not possess the means to decrypt it. Plain-text data \(something you can read\) is turned into cipher-text data \(something you can’t read\) by the application of some form of encryption. Encrypting data provides confidentiality because only those with the “key” can see it. Integrity can also be provided by hashing algorithms. Nonrepudiation is the means by which a recipient can ensure the identity of the sender and that neither party can deny having sent or received the message.



  Encryption algorithms—mathematical formulas used to encrypt and decrypt data—are highly specialized and complex. There are two methods in which the algorithms actually work, and there are two methods by which keys can be used and shared. In stream ciphers, bits of data are encrypted as a continuous stream. In other words, readable bits in their regular pattern are fed into the cipher and are encrypted one at a time. These work at a high rate of speed. Block ciphers combine data bits into blocks and feed them into the cipher. Each block of data, usually 64 bits at a time, is then encrypted with the key and algorithm. These ciphers are considered simpler, and slower, than stream ciphers.



  Symmetric encryption, also known as single key or shared key, simply means one key is used both to encrypt and to decrypt the data. It is considered fast and strong but poses some significant weaknesses. It’s a great choice for bulk encryption because of its speed, but key distribution is an issue because the delivery of the key for the secured channel must be done offline. Additionally, scalability is a concern because as the network gets larger, the number of keys that must be generated goes up exponentially. DES, 3DES, Advanced Encryption Standard \(AES\), International Data Encryption Algorithm \(IDEA\), Twofish, and Rivest Cipher \(RC\) are examples.



  Asymmetric encryption comes down to this: what the one key encrypts, the other key decrypts. It’s important to remember the public key is the one used for encryption, whereas the private key is used for decryption. Either can be used for encryption or decryption within the pair, but in general remember public = encrypt, private = decrypt. Asymmetric encryption can provide both confidentiality and nonrepudiation and solves the problems of key distribution and scalability. The weaknesses include its performance \(asymmetric is slower than symmetric, especially on bulk encryption\) and processing power \(asymmetric usually requires a much longer key length, so it’s suitable for smaller amounts of data\). Diffie-Hellman, Elliptic Curve Cryptosystem \(ECC\), El Gamal, and RSA are examples.



  A hashing algorithm is a one-way mathematical function that takes an input and produces a single number \(integer\) based on the arrangement of the data bits in the input. It provides a means to verify the integrity of a piece of data—change a single bit in the arrangement of the original data, and you’ll get a different response. The attack or effort used against a hashing algorithm is known as a collision or a collision attack. A collision occurs when two or more files create the same output, which is not supposed to happen. To protect against collision attacks and the use of rainbow tables, you can also use a salt, which is a collection of random bits used as a key in addition to the hashing algorithm. MD5, SHA-1, SHA-2, and SHA-3 are examples of hash algorithms.



  Steganography is the practice of concealing a message inside a text, image, audio, or video file in such a way that only the sender and recipient even know of its existence, let alone the manner in which to decipher it. Indications of steganography include character positions \(in text files, look for text patterns, unusual blank spaces, and language anomalies\) and large file sizes and color palette faults in image files. Audio and video files require some statistical analysis and specific tools.



  In image steganography, there are three main techniques: least significant bit insertion, masking and filtering, and algorithmic transformation. Masking hides the data in much the same way as a watermark on a document; however, it’s accomplished by modifying the luminescence of image parts. Algorithmic transformation allows steganographers to hide data in the mathematical functions used in image compression. Tools like OmniHide Pro and Masker do a good job of sticking messages into the video stream smoothly and easily. DeepSound and MP3Stego are both tools for audio steganography. Other tools include QuickStego \(quickcrypto.com\), gifshuffle and SNOW \(darkside.com.au\), Steganography Studio \(stegstudio.sourceforge.net\), and OpenStego \(www.openstego.info\).



  PKI is a structure designed to verify and authenticate the identity of individuals within the enterprise taking part in a data exchange. It can consist of hardware, software, and policies that create, manage, store, distribute, and revoke keys and digital certificates. The system starts at the top, with a \(usually\) neutral party known as the certificate authority \(CA\) that creates and issues digital certificates. The CA also keeps track of all the certificates within the system and maintains a certificate revocation list \(CRL\), used to track which certificates have problems and which have been revoked. The CA may be internal to begin with, and there could be any number of subordinate CAs—known as registration authorities \(RAs\)—to handle things internally \(most root CAs are removed from network access to protect the integrity of the system\). In many PKI systems, an outside entity known as a validation authority \(VA\) is used to validate certificates—usually done via Online Certificate Status Protocol \(OCSP\). A certificate authority can be set up to trust a CA in a completely different PKI through something called cross-certification. This allows both PKI CAs to validate certificates generated from either side.



  CAs work in a trust model. This describes how entities within an enterprise deal with keys, signatures, and certificates, and there are three basic models. In the web of trust, multiple entities sign certificates for one another. In other words, users within this system trust each other based on certificates they receive from other users on the same system. A single authority system has a CA at the top that creates and issues certificates. Users trust each other based on the CA. The hierarchical trust system also has a CA at the top \(which is known as the root CA\) but makes use of one or more registration authorities \(subordinate CAs\) underneath it to issue and manage certificates. This system is the most secure because users can track the certificate back to the root to ensure authenticity without a single point of failure.



  A digital certificate is an electronic file that is used to verify a user’s identity, providing nonrepudiation throughout the system. The certificate typically follows the X.509 standard, which defines what should and should not be in a digital certificate. Version, Serial Number, Subject, Algorithm ID \(or Signature Algorithm\), Issuer, Valid From and Valid To, Key Usage, Subject’s Public Key, and Optional are all fields within a digital certificate.



  A self-signed certificate is one created and signed by the entity internally and never intended to be used in any other situation or circumstance. Signed certificates generally indicate a CA is involved and the signature validating the identity of the entity is confirmed via an external source—in some instances a validation authority \(VA\). Signed certificates, as opposed to self-signed certificates, can be trusted: assuming the CA chain is validated and not corrupted, it’s good everywhere.



  A digital signature is nothing more than an algorithmic output that is designed to ensure the authenticity \(and integrity\) of the sender. FIPS 186-2 specifies that the Digital Signature Algorithm \(DSA\) be used in the generation and verification of digital signatures. DSA is a Federal Information Processing Standard that was proposed by the National Institute of Standards and Technology \(NIST\) in August 1991 for use in their Digital Signature Standard \(DSS\). The steps in the use of a digital signature include the hashing of the message, with the result of the hash being encrypted by the sender’s private key. The recipient then decrypts the hash result using the sender’s public key, verifying the sender’s identity.



  Data at rest \(DAR\) is data that is in a stored state and not currently accessible. Protection of data on mobile devices from loss or theft while it is in a resting state usually entails full disk encryption \(FDE\), where pre-boot authentication \(usually an account and password\) is necessary to “unlock” the drive before the system can even boot up. FDE can be software or hardware based, and can use network-based authentication \(Active Directory, for example\) and/or local authentication sources \(a local account or locally cached from a network source\). Software-based FDE can even provide central management, making key management and recovery actions much easier.



  Tools helpful in encrypting files and folders for other protective services include Microsoft Encrypted File Systems \(EFS\), VeraCrypt, AxCrypt, and GNU Privacy Guard. The point is, full disk encryption may sound like a great idea in the boardroom, but once the drive is unlocked, the data inside is not protected.



  Encrypted communication methods include the following:



  •   Secure Shell \(SSH\)   A secured version of Telnet, using TCP port 22, by default, and relying on public key cryptography for its encryption.



  •   Secure Sockets Layer \(SSL\)   Encrypts data at the transport layer and above, for secure communication across the Internet. It uses RSA encryption and digital certificates and can be used with a wide variety of upper-layer protocols. SSL uses a six-step process for securing a channel.



  •   Transport Layer Security \(TLS\)   Uses an RSA algorithm of 1024 and 2048 bits; TLS is the successor to SSL.



  •   Internet Protocol Security \(IPSec\)   Network layer tunneling protocol that can be used in two modes: tunnel \(entire IP packet encrypted\) and transport \(data payload encrypted\).



  •   PGP \(Pretty Good Privacy\)   Used for signing, compression, and encrypting and decrypting e-mails, files, directories, and even whole disk partitions, mainly in an effort to increase the security of e-mail communications.



  Heartbleed and POODLE were successful attacks against secure communications. Heartbleed exploits the heartbeat feature in OpenSSL, which tricks the server into sending 64Kb of data from its memory. You can use the nmap command nmap -d --script ssl-heartbleed --script-args vulns.showall -sV \[host\] to search for the vulnerability: the return will say “State: NOT VULNERABLE” if you’re good to go. The Metasploit auxiliary module openssl\_heartbleed can be used to exploit this. Open SSL versions 1.0.1 and 1.0.1f are vulnerable, and the CVE notation is CVE-2014-0160.



  POODLE \(Padding Oracle On Downgraded Legacy Encryption\) took advantage of backward-compatibility features in TLS clients, allowing sessions to drop back to the vulnerable SSL 3.0, which has a design flaw that allows the padding data at the end of a block cipher to be changed so that the encryption cipher becomes less secure each time it is passed. Defined as “RC4 biases,” if the same secret is sent over several sessions, more and more information about it will leak. Mitigation for POODLE is to not use SSL 3.0 at all. You can implement TLS\_FALLBACK\_SCSV \(a fake cipher suite advertised in the Client Hello message, which starts the SSL/TLS handshake\) on areas that must remain backward compatible. Another mitigation is to implement something called “anti-POODLE record splitting.” In short, this splits records into several parts, ensuring none of them can be attacked. However, although this may frustrate the exploit’s ability to gather data, it also may cause compatibility issues due to problems in server-side implementations.



  Cipher attacks fall into a few categories and types. Known plain-text attacks, cipher-text-only attacks, and replay attacks are examples. Man-in-the-middle is usually listed as a type of attack by many security professionals and study guides \(depending on the test version you get, it may even be listed as such\). Just keep in mind that a man-in-the-middle situation simply means the attacker has positioned himself between the two communicating entities. Brute force refers to an attempt to try every possible combination against a target until successful.

* Social engineering is the art of manipulating a person, or a group of people, into providing information or a service they otherwise would never have given. Social engineers prey on people’s natural desire to help one another, their tendency to listen to authority, and their trust of offices and entities. ECC defines four phases of successful social engineering:



  1.   Research \(dumpster dive, visit websites, tour the company, and so on\).



  2.   Select the victim \(identify frustrated employee or other promising targets\).



  3.   Develop a relationship.



  4.   Exploit the relationship \(collect sensitive information\).



  Social engineering is a nontechnical method of attacking systems, which means it’s not limited to people with technical know-how. EC-Council defines five main reasons and four factors that allow social engineering to happen. Human nature \(to trust others\), ignorance of social engineering efforts, fear \(of consequences of not providing the requested information\), greed \(promised gain for providing requested information\), and a sense of moral obligation are all reasons people fall victim to social engineering attacks. As for the factors that allow these attacks to succeed, insufficient training, unregulated information \(or physical\) access, complex organizational structure, and lack of security policies all play roles.



  All social engineering attacks fall into one of three categories: human based, computer based, or mobile based. Human-based social engineering uses interaction in conversation or other circumstances between people to gather useful information.



  Dumpster diving is digging through the trash for useful information. Although technically a physical security issue, dumpster diving is covered as a social engineering topic per EC-Council. Impersonation is a name given to a huge swath of attack vectors. Basically the social engineer pretends to be someone or something he or she is not, and that someone or something—like, say, an employee, a valid user, a repairman, an executive, a help desk person, or an IT security expert—is someone or something the target either respects, fears, or trusts. Pretending to be someone you’re not can result in physical access to restricted areas \(providing further opportunities for attacks\), not to mention any sensitive information \(including the credentials\) your target feels you have a need and right to know. Using a phone during a social engineering effort is known as “vishing.”



  Shoulder surfing and eavesdropping are other valuable human-based social engineering methods. An attacker taking part in shoulder surfing simply looks over the shoulder of a user and watches them log in, access sensitive data, or provide valuable steps in authentication. This can also be done “long distance,” using vision-enhancing devices like telescopes and binoculars.



  Tailgating occurs when an attacker has a fake badge and simply follows an authorized person through the opened security door. Piggybacking is a little different in that the attacker doesn’t have a badge but asks for someone to let her in anyway. If you see an exam question listing both tailgating and piggybacking, the difference between the two comes down to the presence of a fake ID badge \(tailgaters have them, piggybackers don’t\). On questions where they both do not appear as answers, the two are used interchangeably.



  Reverse social engineering is when the attacker poses as some form of authority or technical support and sets up a scenario whereby the user feels he must dial in for support. Potential targets for social engineering are referred to as “Rebecca” or “Jessica.” When you’re communicating with other attackers, the terms can provide information on whom to target—for example, “Rebecca, the receptionist, was very pleasant and easy to work with.” Disgruntled employees and insider attacks present the greatest risk to an organization.



  Computer-based attacks are those attacks carried out with the use of a computer. Attacks include specially crafted pop-up windows, hoax e-mails, chain letters, instant messaging, spam, and phishing. Social networking and spoofing sites or access points also belong in the mix.



  Most likely the simplest and most common method of computer-based social engineering is known as phishing. A phishing attack involves crafting an e-mail that appears legitimate but in fact contains links to fake websites or to download malicious content. Another version of this attack is known as spear phishing. Whereas a phishing attack usually involves a mass-mailing of a crafted e-mail in hopes of snagging some unsuspecting reader, spear phishing is a targeted attack against an individual or a small group of individuals within an organization. Spear phishing usually is a result of a little reconnaissance work that has churned up some useful information. Options that can help mitigate against phishing include the Netcraft Toolbar and the PhishTank Toolbar.



  Setting up multiple layers of defense, including change-management procedures and strong authentication measures, is a good start in social engineering mitigation. Other physical and technical controls can also be set up, but the only real defense against social engineering is user education.



  Mobile social engineering attacks are those that take advantage of mobile devices—that is, applications or services in mobile devices—in order to carry out their end goal. ZitMo \(ZeuS-in-the-Mobile\) is a piece of malware for Android phones that exploits an already-owned PC to take control of a phone in order to steal credentials and two-factor codes. EC-Council defines four categories of mobile-based social engineering attacks: publishing malicious apps, repackaging legitimate apps, fake security applications, and SMS \(per EC-Council, this is known as “smishing”\).



  Physical security is perhaps one of the most overlooked areas in an overall security program. Physical security includes the plans, procedures, and steps taken to protect your assets from deliberate or accidental events that could cause damage or loss. Physical security measures come down to three major components: physical, technical, and operational. Physical measures include all the things you can touch, taste, smell, or get shocked by. Technical measures are measures taken with technology in mind to protect explicitly at the physical level. Operational measures are the policies and procedures you set up to enforce a security-minded operation. Access controls are physical measures designed to prevent access to controlled areas. They include biometric controls, identification/entry cards, door locks, and mantraps. FRR, FAR, and CER are important biometric measurements. False rejection rate \(FRR\) is the percentage of time a biometric reader will deny access to a legitimate user. The percentage of time that an unauthorized user is granted access by the system, known as false acceptance rate \(FAR\), is the second major factor. These are usually graphed on a chart, and the intercepting mark, known as crossover error rate \(CER\), becomes a ranking method to determine how well the system functions overall.



  The mantrap, designed as a pure physical access control, provides additional control and screening at the door or access hallway to the controlled area. In the mantrap, two doors are used to create a small space to hold a person until appropriate authentication has occurred. The user enters through the first door, which must shut and lock before the second door can be cleared. Once inside the enclosed room, which normally has clear walls, the user must authenticate through some means—biometric, token with PIN, password, and so on—to open the second door.

* Security assessments can be one of two types: a security audit \(vulnerability assessment\) or a penetration test. The security audit scans and tests a system or network for existing vulnerabilities but does not intentionally exploit any of them. This assessment is designed to uncover potential security holes in the system and report them to the client for their action. It does not fix or patch vulnerabilities, nor does it exploit them. It only points them out for the client’s benefit.



  A penetration test actively seeks to exploit vulnerabilities encountered on target systems or networks. This shows the potential consequences of a hacker breaking in through unpatched vulnerabilities. Penetration tests are carried out by highly skilled individuals according to an agreement signed before testing begins. This agreement spells out the limitations, constraints, and liabilities between the organization and the penetration test team.



  Penetration tests consist of two types of assessment: external and internal. An external assessment analyzes publicly available information and conducts network scanning, enumeration, and testing from the network perimeter—usually from the Internet. An internal assessment is performed from within the organization, from various network access points.



  Black-box testing occurs when the attacker has no prior knowledge of the infrastructure at all \(your scope is defined, and you’ll be provided the minimal amount of information required\). This testing takes the longest to accomplish and simulates a true outside hacker. White-box testing simulates an internal user who has complete knowledge of the company’s infrastructure. Gray-box testing provides limited information on the infrastructure. Sometimes gray-box testing is born out of a black-box test that determines more knowledge is needed.



  Testing can also be further broken down according to the way it is accomplished. Automated testing uses an all-inclusive toolset. Automated tools can provide plenty of information and many legitimate results for a lesser price than manual testing with a full test team. However, they are also susceptible to false positives and false negatives and don’t always stop where they’re supposed to \(software can’t read your agreement contract\). Manual testing is the best choice for security assessment. It requires good planning, design, and scheduling, and it provides the best benefit to the client. Manual testing is accomplished by a pen test team, following the explicit guidelines laid out before the assessment.



  There are three main phases to a pen test. In the pre-attack phase, reconnaissance and data-gathering efforts are accomplished. Gathering competitive intelligence, identifying network ranges, checking network filters for open ports, and so on, are all carried out in this phase. Running whois, DNS enumeration, finding the network IP address range, and network scanning are all examples of tasks in this phase.



  Attempting to penetrate the network perimeter, acquire targets, execute attacks, and elevate privileges are steps taken in the attack phase. Verifying ACLs by crafting packets, checking to see whether you can use any covert tunnels inside the organization, and using XSS, buffer overflows, and SQL injections are all examples of tasks performed in this phase. After acquiring specific targets, you’ll move into password cracking and privilege escalation, using a variety of methods. Finally, once you’ve gained access, it’s time to execute your attack code.



  The post-attack phase consists of two major steps. The first step involves cleaning up your testing efforts. Anything that has been uploaded to the organization’s systems in the way of files or folders needs to be removed. Any tools, malware, backdoors, or other attack software loaded on the client’s systems need to be taken off. Any registry changes you’ve made need to be reset to their original settings. The goal of this phase is to return everything to the pre-test state.



  The second step involves writing the pen test report, due after all testing is complete. The pen test report should contain the following items:



  •   An executive summary of the organization’s overall security posture. \(If you’re testing under the auspices of FISMA, DIACAP, HIPAA, or some other standard, this will be tailored to the standard.\)



  •   The names of all participants and the dates of all tests.



  •   A list of findings, usually presented in order of highest risk.



  •   An analysis of each finding and the recommended mitigation steps \(if available\).



  •   Log files and other evidence from your toolset.

