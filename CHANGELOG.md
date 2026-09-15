# Changelog

## Unreleased

- Move Honcho onto a managed PostgreSQL 17 created with the `pgvector`
  extension, replacing the `postgres` app and its volume.
- Drop the database password input: Cubeship generates one and hands it to the
  API and the worker.
- Require Cubeship 0.9.0, the first release that creates a database with
  extensions.
- Existing installations are not migrated. Their `postgres` app and volume stay
  where they are; moving across means a fresh install and `pg_dump`/`psql`.

## 1.0.0

- Install Honcho v3.1.2 with an authenticated API and a separate memory worker.
- Persist memory in PostgreSQL 17 with pgvector 0.8.2 and use managed Redis 7.4 for caching.
- Wait for dependencies and run migrations before starting the API.
- Document shared memory setup for Hermes agents on a VPS and Mac.
