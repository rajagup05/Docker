
## Chapter 6 – COPY

Copies files from your computer into the image.

Project: 

```
project/

Dockerfile

hello.py
```

hello.py

`print("Docker is fun!")`

Dockerfile

```
FROM python:3.12

COPY hello.py /app/

CMD ["python","/app/hello.py"]
```

Build:

`docker build -t python-demo .`

Run: `docker run python-demo`

Output: `Docker is fun!`
