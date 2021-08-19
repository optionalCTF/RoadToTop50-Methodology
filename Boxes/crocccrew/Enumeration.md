## NMAP Scan
```
# Nmap 7.91 scan initiated Wed Aug 18 17:42:44 2021 as: nmap -sC -sV -oN scans/nmap -vv 10.10.236.98
Nmap scan report for 10.10.236.98
Host is up, received syn-ack (0.031s latency).
Scanned at 2021-08-18 17:42:45 UTC for 53s
Not shown: 987 filtered ports
Reason: 987 no-responses
PORT     STATE SERVICE       REASON  VERSION
53/tcp   open  domain        syn-ack Simple DNS Plus
80/tcp   open  http          syn-ack Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
88/tcp   open  kerberos-sec  syn-ack Microsoft Windows Kerberos (server time: 2021-08-18 17:42:55Z)
135/tcp  open  msrpc         syn-ack Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack Microsoft Windows netbios-ssn
389/tcp  open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: COOCTUS.CORP0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds? syn-ack
464/tcp  open  kpasswd5?     syn-ack
593/tcp  open  ncacn_http    syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped    syn-ack
3268/tcp open  ldap          syn-ack Microsoft Windows Active Directory LDAP (Domain: COOCTUS.CORP0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped    syn-ack
3389/tcp open  ms-wbt-server syn-ack Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: COOCTUS
|   NetBIOS_Domain_Name: COOCTUS
|   NetBIOS_Computer_Name: DC
|   DNS_Domain_Name: COOCTUS.CORP
|   DNS_Computer_Name: DC.COOCTUS.CORP
|   Product_Version: 10.0.17763
|_  System_Time: 2021-08-18T17:42:57+00:00
| ssl-cert: Subject: commonName=DC.COOCTUS.CORP
| Issuer: commonName=DC.COOCTUS.CORP
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2021-06-07T02:37:18
| Not valid after:  2021-12-07T02:37:18
| MD5:   72be 3896 d880 1bc2 2455 1d55 33da 9300
| SHA-1: bb1b c5bc 3aef ede9 3dc2 8b0d 0b00 c1d3 4371 19f4
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQcVzj9bCnAbJClXIOXvxruDANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw9EQy5DT09DVFVTLkNPUlAwHhcNMjEwNjA3MDIzNzE4WhcNMjEx
| MjA3MDIzNzE4WjAaMRgwFgYDVQQDEw9EQy5DT09DVFVTLkNPUlAwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDIlWfTBDMeC0lP+V4DHerDd6le8YRW9tiL
| T0IGz5vXqzaYzZCLKKxJhlLNwwOqUcHfox+DDsOtUYX0zF09xiLTQ4X4cLArDyJ9
| Spgfvm+RZFucQxh9X80LMhET4WmOLP6FvzgVE1/HcLbLk1pRxW5ET2X5Vu/Pq8qY
| E4aKH1ftUTRt/+77bwKk4zoVymrXyYvIcl7kh1Wy4at6ldfNbc7Qli3WprhAlscp
| FMpmajBdL2nk8JuFMqFcPHcMn9Ie5oVxTeac3RNmUDhuzRUGNAcGo1itMjU6EYuR
| /+xY4WYNnTFavDx87rGBKe37nd/w9S9MShcrhv9sEujVLd3DDE9hAgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEAYzHh28iCzH0l/rkke3Ljc/8Y11MafcBnqxSa0eng1SXduev33ZgeFb6p
| U/wg8i3PxohX5O3nIesuA9MOSEopXlJ+ByUVZgaAUHe9Dep8ENdo5PXFfu6GCl+p
| m1955PFC4IPPVebJoV4h5C5u48sy8biUPD3Q+t3wEVamDfJGamyK70CZ7DvViE/P
| ZY53o/FxkEqmsMZHutpuDmwIJ4EoawO4XZSgWXtr1nCOmZCgpW00GUtB4oXQEKid
| r8OZGmSvwiGJyhXpK4Z2aXcKcMqJR/KOodTsQb0+4rHxIl0RT/uI2XFHxoqdMrKh
| jCzuJYoFShV8othwJD6WdsAdxoVsgA==
|_-----END CERTIFICATE-----
|_ssl-date: 2021-08-18T17:43:37+00:00; 0s from scanner time.
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 0s, deviation: 0s, median: 0s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 32525/tcp): CLEAN (Timeout)
|   Check 2 (port 41845/tcp): CLEAN (Timeout)
|   Check 3 (port 38712/udp): CLEAN (Timeout)
|   Check 4 (port 63093/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2021-08-18T17:43:01
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Aug 18 17:43:38 2021 -- 1 IP address (1 host up) scanned in 53.53 seconds

```

## Enum4Linux Output
```
 ====================================
|    Service Scan on COOCTUS.CORP    |
 ====================================  
[*] Checking LDAP                     
[+] LDAP is accessible on 389/tcp        
[*] Checking LDAPS                                                                                       
[+] LDAPS is accessible on 636/tcp      
[*] Checking SMB                                                                                         
[+] SMB is accessible on 445/tcp
[*] Checking SMB over NetBIOS          
[+] SMB over NetBIOS is accessible on 139/tcp

 ====================================================
|    Domain Information via LDAP for COOCTUS.CORP    |
 ====================================================                 
[*] Trying LDAP               
[+] Appears to be root/parent DC                                    
[+] Long domain name is: COOCTUS.CORP

 =================================================== 
|    Domain Information via RPC for COOCTUS.CORP    |
 =================================================== 
[+] Domain: COOCTUS
[+] SID: S-1-5-21-2062199590-3607821280-2073525473
[+] Host is part of a domain (not a workgroup)

```

# Web Enumeration
## Robots.txt Info disclosure
```
User-Agent: *
Disallow:
/robots.txt
/db-config.bak
/backdoor.php
```

## db-config.bak
```
<?php
$servername = "db.cooctus.corp";
$username = "C00ctusAdm1n";
$password = "B4dt0th3b0n3";
// Create connection $conn = new mysqli($servername, $username, $password);
// Check connection if ($conn->connect_error) {
die ("Connection Failed: " .$conn->connect_error);
}
echo "Connected Successfully";
?>
```