
## Chapter 8 – Real Database Example

Run PostgreSQL: 

```
docker run -d \
--name postgres-db \
-v pgdata:/var/lib/postgresql/data \
-e POSTGRES_PASSWORD=secret \
postgres
```

Notice the volume: 

```
pgdata

↓

/var/lib/postgresql/data
```

That's where PostgreSQL stores its database files.

Delete the container: `docker rm -f postgres-db` 

Create another PostgreSQL container using the same volume: 

```
docker run -d \
--name postgres-db \
-v pgdata:/var/lib/postgresql/data \
-e POSTGRES_PASSWORD=secret \
postgres
```

Your database is still there.
