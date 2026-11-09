
## LAB 3.2 – Install Software

Create:

```
FROM ubuntu

RUN apt update

RUN apt install -y curl git vim

CMD ["bash"]
```
Build: `docker build -t tools .`

Run: `docker run -it tools`

Verify: 

```
`git --version

curl --version

vim --version
```
