You can enumerate SMB shares as such

## SMBMAP 

`smbmap -H <IP> -u '<USER>' -p '<PASS>'`


## Smbclient

You are able to conntect to remote SMBs with smbclient. Syntax below
`smbclient \\\\<IP>\\<SHARENAME> -U <USER> -p '<PASS>'`