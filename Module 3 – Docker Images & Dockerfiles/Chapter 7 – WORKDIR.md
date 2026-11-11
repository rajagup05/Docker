
## Chapter 7 – WORKDIR

Without `WORKDIR`:

```
COPY app.py /project/

CMD ["python","/project/app.py"]
```

With `WORKDIR`: 

```
WORKDIR /project

COPY app.py .

CMD ["python","app.py"]
```
