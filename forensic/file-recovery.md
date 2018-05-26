# Take a backup of a remote disk

`ssh usr@ip "sudo dcfldd if=/dev/sdb | gzip -1 -" | dcfldd of=data.dd.gz`

# Extract DD backup

`binwalk -Me data.dd`

# TestDisk
# PhotoRec
