
## Chapter 2 – Image Layers vs Writable Layer

Consider this Dockerfile:

```
FROM ubuntu

RUN apt update

RUN apt install -y curl
```

Docker creates read-only layers:

```
Layer 1
Ubuntu

↓

Layer 2
apt update

↓

Layer 3
Install curl
```

When you run a container: 

```
Read-only Layers
────────────────────

Ubuntu

apt update

curl

────────────────────
Writable Layer
```

If you create:  `touch hello.txt`

The file is stored only in the writable layer.

The image itself never changes.
