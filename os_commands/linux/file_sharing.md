# Start FTP

`atftpd --daemon --bind-address 192.168.20.9 /tmp`

# Mount NFS shares

`mount -t nfs -o nolock 192.168.20.11:/export/georgia /tmp/mount`
