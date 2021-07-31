More commands can be found here
[https://redis.io/commands](https://redis.io/commands)

## Passwords
If you have access to the `redis.conf` file, you may be able to find a master password contained within. 

## Connection
Initiate a connection with 
`redis-cli -h <HOST>`

if you have a password you can throw on a `-a <password>`

## Dumping Keys
With any luck you'll be able to dump keys with
`KEYS *`

From this you can read these with 

`GET <KEY NAME>`

or in some instances they may be a list so 
`lrange <KEY NAME> -1`


