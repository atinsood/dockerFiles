- Build the docker environment by using
```
docker build -t asood\javaAndMaven .
```

- Instantiate this with 
```
docker run -d asood\javaAndMaven /usr/bin/sshd -D
```
- Login to this environment by using
```
docker ps -a
ssh root@localhost -p 49154
```

For further reference please see http://www.infoq.com/articles/docker-containers
