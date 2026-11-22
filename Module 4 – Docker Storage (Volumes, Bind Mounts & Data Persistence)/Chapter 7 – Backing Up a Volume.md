
## Chapter 7 – Backing Up a Volume

Create a backup: 

```
docker run --rm \
-v mydata:/data \
-v $(pwd):/backup \
ubuntu \
tar czf /backup/mydata.tar.gz -C /data .
```

This creates: `mydata.tar.gz`

containing everything in the volume.
