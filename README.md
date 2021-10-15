# docker-cheatsheet
docker cheat sheet

# Basic commands

Build docker image

```bash
docker build .
```

Run container 

```bash
docker run -p <local_port>:<internal_port> <image> 
```

Run container and expose an interactive session

```bash
docker run -it <image> 
```

List running containers

```bash
docker ps
```

List all containers

```bash
docker ps -a
```

Stop container

```bash
docker stop <container>
```

# Dockerfile

```Dockerfile
FROM <baseImage>

# Will also create a directory
WORKDIR <path>

COPY <from> <to>

RUN <command>

EXPOSE <port>

CMD [<cmd>,<options>]
```
