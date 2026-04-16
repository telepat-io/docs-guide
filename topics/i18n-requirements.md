# i18n Requirements Standard

## Purpose

Define the minimum localization baseline for documentation sites using Docusaurus i18n.

## Principles alignment

- Comprehensive: core docs should be available in required locales.
- Current: translated pages should track canonical updates.
- Discoverable: locale paths and navigation must be predictable.
- Consistent: locale naming and structure should remain stable across repos.

See [principles.md](./principles.md) for the full principle taxonomy.

## Required baseline locales

Projects adopting this standard should ship at least two locales:

1. English (default locale): `en`
2. Simplified Chinese: `zh-Hans` (preferred)

## Required content baseline

- English canonical docs source stays in repo-root `docs/`.
- Chinese translation files are stored in Docusaurus i18n paths.

Recommended tree:

```text
docs/
  ... English canonical docs

i18n/
  zh-Hans/
    docusaurus-plugin-content-docs/
      current/
        ... translated docs
      current.json
    docusaurus-theme-classic/
      navbar.json
      footer.json
    code.json
```

## Docusaurus config requirement

Use explicit i18n config in `docusaurus.config`:

```js
i18n: {
  defaultLocale: 'en',
  locales: ['en', 'zh-Hans']
}
```

## URL path guidance

- Docusaurus default locale (`en`) is served without locale prefix.
- Non-default locale (`zh-Hans`) is served with locale prefix by default.

Example:

- English: `/getting-started/quickstart`
- Chinese: `/zh-Hans/getting-started/quickstart`

If your product requires a short path like `/cn/...`, you may use locale key `cn` instead of `zh-Hans`, but set `htmlLang: 'zh-CN'` and document the exception.

## Dev vs production locale behavior

- Docusaurus dev mode typically serves one locale at a time.
- Production build output should include all configured locales.
- Teams should document this behavior to prevent false bug reports when `/zh-Hans/...` appears unavailable during single-locale dev sessions.

Recommended root scripts:

```json
{
  "scripts": {
    "docs:start:en": "npm --prefix docs-site run start -- --locale en",
    "docs:start:zh": "npm --prefix docs-site run start -- --locale zh-Hans",
    "docs:preview:all-locales": "npm run docs:build && npm run docs:serve"
  }
}
```

## Translation workflow requirements

1. Configure locales in site config.
2. Initialize translation files with `docusaurus write-translations`.
3. Translate docs pages and UI labels (`navbar`, `footer`, `code.json`).
4. Build localized docs and validate link integrity in both locales.

## Translation parity policy

- User-visible docs changes must update matching localized pages in the same PR when localized pages exist.
- If a page is intentionally not localized yet, add an explicit TODO note in the locale mirror or create a placeholder page to avoid silent drift.

## SEO and i18n

- Keep locale metadata accurate.
- Do not localize by machine-changing slugs only; ensure translated page copy quality.
- Rely on Docusaurus hreflang generation and locale-aware builds.

## Quality checks for i18n

1. Locale config includes `en` and `zh-Hans` (or documented `cn` exception).
2. Core docs categories exist in both locales.
3. Navbar/footer labels are translated.
4. Broken links check passes in both locale builds.

## Related standards

- [principles.md](./principles.md)
