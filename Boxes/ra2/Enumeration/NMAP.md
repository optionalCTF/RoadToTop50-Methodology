```
# Nmap 7.91 scan initiated Sat Sep 11 21:20:40 2021 as: nmap -sC -sV -vv -oN scans/nmap windcorp.thm
Nmap scan report for windcorp.thm (10.10.136.69)
Host is up, received syn-ack (0.032s latency).
Scanned at 2021-09-11 21:20:40 BST for 94s
Not shown: 978 filtered ports
Reason: 978 no-responses
PORT     STATE SERVICE             REASON  VERSION
53/tcp   open  domain              syn-ack Simple DNS Plus
80/tcp   open  http                syn-ack Microsoft IIS httpd 10.0
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Microsoft-IIS/10.0
|_http-title: Did not follow redirect to https://fire.windcorp.thm/
88/tcp   open  kerberos-sec        syn-ack Microsoft Windows Kerberos (server time: 2021-09-11 20:20:54Z)
135/tcp  open  msrpc               syn-ack Microsoft Windows RPC
139/tcp  open  netbios-ssn         syn-ack Microsoft Windows netbios-ssn
389/tcp  open  ldap                syn-ack Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:selfservice.windcorp.thm, DNS:selfservice.dev.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-29T03:31:08
| Not valid after:  2028-05-29T03:41:03
| MD5:   804b dc39 5ce5 dd7b 19a5 851c 01d1 23ad
| SHA-1: 37f4 e667 cef7 5cc4 47c9 d201 25cf 2b7d 20b2 c1f4
| -----BEGIN CERTIFICATE-----
| MIIDajCCAlKgAwIBAgIQUI2QvXTCj7RCVdv6XlGMvjANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTAeFw0yMDA1MjkwMzMxMDhaFw0y
| ODA1MjkwMzQxMDNaMBwxGjAYBgNVBAMMEWZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAv900af0f6n80F0J6U9jMgcwQrozr
| kXmi02esW1XAsHpWnuuMQDIN6AtiYmDcoFEXz/NteLI7T6PusqQ6SXqLBurTnR8V
| InPD3Qea6lxOXNjuNeqqZKHhUaXiwSaqtAB+GzPkNtevw3jeEj99ST/G1qwY9Xce
| sfeqR2J4kQ+8U5yKLJDPBxOSx3+SHjKErrLTk66lrlEi4atr+P/ccXA5TBkZFkYh
| i3YdKTDnYeP2fMrqvOqpw82eniHAGJ2N8JJbNep86ps8giIRieBUUclF/WCp4c33
| p4i1ioVxJIYJj6f0tjGhy9GxB7l69OtUutcIG0/FhxL2dQ86MmnHH0dE7QIDAQAB
| o4GnMIGkMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYB
| BQUHAwEwVAYDVR0RBE0wS4IRZmlyZS53aW5kY29ycC50aG2CGHNlbGZzZXJ2aWNl
| LndpbmRjb3JwLnRobYIcc2VsZnNlcnZpY2UuZGV2LndpbmRjb3JwLnRobTAdBgNV
| HQ4EFgQUIZvYlCIhAOFLRutycf6U2H6LhqIwDQYJKoZIhvcNAQELBQADggEBAKVC
| ZS6HOuSODERi/glj3rPJaHCStxHPEg69txOIDaM9fX4WBfmSjn+EzlrHLdeRS22h
| nTPirvuT+5nn6xbUrq9J6RCTZJD+uFc9wZl7Viw3hJcWbsO8DTQAshuZ5YJ574pG
| HjyoVDOfYhy8/8ThvYf1H8/OaIpG4UIo0vY9qeBQBOPZdbdVjWNerkFmXVq+MMVf
| pAt+FffQE/48kTCppuSKeM5ZMgHP1/zhZqyJ3npljVDlgppjvh1loSYB+reMkhwK
| 2gpGJNwxLyFDhTMLaj0pzFL9okqs5ovEWEj8p96hEE6Xxl4ZApv6mxTs9j2oY6+P
| MTUqFyYKchFUeYlgf7k=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:14+00:00; +1s from scanner time.
443/tcp  open  ssl/http            syn-ack Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:selfservice.windcorp.thm, DNS:selfservice.dev.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-29T03:31:08
| Not valid after:  2028-05-29T03:41:03
| MD5:   804b dc39 5ce5 dd7b 19a5 851c 01d1 23ad
| SHA-1: 37f4 e667 cef7 5cc4 47c9 d201 25cf 2b7d 20b2 c1f4
| -----BEGIN CERTIFICATE-----
| MIIDajCCAlKgAwIBAgIQUI2QvXTCj7RCVdv6XlGMvjANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTAeFw0yMDA1MjkwMzMxMDhaFw0y
| ODA1MjkwMzQxMDNaMBwxGjAYBgNVBAMMEWZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAv900af0f6n80F0J6U9jMgcwQrozr
| kXmi02esW1XAsHpWnuuMQDIN6AtiYmDcoFEXz/NteLI7T6PusqQ6SXqLBurTnR8V
| InPD3Qea6lxOXNjuNeqqZKHhUaXiwSaqtAB+GzPkNtevw3jeEj99ST/G1qwY9Xce
| sfeqR2J4kQ+8U5yKLJDPBxOSx3+SHjKErrLTk66lrlEi4atr+P/ccXA5TBkZFkYh
| i3YdKTDnYeP2fMrqvOqpw82eniHAGJ2N8JJbNep86ps8giIRieBUUclF/WCp4c33
| p4i1ioVxJIYJj6f0tjGhy9GxB7l69OtUutcIG0/FhxL2dQ86MmnHH0dE7QIDAQAB
| o4GnMIGkMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYB
| BQUHAwEwVAYDVR0RBE0wS4IRZmlyZS53aW5kY29ycC50aG2CGHNlbGZzZXJ2aWNl
| LndpbmRjb3JwLnRobYIcc2VsZnNlcnZpY2UuZGV2LndpbmRjb3JwLnRobTAdBgNV
| HQ4EFgQUIZvYlCIhAOFLRutycf6U2H6LhqIwDQYJKoZIhvcNAQELBQADggEBAKVC
| ZS6HOuSODERi/glj3rPJaHCStxHPEg69txOIDaM9fX4WBfmSjn+EzlrHLdeRS22h
| nTPirvuT+5nn6xbUrq9J6RCTZJD+uFc9wZl7Viw3hJcWbsO8DTQAshuZ5YJ574pG
| HjyoVDOfYhy8/8ThvYf1H8/OaIpG4UIo0vY9qeBQBOPZdbdVjWNerkFmXVq+MMVf
| pAt+FffQE/48kTCppuSKeM5ZMgHP1/zhZqyJ3npljVDlgppjvh1loSYB+reMkhwK
| 2gpGJNwxLyFDhTMLaj0pzFL9okqs5ovEWEj8p96hEE6Xxl4ZApv6mxTs9j2oY6+P
| MTUqFyYKchFUeYlgf7k=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:13+00:00; +1s from scanner time.
| tls-alpn: 
|_  http/1.1
445/tcp  open  microsoft-ds?       syn-ack
464/tcp  open  kpasswd5?           syn-ack
593/tcp  open  ncacn_http          syn-ack Microsoft Windows RPC over HTTP 1.0
636/tcp  open  ssl/ldap            syn-ack Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:selfservice.windcorp.thm, DNS:selfservice.dev.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-29T03:31:08
| Not valid after:  2028-05-29T03:41:03
| MD5:   804b dc39 5ce5 dd7b 19a5 851c 01d1 23ad
| SHA-1: 37f4 e667 cef7 5cc4 47c9 d201 25cf 2b7d 20b2 c1f4
| -----BEGIN CERTIFICATE-----
| MIIDajCCAlKgAwIBAgIQUI2QvXTCj7RCVdv6XlGMvjANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTAeFw0yMDA1MjkwMzMxMDhaFw0y
| ODA1MjkwMzQxMDNaMBwxGjAYBgNVBAMMEWZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAv900af0f6n80F0J6U9jMgcwQrozr
| kXmi02esW1XAsHpWnuuMQDIN6AtiYmDcoFEXz/NteLI7T6PusqQ6SXqLBurTnR8V
| InPD3Qea6lxOXNjuNeqqZKHhUaXiwSaqtAB+GzPkNtevw3jeEj99ST/G1qwY9Xce
| sfeqR2J4kQ+8U5yKLJDPBxOSx3+SHjKErrLTk66lrlEi4atr+P/ccXA5TBkZFkYh
| i3YdKTDnYeP2fMrqvOqpw82eniHAGJ2N8JJbNep86ps8giIRieBUUclF/WCp4c33
| p4i1ioVxJIYJj6f0tjGhy9GxB7l69OtUutcIG0/FhxL2dQ86MmnHH0dE7QIDAQAB
| o4GnMIGkMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYB
| BQUHAwEwVAYDVR0RBE0wS4IRZmlyZS53aW5kY29ycC50aG2CGHNlbGZzZXJ2aWNl
| LndpbmRjb3JwLnRobYIcc2VsZnNlcnZpY2UuZGV2LndpbmRjb3JwLnRobTAdBgNV
| HQ4EFgQUIZvYlCIhAOFLRutycf6U2H6LhqIwDQYJKoZIhvcNAQELBQADggEBAKVC
| ZS6HOuSODERi/glj3rPJaHCStxHPEg69txOIDaM9fX4WBfmSjn+EzlrHLdeRS22h
| nTPirvuT+5nn6xbUrq9J6RCTZJD+uFc9wZl7Viw3hJcWbsO8DTQAshuZ5YJ574pG
| HjyoVDOfYhy8/8ThvYf1H8/OaIpG4UIo0vY9qeBQBOPZdbdVjWNerkFmXVq+MMVf
| pAt+FffQE/48kTCppuSKeM5ZMgHP1/zhZqyJ3npljVDlgppjvh1loSYB+reMkhwK
| 2gpGJNwxLyFDhTMLaj0pzFL9okqs5ovEWEj8p96hEE6Xxl4ZApv6mxTs9j2oY6+P
| MTUqFyYKchFUeYlgf7k=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:13+00:00; +1s from scanner time.
2179/tcp open  vmrdp?              syn-ack
3268/tcp open  ldap                syn-ack Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:selfservice.windcorp.thm, DNS:selfservice.dev.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-29T03:31:08
| Not valid after:  2028-05-29T03:41:03
| MD5:   804b dc39 5ce5 dd7b 19a5 851c 01d1 23ad
| SHA-1: 37f4 e667 cef7 5cc4 47c9 d201 25cf 2b7d 20b2 c1f4
| -----BEGIN CERTIFICATE-----
| MIIDajCCAlKgAwIBAgIQUI2QvXTCj7RCVdv6XlGMvjANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTAeFw0yMDA1MjkwMzMxMDhaFw0y
| ODA1MjkwMzQxMDNaMBwxGjAYBgNVBAMMEWZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAv900af0f6n80F0J6U9jMgcwQrozr
| kXmi02esW1XAsHpWnuuMQDIN6AtiYmDcoFEXz/NteLI7T6PusqQ6SXqLBurTnR8V
| InPD3Qea6lxOXNjuNeqqZKHhUaXiwSaqtAB+GzPkNtevw3jeEj99ST/G1qwY9Xce
| sfeqR2J4kQ+8U5yKLJDPBxOSx3+SHjKErrLTk66lrlEi4atr+P/ccXA5TBkZFkYh
| i3YdKTDnYeP2fMrqvOqpw82eniHAGJ2N8JJbNep86ps8giIRieBUUclF/WCp4c33
| p4i1ioVxJIYJj6f0tjGhy9GxB7l69OtUutcIG0/FhxL2dQ86MmnHH0dE7QIDAQAB
| o4GnMIGkMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYB
| BQUHAwEwVAYDVR0RBE0wS4IRZmlyZS53aW5kY29ycC50aG2CGHNlbGZzZXJ2aWNl
| LndpbmRjb3JwLnRobYIcc2VsZnNlcnZpY2UuZGV2LndpbmRjb3JwLnRobTAdBgNV
| HQ4EFgQUIZvYlCIhAOFLRutycf6U2H6LhqIwDQYJKoZIhvcNAQELBQADggEBAKVC
| ZS6HOuSODERi/glj3rPJaHCStxHPEg69txOIDaM9fX4WBfmSjn+EzlrHLdeRS22h
| nTPirvuT+5nn6xbUrq9J6RCTZJD+uFc9wZl7Viw3hJcWbsO8DTQAshuZ5YJ574pG
| HjyoVDOfYhy8/8ThvYf1H8/OaIpG4UIo0vY9qeBQBOPZdbdVjWNerkFmXVq+MMVf
| pAt+FffQE/48kTCppuSKeM5ZMgHP1/zhZqyJ3npljVDlgppjvh1loSYB+reMkhwK
| 2gpGJNwxLyFDhTMLaj0pzFL9okqs5ovEWEj8p96hEE6Xxl4ZApv6mxTs9j2oY6+P
| MTUqFyYKchFUeYlgf7k=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:14+00:00; +1s from scanner time.
3269/tcp open  ssl/ldap            syn-ack Microsoft Windows Active Directory LDAP (Domain: windcorp.thm0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:selfservice.windcorp.thm, DNS:selfservice.dev.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-29T03:31:08
| Not valid after:  2028-05-29T03:41:03
| MD5:   804b dc39 5ce5 dd7b 19a5 851c 01d1 23ad
| SHA-1: 37f4 e667 cef7 5cc4 47c9 d201 25cf 2b7d 20b2 c1f4
| -----BEGIN CERTIFICATE-----
| MIIDajCCAlKgAwIBAgIQUI2QvXTCj7RCVdv6XlGMvjANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTAeFw0yMDA1MjkwMzMxMDhaFw0y
| ODA1MjkwMzQxMDNaMBwxGjAYBgNVBAMMEWZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAv900af0f6n80F0J6U9jMgcwQrozr
| kXmi02esW1XAsHpWnuuMQDIN6AtiYmDcoFEXz/NteLI7T6PusqQ6SXqLBurTnR8V
| InPD3Qea6lxOXNjuNeqqZKHhUaXiwSaqtAB+GzPkNtevw3jeEj99ST/G1qwY9Xce
| sfeqR2J4kQ+8U5yKLJDPBxOSx3+SHjKErrLTk66lrlEi4atr+P/ccXA5TBkZFkYh
| i3YdKTDnYeP2fMrqvOqpw82eniHAGJ2N8JJbNep86ps8giIRieBUUclF/WCp4c33
| p4i1ioVxJIYJj6f0tjGhy9GxB7l69OtUutcIG0/FhxL2dQ86MmnHH0dE7QIDAQAB
| o4GnMIGkMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAgYIKwYB
| BQUHAwEwVAYDVR0RBE0wS4IRZmlyZS53aW5kY29ycC50aG2CGHNlbGZzZXJ2aWNl
| LndpbmRjb3JwLnRobYIcc2VsZnNlcnZpY2UuZGV2LndpbmRjb3JwLnRobTAdBgNV
| HQ4EFgQUIZvYlCIhAOFLRutycf6U2H6LhqIwDQYJKoZIhvcNAQELBQADggEBAKVC
| ZS6HOuSODERi/glj3rPJaHCStxHPEg69txOIDaM9fX4WBfmSjn+EzlrHLdeRS22h
| nTPirvuT+5nn6xbUrq9J6RCTZJD+uFc9wZl7Viw3hJcWbsO8DTQAshuZ5YJ574pG
| HjyoVDOfYhy8/8ThvYf1H8/OaIpG4UIo0vY9qeBQBOPZdbdVjWNerkFmXVq+MMVf
| pAt+FffQE/48kTCppuSKeM5ZMgHP1/zhZqyJ3npljVDlgppjvh1loSYB+reMkhwK
| 2gpGJNwxLyFDhTMLaj0pzFL9okqs5ovEWEj8p96hEE6Xxl4ZApv6mxTs9j2oY6+P
| MTUqFyYKchFUeYlgf7k=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:14+00:00; +2s from scanner time.
3389/tcp open  ms-wbt-server       syn-ack Microsoft Terminal Services
| rdp-ntlm-info: 
|   Target_Name: WINDCORP
|   NetBIOS_Domain_Name: WINDCORP
|   NetBIOS_Computer_Name: FIRE
|   DNS_Domain_Name: windcorp.thm
|   DNS_Computer_Name: Fire.windcorp.thm
|   DNS_Tree_Name: windcorp.thm
|   Product_Version: 10.0.17763
|_  System_Time: 2021-09-11T20:21:32+00:00
| ssl-cert: Subject: commonName=Fire.windcorp.thm
| Issuer: commonName=Fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2021-09-10T20:20:10
| Not valid after:  2022-03-12T20:20:10
| MD5:   1b0f 7f75 ee7e e15f 8562 40ee 26d6 a23a
| SHA-1: a083 d48b 0747 dc83 54a5 b09f 4f59 3b67 7bc8 a34c
| -----BEGIN CERTIFICATE-----
| MIIC5jCCAc6gAwIBAgIQLJ2YioKpgKJFsT5cK9NmujANBgkqhkiG9w0BAQsFADAc
| MRowGAYDVQQDExFGaXJlLndpbmRjb3JwLnRobTAeFw0yMTA5MTAyMDIwMTBaFw0y
| MjAzMTIyMDIwMTBaMBwxGjAYBgNVBAMTEUZpcmUud2luZGNvcnAudGhtMIIBIjAN
| BgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAsWRaSKCPBwvrBZ1ZahSrkuw8obXj
| YcOWrtNeeDZodO9ejE5EsuDHbYyVecvCSkdffYCIRzQmBMldkcBK6ue+p3M3xPFz
| UyB7XRiVWPVtRjshESPLvtIS3/bsIoi+J6+2aJhPeqg6A0t+PFjcT3fgfPi/jKWI
| EvY4ktf57d8n1BPTrNYvDcu91mU1kp403qLJmVhyQRHQTefY3sQdh5DAAEie267I
| WAWcCAjoj5iHbXLGoUtUpbFbRSoxt/a33EoyDlqQeJHo4IUog7KGXQDx8GMZRuK0
| Wc1h6C6e7Qb88gdyrj4lj7hb2YKT5EQdORV1ZXh4SKXLXlK9KEnl/FYYUQIDAQAB
| oyQwIjATBgNVHSUEDDAKBggrBgEFBQcDATALBgNVHQ8EBAMCBDAwDQYJKoZIhvcN
| AQELBQADggEBAJEOCT7Nj/6F/iO0/B6+SUJUTLdaCcwPxWpjoipSdvwaCPcsMWMm
| bgQ/5phl/vG8GKXjCdWxmuuwRvCAFgd5R9vqfGlFu4QFT4tRibGGmotHzw8Mi9DT
| bii2If/COxHSbJcG8bziV2pDkATX4OiptYn22pjR3EkfOk+alGv+N6Ij3tVyQZuM
| x6bQuhS3LhCcFtM+aKAIG3ocn4zL7F+GR9xqMcZwu0Mw2Io3J9uSwhJO1IPV78BF
| qegHU9b4Yo949f4JWMHIbXu9C/nfHZ1uCl3D3kE89nugPhXbhWWIZUPKnBOWIIWx
| nNL806xmhsF6tBSnSeJiTQJ/AsT4EytILnA=
|_-----END CERTIFICATE-----
|_ssl-date: 2021-09-11T20:22:14+00:00; +2s from scanner time.
5222/tcp open  jabber              syn-ack Ignite Realtime Openfire Jabber server 3.10.0 or later
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-01T08:39:00
| Not valid after:  2025-04-30T08:39:00
| MD5:   b715 5425 83f3 a20f 75c8 ca2d 3353 cbb7
| SHA-1: 97f7 0772 a26b e324 7ed5 bbcb 5f35 7d74 7982 66ae
| -----BEGIN CERTIFICATE-----
| MIIDLzCCAhegAwIBAgIIXUFELG7QgAIwDQYJKoZIhvcNAQELBQAwHDEaMBgGA1UE
| AwwRZmlyZS53aW5kY29ycC50aG0wHhcNMjAwNTAxMDgzOTAwWhcNMjUwNDMwMDgz
| OTAwWjAcMRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTCCASIwDQYJKoZIhvcN
| AQEBBQADggEPADCCAQoCggEBAKLH0/j17RVdD8eXC+0IFovAoql2REjOSf2NpJLK
| /6fgtx3CA4ftLsj7yOpmj8Oe1gqfWd2EM/zKk+ZmZwQFxLQL93t1OD/za1gyclxr
| IVbPVWqFoM2BUU9O3yU0VVRGP7xKDHm4bcoNmq9UNurEtFlCNeCC1fcwzfYvKD89
| X04Rv/6kn1GlQq/iM8PGCLDUf1p1WJcwGT5FUiBa9boTU9llBcGqbodZaBKzPPP8
| DmvSYF71IKBT8NsVzqiAiO3t/oHgApvUd9BqdbZeN46XORrOhBQV0xUpNVy9L5OE
| UAD1so3ePTNjpPE5SfTKymT1a8Fiw5kroKODN0nzy50yP3UCAwEAAaN1MHMwMQYD
| VR0RBCowKIIRZmlyZS53aW5kY29ycC50aG2CEyouZmlyZS53aW5kY29ycC50aG0w
| HQYDVR0OBBYEFOtMzqgfsY11qewZNfPjiLxnGykGMB8GA1UdIwQYMBaAFOtMzqgf
| sY11qewZNfPjiLxnGykGMA0GCSqGSIb3DQEBCwUAA4IBAQAHofv0VP+hE+5sg0KR
| 2x0Xeg4cIXEia0c5cIJ7K7bhfoLOcT7WcMKCLIN3A416PREdkB6Q610uDs8RpezJ
| II/wBoIp2G0Y87X3Xo5FmNJjl9lGX5fvayen98khPXvZkurHdWdtA4m8pHOdYOrk
| n8Jth6L/y4L5WlgEGL0x0HK4yvd3iz0VNrc810HugpyfVWeasChhZjgAYXUVlA8k
| +QxLxyNr/PBfRumQGzw2n3msXxwfHVzaHphy56ph85PcRS35iNqgrtK0fe3Qhpq7
| v5vQYKlOGq5FI6Mf9ni7S1pXSqF4U9wuqZy4q4tXWAVootmJv1DIgfSMLvXplN9T
| LucP
|_-----END CERTIFICATE-----
| xmpp-info: 
|   STARTTLS Failed
|   info: 
|     unknown: 
| 
|     errors: 
|       invalid-namespace
|       (timeout)
|     compression_methods: 
| 
|     auth_mechanisms: 
| 
|     capabilities: 
| 
|     stream_id: umiwpol6q
|     features: 
| 
|     xmpp: 
|_      version: 1.0
5269/tcp open  xmpp                syn-ack Wildfire XMPP Client
| xmpp-info: 
|   Respects server name
|   STARTTLS Failed
|   info: 
|     unknown: 
| 
|     errors: 
|       host-unknown
|       (timeout)
|     compression_methods: 
| 
|     auth_mechanisms: 
| 
|     capabilities: 
| 
|     stream_id: 4c98rbx41p
|     features: 
| 
|     xmpp: 
|_      version: 1.0
7070/tcp open  http                syn-ack Jetty 9.4.18.v20190429
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Jetty(9.4.18.v20190429)
|_http-title: Openfire HTTP Binding Service
7443/tcp open  ssl/http            syn-ack Jetty 9.4.18.v20190429
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Jetty(9.4.18.v20190429)
|_http-title: Openfire HTTP Binding Service
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-01T08:39:00
| Not valid after:  2025-04-30T08:39:00
| MD5:   b715 5425 83f3 a20f 75c8 ca2d 3353 cbb7
| SHA-1: 97f7 0772 a26b e324 7ed5 bbcb 5f35 7d74 7982 66ae
| -----BEGIN CERTIFICATE-----
| MIIDLzCCAhegAwIBAgIIXUFELG7QgAIwDQYJKoZIhvcNAQELBQAwHDEaMBgGA1UE
| AwwRZmlyZS53aW5kY29ycC50aG0wHhcNMjAwNTAxMDgzOTAwWhcNMjUwNDMwMDgz
| OTAwWjAcMRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTCCASIwDQYJKoZIhvcN
| AQEBBQADggEPADCCAQoCggEBAKLH0/j17RVdD8eXC+0IFovAoql2REjOSf2NpJLK
| /6fgtx3CA4ftLsj7yOpmj8Oe1gqfWd2EM/zKk+ZmZwQFxLQL93t1OD/za1gyclxr
| IVbPVWqFoM2BUU9O3yU0VVRGP7xKDHm4bcoNmq9UNurEtFlCNeCC1fcwzfYvKD89
| X04Rv/6kn1GlQq/iM8PGCLDUf1p1WJcwGT5FUiBa9boTU9llBcGqbodZaBKzPPP8
| DmvSYF71IKBT8NsVzqiAiO3t/oHgApvUd9BqdbZeN46XORrOhBQV0xUpNVy9L5OE
| UAD1so3ePTNjpPE5SfTKymT1a8Fiw5kroKODN0nzy50yP3UCAwEAAaN1MHMwMQYD
| VR0RBCowKIIRZmlyZS53aW5kY29ycC50aG2CEyouZmlyZS53aW5kY29ycC50aG0w
| HQYDVR0OBBYEFOtMzqgfsY11qewZNfPjiLxnGykGMB8GA1UdIwQYMBaAFOtMzqgf
| sY11qewZNfPjiLxnGykGMA0GCSqGSIb3DQEBCwUAA4IBAQAHofv0VP+hE+5sg0KR
| 2x0Xeg4cIXEia0c5cIJ7K7bhfoLOcT7WcMKCLIN3A416PREdkB6Q610uDs8RpezJ
| II/wBoIp2G0Y87X3Xo5FmNJjl9lGX5fvayen98khPXvZkurHdWdtA4m8pHOdYOrk
| n8Jth6L/y4L5WlgEGL0x0HK4yvd3iz0VNrc810HugpyfVWeasChhZjgAYXUVlA8k
| +QxLxyNr/PBfRumQGzw2n3msXxwfHVzaHphy56ph85PcRS35iNqgrtK0fe3Qhpq7
| v5vQYKlOGq5FI6Mf9ni7S1pXSqF4U9wuqZy4q4tXWAVootmJv1DIgfSMLvXplN9T
| LucP
|_-----END CERTIFICATE-----
7777/tcp open  socks5              syn-ack (No authentication; connection failed)
| socks-auth-info: 
|_  No authentication
9090/tcp open  zeus-admin?         syn-ack
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Date: Sat, 11 Sep 2021 20:20:52 GMT
|     Last-Modified: Fri, 31 Jan 2020 17:54:10 GMT
|     Content-Type: text/html
|     Accept-Ranges: bytes
|     Content-Length: 115
|     <html>
|     <head><title></title>
|     <meta http-equiv="refresh" content="0;URL=index.jsp">
|     </head>
|     <body>
|     </body>
|     </html>
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Date: Sat, 11 Sep 2021 20:20:57 GMT
|     Allow: GET,HEAD,POST,OPTIONS
|   JavaRMI, drda, ibm-db2-das, informix: 
|     HTTP/1.1 400 Illegal character CNTL=0x0
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x0</pre>
|   SqueezeCenter_CLI: 
|     HTTP/1.1 400 No URI
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 49
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: No URI</pre>
|   WMSRequest: 
|     HTTP/1.1 400 Illegal character CNTL=0x1
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|_    <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x1</pre>
9091/tcp open  ssl/xmltec-xmlmail? syn-ack
| fingerprint-strings: 
|   DNSStatusRequestTCP, DNSVersionBindReqTCP: 
|     HTTP/1.1 400 Illegal character CNTL=0x0
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 69
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x0</pre>
|   GetRequest: 
|     HTTP/1.1 200 OK
|     Date: Sat, 11 Sep 2021 20:21:15 GMT
|     Last-Modified: Fri, 31 Jan 2020 17:54:10 GMT
|     Content-Type: text/html
|     Accept-Ranges: bytes
|     Content-Length: 115
|     <html>
|     <head><title></title>
|     <meta http-equiv="refresh" content="0;URL=index.jsp">
|     </head>
|     <body>
|     </body>
|     </html>
|   HTTPOptions: 
|     HTTP/1.1 200 OK
|     Date: Sat, 11 Sep 2021 20:21:15 GMT
|     Allow: GET,HEAD,POST,OPTIONS
|   Help: 
|     HTTP/1.1 400 No URI
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 49
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: No URI</pre>
|   RPCCheck: 
|     HTTP/1.1 400 Illegal character OTEXT=0x80
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 71
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Illegal character OTEXT=0x80</pre>
|   RTSPRequest: 
|     HTTP/1.1 400 Unknown Version
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 58
|     Connection: close
|     <h1>Bad Message 400</h1><pre>reason: Unknown Version</pre>
|   SSLSessionReq: 
|     HTTP/1.1 400 Illegal character CNTL=0x16
|     Content-Type: text/html;charset=iso-8859-1
|     Content-Length: 70
|     Connection: close
|_    <h1>Bad Message 400</h1><pre>reason: Illegal character CNTL=0x16</pre>
| ssl-cert: Subject: commonName=fire.windcorp.thm
| Subject Alternative Name: DNS:fire.windcorp.thm, DNS:*.fire.windcorp.thm
| Issuer: commonName=fire.windcorp.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-05-01T08:39:00
| Not valid after:  2025-04-30T08:39:00
| MD5:   b715 5425 83f3 a20f 75c8 ca2d 3353 cbb7
| SHA-1: 97f7 0772 a26b e324 7ed5 bbcb 5f35 7d74 7982 66ae
| -----BEGIN CERTIFICATE-----
| MIIDLzCCAhegAwIBAgIIXUFELG7QgAIwDQYJKoZIhvcNAQELBQAwHDEaMBgGA1UE
| AwwRZmlyZS53aW5kY29ycC50aG0wHhcNMjAwNTAxMDgzOTAwWhcNMjUwNDMwMDgz
| OTAwWjAcMRowGAYDVQQDDBFmaXJlLndpbmRjb3JwLnRobTCCASIwDQYJKoZIhvcN
| AQEBBQADggEPADCCAQoCggEBAKLH0/j17RVdD8eXC+0IFovAoql2REjOSf2NpJLK
| /6fgtx3CA4ftLsj7yOpmj8Oe1gqfWd2EM/zKk+ZmZwQFxLQL93t1OD/za1gyclxr
| IVbPVWqFoM2BUU9O3yU0VVRGP7xKDHm4bcoNmq9UNurEtFlCNeCC1fcwzfYvKD89
| X04Rv/6kn1GlQq/iM8PGCLDUf1p1WJcwGT5FUiBa9boTU9llBcGqbodZaBKzPPP8
| DmvSYF71IKBT8NsVzqiAiO3t/oHgApvUd9BqdbZeN46XORrOhBQV0xUpNVy9L5OE
| UAD1so3ePTNjpPE5SfTKymT1a8Fiw5kroKODN0nzy50yP3UCAwEAAaN1MHMwMQYD
| VR0RBCowKIIRZmlyZS53aW5kY29ycC50aG2CEyouZmlyZS53aW5kY29ycC50aG0w
| HQYDVR0OBBYEFOtMzqgfsY11qewZNfPjiLxnGykGMB8GA1UdIwQYMBaAFOtMzqgf
| sY11qewZNfPjiLxnGykGMA0GCSqGSIb3DQEBCwUAA4IBAQAHofv0VP+hE+5sg0KR
| 2x0Xeg4cIXEia0c5cIJ7K7bhfoLOcT7WcMKCLIN3A416PREdkB6Q610uDs8RpezJ
| II/wBoIp2G0Y87X3Xo5FmNJjl9lGX5fvayen98khPXvZkurHdWdtA4m8pHOdYOrk
| n8Jth6L/y4L5WlgEGL0x0HK4yvd3iz0VNrc810HugpyfVWeasChhZjgAYXUVlA8k
| +QxLxyNr/PBfRumQGzw2n3msXxwfHVzaHphy56ph85PcRS35iNqgrtK0fe3Qhpq7
| v5vQYKlOGq5FI6Mf9ni7S1pXSqF4U9wuqZy4q4tXWAVootmJv1DIgfSMLvXplN9T
| LucP
|_-----END CERTIFICATE-----
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port9090-TCP:V=7.91%I=7%D=9/11%Time=613D0FA2%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,11D,"HTTP/1\.1\x20200\x20OK\r\nDate:\x20Sat,\x2011\x20Sep\x202
SF:021\x2020:20:52\x20GMT\r\nLast-Modified:\x20Fri,\x2031\x20Jan\x202020\x
SF:2017:54:10\x20GMT\r\nContent-Type:\x20text/html\r\nAccept-Ranges:\x20by
SF:tes\r\nContent-Length:\x20115\r\n\r\n<html>\n<head><title></title>\n<me
SF:ta\x20http-equiv=\"refresh\"\x20content=\"0;URL=index\.jsp\">\n</head>\
SF:n<body>\n</body>\n</html>\n\n")%r(JavaRMI,C3,"HTTP/1\.1\x20400\x20Illeg
SF:al\x20character\x20CNTL=0x0\r\nContent-Type:\x20text/html;charset=iso-8
SF:859-1\r\nContent-Length:\x2069\r\nConnection:\x20close\r\n\r\n<h1>Bad\x
SF:20Message\x20400</h1><pre>reason:\x20Illegal\x20character\x20CNTL=0x0</
SF:pre>")%r(WMSRequest,C3,"HTTP/1\.1\x20400\x20Illegal\x20character\x20CNT
SF:L=0x1\r\nContent-Type:\x20text/html;charset=iso-8859-1\r\nContent-Lengt
SF:h:\x2069\r\nConnection:\x20close\r\n\r\n<h1>Bad\x20Message\x20400</h1><
SF:pre>reason:\x20Illegal\x20character\x20CNTL=0x1</pre>")%r(ibm-db2-das,C
SF:3,"HTTP/1\.1\x20400\x20Illegal\x20character\x20CNTL=0x0\r\nContent-Type
SF::\x20text/html;charset=iso-8859-1\r\nContent-Length:\x2069\r\nConnectio
SF:n:\x20close\r\n\r\n<h1>Bad\x20Message\x20400</h1><pre>reason:\x20Illega
SF:l\x20character\x20CNTL=0x0</pre>")%r(SqueezeCenter_CLI,9B,"HTTP/1\.1\x2
SF:0400\x20No\x20URI\r\nContent-Type:\x20text/html;charset=iso-8859-1\r\nC
SF:ontent-Length:\x2049\r\nConnection:\x20close\r\n\r\n<h1>Bad\x20Message\
SF:x20400</h1><pre>reason:\x20No\x20URI</pre>")%r(informix,C3,"HTTP/1\.1\x
SF:20400\x20Illegal\x20character\x20CNTL=0x0\r\nContent-Type:\x20text/html
SF:;charset=iso-8859-1\r\nContent-Length:\x2069\r\nConnection:\x20close\r\
SF:n\r\n<h1>Bad\x20Message\x20400</h1><pre>reason:\x20Illegal\x20character
SF:\x20CNTL=0x0</pre>")%r(drda,C3,"HTTP/1\.1\x20400\x20Illegal\x20characte
SF:r\x20CNTL=0x0\r\nContent-Type:\x20text/html;charset=iso-8859-1\r\nConte
SF:nt-Length:\x2069\r\nConnection:\x20close\r\n\r\n<h1>Bad\x20Message\x204
SF:00</h1><pre>reason:\x20Illegal\x20character\x20CNTL=0x0</pre>")%r(HTTPO
SF:ptions,56,"HTTP/1\.1\x20200\x20OK\r\nDate:\x20Sat,\x2011\x20Sep\x202021
SF:\x2020:20:57\x20GMT\r\nAllow:\x20GET,HEAD,POST,OPTIONS\r\n\r\n");
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port9091-TCP:V=7.91%T=SSL%I=7%D=9/11%Time=613D0FB9%P=x86_64-pc-linux-gn
SF:u%r(GetRequest,11D,"HTTP/1\.1\x20200\x20OK\r\nDate:\x20Sat,\x2011\x20Se
SF:p\x202021\x2020:21:15\x20GMT\r\nLast-Modified:\x20Fri,\x2031\x20Jan\x20
SF:2020\x2017:54:10\x20GMT\r\nContent-Type:\x20text/html\r\nAccept-Ranges:
SF:\x20bytes\r\nContent-Length:\x20115\r\n\r\n<html>\n<head><title></title
SF:>\n<meta\x20http-equiv=\"refresh\"\x20content=\"0;URL=index\.jsp\">\n</
SF:head>\n<body>\n</body>\n</html>\n\n")%r(HTTPOptions,56,"HTTP/1\.1\x2020
SF:0\x20OK\r\nDate:\x20Sat,\x2011\x20Sep\x202021\x2020:21:15\x20GMT\r\nAll
SF:ow:\x20GET,HEAD,POST,OPTIONS\r\n\r\n")%r(RTSPRequest,AD,"HTTP/1\.1\x204
SF:00\x20Unknown\x20Version\r\nContent-Type:\x20text/html;charset=iso-8859
SF:-1\r\nContent-Length:\x2058\r\nConnection:\x20close\r\n\r\n<h1>Bad\x20M
SF:essage\x20400</h1><pre>reason:\x20Unknown\x20Version</pre>")%r(RPCCheck
SF:,C7,"HTTP/1\.1\x20400\x20Illegal\x20character\x20OTEXT=0x80\r\nContent-
SF:Type:\x20text/html;charset=iso-8859-1\r\nContent-Length:\x2071\r\nConne
SF:ction:\x20close\r\n\r\n<h1>Bad\x20Message\x20400</h1><pre>reason:\x20Il
SF:legal\x20character\x20OTEXT=0x80</pre>")%r(DNSVersionBindReqTCP,C3,"HTT
SF:P/1\.1\x20400\x20Illegal\x20character\x20CNTL=0x0\r\nContent-Type:\x20t
SF:ext/html;charset=iso-8859-1\r\nContent-Length:\x2069\r\nConnection:\x20
SF:close\r\n\r\n<h1>Bad\x20Message\x20400</h1><pre>reason:\x20Illegal\x20c
SF:haracter\x20CNTL=0x0</pre>")%r(DNSStatusRequestTCP,C3,"HTTP/1\.1\x20400
SF:\x20Illegal\x20character\x20CNTL=0x0\r\nContent-Type:\x20text/html;char
SF:set=iso-8859-1\r\nContent-Length:\x2069\r\nConnection:\x20close\r\n\r\n
SF:<h1>Bad\x20Message\x20400</h1><pre>reason:\x20Illegal\x20character\x20C
SF:NTL=0x0</pre>")%r(Help,9B,"HTTP/1\.1\x20400\x20No\x20URI\r\nContent-Typ
SF:e:\x20text/html;charset=iso-8859-1\r\nContent-Length:\x2049\r\nConnecti
SF:on:\x20close\r\n\r\n<h1>Bad\x20Message\x20400</h1><pre>reason:\x20No\x2
SF:0URI</pre>")%r(SSLSessionReq,C5,"HTTP/1\.1\x20400\x20Illegal\x20charact
SF:er\x20CNTL=0x16\r\nContent-Type:\x20text/html;charset=iso-8859-1\r\nCon
SF:tent-Length:\x2070\r\nConnection:\x20close\r\n\r\n<h1>Bad\x20Message\x2
SF:0400</h1><pre>reason:\x20Illegal\x20character\x20CNTL=0x16</pre>");
Service Info: Host: FIRE; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 1s, deviation: 0s, median: 0s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 23815/tcp): CLEAN (Timeout)
|   Check 2 (port 12583/tcp): CLEAN (Timeout)
|   Check 3 (port 17187/udp): CLEAN (Timeout)
|   Check 4 (port 13589/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2021-09-11T20:21:34
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Sep 11 21:22:14 2021 -- 1 IP address (1 host up) scanned in 94.18 seconds
```