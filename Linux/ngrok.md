## Usage

Ngrok allows you portforward without messing around with your router.

You can set up a simple nc listener such as `nc -lvnp 1234` and use ngrok to forward requests to this. 

You can do this with 
`ngrok tcp <port>`
or if you forwarding HTTP traffic you can use 
`ngrok http <port>`
