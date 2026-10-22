
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
