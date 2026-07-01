---
name: update-generated-dev-docs
description: Workflow command scaffold for update-generated-dev-docs in windows.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-generated-dev-docs

Use this workflow when working on **update-generated-dev-docs** in `windows`.

## Goal

Regenerate and update developer documentation for tweaks, usually after tweaks are added or changed.

## Common Files

- `docs/content/dev/tweaks/**/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Generate or update markdown files for each tweak in docs/content/dev/tweaks/...
- Commit the changes with a message referencing dev docs update.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.