# Check for live hosts in a /24 network

```bash
#!/bin/bash
# Author: pr0b3r7

# Check for arguments
if [[ "$1" == "" ]] ; then
# Notify the user this script does not require arguments and display proper syntax
echo "[*] - This script requires the first three octets of the /24 network! - Usage: ./ping-sw.sh 192.168.1"
else
# Iterate over 1-255 (/24 subnet) ; ping each IP with 1 ICMP Echo Request
# (cont.) display only the lines containing "64 bytes" (ICMP Echo Responses)
# (cont.) & performs each ping at the same time ; Redirect standard error to /dev/null
# (cont.) AWK prints the 4th column containing the IP address ; cut the first field using : as delimiter
# (cont.) to print only the IP address without the trailing ":".
for i in {1..255} ; do ping -c 1 $1.$i | grep "64 bytes" & done 2> /dev/null | awk '{print $4}' | cut -d ":" -f 1
fi
```

![sample run + source](../../../../.gitbook/assets/image%20%2879%29.png)

**Optional:**

Save ping**-**sw.sh script **output** to a text file:

`./ping-sw.sh 192.168.1 > iplist.txt`

Show contents of iplist.txt and **sort** by unique value

`cat iplist | sort -unique`

**Creative usage:**

For loop to do basic scan of the **IPs in the list** and save to text file

`for ip in $(cat iplist.txt); do nmap -Pn $ip; done > nmapresults.txt`

