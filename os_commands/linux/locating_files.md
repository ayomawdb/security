# List all files in curr dir and sub DirBuster

`find . -type f -printf '%f\t%p\t%u\t%g\t%m\n' 2>/dev/null | column -t`

# Find files modified between give two dates

find / -type -f -newermt 2017-08-20 ! -newermt 2017-08-24 -ls 2>/dev/null

# With database:

`updatedb ; locate sbd.exe`

# Withing PATH:

`which sbd`

# Complex:

`find  /  -­‐name  sbd* `

`find / --name sdb* --exec file {} \;`
