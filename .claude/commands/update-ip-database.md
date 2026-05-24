---
name: update-ip-database
description: Workflow command scaffold for update-ip-database in ip2region.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-ip-database

Use this workflow when working on **update-ip-database** in `ip2region`.

## Goal

Updates the underlying IP database and merged data file to a new version.

## Common Files

- `data/ip.merge.txt`
- `data/ip2region.db`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Replace data/ip.merge.txt with new version
- Replace data/ip2region.db with new version
- Commit with a message referencing the new data version

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.