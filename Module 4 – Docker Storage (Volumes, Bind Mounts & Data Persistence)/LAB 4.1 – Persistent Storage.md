
## LAB 4.1 – Persistent Storage

**Goal**

Prove that volumes preserve data.

**Steps**

Create volume:

`docker volume create student-data`

Run: 

```
docker run -it \
-v student-data:/notes \
ubuntu
```

