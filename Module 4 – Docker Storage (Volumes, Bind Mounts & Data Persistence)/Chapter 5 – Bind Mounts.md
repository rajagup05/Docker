
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

If your current directory contains: 

```
app.py
README.md
config.json
```

Inside the container: 

```
cd /app

ls
```

You'll see:

```
app.py

README.md

config.json
```

The container is using the host directory directly.

### Volume vs Bind Mount

    Feature	Volume	Bind Mount
    
    Managed by Docker  ✅	❌
    Uses host directory  ❌	✅
    Easy backup  ✅	Depends
    Good for databases  ✅	Sometimes
    Good for source code  ❌	✅


### Workflow

Suppose you have:

```
project/

app.py
requirements.txt
Dockerfile
```

Run: 

```
docker run \
-v $(pwd):/app \
python:3.12 \
python /app/app.py
```

Edit `app.py` on your host.

Run again.

The container immediately sees the updated file.

No image rebuild needed.
