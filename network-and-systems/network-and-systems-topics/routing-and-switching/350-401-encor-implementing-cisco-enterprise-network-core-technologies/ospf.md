# OSPF

Open Shortest Path First or **OSPF**, is a link state routing protocol in which every router receives a complete picture of the network. This allows the routers in the OSPF domain to make routing decisions, using the full picture to map the shortest distance to its end destination.

All routers will select their own router ID \(**RID**\), providing the router with a unique identifier on the network. The topology of a network is stored in the Link State Database \(**LSDB**\), where the router IDs are used to identify each router using OSPF.   
****

Before you configure OSPF, you need to configure an ip address on the router's loopback interface. The loopback interface IP address determines the Router ID for the router. This can be used to influence which router ends up becoming the DR or BDR.

  


| Configure OSPF |  |
| :--- | :--- |
| start ospf with router ospf &lt;process id&gt; | _router ospf 1_ |
| specify the network and an area to assign those IPs to | _network 10.10.10.1 0.0.0.255 area 0_ |

\_\_

| OSPF Example Commands | \*each command can be made more specific |
| :--- | :--- |
| displays general information about OSPF routing  | _show ip ospf \[\]_ |
| displays OSPF database on router | _show ip ospf database \[\]_ |
| displays information about OSPF enabled interfaces | _show ip ospf interface \[\]_ |
| displays neighbor information  | _show ip ospf neighbor \[\]_ |

\*[https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/iproute\_ospf/command/iro-cr-book/ospf-s1.html\#wp8749965360](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/iproute_ospf/command/iro-cr-book/ospf-s1.html#wp8749965360)



### LSAs **\(Types & neighbor states\)**      

A LSA is a fundamental tool for OSPF to exchange routing information/topology with routers in the same area. LSAs are stored in the LSDB.                                                                                                                                                           ****

* **LSA Type 2:    Network LSA**
* **LSA Type 3:    Inter-area prefix LSA**
* **LSA Type 4:    Inter-area router LSA**
* **LSA Type 5:    AS external LSA**
* **LSA Type 6:    Group Membership LSA**
* **LSA Type 7:    Not-so-stubby area LSA** 
* **LSA Type 8:    Link LSA** 
* **LSA Type 9:    Intra-area prefix LSA**

_Routers will reach FULL state when neighbors have exchanged their LSA databases_

1. Down state
2. Attempt state
3. Init state
4. 2-way state
5. Exstart state
6. Exchange state
7. Loading state
8. Full state

### DR & BDR

OSPF uses DRs \(designated routers\) & BDRs \(backup designated routers\) to act as a hub for routers on the same broadcast segment to exchange OSPF information. The DR and BDR are the only routers in the segment who provide and receive OSPF information from every router. All Non-DR/BDR routers rely on the DR/BDR for updates. This helps to limit the number of routing updates needed throughout the segment. 

An election process is used to decide which router will become DR and BDR. There are two factors in this decision:



1. **Priority -** The router with the highest priority will become the DR.
2. **Router ID** - If two routers have the same priority, the one with the higher Router ID will become the DR.

  






  




