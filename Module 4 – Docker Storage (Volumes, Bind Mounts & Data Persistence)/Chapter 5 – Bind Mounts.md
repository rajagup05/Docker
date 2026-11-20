
## Chapter 5 – Bind Mounts

Volumes are managed by Docker.

Sometimes you want to use an existing folder on your computer.

That's where bind mounts come in.

Example:

```
Your Computer

/home/raja/project

↓

Container

/app
```

Run: 

```
docker run -it \
-v $(pwd):/app \
ubuntu
```
