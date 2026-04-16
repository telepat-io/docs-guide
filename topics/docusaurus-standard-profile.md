# Docusaurus Standard Profile

## Purpose

Define the exact Docusaurus implementation baseline for Telepat projects.

## Principles alignment

- Consistent: repos share one documented baseline.
- Discoverable: navbar and footer must expose high-value docs paths.
- Addressable: canonical URLs and strict link handling preserve reference integrity.
- Beautiful: CSS baseline supports clear, intentional presentation.

See [principles.md](./principles.md) for the full principle taxonomy.

This profile is based on current production implementations and is the default for new repos.

## Required filesystem conventions

1. Docusaurus app directory is `docs-site/`.
2. Canonical Markdown docs live at repo-root `docs/`.
3. Docusaurus reads canonical docs using `docs.path: '../docs'`.

## Required root scripts contract

Each adopting repository must provide:

- `docs:start`
- `docs:build`
- `docs:serve`
- `docs:deploy` (optional but recommended)
- `docs:write-translations` (required when i18n is enabled)

Recommended root script pattern:

```json
{
  "scripts": {
    "docs:start": "npm --prefix docs-site run start",
    "docs:build": "npm --prefix docs-site run build",
    "docs:serve": "npm --prefix docs-site run serve",
    "docs:deploy": "npm --prefix docs-site run deploy",
    "docs:write-translations": "npm --prefix docs-site run write-translations"
  }
}
```

## Required config behaviors

Use this baseline behavior in `docusaurus.config`:

1. `routeBasePath` is `/`.
2. `trailingSlash` is `false`.
3. `onBrokenLinks` is `throw`.
4. Broken Markdown links are strict (`throw` preferred, `warn` allowed only with explicit transition note).
5. `blog` is disabled unless intentionally needed.
6. `theme.customCss` points to `./src/css/custom.css`.
7. Navbar includes direct links to Docs, CLI Reference, Technical, and GitHub.
8. When i18n is enabled, navbar includes a visible locale switcher (`type: 'localeDropdown'`) for both desktop and mobile navigation.
9. Footer includes at least Getting Started and CLI Reference links.
10. Do not set `themeConfig.image` as a global default meta image.
11. Prefer front matter metadata per page (`title`, `description`, `keywords`, and page-specific `image` when needed).
12. Set i18n locales with English default and Simplified Chinese secondary locale.

Recommended i18n block:

```js
i18n: {
  defaultLocale: 'en',
  locales: ['en', 'zh-CN']
}
```

Recommended locale switcher block (when i18n is enabled):

```js
themeConfig: {
  navbar: {
    items: [
      {
        type: 'localeDropdown',
        position: 'right'
      }
    ]
  }
}
```

## Standard config template

```js
/** @type {import('@docusaurus/types').Config} */
const config = {
  title: 'Project Docs',
  tagline: 'Short product tagline.',
  url: process.env.DOCS_LOCAL === 'true' ? 'http://localhost' : (process.env.DOCS_URL || 'https://docs.telepat.io'),
  baseUrl: process.env.DOCS_LOCAL === 'true' ? '/' : (process.env.DOCS_BASE_URL || '/project/'),
  organizationName: process.env.GITHUB_OWNER || 'telepat-io',
  projectName: process.env.GITHUB_REPO || 'project',
  trailingSlash: false,
  onBrokenLinks: 'throw',
  markdown: {
    hooks: {
      onBrokenMarkdownLinks: 'throw'
    }
  },
  presets: [
    [
      'classic',
      {
        docs: {
          path: '../docs',
          routeBasePath: '/',
          sidebarPath: require.resolve('./sidebars.js'),
          editUrl: 'https://github.com/telepat-io/project/tree/main/'
        },
        blog: false,
        theme: {
          customCss: require.resolve('./src/css/custom.css')
        }
      }
    ]
  ]
};

module.exports = config;
```

## SEO requirement note

- Remove the default Docusaurus social image pattern from standardized configs.
- Metadata quality must come from page-level front matter, not one shared site image.

## Required CSS baseline (copy-paste)

Use this exact baseline in `src/css/custom.css` unless a documented exception is approved.

```css
:root {
  --ifm-color-primary: #1f6feb;
  --ifm-color-primary-dark: #1557bf;
  --ifm-color-primary-darker: #124da8;
  --ifm-color-primary-darkest: #0f3f89;
  --ifm-color-primary-light: #3b82f6;
  --ifm-color-primary-lighter: #5b97f7;
  --ifm-color-primary-lightest: #8ab5fa;
  --ifm-background-color: #fbfdff;
  --ifm-code-font-size: 95%;
}

[data-theme='dark'] {
  --ifm-color-primary: #7cb4ff;
  --ifm-color-primary-dark: #5d9fff;
  --ifm-color-primary-darker: #4d94ff;
  --ifm-color-primary-darkest: #267cff;
  --ifm-color-primary-light: #9bc8ff;
  --ifm-color-primary-lighter: #abd0ff;
  --ifm-color-primary-lightest: #d7e8ff;
}

.navbar {
  box-shadow: 0 1px 0 rgba(15, 23, 42, 0.08);
}

.footer {
  background: #0f172a;
}
```

## Legacy exception

- Lore currently uses a green variant.
- Treat it as a temporary exception and document migration timing when standardizing.

## Quality gates (mandatory for adopters)

Projects implementing this profile must require all of the following before merge:

1. `typecheck` or `tscheck` (repo naming variant).
2. `lint` using ESLint.
3. `build`.

## Related standards

- [principles.md](./principles.md)
