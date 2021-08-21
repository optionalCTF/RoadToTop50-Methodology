## NMAP Scan
[[Boxes/0day/Enumeration/NMAP]]


## FFUF returns backup
We find an encrypted RSA token on `/backup`

We can brute force the password on it with ssh2john
`letmein`

We find a juicy lil cgi-bin 

fuzzing that returns test.cgi

This indicates we may be running it back and using shellshock. Everything seems to be pointing towards that, what with the cgi-bin directory and the turtle..

Running metasploit because we're kings, returns a nice lil shell.

