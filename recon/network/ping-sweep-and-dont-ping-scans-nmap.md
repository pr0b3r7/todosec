---
description: >-
  -sN (Ping Scan - disable port scan) and -Pn (Treat all hosts as online -- skip
  host discovery)
---

# Ping Sweep & Don't Ping Scans - nmap

## `-sn` [\(No port scan\)](https://nmap.org/book/man-host-discovery.html)

This option tells Nmap not to do a port scan after host discovery, and only print out the available hosts that responded to the host discovery probes. This is often known as a “ping scan”, but you can also request that trace-route and NSE host scripts be run. This is by default one step more intrusive than the list scan, and can often be used for the same purposes. It allows light reconnaissance of a target network without attracting much attention. Knowing how many hosts are up is more valuable to attackers than the list provided by list scan of every single IP and host name.

Systems administrators often find this option valuable as well. It can easily be used to count available machines on a network or monitor server availability. This is often called a ping sweep, and is more reliable than pinging the broadcast address because many hosts do not reply to broadcast queries.

The default host discovery done with `-sn` consists of an ICMP echo request, TCP SYN to port 443, TCP ACK to port 80, and an ICMP timestamp request by default. When executed by an unprivileged user, only SYN packets are sent \(using a `connect` call\) to ports 80 and 443 on the target. When a privileged user tries to scan targets on a local Ethernet network, ARP requests are used unless `--send-ip` was specified. The `-sn` option can be combined with any of the discovery probe types \(the `-P*` options, excluding `-Pn`\) for greater flexibility. If any of those probe type and port number options are used, the default probes are overridden. When strict firewalls are in place between the source host running Nmap and the target network, using those advanced techniques is recommended. Otherwise hosts could be missed when the firewall drops probes or their responses.

In previous releases of Nmap, `-sn` was known as `-sP`.

## `-Pn` [\(No ping\)](https://nmap.org/book/man-host-discovery.html)

This option skips the Nmap discovery stage altogether. Normally, Nmap uses this stage to determine active machines for heavier scanning. By default, Nmap only performs heavy probing such as port scans, version detection, or OS detection against hosts that are found to be up. Disabling host discovery with `-Pn` causes Nmap to attempt the requested scanning functions against _every_ target IP address specified. So if a class B target address space \(/16\) is specified on the command line, all 65,536 IP addresses are scanned. Proper host discovery is skipped as with the list scan, but instead of stopping and printing the target list, Nmap continues to perform requested functions as if each target IP is active. To skip ping scan _and_ port scan, while still allowing NSE to run, use the two options `-Pn -sn` together.

For machines on a local Ethernet network, ARP scanning will still be performed \(unless `--disable-arp-ping` or `--send-ip` is specified\) because Nmap needs MAC addresses to further scan target hosts. In previous versions of Nmap, `-Pn` was `-P0` and `-PN`.

To perform a Ping Sweep we can employ nmap:

```text
nmap -sn 200.200.200.0/24
```

![](../../.gitbook/assets/image%20%2827%29.png)

#### Misc Scanning Syntax:

Scan 2 given hosts:

```text
nmap -sn 200.200.200.1, 200.200.200.129
```

Scan a subnet and exclude a given host:

```text
nmap -sn 200.200.200.0/24 --exclude 200.200.200.1
```

Scan a subnet and exclude hosts given in a text file:

```text
nmap -sn 200.200.200.0/24 --excludefile hosts.txt
```

To perform a scan using the hosts in a given text file:

```text
nmap -sn -iL hosts.txt
```

### Don't PING scan

```text
nmap -Pn 200.200.200.129
```

![Pay attention to the Open and filtered ports](../../.gitbook/assets/image%20%2818%29.png)

![This is how nmap determines a port to be open or filtered:](../../.gitbook/assets/image%20%2828%29.png)

1. If the host being scanned on 53/TCP responds with a SYN,ACK, the port is considered open, in this case DNS - 53/TCP. 
2. If the host being scanned does not respond to the SYN, the port is considered closed.

![](../../.gitbook/assets/image%20%2813%29.png)

