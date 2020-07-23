# Open Source Intelligence

* Google 
* Exploit-DB/Google Hacking DB 
* WHOIS 
* Netcraft 
* theharverster 
* Shodan

Google Fu On the google search bar type

To restrict websites to a specific Domain

```text
 <site:xyz.com>. i.e oscp.com
```

To filter out a specific subdomain, in this case WEB do -site:www.oscp.com Why? To try to find an ftp for example

```text
site:oscp.com -site:www.oscp.com
```

To look for a specific filetype use . i.e pdf

```text
site:oscp.com -site:www.oscp.com filetype:pdf 
```

On search settings, access Advanced search for extended filters \(if unsure about syntax\)

```text
PENDING***Search for Google Syntax (must)
```

Google Hacking Database Exploit Database

```text
example search to do on google under Files containing passwords: enable secret ext:cfg -git -cisco.com 
```

Shodan Webcams, default passwords, web servers,

Netcraft

```text
add *.domain.com for subdomain wildcard
```

WHOIS

```text
whois oscp.com
```

Theharvester - Searches for emails

```text
theharvester -d #domain examplestore.com -b #searchengines google/all/bing
```

