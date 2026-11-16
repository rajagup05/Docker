
## Chapter 1 – Where Does Container Data Go?

Let's create a container.

`docker run -it --name demo ubuntu`

Inside the container:

```
mkdir /data

echo "Hello Docker" > /data/file.txt

cat /data/file.txt
```

Output: `Hello Docker`

Now exit: `exit`

Delete the container: `docker rm demo`

Create a new container: `docker run -it ubuntu`

Check: `cat /data/file.txt`

Result: `No such file`

### Why?

Every container gets its own **writable layer**.

```
Ubuntu Image (Read Only)
        │
        ▼
Container
------------------------
Writable Layer`
```

Anything you create lives only in that writable layer.

When the container is removed:

```
Container Deleted

↓

Writable Layer Deleted

↓

Your Data Is Gone
```

This behavior is intentional. Containers are designed to be disposable.
