
## Chapter 1 – Docker CLI

The Docker CLI (Command Line Interface) is how you communicate with the Docker Engine.
Every command begins with: `docker`

examples: 

```
docker version
docker info
docker images
docker ps
docker run nginx
```

Think of it like this:

```
You
   │
docker command
   │
Docker CLI
   │
Docker Engine
   │
Container/Image
```

The CLI doesn't run containers itself—it sends requests to the Docker daemon.
