## NMAP FULL

## NMAP sC sV 
```
# Nmap 7.91 scan initiated Sat Aug 21 21:51:17 2021 as: nmap -sC -sV -oN scans/nmap -Pn -vv 10.10.209.35
Nmap scan report for 10.10.209.35
Host is up, received user-set (0.036s latency).
Scanned at 2021-08-21 21:51:17 BST for 68s
Not shown: 988 filtered ports
Reason: 988 no-responses
PORT     STATE SERVICE       REASON  VERSION
53/tcp   open  domain        syn-ack Simple DNS Plus
80/tcp   open  http          syn-ack Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-title: Windcorp.
88/tcp   open  kerberos-sec  syn-ack Microsoft Windows Kerberos (server time: 2021-08-21 20:51:26Z)
135/tcp  open  msrpc         syn-ack Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack
464/tcp  open  kpasswd5?     syn-ack
593/tcp  open  ncacn_http    syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack
2179/tcp open  vmrdp?        syn-ack
7777/tcp open  socks5        syn-ack (No authentication; connection failed)
| socks-auth-info: 
|_  No authentication
Service Info: Host: FIRE; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: -2s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 37844/tcp): CLEAN (Timeout)
|   Check 2 (port 61127/tcp): CLEAN (Timeout)
|   Check 3 (port 8594/udp): CLEAN (Timeout)
|   Check 4 (port 60247/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2021-08-21T20:51:46
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 21 21:52:25 2021 -- 1 IP address (1 host up) scanned in 68.78 seconds
```