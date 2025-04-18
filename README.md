## Key Commands

### Build an Image Based on a Dockerfile
```bash
docker build -t [NAME]:[VERSION] [CONTEXT]
# Example:
docker build -t nodeapp:version1 .
```

### Run a container Based on a remote or local image
```bash
docker run --name [NAME] --rm -d [IMAGE]
# Example:
docker run --name --rm -d nodeapp
```

### Share (push) an Image to a Registry (default: DockerHub)
```bash
docker push REPOSITORY/NAME:TAG
```

### Fetch (pull) an Image to a Registry (default: DockerHub)
```bash
docker pull REPOSITORY/NAME:TAG
```

### Volumes (bind mounts - to connect host machine folders)
```bash
-v /local/path:/container/path
```

### Volumes (volumes to persist data)
```bash
-v NAME:/container/path
```

### Docker compose (avid repeating docker build and docker run)
### Docker compose up (build missing images and start all containers)
```bash
docker-compose up 
```

### Docker compose down (stop all started containers)
```bash
docker-compose down
```

### Local Host (Development)
- **Isolated, encapsulated, reproducible development environments**  
    Docker ensures that each project runs in its own containerized environment, avoiding conflicts between dependencies or software versions.
- **No dependency or software clashes for working in different projects**  
    Each container operates independently, allowing seamless switching between projects without interference.

### Remote Host (Production)
- **Isolated, encapsulated, reproducible environments**  
    Docker ensures that production environments are consistent and isolated, reducing the risk of deployment issues.
- **Easy updates**  
    Simply replace a running container with an updated one, minimizing downtime and simplifying the deployment process.
- **Scalability**  
    Easily scale applications by running multiple instances of containers across different hosts.
- **Portability**  
    Containers can run on any system with Docker installed, ensuring seamless migration between environments.

### Deployment considerations
- **Replace Bind mounts with volumes or COPY**
- **Multiple containers might need multiple hosts**
- **But they can also run on the same host (depends on application)**
- **Multi-stage builds help with apps that need a build step**
