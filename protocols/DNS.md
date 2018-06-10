# DNS on TCP

Only need for exposing DNS over TCP when response is > 512 bytes
* zone-transfers.
* DNSSec
* IPv6

# DNS Zone Transfer

`dig axfr IP_OF_DNS_SERVER example.com`

# DNS query

`dig @IP_OF_DNS_SERVER example.com`

# DNS cache poisoning

`dnsspoof -i eth0 -f hosts.txt`

hosts.txt
```
192.168.1.111 example.com
```
