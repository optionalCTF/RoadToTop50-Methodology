# Enumeration

Initially we can identify that we were in a docker container

Running 
`find / -perm -4500 2>/dev/null`

We can identify that the 
`env` binary has a suid bit allowing privilege escalation to root within the container

`env /bin/bash -i -p` 

Once we have root we able to run deepce which will identify any potential break out vectors.

In this instance it reveals that there were mount points to the host via `/opt/backups`
and that there is a cron running the `backup.sh` script within. 

We able to override that with our own malicious code. In this instance we input a bash reverse shell.

We then wait until the cron fires (every minute), which lands a root shell.
