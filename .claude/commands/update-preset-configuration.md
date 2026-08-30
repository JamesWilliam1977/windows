---
name: update-preset-configuration
description: Workflow command scaffold for update-preset-configuration in windows.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-preset-configuration

Use this workflow when working on **update-preset-configuration** in `windows`.

## Goal

Updates to the preset configuration for the application, typically to adjust default settings or available options.

## Common Files

- `config/preset.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit config/preset.json with new or updated preset values.
- Commit the changes with a message referencing preset updates.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.