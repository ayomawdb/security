```
IFS=$'\n'

old_p=$(ps -eo command)

while true do;
   new_p=$(ps -eo command)
   diff <(echo "$old_p") <(echo "$new_p")
   sleep 1
   old_p=$new_p
done
```
