`nc  -­‐nv  <IP>  25`

# "VRFY" Command:

```
VRFY existing_user
Results in: 250
```

```
VRFY nonexisting_user
Results in: 550
```

`for user in $(cat users.txt); do echo VRFY $user | nc -nv -w <ip> 25 2>/dev/null | grep ^"250"; done`

# "HELP" Command
