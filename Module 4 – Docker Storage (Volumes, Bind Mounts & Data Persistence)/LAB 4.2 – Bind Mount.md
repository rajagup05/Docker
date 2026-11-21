
## LAB 4.2 – Bind Mount

Create a folder: `docker-storage/`

Create: `hello.py`

`print("Running from Host")`

Run:

```
docker run -it \
-v $(pwd):/app \
python:3.12 \
python /app/hello.py
```

Modify: `print("Updated File")`

Run again.

Expected:

`Updated File`

No rebuild required.
