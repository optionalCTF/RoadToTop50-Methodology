## Password Bruteforce
`crackmapexec smb <IP> -u <USERNAME/USERLIST> -p <PASSWORD/PASSLIST`

## RID Brute Force 
`crackmapexec smb <IP> --rid-brute`

**General note, RID brute force will potentially return differing users compared to RPC enumdomusers**

## MSSQL 
If the SMB protocol doesn't return authenticated users. You may be able to spray the MSSQL service for valid credentials **OR** gain a limited shell to read databases/exec system commands 
[[MSSQL]]