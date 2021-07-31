Basic fuff syntax for directory brute forcing

## Directory Brute Force
`ffuf -u http/s://<URL>/FUZZ -w <WORDLIST>`

You can filter out responses with `-fc <RESPONSE CODE>`

You may have hidden responses in which you can do `-mc all`

## Sub-domain enumeration
`ffuf -u http/s://<URL> -H "Host: FUZZ.<URL>" -w <WORDLIST>`