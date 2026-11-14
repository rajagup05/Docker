
## LAB 3.4 – Complete Dockerfile

Create:

```
FROM python:3.12

WORKDIR /app

COPY app.py .

ENV APP=Docker

CMD ["python","app.py"]
```

**app.py**

```
import os

print("Application:", os.getenv("APP"))
```
