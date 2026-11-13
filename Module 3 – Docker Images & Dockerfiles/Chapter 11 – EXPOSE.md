
## Chapter 11 – EXPOSE

Documents which port the application listens on.

`EXPOSE 8080`

Example: 

```
FROM nginx

EXPOSE 80
```

> [!IMPORTANT]
> `EXPOSE` does **not** publish the port. It is documentation/metadata. To make the service reachable from your host, you still use: `docker run -p 8080:80 nginx`
