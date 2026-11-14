
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

Build #2 (only `app.py` changed):

```
Layer 1 ✓ Cached

Layer 2 ✓ Cached

Layer 3 ✓ Cached

Layer 4 Rebuilt

Layer 5 Reused
```

This is why Docker builds become much faster after the first build.
