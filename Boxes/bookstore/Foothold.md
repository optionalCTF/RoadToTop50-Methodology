# Foothold
Initial recon shows an API endpoint in api.js

When going to port 5000/api we are given a bunch of v2 endpoints. 

By changing that to v1 and fuzzing the books endpoint, we find a hidden parameter called `?show` 
This is vulnerable to LFI as hinted in `api.js`


This does not work:
```
We can use this LFI to create our own werkzeug pin 
username - sid
modname - flask.app
machine id - d86a656616e9492d93f4ab7905f44292

address - 02:53:61:5c:3f:2b
Returned address -2557138976555
```

Turns out the above is a rabbit hole I fell into. Infact by fuzzing what is in the sid home directory we find `.bash_history` contains the pin...
`/home/sid/bash_history`
```
cd /home/sid
whoami
export WERKZEUG_DEBUG_PIN=123-321-135
echo $WERKZEUG_DEBUG_PIN
python3 /home/sid/api.py
ls
exit
```