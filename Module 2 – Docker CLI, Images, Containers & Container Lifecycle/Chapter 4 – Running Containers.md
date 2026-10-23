
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
