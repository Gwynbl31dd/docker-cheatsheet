# docker-cheatsheet
docker cheat sheet

# Basic commands

Build docker image

```bash
docker build .
```

Build docker image with a tag

```bash
docker build -t <tag> .
```

Re-tag image

```bash
docker tag <image/tag> <new_tag>
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

Start with a specific drive

```
minikube start --drive=<driver> (E.g docker)
```

Show the status

```sh
minikube status
```

Open the minikube dashboard

```sh
minikube dashboard
```

Expose a servive

```sh
minikube service <name>
```

## Kubectls

cluster info

```sh
kubectl cluster-info
```

Get the deployments

```sh
kubectl get deployments
```

Get the pods

```sh
kubectl get pods
```

Delete deployment

```
kubectl delete deployment <name>
```

Create simple deployment

```
kubectl create deployment <name> --image=<image>
```

Expose a deployment

```sh
kubectl expose deployments name --type=<type> --port=<port>
```

Get services

```sh
kubectl get services
```

Scale replicas

```sh
kubectl scale deployment/<name> --replicas=<number_of_replica>
```

Update deployment

```sh
kubectl set image deployment/<name> <container_name>=<new_image>
```

Rollout deployment

```sh
kubectl rollout status deployment/<name>
```
