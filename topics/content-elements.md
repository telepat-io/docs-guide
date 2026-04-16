# Content Elements Policy

## Purpose

Define when to use tables, diagrams, and banners so pages stay clear and consistent.

## Principles alignment

- Skimmable: choose elements that reduce scan time.
- Exemplary: include examples that clarify common usage.
- Beautiful: keep presentation intentional and readable.
- Consistent: apply the same element semantics across pages.

See [principles.md](./principles.md) for the full principle taxonomy.

## Tables

Use tables when content has repeated fields or direct comparison needs.

Use for:

- Command flags and arguments.
- API schemas and errors.
- Feature comparison matrices.

Avoid tables for:

- Long narrative explanations.
- Single-item notes.

## Diagrams

Use Mermaid diagrams for workflows and multi-system interactions.

Preferred types:

- `flowchart` for process logic.
- `sequenceDiagram` for service interactions.

Rules:

- Include a short lead-in sentence and a short interpretation after the diagram.
- Do not rely on diagram-only explanation.
- Keep labels literal and compact.

## Banners and admonitions

Use Docusaurus admonitions sparingly.

Allowed mapping:

- `:::note` supplementary context.
- `:::tip` productivity shortcut or best practice.
- `:::info` required prerequisite or context.
- `:::warning` risky operation or common failure point.
- `:::danger` irreversible action or data loss risk.

Rules:

- At most one admonition per major section unless required.
- Every warning or danger must include explicit recovery guidance.

## Accessibility rules

Use these rules for all visual and structured elements:

1. Any informative image or GIF must have meaningful alt text.
2. Decorative visuals must not carry required instructions.
3. Do not encode critical steps in color-only cues.
4. Diagrams must include a short textual interpretation.
5. Tables should use clear headers and concise cell content.
6. Warning and danger admonitions must include recovery guidance.
7. Media with spoken content should provide captions or transcripts when used.

For wording and bias checks, see [accessibility-and-bias.md](./accessibility-and-bias.md).

## Related standards

- [principles.md](./principles.md)
- [accessibility-and-bias.md](./accessibility-and-bias.md)
