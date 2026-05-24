---
name: add-new-language-binding
description: Workflow command scaffold for add-new-language-binding in ip2region.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-language-binding

Use this workflow when working on **add-new-language-binding** in `ip2region`.

## Goal

Adds support for a new programming language binding, including implementation, test/example, and documentation.

## Common Files

- `binding/<language>/*`
- `binding/<language>/README.md`
- `binding/<language>/ip2Region.*`
- `binding/<language>/testSearcher.*`
- `binding/<language>/main.*`
- `binding/<language>/Program.cs`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create new directory under binding/<language>/
- Add core implementation files (e.g., ip2Region.*)
- Add test/example files (e.g., testSearcher.*, main.*, Program.cs)
- Add or update README.md for the new binding
- Update top-level README.md to mention the new binding

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.