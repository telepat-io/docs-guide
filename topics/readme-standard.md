# Project README.md Standard

## Goal

Keep README concise, user-centered, and useful as a front door to the project.

## Principles alignment

- Discoverable: README must route users to quickstart and full docs fast.
- Skimmable: structure should pass the 60-second scan.
- Cumulative: present prerequisites before advanced detail.
- Current: quickstart and requirements must match current behavior.

See [principles.md](./principles.md) for the full principle taxonomy.

## Required section order

1. Project name and one-sentence value proposition
2. Language switcher block (required for multilingual repos)
3. Badges
4. What it solves and primary use cases
5. Quick start (fastest working path)
6. Requirements
7. How it works (high-level)
8. Security and trust
9. Links to full docs and support
10. Contributing (short pointer)
11. License

## README i18n requirement

For multilingual repositories, add a language switcher link block at the top of the README (directly below project title/value proposition).

Required baseline locales:

- English (default): `README.md`
- Simplified Chinese: `README.zh-CN.md`

Required top-of-file switcher example for en + zh-CN:

```md
[🇺🇸 English](./README.md) | [🇨🇳 简体中文](./README.zh-CN.md)
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

Recommended badges:

- Build or CI status
- Test coverage (if available)
- Package version (if published)
- License

Rules:

- Keep badge count small (usually 4 to 7).
- Prefer meaningful health badges over vanity badges.
- Badges must link to trustworthy first-party sources.

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
