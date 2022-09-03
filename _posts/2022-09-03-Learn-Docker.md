With Docker, you can manage your infrastructure in the same ways you manage your applications

Docker provides the ability to package and run an application in a loosely isolated environment called a container(lightweight) 

Container contain everything needed to run the application, so you do not need to rely on what is currently installed on the host

getting the fix to the customer is as simple as pushing the updated image to the production environment.

![Architecture](https://docs.docker.com/engine/images/architecture.svg)

Docker Objects:

### Image
An image is a read-only template with instructions for creating a Docker container. Often, an image is based on another image, with some additional customization.

To build your own image, you create a Dockerfile

Each instruction in a Dockerfile creates a layer in the image. When you change the Dockerfile and rebuild the image, only those layers which have changed are rebuilt. This is part of what makes images so lightweight, small, and fast, when compared to other virtualization technologies.

### Containers

a container is a sandboxed process on your machine that is isolated from all other processes on the host machine

A container is a runnable instance of an image.

You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.

namespaces provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

**Note**
- A Dockerfile is a recipe for creating Docker images.
- A Docker image gets built by running a Docker command (which uses that Dockerfile)
- A Docker container is a running instance of a Docker image

```bash
# build image from Dockerfile
# docker build -t <user-defined-img-tagname> <path-to-look-Dockerfile>
docker build -t getting-started .

# start a container
# docker run <options> <image-ref>
docker run --detach --port 3000:3000 getting-started

# made any changes to source code
# update the image 
docker build -t getting-started .

# stop and remove old container listening to same port 3000 as this new one 
# get container ID
docker ps 
docker stop <the-container-id>
docker rm <the-container-id>

# start updated container from updated image
# note: data didn't persist from old to new container when our app is updated.
docker run -dp 3000:3000 getting-started
```
