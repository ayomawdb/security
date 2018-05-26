# Scan Types

## TCP Connect Scan

* Full 3 way handshake
* `nc -nvv -w 1 -z <ip> <port-range>`

## SYN / Stealth Scan

* Send SYN
* SYN-ACK means open
* RST means closed

## UDP Scanning

* ICMP port unreachable means closed
* No response means open
* `nc -nv -u -z -w 1 <ip> <port-range>`

# Nmap

```
nmap -sV -sC -oA <ip>
```

## Port Related Information:
`/usr/share/nmap/nmap-servies`

## ICMP (Ping) Sweep:

`nmap -sn <pi-rage>`

`nmap -sn <ip-range> -oG filename`   (grepable format)

## Sweep TCP / UDP ports

`nmap -p 80 <ip-range> -oG filename`

## Sweep full network for top ports

`nmap -sT -A --top-ports=20 <ip-range> -G filename`

## Nmap script engine:

`ls -l /usr/share/nmap/scripts | grep smb`

## Important Flags    

`-O` for OS Fingerprinting
`-sV` for banner grabbing
