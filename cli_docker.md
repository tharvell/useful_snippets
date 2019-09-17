# Git a bash prompt in a new container 
```bash 
docker run -it <image> /bin/bash
```

# Remove all stopped containers 
```bash
docker rm $(docker ps -a -q)
```
# Remove all images 
```bash
docker rmi $(docker images -q)
```

# Copy a file into a container 
```bash
docker cp foo.txt mycontainer:/foo.txt
```

# Copy a file from a container
```bash
docker cp mycontainer:/foo.txt foo.txt
```
