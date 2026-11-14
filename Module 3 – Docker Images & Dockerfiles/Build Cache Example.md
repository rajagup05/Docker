
## Build Cache Example

Dockerfile:

```
FROM ubuntu

RUN apt update

RUN apt install -y python3

COPY app.py /app/

CMD ["python3","/app/app.py"]
```

Build #1: `Everything builds`
