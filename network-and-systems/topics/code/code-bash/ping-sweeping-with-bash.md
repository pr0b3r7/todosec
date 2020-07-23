# Ping Sweeping with Bash

```bash
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

**Optional:**

Save pingsweep script **output** to a text file:

`./pingsweep.sh 192.168.1 > iplist.txt`

Show contents of iplist.txt and **sort** by unique value

`cat iplist | sort -unique`

**Creative usage:**

For loop to do basic scan of the **IPs in the list** and save to text file

`for ip in $(cat iplist.txt); do nmap -Pn $ip; done > nmapresults.txt`

