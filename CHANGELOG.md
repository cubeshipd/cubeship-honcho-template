# Changelog

## 1.0.0

- Install Honcho v3.1.2 with an authenticated API and a separate memory worker.
- Persist memory in PostgreSQL 17 with pgvector 0.8.2 and use managed Redis 7.4 for caching.
- Wait for dependencies and run migrations before starting the API.
- Document shared memory setup for Hermes agents on a VPS and Mac.
