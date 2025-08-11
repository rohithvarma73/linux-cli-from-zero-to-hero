# 🐳 Docker

Docker is a platform for developing, shipping, and running applications inside lightweight, portable containers.  
It ensures consistency across different environments and simplifies deployment.

---

## 1. Introduction & Installation

### Commands
```bash
docker --help                       # Check if Docker is installed, show help
sudo apt install docker.io -y       # Install Docker package
whatis docker                        # One-line description of Docker
````

---

## 2. First Container

### Commands

```bash
docker --help                        # Docker help
sudo docker ps                       # List running containers
sudo docker ps -a                    # List running + stopped containers
sudo docker images                   # List images
sudo docker run hello-world          # Run container from image

# Common Docker commands
docker search <image>                # Search for an image in Docker Hub
docker pull <image>                  # Download image from Docker Hub
docker rm <container>                # Remove container
docker rmi <image>                    # Remove image
docker stop <container>              # Stop container
docker build -t <tag> .               # Build image from Dockerfile
docker exec -it <container> <cmd>     # Run command inside container
```

---

## 3. Container with Documentation

### Commands

```bash
sudo groupadd docker                  # Create docker group
tail /etc/group                       # View last 10 lines of groups
sudo usermod -aG docker $USER         # Add current user to docker group
groups itguy                          # List groups for a user
sudo systemctl restart docker         # Restart Docker service
newgrp docker                         # Reload group membership

# Run containers
sudo docker run hello-world
docker run hello-world                # Without sudo
docker run -dp 80:80 docker/getting-started   # Run doc container on port 80
docker ps                              # List running containers

# Stop container
docker stop <container_id>
```

---

## 4. Nginx Web Server in Docker

### Commands

```bash
docker search nginx                   # Search nginx image
docker images                         # List images
docker pull nginx                     # Pull nginx image
docker run nginx -d -p 8123:80         # Run nginx container on port 8123
docker ps                              # List running containers

# Stop containers
docker stop <container_name>
docker stop <container_id>

# Inside container
nginx -t                               # Check nginx configuration
systemctl status nginx                 # Check nginx service
docker exec -it <container> /bin/bash  # Bash inside container
whoami                                 # Show current user
find / -name index.html                # Find index.html
cat <file>                             # View file
rm <file>                              # Delete file
cat > <file>                           # Overwrite file
```

---

## 5. Dockerfile & Running a Web Server

**Documentation:**

* [Dockerfile Reference](https://docs.docker.com/reference/dockerfile/)

### Commands

```bash
whatis dockerfile                     # One-line description
mkdir nginx_project                   # Create project folder
cd nginx_project                      # Move into folder
nano Dockerfile                       # Create Dockerfile
cat Dockerfile                        # View Dockerfile contents
docker images                         # List images
docker build -t my_nginx_image .       # Build image from Dockerfile
ll                                     # List files
docker run -d -p 9000:80 my_nginx_image  # Run container from image
docker ps                              # List running containers
```

**Example Dockerfile:**

```dockerfile
FROM debian
MAINTAINER Pragmatic Programmer
RUN apt-get update
RUN apt-get install nginx -y
VOLUME "/var/www/html"
EXPOSE 80
CMD /usr/sbin/nginx -g "daemon off;"
```

---

## 6. Docker Compose

**Documentation & Resources:**

* [Docker Compose Examples](https://github.com/docker/awesome-compose/tree/master)
* [Official Docker Compose Docs](https://docs.docker.com/compose/)
* [Habr Article on Compose](https://habr.com/ru/companies/ruvds/articles/450312/)

---

## 📌 Section Summary

In this section, you learned:

* Installing and running Docker
* Working with containers, images, and Docker Hub
* Running Nginx in Docker
* Writing a Dockerfile to build custom images
* Using Docker Compose for multi-container setups

---

### 📜 Commands Learned

```bash
docker --help
sudo apt install docker.io -y
whatis docker
sudo docker ps
sudo docker ps -a
sudo docker images
sudo docker run hello-world
docker search
docker pull
docker rm
docker rmi
docker stop
docker build -t <tag> .
docker exec -it <container> <cmd>
sudo groupadd docker
tail /etc/group
sudo usermod -aG docker $USER
groups itguy
sudo systemctl restart docker
newgrp docker
docker run -dp 80:80 docker/getting-started
docker search nginx
docker pull nginx
docker run nginx -d -p 8123:80
nginx -t
systemctl status nginx
docker exec -it <container> /bin/bash
whoami
find / -name index.html
cat
rm
cat >
whatis dockerfile
mkdir nginx_project
cd nginx_project
nano Dockerfile
docker build -t my_nginx_image .
docker run -d -p 9000:80 my_nginx_image
```

---

**💡 Why This Matters:**
Docker streamlines application deployment by packaging everything needed into a container, ensuring consistency and reducing "it works on my machine" issues.

```
