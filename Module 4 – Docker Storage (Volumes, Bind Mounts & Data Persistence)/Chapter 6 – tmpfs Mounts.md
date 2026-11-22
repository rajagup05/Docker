
## Chapter 6 – tmpfs Mounts

A **tmpfs** mount stores data **only in memory (RAM)**. 

Characteristics:
- Very fast
- Never written to disk
- Data disappears when the container stops

Example:

```
docker run \
--tmpfs /cache \
ubuntu
```

Use cases:
- Temporary cache
- Session data
- Sensitive temporary information
