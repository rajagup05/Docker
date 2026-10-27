
## Chapter 4 – Running Containers

General syntax: `docker run [OPTIONS] IMAGE [COMMAND]`

Example: `docker run ubuntu`

What happens?
1. Docker checks for the image.
2. Downloads it if needed.
3. Creates a container.
4. Starts the container.
5. Executes the default command.
6. Stops when the command finishes.

### Why Did Ubuntu Exit Immediately?

Many beginners think Docker is broken.

Run: `docker run ubuntu`

Then check: `docker ps`

Nothing appears.

Why?

Because Ubuntu's default command finishes immediately.

The container exits because there's no running process.

Think of it like this:

```
Container

↓

Runs command

↓

Command finishes

↓

Container stops
```

A container lives only as long as its main process.
