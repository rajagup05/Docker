
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
