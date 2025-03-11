# Linux
Some Linux commands that have really helped me in the past.

### StrictHostKeyChecking
First time SSH session into a remote host, do this to prevent key error:
```
ssh root@<ipv4_address> -o StrictHostKeyChecking=no
```

### faillock
Unlock an SSH user account if it gets "Access Denied" after failed login attempts. View failed users:
```
faillock --user <username>
```
Reset them:
```
faillock --user <username> --reset
```
Verify:
```
faillock --user <username>
```

### tmux
Create a tmux session with a name:
```
tmux new -s <session_name>
```
Get back into your tmux session:
```
tmux a -t <session_name>
```

### rsync
Send files from one device to another. These options should skip over files already present, and give you an output of progress:
```
rsync -chavzP --stats /path/you/want/to/send <username>@<ipv4_address>:/path/to/be/sent/to
```


### chown
This will recursively set ownership to all directories and files in the specific directory to the user and/or group that you specify. You can use both as such:
```
chown -R <user>:<group> /directory
```
