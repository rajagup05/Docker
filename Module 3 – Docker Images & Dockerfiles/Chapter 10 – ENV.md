
## Chapter 10 – ENV

Sets environment variables in the image. 

`ENV APP_NAME=DockerCourse`

Test: 

```
FROM ubuntu

ENV NAME=Raja

CMD ["bash","-c","echo $NAME"]
```

Output: `Raja`
