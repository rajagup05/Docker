
## Chapter 1 – Where Does Container Data Go?

Let's create a container.

`docker run -it --name demo ubuntu`

Inside the container:

```
mkdir /data

echo "Hello Docker" > /data/file.txt

cat /data/file.txt
```
