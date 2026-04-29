# Project README.md Standard

## Goal

Keep README concise, user-centered, and useful as a front door to the project.

## Principles alignment

- Discoverable: README must route users to quickstart and full docs fast.
- Skimmable: structure should pass the 60-second scan.
- Cumulative: present prerequisites before advanced detail.
- Current: quickstart and requirements must match current behavior.

See [principles.md](./principles.md) for the full principle taxonomy.

## Header layout

Center the following elements at the top of the README, in this order:

1. Logo image
2. Project title (`h1`)
3. Horizontal rule (`<hr>`)
4. One-sentence subtitle / tagline
5. Documentation links (one link per available language)
6. Badges

Keep all content below the header block left-aligned.

Example:

```html
<p align="center"><img src="./project-logo.webp" width="128" alt="Project"></p>
<h1 align="center">Project</h1>
<hr>
<p align="center"><em>One-sentence value proposition.</em></p>

<p align="center">
  <a href="https://docs.telepat.io/project">📖 Docs</a>
  · <a href="./README.md">🇺🇸 English</a>
  · <a href="./README.zh-CN.md">🇨🇳 简体中文</a>
</p>

<p align="center">
  <a href="https://github.com/telepat-io/project/actions/workflows/ci.yml"><img src="https://github.com/telepat-io/project/actions/workflows/ci.yml/badge.svg?branch=main" alt="Build"></a>
  <a href="https://codecov.io/gh/telepat-io/project"><img src="https://codecov.io/gh/telepat-io/project/graph/badge.svg" alt="Codecov"></a>
  <a href="https://www.npmjs.com/package/@telepat/project"><img src="https://img.shields.io/npm/v/@telepat/project" alt="npm"></a>
  <a href="https://github.com/telepat-io/project/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-yellow.svg" alt="License"></a>
</p>
```

## Required section order

1. Header block (logo, title, subtitle, docs links, badges)
2. What it solves and primary use cases
3. Quick start (fastest working path)
4. Requirements
5. How it works (high-level)
6. Using With AI Agents
7. Security and trust
8. Links to full docs and support
9. Contributing (short pointer)
10. License

## README i18n requirement

For multilingual repositories, include language links inside the centered docs-links paragraph in the header block.

Required baseline locales:

- English (default): `README.md`
- Simplified Chinese: `README.zh-CN.md`

Required header docs-links example for en + zh-CN:

```html
<p align="center">
  <a href="https://docs.telepat.io/project">📖 Docs</a>
  · <a href="./README.md">🇺🇸 English</a>
  · <a href="./README.zh-CN.md">🇨🇳 简体中文</a>
</p>
```

Required root file layout for en + zh-CN:

```text
README.md               ← default (English)
README.zh-CN.md
```

Rules:

- Keep links relative and root-local.
- Keep section structure aligned across locale files.
- If one locale is temporarily incomplete, add an explicit TODO marker in that locale file instead of silent drift.
- All sections, including "Using With AI Agents", must exist in every locale file.

## Badges policy

Required badges (in order):

1. **Build** — CI status
2. **Codecov** — Test coverage
3. **npm** — Package version (if published)
4. **License**

Rules:

- Keep badge count small (exactly these four by default).
- Prefer meaningful health badges over vanity badges.
- Badges must link to trustworthy first-party sources.
- Place badges inside the centered header block, below the docs links.

## Quick start rules

- Include one minimal copy-paste path.
- Include expected outcome.
- Keep advanced setup out of README and link to docs.

## Requirements section

Explicitly state:

- Supported OS/platform constraints.
- Required runtime versions.
- Required external tools.

## Using With AI Agents

Every project README must include this section, positioned after "How it works" and before "Security and trust."

Purpose:

- Explain why the project is compelling for agentic use.
- Surface MCP servers, agent-specific CLI commands, non-interactive/automation flags, and skill packages.
- Link to agent-specific documentation under `docs/for-agents/` or equivalent.

Required content (include all that apply):

1. **MCP server** — command to start, transport (stdio/sse), number of tools, and a link to MCP docs.
2. **Agent CLI commands** — commands designed for automation (for example `--json`, `--non-interactive`, `agent status`).
3. **Non-interactive / CI mode** — flags or environment variables that remove interactive prompts.
4. **Skill packages** — installable skill directories and where to place them.
5. **Programmatic API** — HTTP/WebSocket endpoints, OpenAPI specs, or direct integration paths.
6. **Agent docs entrypoint** — link to `https://docs.telepat.io/<project>/for-agents` or equivalent.

Tone should be concise and action-oriented. Avoid vague marketing language; show runnable commands.

## Security section

Include:

- Security model summary.
- Where to report vulnerabilities.
- Link to dedicated security policy.

## Readability and portability rules

- README must be readable as raw Markdown text.
- Do not rely on heavy HTML layouts for core meaning.
- Visuals must support prose, never replace it.
- Do not use tracking pixels or hidden analytics in README.

## Clickable links policy

All documentation links inside the README must be full, clickable URLs pointing to the published docs site.

Rules:

- Use `https://docs.telepat.io/<project>/...` for all cross-file doc references.
- Do not use relative file paths (for example `docs/getting-started/quickstart.md`) in the README body.
- Relative paths are permitted only inside the header block for language-switch links (for example `./README.zh-CN.md`).
- Verify that every URL resolves correctly before committing.

Example:

```markdown
- [Quickstart](https://docs.telepat.io/project/getting-started/quickstart)
- [CLI reference](https://docs.telepat.io/project/reference/cli-reference)
```

## Appeal and persuasion guidelines

The README is the front door. Make it compelling:

- Lead with a clear, concrete value proposition (not abstract marketing).
- Keep the intro scannable: bullets over paragraphs where possible.
- Use the tagline to communicate differentiation.
- End sections with a clear next step or link.
- Avoid walls of text: if a section exceeds ~15 lines, move detail to docs and link there.
- Every project README should make a user want to install within 60 seconds.

## Common anti-patterns

- Marketing-heavy intro with no runnable quickstart.
- Walls of badges or decorative emojis.
- Image-only feature explanations.
- Missing requirements or missing license link.
- Broken or non-clickable documentation links.
- Missing "Using With AI Agents" section.
- Excessive detail that belongs in the docs site rather than the README.

## 60-second skim test

A new visitor should answer all in under 60 seconds:

1. What is this?
2. Is this for me?
3. How do I run it now?
4. Where is the full documentation?
5. How do I use it with an AI agent?

## Related standards

- [principles.md](./principles.md)
- [ai-agent-navigation.md](./ai-agent-navigation.md)
