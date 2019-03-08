# Git a bash prompt in a new container 
```bash 
docker run -it <image> /bin/bash
```

# Remove all stopped containers 
```bash
docker rm $(docker ps -a -q)
```


