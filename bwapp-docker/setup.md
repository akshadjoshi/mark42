
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

to configure :

http://IP/install.php 

