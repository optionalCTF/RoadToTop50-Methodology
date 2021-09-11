# Basic 

```
# Nmap 7.91 scan initiated Sat Sep 11 20:10:35 2021 as: nmap -sC -sV -oN scans/nmap -vv 10.10.254.61
Nmap scan report for 10.10.254.61
Host is up, received syn-ack (0.028s latency).
Scanned at 2021-09-11 20:10:35 BST for 8s
Not shown: 998 closed ports
Reason: 998 conn-refused
PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.2p2 Ubuntu 4ubuntu2.7 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 3e:79:78:08:93:31:d0:83:7f:e2:bc:b6:14:bf:5d:9b (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDgHGMuutSoQktLWJfDa8F4+zCvINuPv8+mL2sHPJmSfFDaQ3jlsxitYWH7FWdj3zPzXLW01aY+AySXW593T3XZpzCSAjm3ImnPtNTaQsbsdkgmhj8eZ3q9hPxU5UD5593K+/FDdIiN5xIBLegm6y0SAd3sRtpdrcpHpkqOIZvoCyJTV7ncbRY0gppvfTEObo2PiCtzh31gbaDPrJICPnDuuF5aWAUTeUMc0YcMYaB9cCvfVT6Y1Cdfh4IwMHslafXRhRt5tn5l47xR0xwd3cddUEez/CHxiNthNTgv+BSo+TPPciPAiCN3QGSqTcPQ74RvFiAznL2irkENq+Qws2A3
|   256 3a:67:9f:af:7e:66:fa:e3:f8:c7:54:49:63:38:a2:93 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBLzJknVQsubSrZMKNLlNAP1HXXuXzhtAf24ScY17eIS03NfxjFwiSESz8xKwVcmbODQGc+b9PvepngTTGlVrMf4=
|   256 8c:ef:55:b0:23:73:2c:14:09:45:22:ac:84:cb:40:d2 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIG/WxvJRsI0dvT84mxR/y3AH3C8KP/1Njv4wP6DylZeQ
80/tcp open  http    syn-ack Apache httpd 2.4.18 ((Ubuntu))
|_http-favicon: Unknown favicon MD5: D41D8CD98F00B204E9800998ECF8427E
|_http-generator: WordPress 5.3.2
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-robots.txt: 1 disallowed entry 
|_/wp-admin/
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Jack&#039;s Personal Site &#8211; Blog for Jacks writing adven...
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Sep 11 20:10:43 2021 -- 1 IP address (1 host up) scanned in 8.56 seconds
```