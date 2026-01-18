# Ingest API (v0)

The ingest API is used by clients (extension/apps) to upload usage events to a user’s FediPay server.

## Endpoint

`POST /api/v0/ingest`

## Authentication (v0)

- API key or bearer token (server-defined)
- Keep it simple for v0; revisit OAuth later.

## Request body

A batch of events:

```json
{
  "events": [
    { "event_id": "uuid...", "type": "view", "occurred_at": "2026-01-18T12:00:00Z", "...": "..." }
  ]
}
```

### Response

Server should respond with per-event status so clients can retry safely.

Conceptual:

```json
{
  "accepted": ["event_id_1", "event_id_2"],
  "rejected": [
    { "event_id": "event_id_3", "reason": "schema_validation_failed" }
  ]
}
```

### Design goals
- Idempotent: event IDs prevent double counting
- Batch-friendly: reduce network overhead
- Privacy-minimal: upload only what’s needed for allocation
