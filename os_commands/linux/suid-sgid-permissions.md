# suid - Set User ID

The process's effective user ID gets set to that of the program file itself (rather than that of the user running it).

* S - just the setuid bit
* s - setuid bit and execute x

**No effect on DIRs**

# sgid - Set Group ID

The process's effective group ID gets set to that of the program file (rather than that of the user's primary group).

Dir - any files created in that directory will have the same group as that directory

# References

* http://www.tutonics.com/2012/12/linux-file-permissions-chmod-umask.html

# Check file access permissions

## access(2)

The check is done using the calling process's real UID and GID, rather than the effective IDs as is done when actually attempting an operation (e.g., open(2)) on the file.

Check permissions for the UID and GID of the process (executable file owner / group)
