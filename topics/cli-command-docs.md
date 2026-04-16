# CLI Command Documentation Standard

## Goal

Make every command page skimmable, copy-paste safe, and machine-parseable.

## Principles alignment

- Skimmable: sections and tables must support fast scanning.
- Complete: command behavior, options, and outcomes must be fully documented.
- Current: examples and flags must match shipped behavior.
- Addressable: keep stable command page structure for deep links.

See [principles.md](./principles.md) for the full principle taxonomy.

## Required sections per command page

1. What this command does
2. Usage
3. Arguments and options
4. Examples
5. Output and exit codes
6. Related commands
7. Versioning and deprecation notes (when applicable)

## Usage syntax rules

- Use conventional notation:
  - `[]` optional
  - `<>` required user value
  - `|` mutually exclusive
  - `...` repeatable
- Keep usage to one line unless readability suffers.

Example:

```bash
tool deploy <project> [--env <name>] [--output <table|json|yaml>] [--wait]
```

## Mandatory argument table format

Use this exact column order:

| Flag / Argument | Shorthand | Required | Type | Default | Allowed Values | Description |
|---|---|---|---|---|---|---|
| `--project <id>` | `-p` | Yes | string | none | any valid project id | Target project identifier. |
| `--output <format>` | `-o` | No | enum | `table` | `table`, `json`, `yaml` | Output format. |
| `--force` | `-f` | No | boolean | `false` | `true`, `false` | Bypass confirmation prompts. |

## Example rules

- Include at least 3 runnable examples:
  - Minimal happy path.
  - Common real-world path.
  - One safety-focused or debug-focused path.
- Use real values, not placeholders like `<VALUE>` in copy blocks.

## Output and exit code rules

- Document stdout format and key fields.
- Document stderr style for user-facing errors.
- Provide an exit code table when non-trivial.

Example:

| Exit Code | Meaning |
|---|---|
| `0` | Success |
| `1` | General command failure |
| `2` | Validation or argument error |

## AI parsing notes

- Keep one canonical command page per command.
- Keep argument table schema identical across commands.
- Avoid embedding critical flag semantics only in prose.

## Related standards

- [principles.md](./principles.md)
