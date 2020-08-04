# Basics of CLI, Services in Kali \(SSH\) and how to change your motd \(Banner\)

Linux basic command refresher:

**echo** - display a line of text i.e

`echo "hola"`

Include text string "foobar3" into file

`echo foobar3 > file.txt`

Include text string "foobar2" into next line of file.txt

`echo foobar2 >> file.txt`

If we ran cat against file.txt, it would look like this:

`foobar3`

`foobar2`

**Kali Linux Services**

HTTP via Apache2

Enable service on startup

`systemctl enable/disable Apache2`

Toggle service On/Off

`service apache2 stop/start`

Note: HTTP files are stored at /var/www/html

View all files in /var/www/html with -la flag for display a list and all hidden files in the present directory

`ls -la /var/www/html`

Present directory can be shown with:

`pwd`

**SSH via** _**ssh**_

enable ssh service on startup\#\#

`systemctl enable/stop ssh`

toggle ssh service On/Off

`service ssh stop/start`

**Configure SSH on Kali to allow login w root password \(insecure\)**

1. In '/etc/ssh/sshd\_config' replace 'PermitRootLogin without-password'by 'PermitRootLogin yes'
2. Restart your ssh daemon

`service ssh restart`

1. Change Kali default ssh keys to avoid MITM attack:
2. Move the default Kali ssh keys to a new folder:

`cd /etc/ssh/`

`mkdir default_keys`

`mv ssh_host_* default_keys/`

1. Regenerate the keys

   `/etc/ssh# dpkg-reconfigure openssh-server`

2. Verify Hashes are different

**New Keys**

`root@kali:~/Desktop# md5sum /etc/ssh/ssh_host_*`

**Old keys**

`root@kali~/Desktop# md5sum /etc/ssh/default_keys/ssh_host_*`

1. Restart SSH service 

`systemctl restart ssh.service`

1. SET MOTD for extra badassness

   \(Essential\)

`sudo nano /etc/MOTD`

1. Remove current MOTD

   \(Possibly Wack\)

`rm /etc/motd`

**11. Don't forget to backup ssh config !**

`cp /etc/ssh/sshd_config /etc/ssh/sshd_config_backup`

**12. Change port ssh listens on**

`find '#Port 22' change 22 to desired TCP port.`

**13. Restart openssh**

`systemctl restart ssh`

**14. Profit!**

