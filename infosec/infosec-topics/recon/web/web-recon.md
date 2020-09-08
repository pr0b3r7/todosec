# Web Recon

## **Gobuster**

Tool used to brute-force:

* URIs \(directories and files\) in web sites - Mode: dir - the classic directory brute-forcing mode
* DNS subdomains \(with wildcard support\) - Mode: dns - DNS subdomain brute-forcing mode
* Virtual Host names on target web servers - Mode: vhost - virtual host brute-forcing mode \(not the same as DNS!\)

```text
gobuster dir -u http://<target-ip>/<directory-to-enumerate> -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt | tee /<target-directory>/gobust_<target-ip>-<target-directory>.txt
```



