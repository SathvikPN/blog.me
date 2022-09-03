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

A container is a runnable instance of an image.

You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.

namespaces provide a layer of isolation. Each aspect of a container runs in a separate namespace and its access is limited to that namespace.

**Note**
- A Dockerfile is a recipe for creating Docker images
- A Docker image gets built by running a Docker command (which uses that Dockerfile)
- A Docker container is a running instance of a Docker image