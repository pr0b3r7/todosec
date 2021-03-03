---
description: How to find a given tcp port and ip protocol on a pcap using wireshark filters
---

# Wireshark

Wireshark Filter 'tcp.port' + operator 'eq or ==' + tcp port number '8080'

```text
tcp.port == 8080
```

Wireshark filter IP packets by IP protocol number. \([IP Protocol Numbers](https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml)\)

```text
ip.proto == ()
```



