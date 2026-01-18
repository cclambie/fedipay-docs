# Usage Events (v0)

Usage events represent a privacy-minimal record that a user engaged with a creator/project/content.

This doc will define the canonical JSON schema for events, including:

- event identity and idempotency
- timestamps and client metadata
- subject identity (ActivityPub, web, RSS, package, etc.)
- optional weighting fields (dwell time, percent viewed, etc.)

## Event goals

- Good enough to compute allocations
- Minimal enough to avoid surveillance
- Flexible enough to extend later

## Next
