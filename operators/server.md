# For Operators: Server (planned)

## Status

Server is in early development.

## Goals

- Accept batches of usage events from clients
- Validate, store, and deduplicate events
- Resolve “subjects” (creators/projects) into payout destinations
- Compute monthly allocations and generate payout plans

## Deployment (future)

This doc will cover:

- Docker-based deployment
- Configuration and secrets
- Backup/restore
- Federation and trust model (future)
