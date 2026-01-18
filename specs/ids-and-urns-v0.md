# IDs & URNs (v0)

FediPay needs identifiers that work across:

- ActivityPub actors/objects
- Websites and RSS feeds
- Apps and software packages
- “Creators” that may not have a single canonical URL

## Recommendation: URNs

Use URNs when there is no stable HTTP(S) URL or when you want a consistent internal namespace.

Pattern:

- `urn:fedipay:<type>:<id>`

Examples:

- `urn:fedipay:ap-actor:https://example.social/users/alice`
- `urn:fedipay:web:https://example.com/posts/123`
- `urn:fedipay:rss:https://example.com/feed.xml`
- `urn:fedipay:package:org.gimp.GIMP`

## Notes

- URNs must be stable and deterministic.
- Prefer canonical URLs inside URNs where possible.
- Keep them opaque to clients where feasible (treat as identifiers, not content).
