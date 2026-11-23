
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
