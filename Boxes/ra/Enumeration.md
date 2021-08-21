## NMAP Scans
[[Boxes/ra/Enumeration/NMAP]]


## Enum4Linux
[[Boxes/ra/Enumeration/ENUM4LINUX]]

-  Manual enumeration of usernames shows images which reveal both username and also a rat with the name sparky. This can be used to reset the password to 
-  `lilyle:<REDACTED>`

These can be used with smb to view shares
```
[+] IP: windcorp.thm:445        Name: unknown                                           
        Disk                                                    Permissions     Comment
        ----                                                    -----------     -------
        ADMIN$                                                  NO ACCESS       Remote Admin
        C$                                                      NO ACCESS       Default share
        IPC$                                                    READ ONLY       Remote IPC
        NETLOGON                                                READ ONLY       Logon server share 
        Shared                                                  READ ONLY
        SYSVOL                                                  READ ONLY       Logon server share 
        Users                                                   READ ONLY
```