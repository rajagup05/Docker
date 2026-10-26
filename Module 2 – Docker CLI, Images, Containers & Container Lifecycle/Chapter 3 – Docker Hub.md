
## Chapter 3 – Docker Hub

Docker Hub is the default public image registry.
It stores millions of images such as:
- ubuntu
- nginx
- redis
- postgres
- mysql
- node
- python

When you run:

`docker run nginx`

Docker does this:

```
Check Local Image

↓

Found?
 │
 ├── Yes → Run
 └── No
       │
       ▼
Download from Docker Hub

↓

Create Container
```

### Pull an Image

Download an image without running it.

`docker pull ubuntu`

Output: 

```
Using default tag: latest

Downloading...

Status: Downloaded newer image
```

View downloaded images: `docker images`

Example: 

```
REPOSITORY   TAG      IMAGE ID      SIZE

ubuntu       latest   65ae...       78MB

nginx        latest   4ab...        190MB
```
