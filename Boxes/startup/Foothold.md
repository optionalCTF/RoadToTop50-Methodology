# Foothold


## Noteworthy 
- Anonymous FTP  
- `/files/` directory indexing 


## Reverse Shell
Upon enumerating the anonymous ftp share, we have write access in a directory called `ftp`, we verify that we can upload and execute PHP on the web server by uploading a simple `info.php` file containing
```
<php
phpinfo();
?>
```
when navigating the web server, by going into `<ip>/files/ftp/info.php` we see that it executes. 


## Question 1 
`What is the secret spicy soup recipe?`
You can find the answer to this under the `/` in `recipe.txt`


## Escalating to User
under `/incidents` you will find a pcap which will contain the user password.

## User Credentials
`lennie:c4ntg3t3n0ughsp1c3`