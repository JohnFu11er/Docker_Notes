# Docker Notes

### Resources
[Docker getting started](https://www.docker.com/get-started)

### Sections


### Intro
- Runs natively on Linux or Windows server
- Runs on Windows or Mac Development machine (with virtual machine)
- `Image` is the blueprints to create a container
- `Container`
  - Created from image
  - Runs your application
  - Can be started, stopped, moved, and deleted

### Benefits for Web Developers
- Accelerte developer onboarding
- Eliminate App conflicts
- Environment consistency (Dev, Staging, Prod)
- Ship software faster

### Docker tools
- `Docker ToolBox`
  - Legacy program
  - Runs on Windows 7/8/10
  - Provides image and container tools
      - Docker Client
        - Lets us interact with Docker images and Docker containers
      - Docker Machine
      - Docker Compose
        - Orchestration mechanism
      - Docker Kitematic
        - GUI tool
      - VirtualBox
  - runs on virtual machine
- `Docker Desktop`
  - Windows 10 Pro+ or Mac
  - Provides image and container tools
  - Uses Hyper-V/Hyperkit to run VMs
  - Works on Windows, Mac, Linux (Docker Engine)

### Docker Desktop Installation for Windows
- [Download here](https://www.docker.com/get-started)
- Install Docker
- Search for Docker on PC and run application

### Docker CLI Installation on AWS Linux
- Apply pending updates:
  ```
  sudo yum update
  ```
- Install Docker:
  ```
  sudo yum install docker
  ```
- Add group membership for the default ec2-user so you can run all docker commands without using the sudo command:
  ```
  sudo usermod -aG docker ec2-user
  ```
- Reload a Linux user's group assignments to docker w/o logout:
  ```
  newgrp docker
  ```
- Enable Docker service at AMI boot time:
  ```
  sudo systemctl enable docker.service
  ```
- Start the Docker service:
  ```
  sudo systemctl start docker.service
  ```

### Getting started with Docker Client
- Allows us to:
  - Interact with Docker Engine
  - Build and Manage Images
  - Run and Manage Containers
- Common commands:
  - `docker pull [image name]` - Pulls an image from a Docker image repository
  - `docker run [image name]` - Runs a Docker image
  - `docker images` - Lists all Docker images on your machine
  - `docker ps` - Lists all containers on you machine
  - `docker rm [first few characters of container ID]` - Deletes a container
