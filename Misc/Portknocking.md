Port knocking is when you make connection requests to a number of ports in sequence to open another port. This is usually configured via knockd. 

## Simple Bash One Liner
`for PORT in <port list e.g 1111 2222>; do nc -vz <TARGET_IP> $PORT; done;`
