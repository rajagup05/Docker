
## Chapter 3 – Your First Dockerfile

Create a folder: `docker-demo/`

Create: `Dockerfile`

Contents:

```
FROM ubuntu

CMD ["echo","Hello Docker"]
```

Build: `docker build -t hello-image .`

Run: `docker run hello-image`

Output: `Hello Docker`
