# Blog_Microservice
Blog Project: Building Microservice from scratch using node js , Docker, Docker Hub, Kubernetes

# To Build a Docker File
docker build .

# or(Better way to attach a tag)To Build a Docker File
docker build -t blog_microservice/posts .
docker build -t blog_microservice/event_bus .

# To Run the
docker run <imageid / image tag>
docker run blog_microservice/event_bus

# Create and start container, but also override default commands
docker run -it <imageid / image tag> [cmd]
docker run -it blog_microservice/posts sh // To run the shellinside that container

# to see all the running containers
docker ps
docker container ls


# to See all the images
docker images

# to see all the containers
docker ps -a

# Excute the given command in a running container
docker exec -it [container id] [cmd]
docker exec -it blog_microservice/posts sh // need tocheck

docker logs [container id]

# To Stop a running container
docker container stop dd526582d2dd


# ----------------- Kubernetes (kubectl) commands------------------->

1. kubectl get pods
2. kubectl exec it [pod name] [cmd]
3. kubectl logs [pod name]
4. kubectl delete pod [pod name]
5. kubectl apply -f [config file name]
6. kubectl describe pods

7. kubectl get dployments
8. kubectl describe deployment [deployment name]
9. kubectl apply -f [config file name]
10. kubectldelete deployment [deployment name]
