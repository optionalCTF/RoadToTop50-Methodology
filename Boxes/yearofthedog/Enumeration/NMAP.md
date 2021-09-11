# NMAP sC sV 
```
# Nmap 7.91 scan initiated Wed Sep  1 21:34:46 2021 as: nmap -sC -sV -oN scans/nmap -vv 10.10.20.68
Nmap scan report for 10.10.20.68
Host is up, received syn-ack (0.032s latency).
Scanned at 2021-09-01 21:34:47 BST for 8s
Not shown: 998 closed ports
Reason: 998 conn-refused
PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 e4:c9:dd:9b:db:95:9e:fd:19:a9:a6:0d:4c:43:9f:fa (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDrxDlZxvJUZk2qXaeBdjHxfM3MSGpZ8H6zPqgarnP3K806zE1Y/CryyT4wgIZYomtV8wUWHlFkuqbWjcKcM1MWcPjzGWfPZ2wHTNgUkHvBWZ+fxoX8vJoC6wfpifa7bSMaOItFWSLnMGOXigHbF6dPNyP+/kXAJE+tg9TurrTKaPiL6u+02ITeVUuLWsjwlLDJAnu1zDhPONR2b7WTcU/zQxHUYZiHpHn5eBtXpCZPZyfOZ+828ibobM/CAHIBZqJsYksAe5RbtDw7Vdw/8OtYuo4Koz8C2kBoWCHvsmyDfwZ57E2Ycss4JG5j7fMt7sI+lh/NHE+/7zrXdH/4njCD
|   256 c3:fc:10:d8:78:47:7e:fb:89:cf:81:8b:6e:f1:0a:fd (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBMlni4gM6dVkvfGeMy6eg/18HsCYvvFhbpycXiGYM3fitNhTXW4WpMpr8W/0y2FszEB6TGD93ib/lCTsBOQG5Uw=
|   256 27:68:ff:ef:c0:68:e2:49:75:59:34:f2:bd:f0:c9:20 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICQIHukp5WpajvhF4juRWmL2+YtbN9HbhgLScgqYNien
80/tcp open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Canis Queue
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Wed Sep  1 21:34:55 2021 -- 1 IP address (1 host up) scanned in 8.91 seconds
```
