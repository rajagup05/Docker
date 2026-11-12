
## Chapter 9 – ENTRYPOINT

Many people confuse `CMD` and `ENTRYPOINT`.

**CMD**

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
