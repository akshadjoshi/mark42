Docker cheatsheat

I have taken example of game installation to bifurcate IMAGE & CONTAINER (Ignore the eg. if it offends you)

command to remove any conflicting files 
```bash
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

# installing docker 

`adding repo`

```bash 
 printf '%s\n' "deb https://download.docker.com/linux/debian bullseye stable" |
  sudo tee /etc/apt/sources.list.d/docker-ce.list

```

`Import the gpg key`

```bash
curl -fsSL https://download.docker.com/linux/debian/gpg |
  sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/docker-ce-archive-keyring.gpg
```
```bash
sudo apt update

sudo apt install -y docker-ce docker-ce-cli containerd.io
```
Need to **create the docker group and add your user**

```bash
sudo groupadd docker
```
```bash
sudo usermod -aG docker $USER   # $USER is just a variable
```
**get various docker images from** https://hub.docker.com/


>IMAGE (SETUP)
```bash
 docker images                         #to see docker images

 docker pull kalilinux/kali-rolling    #cmd to download image/setup from site

```



>CONTAINER (machine/game)
```bash

 docker run -it -d --name <container_name> <image_name> bash   #to create new containers 
#eg `docker run -it -d --name kalilinux kalilinux/kali-rolling  bash`
                                        *image_name*
```
```bash
 docker rm <container_name>        #to **remove** the container 
 ```
 ```bash
 docker start <container_name>
 ```
 ```bash
 docker exec -it <existing_container_ID_or_name> /bin/bash     #to **start** a container
 ```
 ```bash
 docker stop <container_name>.    #to **stop/exit** a container (# exit)
 ```
 ```bash
 docker ps                       #to check for **running** containers
 ```
 ```bash
 docker ps -a                    #to check for *all* containers
```



Switches : `-i interactive `
           `-t terminal`
           `-a to show all containers`
           `-d Run container in background and print container ID`


NOTE : `you can make various docker container out of one image (setup)`


TROUBLESHOOT (FOR THIS ERROR) : `docker exec -it kalilinux /bin/bash
Error response from daemon: Container 22c01b4af62c4e2d1df043224eb25864afa7637adb01ef34289e3de9dc44ae78 is not running`

USE THIS COMMAND 
```bash
 docker start <container_name>
#eg `docker start kalilinux`           **then use** $> docker exec -it kalilinux /bin/bash 
```
