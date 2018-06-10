# IPv6 Link-Local Address from MAC (Linux)

* Start with fe80
* Invert 7th bit of MAC
* Add three groups
* Add ff fe
* Add Remaining three groups

MAC: `0050:56aa:8125`
Link local address: `fffe::0250:56ff:feaa:8125`

* MAC address can be observed with ARP table (`arp -n`) after doing a ping on desired host.

# Connect with Link Local

`pin6 fffe::0250:56ff:feaa:8125%interface_name`
`ssh example@fffe::0250:56ff:feaa:8125%interface_name`

# Check neighbors in IPv6 (similar to ARP in IPv4)

Do a multicast ping with
* `ping6 -I interface_name ff02::1`
* `ping6 -I interface_name dead:beef::feaa:8125 ff02:1` (source is dead:beef, destination is multicast)

`ip -6 neigh`

Windows does not respond to ping packets. Send an invalid ping packet to get windows to reply, saying invalida packet was received. Use `The Hackers Choice` `alive6`.
