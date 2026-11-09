
## Chapter 5 – RUN

`RUN` executes commands **during image build**.

Example: `RUN apt update`

or `RUN apt install -y curl`

Example: 

```
FROM ubuntu

RUN apt update

RUN apt install -y curl

CMD ["bash"]
```

Now every container created from this image already has curl.

Verify: `docker run -it myimage`

Inside: `curl --version`
