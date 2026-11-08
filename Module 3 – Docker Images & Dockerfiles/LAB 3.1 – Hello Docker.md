
## LAB 3.1 – Hello Docker

### Goal

Create your first custom image.

### Steps

Create: `Dockerfile`

```
FROM ubuntu

CMD ["echo","Welcome to Docker"]
```

Build: `docker build -t welcome .`

Run: `docker run welcome`

Expected: `Welcome to Docker`
