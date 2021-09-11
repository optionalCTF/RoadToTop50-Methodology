## top1000
```
# Nmap 7.91 scan initiated Sat Sep 11 19:24:36 2021 as: nmap -vv -oN scans/nmap -sC -sV 10.10.175.250
Nmap scan report for 10.10.175.250
Host is up, received syn-ack (0.039s latency).
Scanned at 2021-09-11 19:24:36 BST for 18s
Not shown: 959 closed ports
Reason: 959 conn-refused
PORT      STATE SERVICE       REASON  VERSION
22/tcp    open  ssh           syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 d7:ec:1a:7f:62:74:da:29:64:b3:ce:1e:e2:68:04:f7 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDBR1uDh8+UHIoUl3J5AJApSgrmxFtvWtauxjTLxH9B5s9E0SThz3fljXo7uSL+2hjphfHyqrdAxoCGQJgRn/o5xGDSpoSoORBIxv1LVaZJlt/eIEhjDP48NP9l/wTRki9zZl5sNVyyyy/lobAj6BYH+dU3g++2su9Wcl0wmFChG5B2Kjrd9VSr6TC0XJpGfQxu+xJy29XtoTzKEiZCoLz3mZT7UqwsSgk38aZjEMKP9QDc0oa5v4JmKy4ikaR90CAcey9uIq8YQtSj+US7hteruG/HLo1AmOn9U3JAsVTd4vI1kp+Uu2vWLaWWjhfPqvbKEV/fravKSPd0EQJmg1eJ
|   256 de:4f:ee:fa:86:2e:fb:bd:4c:dc:f9:67:73:02:84:34 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBKFhVdH50NAu45yKvSeeMqyvWl1aCZ1wyrHw2MzGY5DVosjZf/rUzrdDRS0u9QoIO4MpQAvEi7w7YG7zajosRN8=
|   256 e2:6d:8d:e1:a8:d0:bd:97:cb:9a:bc:03:c3:f8:d8:85 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIAdzynTIlsSkYKaqfCAdSx5J2nfdoWFw1FcpKFIF8LRv
23/tcp    open  tcpwrapped    syn-ack
25/tcp    open  tcpwrapped    syn-ack
|_smtp-commands: Couldn't establish connection on port 25
80/tcp    open  http          syn-ack Apache httpd 2.4.29 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Dante's Inferno
88/tcp    open  tcpwrapped    syn-ack
106/tcp   open  pop3pw?       syn-ack
110/tcp   open  tcpwrapped    syn-ack
389/tcp   open  tcpwrapped    syn-ack
443/tcp   open  tcpwrapped    syn-ack
464/tcp   open  tcpwrapped    syn-ack
636/tcp   open  tcpwrapped    syn-ack
777/tcp   open  tcpwrapped    syn-ack
783/tcp   open  tcpwrapped    syn-ack
808/tcp   open  ccproxy-http? syn-ack
873/tcp   open  tcpwrapped    syn-ack
1001/tcp  open  webpush?      syn-ack
1236/tcp  open  tcpwrapped    syn-ack
1300/tcp  open  tcpwrapped    syn-ack
2000/tcp  open  tcpwrapped    syn-ack
2003/tcp  open  tcpwrapped    syn-ack
2121/tcp  open  tcpwrapped    syn-ack
2601/tcp  open  tcpwrapped    syn-ack
2602/tcp  open  tcpwrapped    syn-ack
2604/tcp  open  tcpwrapped    syn-ack
2605/tcp  open  tcpwrapped    syn-ack
2607/tcp  open  tcpwrapped    syn-ack
2608/tcp  open  tcpwrapped    syn-ack
4224/tcp  open  tcpwrapped    syn-ack
5051/tcp  open  tcpwrapped    syn-ack
5432/tcp  open  tcpwrapped    syn-ack
5555/tcp  open  tcpwrapped    syn-ack
5666/tcp  open  tcpwrapped    syn-ack
6346/tcp  open  tcpwrapped    syn-ack
6566/tcp  open  tcpwrapped    syn-ack
6667/tcp  open  tcpwrapped    syn-ack
|_irc-info: Unable to open connection
8021/tcp  open  tcpwrapped    syn-ack
8081/tcp  open  tcpwrapped    syn-ack
|_mcafee-epo-agent: ePO Agent not found
8088/tcp  open  radan-http?   syn-ack
9418/tcp  open  tcpwrapped    syn-ack
10000/tcp open  tcpwrapped    syn-ack
10082/tcp open  tcpwrapped    syn-ack
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Sep 11 19:24:54 2021 -- 1 IP address (1 host up) scanned in 18.54 seconds
```
