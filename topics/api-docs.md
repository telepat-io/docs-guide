# API Documentation Standard

## Scope

Use this for REST, RPC, and SDK-adjacent API pages in `Reference`.

## Principles alignment

- Complete: cover selected endpoint scope fully.
- Current: include versioning and deprecation status when applicable.
- Addressable: keep stable endpoint headings and linkable sections.
- Discoverable: make API pages easy to find from nav and related CLI docs.

See [principles.md](./principles.md) for the full principle taxonomy.

## Required sections

1. Endpoint summary
2. Authentication
3. Request schema
4. Response schema
5. Error semantics
6. Examples
7. Related CLI mapping
8. Versioning and deprecation notes (when applicable)

## Endpoint summary format

| Method | Path | Purpose |
|---|---|---|
| `POST` | `/v1/projects` | Create a project. |

## Request schema format

| Field | Type | Required | Default | Allowed Values | Description |
|---|---|---|---|---|---|
| `name` | string | Yes | none | 1..80 chars | Project display name. |

## Response schema format

| Field | Type | Description |
|---|---|---|
| `id` | string | Unique project id. |
| `createdAt` | string (ISO-8601) | Creation timestamp. |

## Error table format

| Status | Code | Meaning | Recovery |
|---|---|---|---|
| `400` | `invalid_input` | Payload validation failed. | Fix request fields and retry. |
| `401` | `unauthorized` | Missing or invalid auth token. | Refresh credentials and retry. |

## Example rules

- Provide request and response examples.
- Use one short happy-path sample and one failure sample.
- Keep examples executable.

## CLI mapping rule

If a CLI command wraps this endpoint, include a short mapping block.

Example:

```text
CLI: tool project create --name "My Project"
API: POST /v1/projects { "name": "My Project" }
```

## Related standards

- [principles.md](./principles.md)
