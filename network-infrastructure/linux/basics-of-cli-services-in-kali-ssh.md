# Basics of CLI, Services in Kali \(SSH\) and how to change your motd \(Banner\)

Linux basic command refresher:



`echo







`echo foobar2 >> file.txt`



`foobar3`

`foobar2`



HTTP via Apache2

Enable service on startup



Toggle service





View all files in /var/www/html with -la flag

`ls -la /var/www/html` 



`pwd`

**SSH via** _**ssh**_



`systemctl enable/stop ssh`





**Configure SSH on Kali to allow login w root password \(insecure\)**

 

    1. In '/etc/ssh/sshd\_config' replace 'PermitRootLogin without-password'by 'PermitRootLogin yes'

    2. Restart your ssh daemon

`service ssh restart`







`mkdir default_keys`

`mv ssh_host_* default_keys/`



   `/etc/ssh#  dpkg-reconfigure openssh-server`    





`root@kali:~/Desktop#  md5sum /etc/ssh/ssh_host_*`

**Old keys**

`root@kali~/Desktop# md5sum /etc/ssh/default_keys/ssh_host_*`

7. Restart SSH service 











**11. Don't forget to backup ssh config



**12. Change port ssh listens on** 

`find '#Port 22' change 22 to desired TCP port.` 

**13. 

`systemctl restart ssh`

**14. Profit!**
