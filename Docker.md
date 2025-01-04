### 1. **`docker run`**
The `docker run` command is used to start a container from a Docker image.

- `-d` or `--detach`: Run the container in the background (detached mode).
  ```bash
  docker run -d <image_name>
  ```
- `--name`: Assign a name to the container.
  ```bash
  docker run --name my-container <image_name>
  ```
- `-p` or `--publish`: Map a port on the host machine to a port in the container.
  ```bash
  docker run -p 8080:80 <image_name>
  ```
- `-e` or `--env`: Set environment variables inside the container.
  ```bash
  docker run -e VAR=value <image_name>
  ```
- `-v` or `--volume`: Mount a volume or bind mount from the host to the container.
  ```bash
  docker run -v /host/path:/container/path <image_name>
  ```
- `--rm`: Automatically remove the container when it exits.
  ```bash
  docker run --rm <image_name>
  ```
- `-it`: Run the container in interactive mode, useful for running commands inside the container.
  ```bash
  docker run -it <image_name> /bin/bash
  ```

### 2. **`docker ps`**
The `docker ps` command lists running containers.

- `-a` or `--all`: Show all containers (default shows only running containers).
  ```bash
  docker ps -a
  ```
- `-q` or `--quiet`: Show only container IDs.
  ```bash
  docker ps -q
  ```
- `--filter`: Filter containers based on specific criteria (e.g., status, name, etc.).
  ```bash
  docker ps --filter "status=exited"
  ```

### 3. **`docker build`**
The `docker build` command builds a Docker image from a Dockerfile.

- `-t` or `--tag`: Tag the image with a name and optionally a version.
  ```bash
  docker build -t my-image:v1 .
  ```
- `--no-cache`: Build the image without using cache.
  ```bash
  docker build --no-cache -t my-image:v1 .
  ```
- `-f` or `--file`: Specify a Dockerfile location other than the default `Dockerfile`.
  ```bash
  docker build -f /path/to/Dockerfile .
  ```

### 4. **`docker images`**
The `docker images` command lists all images available locally.

- `-a` or `--all`: Show all images, including intermediate layers.
  ```bash
  docker images -a
  ```
- `-q` or `--quiet`: Show only image IDs.
  ```bash
  docker images -q
  ```

### 5. **`docker exec`**
The `docker exec` command is used to run commands in a running container.

- `-it`: Run the container interactively with a terminal.
  ```bash
  docker exec -it <container_name> /bin/bash
  ```
- `-d`: Run the command in the background (detached mode).
  ```bash
  docker exec -d <container_name> <command>
  ```

### 6. **`docker stop`**
The `docker stop` command is used to stop a running container.

- `-t` or `--time`: Set the grace period before killing the container (in seconds).
  ```bash
  docker stop -t 10 <container_name>
  ```

### 7. **`docker rm`**
The `docker rm` command removes stopped containers.

- `-f` or `--force`: Force the removal of a running container (use with caution).
  ```bash
  docker rm -f <container_name>
  ```
- `-v` or `--volumes`: Remove volumes associated with the container.
  ```bash
  docker rm -v <container_name>
  ```

### 8. **`docker rmi`**
The `docker rmi` command removes Docker images.

- `-f` or `--force`: Force remove an image (even if it's being used by stopped containers).
  ```bash
  docker rmi -f <image_name>
  ```
- `-no-prune`: Don't delete untagged parents.
  ```bash
  docker rmi --no-prune <image_name>
  ```

### 9. **`docker logs`**
The `docker logs` command is used to fetch the logs of a container.

- `-f` or `--follow`: Continuously show logs in real-time.
  ```bash
  docker logs -f <container_name>
  ```
- `--tail`: Show the last `n` lines of logs.
  ```bash
  docker logs --tail 100 <container_name>
  ```

### 10. **`docker network`**
The `docker network` command manages Docker networks.

- `create`: Create a new network.
  ```bash
  docker network create <network_name>
  ```
- `ls`: List all networks.
  ```bash
  docker network ls
  ```
- `inspect`: Get detailed information about a network.
  ```bash
  docker network inspect <network_name>
  ```

### 11. **`docker volume`**
The `docker volume` command manages Docker volumes.

- `create`: Create a new volume.
  ```bash
  docker volume create <volume_name>
  ```
- `ls`: List all volumes.
  ```bash
  docker volume ls
  ```
- `inspect`: Get detailed information about a volume.
  ```bash
  docker volume inspect <volume_name>
  ```

### 12. **`docker info`**
The `docker info` command shows system-wide information about Docker.

- This command doesn't have flags but provides useful information like the number of containers, images, storage driver, and more.
  ```bash
  docker info
  ```

### 13. **`docker system prune`**
The `docker system prune` command removes unused data (images, containers, volumes, and networks).

- `-a` or `--all`: Remove all unused images, not just dangling ones.
  ```bash
  docker system prune -a
  ```
- `-f` or `--force`: Don't ask for confirmation.
  ```bash
  docker system prune -f
  ```

### 14. **`docker-compose`** (for Docker Compose)
Docker Compose commands are used for managing multi-container applications.

- `up`: Start and run a multi-container application.
  ```bash
  docker-compose up
  ```
  - `-d`: Run in detached mode.
  ```bash
  docker-compose up -d
  ```
- `down`: Stop and remove containers, networks, and volumes defined in `docker-compose.yml`.
  ```bash
  docker-compose down
  ```
- `build`: Build images defined in `docker-compose.yml`.
  ```bash
  docker-compose build
  ```
# Below are additional flags and commands that might be useful in more specialized scenarios:

### 15. **`docker attach`**
The `docker attach` command is used to attach to a running container’s main process.

- `-i` or `--interactive`: Attach to the container in interactive mode.
  ```bash
  docker attach -i <container_name>
  ```
- `--sig-proxy`: Proxy signals (useful for handling termination signals like `Ctrl+C`).
  ```bash
  docker attach --sig-proxy=false <container_name>
  ```

### 16. **`docker exec`** (Advanced)
The `docker exec` command is used to run commands inside a running container.

- `--privileged`: Give extended privileges to the command inside the container.
  ```bash
  docker exec --privileged <container_name> <command>
  ```
- `--user`: Specify the user to run the command as inside the container.
  ```bash
  docker exec --user root <container_name> <command>
  ```

### 17. **`docker build` (Advanced)**
More advanced flags for building images.

- `--build-arg`: Pass build-time variables to the Dockerfile.
  ```bash
  docker build --build-arg VERSION=1.0 .
  ```
- `--pull`: Always attempt to pull the latest version of the image before building.
  ```bash
  docker build --pull -t my-image .
  ```

### 18. **`docker tag`**
The `docker tag` command is used to tag an image with a new name.

- No specific flags, but the format for usage:
  ```bash
  docker tag <source_image> <target_image>
  ```

### 19. **`docker push`**
The `docker push` command uploads images to a registry.

- `--disable-content-trust`: Skip image signature verification when pushing.
  ```bash
  docker push --disable-content-trust <image_name>
  ```

### 20. **`docker pull`**
The `docker pull` command downloads images from a registry.

- `--all-tags`: Pull all tags associated with an image.
  ```bash
  docker pull --all-tags <image_name>
  ```
- `--disable-content-trust`: Skip image signature verification when pulling.
  ```bash
  docker pull --disable-content-trust <image_name>
  ```

### 21. **`docker save`**
The `docker save` command is used to save an image to a tarball (archive).

- `-o` or `--output`: Specify the output file.
  ```bash
  docker save -o my_image.tar <image_name>
  ```

### 22. **`docker load`**
The `docker load` command is used to load an image from a tarball.

- `-i` or `--input`: Specify the input file.
  ```bash
  docker load -i my_image.tar
  ```

### 23. **`docker cp`**
The `docker cp` command is used to copy files or directories between containers and the local filesystem.

- No special flags but used as:
  ```bash
  docker cp <container_name>:<path_in_container> <local_path>
  docker cp <local_path> <container_name>:<path_in_container>
  ```

### 24. **`docker inspect`**
The `docker inspect` command provides detailed information about containers or images in JSON format.

- `--format`: Format the output using Go templating.
  ```bash
  docker inspect --format '{{.State.Status}}' <container_name>
  ```

### 25. **`docker stats`**
The `docker stats` command provides a live stream of container resource usage statistics.

- `--no-stream`: Only show the statistics once (without continuous updates).
  ```bash
  docker stats --no-stream
  ```

### 26. **`docker info`** (Advanced)
Shows detailed Docker system information.

- `--format`: Customize the output format using Go templating.
  ```bash
  docker info --format '{{.Containers}}'
  ```

### 27. **`docker history`**
The `docker history` command shows the history of an image, including layers and commands.

- `-q` or `--quiet`: Show only the image IDs.
  ```bash
  docker history -q <image_name>
  ```

### 28. **`docker volume prune`**
Removes unused volumes.

- `-f` or `--force`: Don't prompt for confirmation before pruning.
  ```bash
  docker volume prune -f
  ```

### 29. **`docker network prune`**
Removes unused networks.

- `-f` or `--force`: Don't prompt for confirmation before pruning.
  ```bash
  docker network prune -f
  ```

### 30. **`docker system df`**
The `docker system df` command displays the disk space used by Docker objects.

- `-v` or `--verbose`: Show detailed output.
  ```bash
  docker system df -v
  ```

### 31. **`docker events`**
The `docker events` command displays real-time events from the Docker daemon.

- `--filter`: Filter events based on specific criteria.
  ```bash
  docker events --filter 'event=start'
  ```

### 32. **`docker version`**
Shows the version information of the Docker client and server.

- No flags, simply run:
  ```bash
  docker version
  ```

### 33. **`docker login`**
The `docker login` command is used to authenticate with a Docker registry.

- `-u` or `--username`: Specify the username for the registry.
  ```bash
  docker login -u username -p password
  ```
- `--email`: Specify an email address associated with the Docker registry account.
  ```bash
  docker login --email email@example.com
  ```

### 34. **`docker logout`**
The `docker logout` command is used to log out from a Docker registry.

- No flags, simply run:
  ```bash
  docker logout
  ```
