
## LAB 2.2 – Ubuntu Container

Task
Run Ubuntu interactively: `docker run -it ubuntu`

Inside Ubuntu: 

```
mkdir dockerlab

cd dockerlab

touch hello.txt

echo "Docker is awesome" > hello.txt

cat hello.txt
```

Exit.

Check: `docker ps -a`
