## NMAP Scan
![[Boxes/ra2/Enumeration/NMAP]]


![[Boxes/ra2/Enumeration/USERLIST]]

## Noteworthy 
- selfservice vhost has basic auth.
- NMAP discovered an additional vhost `selfservice.dev.windcorp.thm`
	- Fuzzing this returned a cert.pfx which was cracked to get the password `ganteng`


We are able to pull certificates from the `cert.pfx` file using this article 
[https://www.ibm.com/docs/en/arl/9.7?topic=certification-extracting-certificate-keys-from-pfx-file](https://www.ibm.com/docs/en/arl/9.7?topic=certification-extracting-certificate-keys-from-pfx-file)


Even better because IBM suck
[https://www.ssl.com/how-to/export-certificates-private-key-from-pkcs12-file-with-openssl/](https://www.ssl.com/how-to/export-certificates-private-key-from-pkcs12-file-with-openssl/)


