
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

### What Happens? 

Run: `docker run -d --name web nginx`

Inspect: `docker inspect web` 

Part of the output: `"IPAddress": "172.17.0.2"` 


Docker automatically assigns:
- an IP address
- a virtual network interface
- a route
to the container.

### Visual

```
Host

Docker Bridge

172.17.0.1

      │

-----------------------

172.17.0.2

Container A

-----------------------

172.17.0.3

Container B

-----------------------

172.17.0.4

Container C
```
