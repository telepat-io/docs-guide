# SEO Requirements Standard

## Purpose

Define mandatory SEO requirements for documentation sites and authored pages.

## Principles alignment

- Discoverable: metadata and routing make pages easier to find.
- Addressable: canonical URLs and page metadata improve reliable deep linking.
- Current: metadata should reflect current product behavior and vocabulary.
- Consistent: keyword and front matter usage should remain uniform across pages.

See [principles.md](./principles.md) for the full principle taxonomy.

This standard follows Docusaurus SEO guidance and is required for projects adopting this playbook.

## Core requirements

1. Do not use a global default social image in Docusaurus config.
2. Set page metadata for every docs page.
3. Use front matter as the primary metadata surface.
4. Use package keyword vocabulary as topic guidance for authored content.

## Global site SEO requirements

### Required

- Set site title and tagline clearly.
- Keep canonical site URL and base URL accurate.
- Keep sitemap generation enabled (preset classic default).
- Provide a robots file in static assets where applicable.

### Disallowed

- Do not define a global `themeConfig.image` default social card image.

Reason:

- It creates low-quality metadata reuse across pages and weakens page-level relevance.

## Per-page metadata requirements

Every docs page must define front matter metadata:

- `title`
- `description`
- `keywords`
- `image` (page-specific social image when the page is shareable or externally discoverable)

When a page does not need a social image, this must be an explicit decision documented by section-level convention.

## Keyword source of truth

When creating or updating docs, agents should:

1. Read the target project's root `package.json`.
2. Use the `keywords` array as preferred topic vocabulary.
3. Integrate those keywords naturally in headings, summary paragraphs, and metadata.
4. Avoid keyword stuffing.

Natural usage rule:

- Keywords should improve clarity for humans first, and machine retrieval second.

## Front matter template

```yaml
---
title: CLI Deployment Guide
description: Deploy and verify the CLI service in local and CI environments.
keywords:
  - cli
  - deployment
  - automation
image: /img/docs/cli-deployment-social.png
---
```

## When to use head tag overrides

Prefer front matter for routine metadata.

Use `<head>` overrides only for:

- Custom canonical links.
- Robots directives for specific pages (`noindex`).
- Structured data blocks (JSON-LD) when needed.

## Image metadata rules

- Follow [accessibility-and-bias.md](./accessibility-and-bias.md) for content accessibility and inclusive language policy.
- Share images should match page topic, not generic site branding.

## QA checklist for SEO

1. No global default meta image in site config.
2. Every docs page has title, description, and keywords.
3. Shareable pages have page-specific image metadata.
4. Page metadata language reflects project `package.json` keyword vocabulary naturally.
5. No keyword stuffing or repetitive boilerplate descriptions.

## Related standards

- [principles.md](./principles.md)
- [accessibility-and-bias.md](./accessibility-and-bias.md)
