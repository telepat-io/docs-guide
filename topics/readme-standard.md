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
6. Security and trust
7. Links to full docs and support
8. Contributing (short pointer)
9. License

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

## Common anti-patterns

- Marketing-heavy intro with no runnable quickstart.
- Walls of badges or decorative emojis.
- Image-only feature explanations.
- Missing requirements or missing license link.

## 60-second skim test

A new visitor should answer all in under 60 seconds:

1. What is this?
2. Is this for me?
3. How do I run it now?
4. Where is the full documentation?

## Related standards

- [principles.md](./principles.md)
