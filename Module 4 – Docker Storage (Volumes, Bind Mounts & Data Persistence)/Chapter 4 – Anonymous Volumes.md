
## Chapter 4 – Anonymous Volumes

Instead of naming the volume: `docker run -v /data ubuntu`

Docker creates a random volume name.

Example: `9f61df9b7b...`

These volumes can be difficult to manage because you don't know their names.

List them: `docker volume ls`

Generally, prefer **named volumes** for production.
