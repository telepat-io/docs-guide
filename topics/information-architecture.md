# Information Architecture Standard

## Purpose

Define a predictable site layout so humans and AI agents can both find the right content quickly.

## Principles alignment

- Discoverable: key entry points must be easy to find.
- Addressable: stable paths and anchors support deep linking.
- Cumulative: prerequisites appear before advanced detail.
- Comprehensive: category coverage should match likely user questions.
- Unique: keep one canonical location for each command or API truth.

See [principles.md](./principles.md) for the full principle taxonomy.

## Required top-level categories

Use this exact baseline:

1. Getting Started
2. Guides
3. Reference
4. Technical
5. Contributing
6. For Agents (parallel track)

## Category ownership

- Getting Started: install, first-run success path, prerequisites.
- Guides: task-oriented workflows and scenarios.
- Reference: command specs, API specs, config schema, exhaustive flags.
- Technical: architecture, internals, design decisions.
- Contributing: local dev setup, tests, release process, docs contribution.
- For Agents: machine-oriented discovery maps, constraints, MCP/skills docs.

## URL and slug rules

- Use lowercase kebab-case slugs.
- Keep path depth <= 3 where possible.
- Prefer stable canonical URLs for reference pages.

Examples:

- `/getting-started/quickstart`
- `/guides/deploying-a-project`
- `/reference/cli-reference`
- `/reference/commands/<command-name>`
- `/technical/architecture`
- `/contributing/development-setup`
- `/for-agents`

## Navigation rules

- Quickstart must be reachable in one click from the docs home.
- CLI reference must be reachable directly from navbar.
- `For Agents` must be visible but separate from end-user tutorials.
- Hardcoded navbar/footer links for `For Agents` should use canonical `/for-agents` route to avoid broken-link drift.

## Page structure rules

- One H1 per page.
- Do not skip heading levels.
- Keep section titles explicit and literal.

## Anti-patterns

- Flat, ungrouped docs trees for large sites.
- Mixing contributor internals into user quickstart pages.
- Duplicating command truth across multiple pages without a canonical source.

## Related standards

- [principles.md](./principles.md)
