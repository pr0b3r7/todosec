# Domain Name System

**When you browse to https://startpage.com**

Initially, a DNS request is made to a destination port of 53/UDP. The DNS protocol acts like a giant phone book for the Internet - It takes an URL \(think of https://startpage.com/\) and turns it into an IP address. 

In practical terms this means that we don’t need to remember IP addresses for each website we browse to. 

[The IP address uniquely identifies each internet connected device, like a web server or your computer. ](osi-and-tcp-ip-fundamentals.md#ipv4-addressing)

[These are formed of 4 groups of numbers, each 0-255 \(x.x.x.x\) and called an octet. An example shown below is 100.70.172.11.](osi-and-tcp-ip-fundamentals.md#ipv4-addressing)

Universal Resource Identifiers or URIs provide the name of the server \(hostname - corresponds to an IP address assigned to a network interface on the web-server\). 

IP Packets are not sent to destination hostnames \(The TCP/IP Protocol header does not have such field\) - However, once the hostname is translated to an IP Address, that IP is used in the Destination Field of the IP Header packet encapsulating the HTTP Request for the webpage indicated by the URL. 

The DNS response shows a UDP header, with source port 53; the source port is 53 because the data is sourced, or sent by, the DNS server.

![DST IP indicates our target Webserver&apos;s address.](../../../.gitbook/assets/image%20%2883%29.png)

![URL](../../../.gitbook/assets/image%20%2882%29.png)

URI and URL are often used as the same - They are not exactly the same, URL is a special type of identifier that defines the protocol used to access the resource \(HTTP/S, FTP, SCP, etc\).

After the IP address of the webserver we will request the page is provided by the DNS server - The client browser starts a TCP connection to the web server 

