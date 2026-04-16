# Quality And Governance

## Principles alignment

- Current: treat stale docs as a defect.
- Unique: keep one canonical source for each policy and spec.
- Complete: if a page covers a scope, it must cover that scope fully.
- Comprehensive: the docs set should answer likely user questions.

See [principles.md](./principles.md) for the full principle taxonomy.

## Docs review checklist

Use this checklist on every docs PR:

1. Correct category placement (Getting Started/Guides/Reference/Technical/Contributing/For Agents).
2. Heading hierarchy is valid.
3. All commands are runnable and copy-safe.
4. Reference tables follow canonical schema.
5. Admonitions are meaningful and not overused.
6. Visuals have supporting prose.
7. Broken links check passes.
8. If behavior changed, docs changed in same PR.
9. Standard quality gates pass: `typecheck` or `tscheck`, `lint` (ESLint), and `build`.
10. SEO checks pass: no global default meta image, page metadata present, and natural keyword alignment with project `package.json` keywords.
11. i18n checks pass: required locales are configured and baseline docs exist in both locales.
12. Translation parity holds: user-visible docs edits update locale mirrors in the same PR (or include explicit locale TODO placeholders).
13. Page intent aligns with [principles.md](./principles.md) and does not create a conflicting source of truth.
14. Accessibility and bias checks are reviewed using [accessibility-and-bias.md](./accessibility-and-bias.md).

## Accessibility and bias advisory checks

Treat these checks as advisory for review quality in this playbook:

1. Informative visuals include meaningful text equivalents.
2. Headings and links are descriptive and scannable.
3. Wording avoids dismissive, ableist, or exclusionary phrasing.
4. Examples avoid narrow regional and demographic assumptions by default.
5. Media includes captions or transcripts when spoken content is essential.

These checks are review requirements, but they are not defined here as mandatory CI blockers.

## Definition of done

- The page has a clear purpose sentence near the top.
- The page has at least one concrete example.
- The page links to related next steps.
- The page is discoverable from sidebar and search.

## Docs-as-code policy

- Treat docs changes as required for user-visible behavior changes.
- Keep docs in the same repository as code when possible.
- Add CI for docs build and broken-link checks.

## Mandatory implementation quality gates

Repositories adopting this standard must enforce these pre-merge checks:

1. Type checking: `typecheck` or `tscheck`.
2. Linting: `lint` backed by ESLint.
3. Build validation: `build`.

Use the canonical script names defined by each repository's `package.json`.

## Drift prevention

- Maintain one canonical command spec location.
- Run periodic docs audits for stale flags and obsolete workflows.
- Track common user failures and update troubleshooting pages.

## SEO governance checks

Repositories adopting this standard must enforce:

1. Global config does not define `themeConfig.image` as default meta image.
2. Docs pages define `title`, `description`, and `keywords` in front matter.
3. Shareable pages provide a page-specific social `image` value.
4. Generated content uses root `package.json` `keywords` naturally, without stuffing.

## i18n governance checks

Repositories adopting this standard should enforce:

1. i18n config includes `en` and `zh-CN` (or documented legacy `zh-Hans` exception).
2. English canonical docs remain in repo-root `docs/`.
3. Chinese translations exist under `i18n/<locale>/docusaurus-plugin-content-docs/current/`.
4. Docs build and broken-link checks succeed for localized output.
5. PRs with user-visible docs edits include synchronized locale updates or explicit locale TODO placeholders.

## AI quality checks

- Validate llms.txt and llms-full.txt freshness.
- Ensure MCP and skills pages reflect current contracts.
- Confirm canonical links are stable and unambiguous.

## Related standards

- [principles.md](./principles.md)
- [accessibility-and-bias.md](./accessibility-and-bias.md)
