# Accessibility And Bias Standard

## Purpose

Define the minimum writing and review standards for accessible, inclusive, and bias-aware documentation content.

This page focuses on content authoring and review policy. It does not replace site-theme implementation guidance.

## Principles alignment

- Skimmable: clear wording and structure reduce cognitive load.
- Consistent: inclusive terminology should be stable across pages.
- Comprehensive: docs should work for people with different abilities, contexts, and backgrounds.
- Beautiful: readability and clarity are part of quality, not optional polish.

See [principles.md](./principles.md) for the full principle taxonomy.

## Scope

Use this standard for:

- prose, examples, and command walkthrough text.
- image, diagram, and media descriptions.
- review checklists and quality gates in docs PRs.

Use related standards for:

- Markdown and MDX implementation patterns: [docusaurus-markdown-features.md](./docusaurus-markdown-features.md)
- element-level usage guidance: [content-elements.md](./content-elements.md)
- review process integration: [quality-and-governance.md](./quality-and-governance.md)

## Accessibility writing checklist

Apply these checks before publishing:

1. Headings are descriptive and follow a clear hierarchy.
2. Link text describes destination or action, not generic text like "click here".
3. Images have meaningful alt text when informative.
4. Decorative images are not used to convey required instructions.
5. Video includes captions; audio-only content includes a transcript when used.
6. Steps and comparisons are not expressed by color alone.
7. Tables include clear headers and simple, scannable cells.
8. Admonitions include concrete recovery guidance for warning and danger states.

## Alt text quality rules

- Describe the purpose of the image in page context.
- Keep alt text concise and specific.
- Do not repeat nearby caption text verbatim.
- Do not use filler phrases like "image of" unless needed for clarity.

Example:

- Weak: `![Dashboard screenshot](./assets/dashboard.png)`
- Better: `![Run history table showing status, duration, and last update time](./assets/dashboard.png)`

## Bias reduction checklist

Apply these checks for prose and examples:

1. Use gender-neutral defaults (for example, "they" or role nouns like "developer").
2. Avoid ableist or dismissive wording (for example, "obvious", "simple", "crazy").
3. Avoid culture-specific idioms when plain alternatives are clearer.
4. Avoid assumptions about region, timezone, language fluency, device, or payment model.
5. Expand acronyms on first use unless they are universally recognized in context.
6. Use realistic sample names and values without stereotyping.
7. Keep failure messages constructive, specific, and action-oriented.

## Preferred wording examples

| Avoid | Prefer |
|---|---|
| "Obviously, run this first." | "Run this first." |
| "This is simple." | "This takes one step." |
| "Kill two birds with one stone." | "Accomplish two tasks at once." |
| "Whitelist/Blacklist" | "Allowlist/Blocklist" |

Keep established technical terms where replacement would reduce clarity (for example process `kill` signal names).

## Reviewer prompts

Use these prompts during review:

1. Could any phrase exclude or confuse readers from a different background?
2. Are examples globally understandable and not tied to one region by default?
3. Is any critical instruction locked in a visual element without text equivalent?
4. Would this page still be clear when scanned quickly or read by assistive tools?

## References

- Write the Docs style guides: https://www.writethedocs.org/guide/writing/style-guides/
- Write the Docs accessibility: https://www.writethedocs.org/guide/writing/accessibility/
- Write the Docs reducing bias: https://www.writethedocs.org/guide/writing/reducing-bias/

## Related standards

- [principles.md](./principles.md)
- [tone-and-style.md](./tone-and-style.md)
- [content-elements.md](./content-elements.md)
- [docusaurus-markdown-features.md](./docusaurus-markdown-features.md)
- [quality-and-governance.md](./quality-and-governance.md)