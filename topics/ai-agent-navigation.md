# AI Agent Navigation Standard

## Goal

Make docs easy for AI agents to discover, parse, and execute against while staying human-friendly.

## Principles alignment

- Participatory: support both human and agent consumers.
- Discoverable: keep machine entrypoints easy to locate.
- Addressable: make canonical references deep-linkable.
- Unique: keep one canonical page per command and endpoint.
- Comprehensive: ensure AI surfaces cover likely questions and recovery paths.

See [principles.md](./principles.md) for the full principle taxonomy.

## IA rules for agent content

- Keep agent content in `For Agents` as a parallel category.
- Do not hide command or API truth inside agent-only pages.
- Agent pages should index and point to canonical user/reference pages.
- Use canonical route `/for-agents` in hardcoded navbar/footer links; avoid hardcoding `/for-agents/index`.

## AGENTS.md policy guidance

Projects using AGENTS.md should include explicit docs parity instructions for agents.

Recommended AGENTS.md policy block:

```md
## Docs Localization Policy (Mandatory)

- Canonical English docs live in `docs/`.
- Localized docs live in `docs-site/i18n/<locale>/docusaurus-plugin-content-docs/current/`.
- For user-visible docs changes, update both canonical and localized pages in the same change when localized pages exist.
- If a localized page is intentionally pending, add a TODO note or placeholder page in the locale path.
- Validate docs with `npm run docs:build` before handoff.
```

## llms.txt standard

Place at site root.

Must include:

1. Site summary and scope.
2. Stable links to key entrypoints.
3. Command reference location.
4. API reference location.
5. Troubleshooting location.
6. Contributing and policy links.

## llms-full.txt standard

- Provide a machine-friendly concatenated view of docs content.
- Exclude nav/footer noise.
- Keep section ordering stable.

## MCP documentation standard

For each MCP server, document:

1. Purpose and capabilities.
2. Auth requirements.
3. Tool list and schemas.
4. Resource list and URI patterns.
5. Failure semantics and retries.
6. Example call flows.

## Skills documentation standard

For each skill, document:

1. What the skill does.
2. Inputs required.
3. Constraints and guardrails.
4. Expected outputs.
5. Failure handling and fallback strategy.
6. Verification prompts.

## Retrieval optimization rules

- Use literal headings like "Arguments" or "Exit codes".
- Keep sections compact and scoped.
- Avoid synonym drift for the same concept.
- Keep one canonical page per command and endpoint.

## Related standards

- [principles.md](./principles.md)
