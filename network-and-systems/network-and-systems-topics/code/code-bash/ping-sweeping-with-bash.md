# Ping Sweeping with Bash

```bash
#!/bin/Bash
# Author: pr0b3r7

if [[ "$1" == "" ]] ; then
echo "Usage: ./pingsweep.sh"
else
for i in {1..255} ; do ping -c 1 192.168.1.$i | grep "64 bytes" & done | awk '{print $4}' | cut -d ":" -f 1 
fi 
```

#### **Parallelize:** 

```bash
for i in {1..255} ; do ping -c 1 192.168.1.$i | grep "bytes from" & done | awk '{print $4}'
```

![script output and printout.](../../../../.gitbook/assets/image%20%2876%29.png)

**Optional:**

Save pingsweep.sh script **output** to a text file:

`./pingsweep.sh 192.168.1 > iplist.txt`

Show contents of iplist.txt and **sort** by unique value

`cat iplist | sort -unique`

**Creative usage:**

For loop to do basic scan of the **IPs in the list** and save to text file

`for ip in $(cat iplist.txt); do nmap -Pn $ip; done > nmapresults.txt`

