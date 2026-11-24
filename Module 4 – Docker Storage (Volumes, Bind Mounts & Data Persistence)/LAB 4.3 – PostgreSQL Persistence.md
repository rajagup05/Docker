
## LAB 4.3 – PostgreSQL Persistence

1. Create a named volume:

`docker volume create pgdata`

2. Run PostgreSQL with that volume.
3. Connect to PostgreSQL and create:
   - A database named `school`
   - A table named `students`
4. Stop and remove the container.
5. Start a new PostgreSQL container using the same `pgdata` volume.
6. Verify that the `school` database and `students` table still exist.
This is how databases are run in production.
