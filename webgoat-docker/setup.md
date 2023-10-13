
docker image - https://hub.docker.com/r/webgoat/webgoat-8.0/

```bash
docker pull webgoat/webgoat-8.0
```

```bash
docker run -p 8080:8080 -t webgoat/webgoat-8.0
```
**on browser** - `IP:8080/WebGoat`

you need to create a user

now commit the changes you made to the docker container 

**SYNTAX**
```bash
docker commit <container_name> <image name>
```
do `docker ps` to know the container details in order to commit the changes you made (user creation)
```bash
docker commit elegant_kilby webgoat/webgoat-8.0
```
don't use the docker run command again and again as it will create a new docker container everytime **use this** 
```bash
docker container start <container_name>
```
to stop the container 
```sh
docker container stop <container_name>
```


