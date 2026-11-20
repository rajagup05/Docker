
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

Inside: `echo "Module 4 Complete" > /notes/status.txt`

Exit.

Remove the container.

Run another Ubuntu container using the same volume:

```
docker run -it \
-v student-data:/notes \
ubuntu
```

Check: `cat /notes/status.txt`

Expected: `Module 4 Complete`
