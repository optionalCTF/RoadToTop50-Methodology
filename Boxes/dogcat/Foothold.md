# Foothold
The first thing we notice within the dogcat web server running on port 80. Is that it is pulling values via the `?view` variable. 

With a little exploration we found that `?view=dog/../index.php` would append `.php` to our files. By using a php filter
`php://filter/convert.base64-encode/resource=dog/../index`

we are able to pull the source code. This reveals that there is another extension, that if not present will append `.php` by adding `&ext=` to our search, we can bypass that and pull files such as `/etc/passwd`

`dog/../../../../../../../etc/passwd&ext=`


