---
description: From Cisco's Networking Academy ENCOR Lab Guide
---

# Tune & Optimize EtherChannel Operations

### 5.1.4 Lab - Tune & Optimize EtherChannel Operations

#### Part 1: Build the Network and Configure Basic Device Settings

Open Standard: Link Aggregation Control Protocol \(LACP\), maintains EtherChannel Bundles. LACP supports 8 active members and 8 standby members in each bundle. Minimum and Maximum \# of links and timing of LACP packets may be configured.

```text
DSW1:
!
enable
!
terminal length 0
!
configure terminal
!
hostname DSW1
!
banner motd # D1, Tuning EtherChannel #
spanning-tree mode rapid-pvst
!
!
line con 0
!  
exec-timeout 0 0
!
logging synchronous
!
exit
!
interface range GigabitEthernet 0/0 - 3
!
!
switchport trunk encapsulation dot1q
!
switchport mode trunk 
no shutdown
!
exit
!
clock timezone UTC -5
!
end
!
write memory
!

DSW2:
!
enable
!
terminal length 0
!
configure terminal
!
hostname DSW2
!
banner motd # D1, Tuning EtherChannel #
spanning-tree mode rapid-pvst
!
!
line con 0
!
exec-timeout 0 0
!
logging synchronous
!
exit
!
interface range GigabitEthernet 0/0 - 3
!
!
switchport trunk encapsulation dot1q
!
switchport mode trunk 
no shutdown
!
exit
!
clock timezone UTC -5
!
end
!
write memory
!
```

### Part 2: Tune LACP based EtherChannel

EtherChannel bundles using LACP as its negotiation protocol can have up to 16 assigned members, with 8 active ports passing traffic and 8 ports on standby.

LACP bundle switched negotiate a master/slave relationship and the designated master switch makes the decision on which members are active and which are in "hot standby" mode when the number of members in the bundle exceeds 8.

Minimum and Maximum \# of ports in a port channel can be configured.

DSW1 & DSW2 EtherChannel Bundle w/ LACP as negotiation protocol with 2 links and a max. of 3. Manually set a master. Enable LACP fast packets and reduce time out period from 30 to 1 second\(s\).

Configure Master Switch Criteria

Each LACP switch has a system-ID value. SW with lowest system-ID is the master. System-ID = system priority \(32768 by default + base MAC Address\). The priority value for LACP doesn't scale in multiples of 4096. \(Unlike Spanning Tree Protocol\).

Use "show lacp sys-id" \(display sys-id\) on DSW1-DSW2.

```text
DSW1:
!
enable
!
terminal length 0
!
show lacp sys-id
!

Output:

DSW1#show lacp sys-id
32768, 5254.000d.8000

DSW2:
!
enable
!
terminal length 0
!
!
show lacp sys-id
!

Output:

DSW2#show lacp sys-id
32768, 5254.0019.8000
```

Modify LACP sys-ID in DSW2 \(lacp system-priority 1\)

```text
DSW2:
!
enable
!
terminal length 0
!
configure terminal
!
no ip domain-lookup
!
lacp system-priority 1
!
end
!
write memory
!
show lacp sys-id
!
```

Configure bundle size and member preferences

Interfaces are selected to be included in the active bundle based on their interface id. Lower numbered interfaces are added to the bundle until maximum size. Remaining interfaces are put in hot standby mode

Shutdown interfaces between DSW1 & DSW2

```text
DSW1 & DSW2:
!
enable
!
terminal length 0
!
show ip interface brief
!
configure terminal
!
no ip domain-lookup
!
interface range GigabitEthernet0/0 - 3
!
shutdown
!
end
!
write memory
!
show ip int brief
!
```

Configure links connecting DSW1 & DSW2 into a LACP EtherChannel bundle. Use Channel Group number 12 and the Active Mode. Configure interfaces for LACP fast

```text
DSW1 & DSW2:
!
enable
!
terminal length 0
!
sh ip interface brief
!
configure terminal
!
no ip domain-lookup
!
interface range GigabitEthernet0/0 - 3
!
channel-group 12 mode active
!
lacp rate fast
!
no shutdown
!
end
!
write memory
!
show EtherChannel summary
!
```

Configure port-channel 12 on DSW1 & DSW2 w/ a LACP minimum bundle size of 2 interfaces, maximum bundle size of 3 interfaces. Max value is only needed in master switch. Configuring it on both ends may help with troubleshooting. Verify that the EtherChannel bundle has formed and note the ports that are included versus the port that is in hot standby mode. \(show EtherChannel summary\).

```text
DSW1 & DSW2:
!
enable
!
terminal length 0
!
sh ip interface brief
!
configure terminal
!
no ip domain-lookup
!
interface port-channel 12
!
port-channel min-links 2
!
lacp max-bundle 3
!
end
!
write memory
!
show EtherChannel summary
!
show lacp internal
!
```

### Part 3: Explore EtherChannel Load Balancing

Load Balancing method in EtherChannel is a global Settings on the switch. All Ether-channels in a SW will use the method selected. Load Balancing methods used at either end of the EtherChannel Bundle do not have to match.

By default Cisco Catalyst 3650 and 2960 SW load-balance using MAC Address.   

```text
!
enable
!
show etherchannel load-balance
!


DSW2#show etherchannel load-balance 
EtherChannel Load-Balancing Configuration:
        src-dst-ip

EtherChannel Load-Balancing Addresses Used Per-Protocol:
Non-IP: Source XOR Destination MAC address
  IPv4: Source XOR Destination IP address
  IPv6: Source XOR Destination IP address
```

