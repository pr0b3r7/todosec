---
description: >-
  Goal Ping Sweep a range, generate a list of hosts that respond to ICMP Echo
  request with a reply
---

# Basic examples of Bash Scripting

**Format:** Explanation of **command + arguments**

**ping** on a **count \(-c\)** of 1

**Grep** = show only quoted string

**Cutting a delimiter \(-d\)** specified in " " - in this case space 

The field specifies the word \(in this case the IP address so the flag yields a list of live hosts\) of 4. 

A _range_ can be specified if _4-9_ format is used

**Sed** is used to remove characters from final output 's/.$//' \*\*\*Research pending on the syntax of "sed" linux command \*\*\* 

Example Command

```text
ping -c 1 192.168.1.1 | grep "64 bytes from" | cut -d " " -f 4 | sed 's/.$//'
```

**For loop** - don't forget to add **"; done"** at the end so we don't run into '&gt;' prompt issue

Below for loop: pings 1-255 hosts in 192.168.1.0/24

**Grep** prints the matching lines "64 bytes from"

**Cut** - remove sections from each \#line of files using **"-d".** 

**--delimiter**=DELIM - use delimiter instead of TAB for field delimiter. \(in this case a space **" "**\)

**Sed** - stream editor for filtering and transforming text helps us \(more research needed on '**s/.$//'**\)

```text
for i in {1..255}; do ping -c 1 192.168.1.$i | grep "64 bytes from" | cut -d " " -f 4 | sed 's/.$//'; done
```

My Traceroute - **mtr**

    **-r** for outputing the results on the terminal

    **--no-dns** does not resolve hostnames

```text
sudo mtr -r -c 5 100.65.150.160 --no-dns | grep "." | cut -d " " -f 4
```

My traceroute and PING test - && executes command to the right of && after command to the left of && has been completed

    In this case, mtr is executed, once it finishes for loop is executed

```text
sudo mtr -r -c 5 192.168.1.1 && sudo mtr -r -c 5 192.168.1.18 && for i in {1..254}; do ping -c 5 192.168.1.$i | grep '1'; done
```

**For loop** + **mtr** - For i in range 160-190 runs a mytraceroute to specified \#X.X.X.$i IP address \(no DNS resolution flag\)

**Grep** prints \#the lines that \#contain a "." \(such as \#ones with dotted decimal IP addresses\)

**Cut -d** uses \#space as delimiter ; done completes the \#loop. 

Useful for checking routing path in a whole subnet in dual homed networks with different egress and ingress paths

```text

for i in {160..190}; do sudo mtr -r -c 5 100.65.150.$i --no-dns | grep "." | cut -d " " -f 4; done
```

But... How to save test results to a file? Add &gt; after command followed by the filename \(thanks to @nin\)

```text
ping -c 1 192.168.1.1 > ping.txt 
```

Use the ping command to obtain the IP address of the specified website

```text
ping -c 1 google.com | grep from | cut -d " " -f 4 
~> 220.181.57.216
```

