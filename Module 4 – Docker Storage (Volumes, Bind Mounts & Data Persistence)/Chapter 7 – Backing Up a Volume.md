
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

### Restore a Volume

Create a new volume: `docker volume create restored`

Restore: 

```
docker run --rm \
-v restored:/data \
-v $(pwd):/backup \
ubuntu \
bash -c "cd /data && tar xzf /backup/mydata.tar.gz"
```

Now `restored` contains the same data.
