
## Chapter 2 – Docker Layers

Layers are one of Docker's biggest optimizations.

Example Dockerfile:

```
FROM ubuntu

RUN apt update

RUN apt install -y python3

COPY app.py /app/

CMD ["python3","/app/app.py"]
```

Internally:

```
Layer 1
Ubuntu Base

↓

Layer 2
apt update

↓

Layer 3
Install Python

↓

Layer 4
Copy app.py

↓

Layer 5
CMD
```
