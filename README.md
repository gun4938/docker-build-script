# dockerfiles-centos-user-adderable
net-tool install
curl install
tree install
base image : ubuntu

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t gun4938/practice .
	docker run -it --name n1 -p 8888:80 gun4938/practice
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        gun4938/practice      "/bin/bash"         7 seconds ago       Up 6 seconds                            n1
```

To test, ("gun4938" is username. )
```
	open 127.0.0.1:8888
```
To Rollback
```
    docker rm n1 -f
    docker rmi gun4938/practice
```
