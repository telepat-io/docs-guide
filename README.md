# CLI Documentation Playbook

This repository contains a practical standard for writing excellent CLI documentation with Docusaurus.

It is strongly inspired by the Write the Docs guides and community best practices: https://www.writethedocs.org/guide/writing/

It is designed for two audiences at once:

- Humans who want fast answers and clear onboarding.
- AI agents that need predictable structure, explicit schemas, and reliable links.

## What this guide covers

- Foundational documentation principles.
- Information architecture for docs sites.
- Tone and writing style.
- Accessibility and bias-aware writing standards.
- CLI command reference standards.
- API documentation standards.
- When to use tables, diagrams, and banners.
- Project README.md standards.
- AI-agent navigation standards (llms.txt, MCP, skills docs).
- Docusaurus implementation guidance.
- Quality gates and governance.
- Reusable templates.

## Required top-level docs categories

Keep these top-level categories as the baseline:

1. Getting Started
2. Guides
3. Reference
4. Technical
5. Contributing

Add `For Agents` as a parallel category. Do not merge it into end-user docs.

## Docs-guide structure

- `README.md`: this entrypoint.
- `topics/`: detailed standards by topic.

## Topic index

- [information-architecture.md](topics/information-architecture.md)
- [tone-and-style.md](topics/tone-and-style.md)
- [accessibility-and-bias.md](topics/accessibility-and-bias.md)
- [cli-command-docs.md](topics/cli-command-docs.md)
- [api-docs.md](topics/api-docs.md)
- [content-elements.md](topics/content-elements.md)
- [readme-standard.md](topics/readme-standard.md)
- [ai-agent-navigation.md](topics/ai-agent-navigation.md)
- [docusaurus-implementation.md](topics/docusaurus-implementation.md)
- [docusaurus-standard-profile.md](topics/docusaurus-standard-profile.md)
- [docusaurus-markdown-features.md](topics/docusaurus-markdown-features.md)
- [seo-requirements.md](topics/seo-requirements.md)
- [i18n-requirements.md](topics/i18n-requirements.md)
- [principles.md](topics/principles.md)
- [quality-and-governance.md](topics/quality-and-governance.md)
- [templates.md](topics/templates.md)

## Markdown features quick reference

Use this as a fast author checklist. Full rules and examples are in [docusaurus-markdown-features.md](topics/docusaurus-markdown-features.md).

| Feature | Default authoring rule |
|---|---|
| React and MDX | Prefer reusable components from `@site/src/components` over page-local complex JSX. |
| Tabs | Use stable `groupId` naming (for example `os`, `pkg-manager`) and explicit `defaultValue`. |
| Code blocks | Always set language; use `title` for larger snippets; prefer comment-based line highlighting. |
| Admonitions | Use intent-based types (`note`, `tip`, `info`, `warning`, `danger`) with Prettier-safe spacing. |
| TOC and headings | Keep heading hierarchy clean and use explicit MDX-safe heading IDs for stable anchors when needed. |
| Assets | Prefer co-located assets and meaningful alt text; avoid image-only critical instructions. |
| Links | Prefer relative file-path links (`.md`/`.mdx`) within the same docs plugin for portability/versioning safety. |
| Diagrams | Use Mermaid for flow/sequence clarity and keep diagrams small with explanatory text nearby. |
| Head metadata | Prefer front matter metadata first; use `<head>` overrides only for exceptional page needs. |
| SEO metadata | Use per-page metadata with natural keyword usage from project `package.json`; do not rely on global default social image. |
| i18n | Provide at least English + Simplified Chinese docs using Docusaurus locale workflow (`docs` + `i18n/<locale>/...`). |

## How to adopt

1. Apply IA rules first.
2. Apply command/API/README templates.
3. Add AI navigation surfaces.
4. Enforce quality checks in review.

## Success criteria

- A new user can run the product from docs in under 10 minutes.
- A user can find any command and flag in under 30 seconds.
- An AI agent can discover command specs, API specs, and workflows without ambiguous names.
- README.md passes a 60-second skim test.
