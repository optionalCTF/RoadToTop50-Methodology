## Manual Enumeration (ROOT SUID)

A quick way of enumerating SUID root binaries is with
`find / -perm -4500 2>/dev/null`

Once you have the list of these you can check [gtfobins.github.io/](gtfobins.github.io/) for a list of binaries with known privilege escalation vectors.