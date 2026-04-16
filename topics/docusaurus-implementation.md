# Docusaurus Implementation Guide

This page explains how to apply the standard profile.
For exact required defaults, use [docusaurus-standard-profile.md](./docusaurus-standard-profile.md) as source of truth.
For MDX/Markdown feature usage standards, use [docusaurus-markdown-features.md](./docusaurus-markdown-features.md) as source of truth.

## Principles alignment

- Discoverable: required nav entry points surface critical docs quickly.
- Addressable: route stability and redirects preserve link reliability.
- Nearby: docs source stays close to code in the same repository workflow.
- Beautiful: component and diagram usage should improve readability, not decorate without purpose.

See [principles.md](./principles.md) for the full principle taxonomy.

## Recommended docs structure

Keep the six categories as explicit navigation groups:

1. Getting Started
2. Guides
3. Reference
4. Technical
5. Contributing
6. For Agents

## Directory and source standard

- Docusaurus app directory name is `docs-site/`.
- Canonical docs content lives at repo-root `docs/`.
- Set `docs.path` to `../docs` in config.

## Sidebar strategy

- Group by user task first, then by depth.
- Keep `Reference` deterministic and exhaustive.
- Keep `For Agents` focused on discovery and operational constraints.

## Navbar strategy

Include direct entry points to:

- Quickstart
- CLI reference
- API reference (if applicable)
- For Agents

## MDX component policy

Use custom components intentionally:

- Tabs: only for platform-specific command variants.
- Admonitions: only for meaningful warnings and tips.
- Cards: for index pages, not deep procedure pages.

## Mermaid usage

- Enable Mermaid plugin in docs config.
- Prefer small diagrams over one giant graph.
- Keep flow labels simple and searchable.

## Route stability

- Avoid changing canonical slugs casually.
- Redirect old pages when slugs change.

## Migration notes

- Repos currently using `website/` should migrate to `docs-site/` on their next docs-structure change window.
- Repos currently sourcing docs from inside site folder should migrate to repo-root `docs/` to align with this standard.

## Related standards

- [principles.md](./principles.md)
