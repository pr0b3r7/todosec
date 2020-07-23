---
description: Linux 'Piping'
---

# Linux Basic Networking

Check which applications listen on which ports and filter with grep

```text
netstat -tulpn | grep <tcp port number>
```

Check if port 8080 is open

```text
netstat   -tap | grep  8080 
```

Traceroute to specific TCP port - &lt;"traceroute" + -p \(port\) + "TCP port number" + target host, dotted decimal&gt;

```text
sudo traceroute -p 9100 192.168.18.250
```

Allow blocked traffic on Linux Firewall \(iptables\)

```text
sudo vi /etc/sysconfig/iptables.cust
```

Add the allowed subnet

```text
sudo /usr/remote/odutils/stop-maintenance.sh
```

Check Printer

```text
ping XX.XX.XX.XX
telnet XX.XX.XX.XX 9100/515
lpstat –s | grep XX.XX.XX.XX
```

tcpdump UAP RSF - \[ Hint: An anagram for the TCP flags: Unskilled Attackers Pester Real Security Folk \]

Show me all URGENT \(URG\) packets...

```text
tcpdump 'tcp[13] & 32 != 0'
```

Show me all ACKNOWLEDGE \(ACK\) packets...

```text
tcpdump 'tcp[13] & 16 != 0'
```

Show me all PUSH \(PSH\) packets...

tcpdump 'tcp\[13\] & 8 != 0'

Show me all RESET \(RST\) packets...

```text
tcpdump 'tcp[13] & 4 != 0'
```

Show me all SYNCHRONIZE \(SYN\) packets...

```text
tcpdump 'tcp[13] & 2 != 0'
```

Show me all FINISH \(FIN\) packets...

```text
tcpdump 'tcp[13] & 1 != 0'
```

Show me all SYNCHRONIZE/ACKNOWLEDGE \(SYNACK\) packets...

```text
tcpdump 'tcp[13] = 18'
```

Note: Only the PSH, RST, SYN, and FIN flags are displayed in tcpdump's flag field output. URGs and ACKs are displayed, but they are shown elsewhere in the output rather than in the flags field

Temporary routes Add, why temporary? Upon server reboot, routing table should be re-built

```text
sudo ip route add 192.0.0.0/8 via 192.168.1.254
sudo /sbin/route add –net X.X.X.X netmask 255.X.X.X gw Y.Y.Y.Y
```

sudo /sbin/route add -net 192.168.100.0 netmask 255.255.255.0 gw 10.0.156.129 && sudo /sbin/route add -net 10.0.0.0 netmask 255.0.0.0 gw 192.168.1.254

Temporary routes Delete

```text
sudo /sbin/route del  –net X.X.X.X netmask 255.X.X.X gw Y.Y.Y.Y
```

Permanent Route editing with VI

```text
sudo vi /etc/sysconfig/network-scripts/route-eth0

    #Press (i)nsert 
    #Example route below <network id + '/' + cidr + 'via' + gateway ipv4 address>

10.0.0.0/8 via 192.168.1.254
192.0.0.0/8 via 192.168.1.254

    #Press (esc)ape
    #Save (wq!)
```

Restart network process

```text
sudo /sbin/service network restart
```

Show routing table & open interface Route-Eth0 routes file

```text
netstat -rn && sudo vi /etc/sysconfig/network-scripts/route-eth1
```

Specific to RHEL7

```text
Restart network service using SYSTEMCTL; PING to host on defined subnet using range {1...(1+n)}

    sudo systemctl restart network && netstat -rn && sudo tcpdump host 100.65.150.111 && for i in {1..254}; do ping -c 5 192.168.1.$i | grep '1'; done 
```

Specific to RHEL6

```text
Restart network service using /sbin/service network + show routing table + PING host(s) within subnet - TESTING

    sudo /sbin/service network restart &&  netstat -rn && for i in {1..254}; do ping -c 1 192.168.1.$i | grep '1'; done && sudo tcpdump host 192.168.1 -nvv

Testing - PING host(s) within subnet 

    for i in {1..254}; do ping -c 1 192.17.254.$i | grep '1'; done
```

Ping sweep and output only live hosts

```text
for i in {1..255}; do ping -c 1 192.168.1.$i | grep "64 bytes from" | cut -d " " -f 4 | sed 's/.$//'; done
```

My Traceroute, -r for outputing the results on the terminal;

```text
sudo mtr -r -c 5 100.65.150.160 --no-dns | grep "." | cut -d " " -f 4
```

My traceroute and PING test

```text
sudo mtr -r -c 5 192.168.1.1 && sudo mtr -r -c 5 192.168.1.18 && for i in {1..254}; do ping -c 5 192.168.1.$i | grep '1'; done
```

For loop with mtr - For i in range 160-190 runs a mytraceroute to specified \#X.X.X.$i IP address \(no DNS resolution flag\); greps prints the lines that \#contain a "." \(such as \#ones with dotted decimal IP addresses\); cut -d uses \#space as delimiter ; done completes the loop. Useful for checking routing path in a whole subnet

```text
  for i in {160..190}; do sudo mtr -r -c 5 100.65.150.$i --no-dns | grep "." | cut -d " " -f 4; done
```

