
## Chapter 1 – What is a Dockerfile?

A Dockerfile is simply a text file containing instructions that tell Docker how to build an image.

Instead of manually running:

```
apt update
apt install python3
apt install pip
copy application
start application
```

You write:

```
FROM ubuntu

RUN apt update

RUN apt install -y python3

COPY app.py /app/

CMD ["python3", "/app/app.py"]
```

Docker executes each instruction and creates an image.

Docker executes each instruction and creates an image.
