
```bash
docker pull hackersploit/bwapp-docker
```
[docker image source](https://hub.docker.com/r/hackersploit/bwapp-docker)

- check for the image if downloaded
```bash
docker images
```
```sh
docker run -d -p 80:80 hackersploit/bwapp-docker
```
`80:80 = machine:local`

```bash
docker ps
```
> visit the IP you will see an error of the database that is because you have not configured the webapp yet

#### to configure :

http://IP/install.php 

now commit the changes you made to the docker container 

**SYNTAX**
```bash
docker commit <container_name> <image name>
```
do `docker ps` to know the container details in order to commit the changes you made (creating a database)

don't use the docker run command again and again as it will create a new docker container everytime use this
