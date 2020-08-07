# Different Types of Security Testing

### What is a Penetration Test? 

Let's define pen testing as simulating attacks against your computer systems networks to check for vulnerabilities that a malicious attacker might exploit. 

Penetration tests have different areas of focus. \(i.e Web Application Penetration testing against a Web Application Firewall such as Imperva\).

### What are the Phases of Hacking/Pen-testing? 

Security testing is an iterative process that should be repeated following 5 steps:

1. Reconnaissance - Identify Business Presence and digital infrastructure - Can be Passive or Active depending on the methods employed to obtain the data. Passive involves gathering information about a target without their knowledge. Active involves taking significant action to signify others that we are watching. i.e social engineering, dumpster diving and network sniffing. 
2. Scanning and Enumeration - Describe applications supporting target environment and identify versions as well as possible misconfigurations and vulnerabilities. Can be a SQL injection, a buffer overflow or any other abuse of a service. 
3. Exploitation/Gaining Access - Attacks against the systems previously identified as vulnerable might be as easy as running a Metasploit module or as obscure as obfuscating shell-code in the payload sent to a target.
4. Maintaining Access/Privilege Escalation - After gaining an initial perch on the system we aim to control the highest privileges and permissions available - We want to become \#_**root**._ For this phase it is essential to identify as much information as possible about the target system. We iterate and perform previous Recon, Scanning, Vulnerability Assessment on the system hoping to find a way to go from a low-privileged user to **NT Authority/System**. The attacker leaves malware in the machine that allows them to access the target at a later time or remotely control it turning the machine into a zombie for the purpose of joining it to a botnet. Common methods include Trojans, rootkits, etc...
5. Covering Tracks/Anti-Forensic Measures - Focus is on avoiding detection, clearing logs that account for the intrusion, removal of artifacts that might be discovered and perhaps even hiding files, corruption of the logs, etc... 

### 3 Main Phases of a Penetration Test 

1. Preparation - Scope definition and contractual obligation
2. Assessment Phase - Security Evaluation
3. Conclusion/Post-Assessment - Final Reporting

### _Types of Hackers - pending_

### _Security Policies- pending_

### _CIA Triad- pending_

### Blackbox Testing - Closed Box

Implies there is no internal knowledge of the components and its aim is to simulate the adversaries that would be attacking our system from outside. 

Tester is not given network topologies, security architecture insider information nor credentials to access. 

Requires the highest level of skill on part of the attacker as they must find their way through the security controls. 

Downside is that assessment of internal controls largely depends on the attackers ability to circumvent defenses. 

### Gray Testing - _Venetian Blinds testing?_ 

This type of testing relies on potential escalation of privileges avenues on a system. Attacker starts from the perspective of a user with operator level access on the system. 

Provides a more efficient approach to security testing since the attacker might focus their efforts in a higher value target direction as more information is available than in a pure Blackbox test. 

This type of testing is suitable to analyze the impact of an attacker's long term presence on the environment. 

### Whitebox Testing - Open Box

Completely opposite from black box testing. 

Penetration tester is given full access to the source code of the application being tested as well as the ability to perform static analysis on the code. 

Prioritization is essential in this type of assessment. Full access to the environment is an advantage only when we know what to focus our efforts on as attackers. 

Massive amounts of information can be useful only when we know _which_ information to use. 

