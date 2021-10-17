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

Run container in detached mode

```bash
docker run -d <image> 
```

Start a container

```bash
docker start <name>
```

Start a container in attached mode

```bash
docker start -a <name>
```
Attach an already running container

```bash
docker attache <name>
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

Check the logs

```bash
docker logs <name>
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

# Kubernetese

## Minikube

Start minikube

```sh
minikube start
```

Open the minikube dashboard

```sh
minikube dashboard
```

## Kubectls

cluster info

```sh
kubectl cluster-info
```
