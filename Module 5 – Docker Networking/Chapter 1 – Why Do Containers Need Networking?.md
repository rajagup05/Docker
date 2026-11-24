
## Chapter 1 – Why Do Containers Need Networking?

Imagine you're running:

```
Frontend (React)

↓

Backend API (Node.js)

↓

PostgreSQL
```

Each application runs inside a separate container.

Question:

**How does the frontend call the backend?**

**How does the backend connect to PostgreSQL?**

Docker networking solves this problem.

### Example Architecture 

```
                    Internet
                        │
                        ▼
               Host Machine
                        │
               Docker Network
        ┌───────────────┼───────────────┐
        │               │               │
        ▼               ▼               ▼
    Nginx          Backend API      PostgreSQL
```

Containers communicate over virtual networks.
