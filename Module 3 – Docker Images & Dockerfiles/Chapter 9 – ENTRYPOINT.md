
## Chapter 9 – ENTRYPOINT

Many people confuse `CMD` and `ENTRYPOINT`.

### CMD

Default command that can be replaced.

Dockerfile:

```
FROM ubuntu

CMD ["echo","Hello"]
```

Run: `docker run image`

Output: `Hello`

Override: `docker run image ls`

Output: `<directory listing>`

### ENTRYPOINT

Defines the executable that always runs.

Dockerfile:

```
FROM ubuntu

ENTRYPOINT ["echo"]

CMD ["Hello Docker"]
```

Run: `docker run image`

Output: `Hello Docker`

Run: `docker run image Raja`

Output: `Raja`

Think of it this way:

```
ENTRYPOINT = Fixed executable

CMD = Default arguments
```
