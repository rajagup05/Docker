
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
