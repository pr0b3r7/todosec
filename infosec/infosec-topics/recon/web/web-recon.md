# Web Recon

## **Gobuster**

Tool used to brute-force:

* URIs \(directories and files\) in web sites - Mode: dir - the classic directory brute-forcing mode
* DNS subdomains \(with wildcard support\) - Mode: dns - DNS subdomain brute-forcing mode
* Virtual Host names on target web servers - Mode: vhost - virtual host brute-forcing mode \(not the same as DNS!\)

```text
gobuster dir -u http://<target-ip>/<directory-to-enumerate> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt | tee /<target-directory>/gobust_<target-ip>-<target-directory>.txt
```

## SMB Client

An SMB client program for UNIX machines is included with the Samba distribution. It provides an ftp-like interface on the command line. You can use this utility to transfer files between a Windows 'server' and a Linux client. 

To recursively download all contents of a share or a directory:

```text
smbclient '\\server\share'
mask ""
recurse ON
prompt OFF
cd 'path\to\remote\dir'
lcd '~/path/to/download/to/'
mget *
```

## Common Web Vulnerabilities:

### Remote file inclusion

**Remote file inclusion \(RFI\)** occurs when the web application downloads and executes a remote file. These remote files are usually obtained in the form of an HTTP or FTP URI as a user-supplied parameter to the web application.

![](../../../../.gitbook/assets/image%20%2871%29.png)

### Local file inclusion

**Local file inclusion \(LFI\)** is similar to a remote file inclusion vulnerability except instead of including remote files, only local files i.e. files on the current server can be included for execution. Unlike RFI, LFI assaults aim to exploit insecure local file upload functions that fail to validate user-supplied/controlled input.

As a result, malicious character uploads and directory/path traversal attacks are allowed for. Perpetrators can then directly upload malware to a compromised system, as opposed to retrieving it using a tempered external referencing function from a remote location.

