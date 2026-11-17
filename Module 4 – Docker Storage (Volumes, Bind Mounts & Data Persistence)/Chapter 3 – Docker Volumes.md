
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
