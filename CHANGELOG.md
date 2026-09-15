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

## [2.0.0](https://github.com/cubeshipd/cubeship-honcho-template/compare/v1.0.0...v2.0.0) (2026-09-15)


### ⚠ BREAKING CHANGES

* an existing installation is not migrated. Its postgres app and volume stay where they are; moving to the managed database means installing fresh and copying the data across with pg_dump and psql. Requires Cubeship 0.9.0.

### Features

* run Honcho on a managed Postgres with pgvector ([3c1a5dc](https://github.com/cubeshipd/cubeship-honcho-template/commit/3c1a5dc4a24332d8c4ab9dbf44b1fe49d24aa2a2))

## 1.0.0

- Install Honcho v3.1.2 with an authenticated API and a separate memory worker.
- Persist memory in PostgreSQL 17 with pgvector 0.8.2 and use managed Redis 7.4 for caching.
- Wait for dependencies and run migrations before starting the API.
- Document shared memory setup for Hermes agents on a VPS and Mac.
