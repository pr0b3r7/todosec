# Ping Sweeping with Bash

```text
#!/bin/Bash
# Author: pr0b3r7

if [] "$1" == "" ]
then
echo "Usage: ./pingsweep.sh [network]"
echo "Example: ./pingsweep.sh 192.168.1"
else
for ip in 'seq 1 254' ; do
ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | sed 's/.$//' &
done
fi 
```

**Optional

Save pingsweep script **output** to a text file

`./pingsweep.sh 192.168.1 > iplist.txt`



`cat iplist | sort -unique`





`for ip in $(cat iplist.txt); do nmap -Pn $ip; done > nmapresults.txt`
