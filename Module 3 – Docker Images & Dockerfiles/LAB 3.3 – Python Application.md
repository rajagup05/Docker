
## LAB 3.3 – Python Application

Create: `app.py`

`print("My first Docker application")`

Dockerfile: 

```
FROM python:3.12

COPY app.py /app/

CMD ["python","/app/app.py"]
```

Build and run.
