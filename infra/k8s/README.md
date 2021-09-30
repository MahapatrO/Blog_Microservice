# To Update the Deployment ------------------->

<!--

apiVersion: apps/v1
kind: Deployment
metadata:
  name: posts-deployment
  labels:
    app: posts
spec:
  replicas: 1
  selector:
    matchLabels:
      app: posts
  template:
    metadata:
      labels:
        app: posts
    spec:
      containers:
      - name: posts
        image: blog_microservice/posts:0.0.1

 -->

# Here we dont need to define the version of the image

# Either we need to use image: blog_microservice/posts:latest

# or image: blog_microservice/posts ------> it will automatically mark as latest

# Steps to update deployment

<!--
1.The Deployment must be using the ':latest' tag in the pod spec section

2.Make and updat to your code

3.Build the image
docker build -t <docker image name>

4.Push the imge to docker
docker push <dockerhub id/image name>

5.Run the below command -
kubectl rollout restart deployment [deployment file name]

 -->
