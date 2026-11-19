
## Chapter 3 – Docker Volumes

A **volume** stores data **outside** the container's writable layer.

```
Container

      │
      ▼

Volume

      │

Host Machine
```

Deleting the container does not delete the volume. 

### Create a Volume

`docker volume create mydata`

List volumes: `docker volume ls`

Output: 

```
DRIVER    VOLUME NAME

local     mydata
```

Inspect: `docker volume inspect mydata`

Example: 

```
[
  {
    "Name": "mydata",
    "Driver": "local",
    "Mountpoint": "/var/lib/docker/volumes/mydata/_data"
  }
]
```

The `Mountpoint` is where Docker stores the volume on the host.

### Using a Volume

Run Ubuntu: 

```
docker run -it \
-v mydata:/data \
ubuntu
```

Inside:

`echo "Docker Storage" > /data/test.txt`

Exit: `exit`

Remove container: `docker rm <container-id>`

Create another container:

```
docker run -it \
-v mydata:/data \
ubuntu
```

Check: `cat /data/test.txt`

Output: `Docker Storage`

Your data survived because it was stored in the volume.

### Visual Explanation

Without volume:

```
Container

┌──────────────┐
│ file.txt     │
└──────────────┘

Delete Container

↓

Everything Gone
```

With volume:
