# Documentation Principles Standard

## Purpose

Define the foundational principles behind this playbook so every standard stays coherent across authoring, review, publication, and maintenance.

This page adapts the Write the Docs principles into Telepat docs policy language.

Source:
- https://www.writethedocs.org/guide/writing/docs-principles/

## How to use this page

- Treat this page as the foundation.
- Treat each topic page as the operational policy for one surface area.
- Avoid duplicating full policy text across topics. Link back here for principle intent.

## Principles taxonomy

### General documentation principles

1. Precursory: document early enough to guide implementation and review.
2. Participatory: include contributors and readers in the docs lifecycle.

### Principles for great content

1. ARID: allow intentional repetition when it improves comprehension.
2. Skimmable: optimize headings, lists, and layout for fast scanning.
3. Exemplary: provide useful examples without overwhelming the page.
4. Consistent: keep language, structure, and formatting stable.
5. Current: stale docs are worse than missing docs.
6. Accessible: written and visual content should remain usable across assistive and non-assistive reading modes.
7. Equitable: wording and examples should avoid avoidable bias and exclusion.

### Principles for content sources

1. Nearby: keep docs close to the code and workflow they describe.
2. Unique: maintain one canonical source for each fact.

### Principles for publications

1. Discoverable: make important content easy to find.
2. Addressable: support direct linking to specific sections.
3. Cumulative: present prerequisites before advanced material.
4. Complete: for any included scope, cover it fully.
5. Beautiful: keep visual presentation intentional and readable.

### Principle for the body of publications

1. Comprehensive: together, docs should answer likely user questions.

## Principle-to-topic map

| Principle | Operationalized in topics |
|---|---|
| Precursory | [templates.md](./templates.md), [quality-and-governance.md](./quality-and-governance.md) |
| Participatory | [tone-and-style.md](./tone-and-style.md), [quality-and-governance.md](./quality-and-governance.md), [ai-agent-navigation.md](./ai-agent-navigation.md) |
| ARID | [templates.md](./templates.md), [cli-command-docs.md](./cli-command-docs.md), [api-docs.md](./api-docs.md) |
| Skimmable | [tone-and-style.md](./tone-and-style.md), [content-elements.md](./content-elements.md), [docusaurus-markdown-features.md](./docusaurus-markdown-features.md), [readme-standard.md](./readme-standard.md) |
| Exemplary | [templates.md](./templates.md), [cli-command-docs.md](./cli-command-docs.md), [api-docs.md](./api-docs.md) |
| Consistent | [information-architecture.md](./information-architecture.md), [tone-and-style.md](./tone-and-style.md), [docusaurus-standard-profile.md](./docusaurus-standard-profile.md) |
| Current | [quality-and-governance.md](./quality-and-governance.md), [seo-requirements.md](./seo-requirements.md), [i18n-requirements.md](./i18n-requirements.md) |
| Accessible | [accessibility-and-bias.md](./accessibility-and-bias.md), [content-elements.md](./content-elements.md), [docusaurus-markdown-features.md](./docusaurus-markdown-features.md), [tone-and-style.md](./tone-and-style.md) |
| Equitable | [accessibility-and-bias.md](./accessibility-and-bias.md), [tone-and-style.md](./tone-and-style.md), [quality-and-governance.md](./quality-and-governance.md) |
| Nearby | [docusaurus-implementation.md](./docusaurus-implementation.md), [ai-agent-navigation.md](./ai-agent-navigation.md) |
| Unique | [quality-and-governance.md](./quality-and-governance.md), [ai-agent-navigation.md](./ai-agent-navigation.md), [information-architecture.md](./information-architecture.md) |
| Discoverable | [information-architecture.md](./information-architecture.md), [docusaurus-implementation.md](./docusaurus-implementation.md), [seo-requirements.md](./seo-requirements.md), [readme-standard.md](./readme-standard.md) |
| Addressable | [information-architecture.md](./information-architecture.md), [docusaurus-markdown-features.md](./docusaurus-markdown-features.md), [api-docs.md](./api-docs.md), [cli-command-docs.md](./cli-command-docs.md) |
| Cumulative | [information-architecture.md](./information-architecture.md), [templates.md](./templates.md), [readme-standard.md](./readme-standard.md) |
| Complete | [api-docs.md](./api-docs.md), [cli-command-docs.md](./cli-command-docs.md), [templates.md](./templates.md), [quality-and-governance.md](./quality-and-governance.md) |
| Beautiful | [content-elements.md](./content-elements.md), [docusaurus-standard-profile.md](./docusaurus-standard-profile.md), [docusaurus-markdown-features.md](./docusaurus-markdown-features.md) |
| Comprehensive | [information-architecture.md](./information-architecture.md), [quality-and-governance.md](./quality-and-governance.md), [i18n-requirements.md](./i18n-requirements.md), [ai-agent-navigation.md](./ai-agent-navigation.md) |

## Author rules

1. Start pages with a clear outcome and audience.
2. Keep one canonical page per command, endpoint, and policy surface.
3. Add concrete examples for common success and failure paths.
4. Keep headings descriptive and stable for deep links.
5. Update docs in the same change as user-visible behavior changes.
6. Prefer portable links and consistent schema tables.
7. Mark partial coverage explicitly to avoid misleading readers.
8. Prefer inclusive, plain wording over idioms and region-specific assumptions.

## Reviewer checks

1. Which principle is most important for this page, and is it visible in structure?
2. Is any critical fact duplicated with conflicting truth sources?
3. Are examples realistic, runnable, and scoped to the page goal?
4. Can users deep-link to exact sections they need?
5. Is anything stale, version-bound, or phrased as timeless when it is not?

## Common failure modes

- DRY overreach that removes useful explanation.
- Repeated facts drifting out of sync across pages.
- References that are broad but not complete in scope.
- Discoverability gaps where key docs are not reachable from home, navbar, or related pages.
- Visual clutter that hurts scan speed.

## Related topics

- [information-architecture.md](./information-architecture.md)
- [tone-and-style.md](./tone-and-style.md)
- [content-elements.md](./content-elements.md)
- [quality-and-governance.md](./quality-and-governance.md)
- [templates.md](./templates.md)
- [accessibility-and-bias.md](./accessibility-and-bias.md)
