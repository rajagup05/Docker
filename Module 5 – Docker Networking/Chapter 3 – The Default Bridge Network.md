
## Chapter 3 – The Default Bridge Network

When Docker starts, it automatically creates a bridge network.

See it: `docker network ls`

Example: 

```
NETWORK ID      NAME      DRIVER

ab12...         bridge    bridge

cd34...         host      host

ef56...         none      null
```

Inspect the bridge network: `docker network inspect bridge`

You'll see:
- Subnet
- Gateway
- Connected containers
