# Docker Cheat Sheet

## Woking the images and containers
- `docker run -it <image>`: Run a container from an image
- `docker run -it nginx`: Run a container from the nginx image, it exits immediately because the container is not running a service.
- If the image is not available locally, it will be downloaded from the Docker Hub. This is done only once, the first time you run the image.
- `docker ps`: List all running containers.
- `docker ps -a`: List all containers, including the ones that are not running.
- `docker stop <container>`: Stop a running container. To stop a container, you need to know its name or ID.
- If the `stop`command was run successfully, you'll see the container's name or ID in the output.
- `docker rm <container>`: Remove a container. To remove a container, you need to know its name or ID.
- `docker images`: List all images available locally.
- `docker rmi <image>`: Remove an image. To remove an image, you need to know its name or ID.
- `docker pull <image>`: Download an image from the Docker Hub, it doesn't run the image like `docker run`.
- Containers are not meant to be long-lived. They are meant to be ephemeral, meaning they are created and destroyed as needed.
- If you run `docker run ubuntu` for example, you'll get a shell prompt. If you exit the shell, the container will stop running.
- The container will still be there, but it will be stopped. You can start it again with `docker start <container>`.
- The container will only be alive as long as the process or task you started is running. If the process stops, the container stops.






