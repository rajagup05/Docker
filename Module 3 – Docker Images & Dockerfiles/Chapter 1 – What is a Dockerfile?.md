
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

### Why Dockerfiles?

Without a Dockerfile:

```
Developer 1

Install Python

Install Flask

Copy files

Run application
```

Developer 2 has to repeat every step manually.

With a Dockerfile:

```
docker build .

↓

Everything happens automatically
```

Benefits:
- Repeatable builds
- Version controlled
- Easy collaboration
- Consistent environments
- Automated CI/CD

### Docker Image Build Process

When you run: `docker build -t myapp .`

Docker performs:

```
Read Dockerfile

↓

Execute Line 1

↓

Create Layer

↓

Execute Line 2

↓

Create Layer

↓

Execute Line 3

↓

Create Layer

↓

Build Image
```

Every instruction creates a layer.
