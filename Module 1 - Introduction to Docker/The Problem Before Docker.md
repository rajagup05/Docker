
## The Problem Before Docker

Imagine you're building a Python application.

Your application needs:

```
Python 3.12
Flask
Redis
PostgreSQL
```

Your laptop has:

```
Ubuntu
Python 3.12
Redis
```

Your teammate has:

```
Windows
Python 3.9
No Redis
```

Another developer has:

```
MacOS
Python 3.11
Redis 6
```

When everyone runs the application:

```
Your PC
✓ Works

Friend's PC
✗ Doesn't work

Server
✗ Different version

Testing machine
✗ Missing package
```

Everyone says: `"It works on my machine."`

This was one of the biggest problems in software development.

### Traditional Deployment

Suppose you're deploying a web application.

```
Application
    │
Python
    │
Libraries
    │
Operating System
```

If any one of these changes, the application may fail.

Example:

```
Python 3.10

↓

Upgrade to Python 3.12

↓

Some library breaks

↓

Application crashes
```

### Docker Solution

Docker packages everything together.

Instead of only sending your code,

you send

```
Application

+

Python

+

Libraries

+

Dependencies

+

Configuration
```

This package is called an Image.
When it runs,
it becomes a Container.

### Real World Analogy

Think about shipping goods.
Without containers

```
TV
Chair
Books
Table
```

Everything is loaded separately.
Messy.
Slow.
Easy to damage.

Shipping containers changed everything.

        +----------------------+
        |     Container        |
        |                      |
        | TV                   |
        | Chair                |
        | Books                |
        | Table                |
        +----------------------+

Every ship,

truck,

and train

can move the same container.

Docker containers work exactly the same way.

Instead of shipping furniture,

Docker ships software.


### What is Docker?

Docker is a platform that packages an application and everything it needs into a portable container that runs consistently across different environments. 

### What is a Container?

A container is a lightweight isolated environment where an application runs.

Imagine your computer is an apartment building.

Computer

        +-------------------------+
        
        Apartment 1
        Python App
        
        Apartment 2
        Node App
        
        Apartment 3
        MySQL
        
        Apartment 4
        Redis
        
        +-------------------------+

Each apartment
- has its own files
- has its own processes
- has its own network
But they all share

```
Electricity
Water
Building
```

Similarly,
containers share

`Operating System Kernel`

while keeping applications isolated.

### What is Isolation?

Suppose you install `Python 3.8` on one container.

Another container has `Python 3.12` 

They don't interfere. 

        Container A
        
        Python 3.8
        
        --------------
        
        Container B
        
        Python 3.12

This is isolation.

### VM vs Docker

Before Docker,
companies used Virtual Machines.
Let's understand both.

### Virtual Machine

A VM looks like this

        Hardware
              │
        Host Operating System
              │
        Hypervisor
              │
        -------------------------
        VM 1
        Guest OS
        Application
        
        VM 2
        Guest OS
        Application
        
        VM 3
        Guest OS
        Application


Each VM has
- Full Operating System
- Kernel
- Drivers

That means
lots of RAM
lots of storage
slow startup

Example
Three Ubuntu VMs

        Ubuntu
        2 GB
        
        Ubuntu
        2 GB
        
        Ubuntu
        2 GB

`6 GB RAM`

just for operating systems.

### Docker

Docker looks like

        Hardware
              │
        Host OS
              │
        Docker Engine
              │
        -------------------
        Container 1
        
        Container 2
        
        Container 3


Containers share `Kernel`

Only applications are isolated.
