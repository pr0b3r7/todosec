---
description: WINDOWS 'Plumbing'
---

# Windows Basic Networking

Displays all connections and listening ports '-a' and ... Displays addresses and port numbers in numerical form '-n' and ... Displays TCP connection template for all connections '-y' \(table style - Proto - Local Address - Foreign Address - State - Template\) find or findstr to filter output

```text
netstat –yan | find “8080” 
netstat –yan | findstr “22” 
```

Filter and show only TCP protocol

```text
netstat –yanp tcp
```

Filter and show only UDP protocol

```text
netstat –yanp udp -a
```

PING ICMP Statistics

```text
netstat -s -p icmp
```

### Powershell

Test Connection with Powershell:

```text
Test-NetConnection -ComputerName www.google.com -InformationLevel Detailed
```

Ping multiple IP using PowerShell

```text
1..99 | % { Test-NetConnection -ComputerName 192.168.1.$_ } | FT -AutoSize
```

Tracert with PowerShell

```text
Test-NetConnection www.domain.com –TraceRoute
```

Use PowerShell to check for open port

```text
Test-NetConnection -ComputerName www.domain.com -Port 80
```

Alternative syntax for port

```text
Test-NetConnection -ComputerName www.domain.com -CommonTCPPort HTTP
```

NSlookup using PowerShell

```text
Resolve-DnsName www.domain.com
Resolve-DnsName www.domain.com -Type MX -Server 8.8.8.8 
```

Permanent Route Add/Remove &lt;"route" + "add"/"DELETE" + network ID + "mask" + subnet mask, dotted decimal + gateway ipv4&gt;

```text
route add -p 10.0.0.0/8 192.168.1.254
```

or route add –p 10.X.X.X mask 255.X.X.X 192.168.X.X or  
route DELETE –p 10.X.X.X mask 255.X.X.X 192.168.X.X

Show Routing table

```text
route print
```

Example of basic workflow

```text
1 - Print routing table prior to change
2 - Delete routes
3 - Add routes
4 - Print routing table post delete/add routes
5 - Ping IP address (presumable in newly added range to test)

    route print
    route DELETE -p 10.0.0.0 mask 255.255.255.0 192.168.1.254
    route DELETE -p 192.0.0.0 mask 255.255.255.0 192.168.1.254
    route ADD -p 10.0.0.0 mask 255.0.0.0 192.168.1.254
    route ADD -p 192.0.0.0 mask 255.0.0.0 192.168.1.254
    route print
    PING 192.168.201.25
    PING 10.1.0.20
```

