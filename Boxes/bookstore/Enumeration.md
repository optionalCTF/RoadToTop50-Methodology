## NMAP Scans
[[Boxes/bookstore/Enumeration/NMAP]]

## API Endpoints
[[API.JS]]


From initial enumeration of the API.js file that we pulled from PORT 80

There is a comment that alerts us to a previous version of the API having an LFI vulnerability.

Further exploration of the port 5000, shows that this is the API.

We can find documentation on 
`http://10.10.154.17:5000/api` 


## API Funky Stuff
Because we are told an older version of the API was vulnerable, we can change the v2 in the api urls to see if v1 is valid.

Shock horror it is.

