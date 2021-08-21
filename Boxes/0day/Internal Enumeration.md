# Enumeration
`find / -perm -4500 2>/dev/null ` returns nothing fun to play with.

`cat /etc/crontab` - nothing interesting

Running the almighty pea, we find that the kernel is extremely out of date and vulnerable to a kernel exploit which gives us a root shell. 
[https://www.exploit-db.com/exploits/37292](https://www.exploit-db.com/exploits/37292)