
## Lab 1 – Install Docker and Run Your First Container

### Goal: Install Docker and verify that it works.

#### Step 1: Check if Docker is installed

Open a terminal and run: `docker --version`

You should see something like: `Docker version 28.x.x, build ...`

#### Step 2: Check Docker is running

`docker info`

If Docker is running, you'll see details about the server, images, storage driver, CPUs, memory, and more.

#### Step 3: Run your first container

`docker run hello-world`

Docker will:
1. Look for the hello-world image locally.
2. Download it if it's not present.
3. Create a container from the image.
4. Run it.
5. Print a success message.
6. Exit because the program has finished.
