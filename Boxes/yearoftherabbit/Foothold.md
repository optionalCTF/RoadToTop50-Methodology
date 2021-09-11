# Foothold
## FTP User
`ftpuser:5iez1wGXKfPKQ`

## User
Within the FTP share we find a brainfuck file. 

Throwing that into an interpreter we get 

```
eli:DSpDiM1wAEwid
```

When we ssh in we get a message saying something hidden in s3cr3t place

Simple find command to grab that
`find / -name "s3cr3t" 2>/dev/null`

We  head to `/usr/games/s3cr3t`
there's a dot file which gives us the password

`Gwendoline:MniVCQVhQHUNI`
user.txt
`THM{1107174691af9ff3681d2b5bdb5740b1589bae53}`
