```markdown
# windows Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns and workflows used in the `windows` TypeScript codebase. You'll learn about file and code organization, naming conventions, and how to perform common configuration and documentation updates. The repository is framework-agnostic and uses structured commit messages and configuration-driven workflows.

## Coding Conventions

**File Naming**
- Use **PascalCase** for file names.
  - Example: `MainWindow.ts`, `PresetManager.ts`

**Import Style**
- Use **relative imports**.
  - Example:
    ```typescript
    import { Preset } from './PresetManager';
    ```

**Export Style**
- Use **named exports**.
  - Example:
    ```typescript
    export function applyTweaks() { ... }
    export const DEFAULT_PRESET = { ... };
    ```

**Commit Messages**
- Prefix with `chore` or `feat`.
- Average commit message length: ~44 characters.
  - Example: `feat: add new dark mode tweak`

## Workflows

### Update Preset Configuration
**Trigger:** When you need to change or update the application's preset configuration.
**Command:** `/update-preset`

1. Edit `config/preset.json` with new or updated preset values.
2. Commit the changes with a message referencing preset updates.
   - Example commit: `chore: update preset configuration for v2`

### Update Tweaks Configuration
**Trigger:** When you want to add, remove, or modify tweak options.
**Command:** `/update-tweaks`

1. Edit `config/tweaks.json` to add, remove, or modify tweak entries.
2. Commit the changes with a message referencing tweaks updates.
   - Example commit: `feat: add 'compact mode' tweak`

### Update Generated Dev Docs
**Trigger:** When tweaks are added or modified and developer documentation needs updating.
**Command:** `/update-dev-docs`

1. Generate or update markdown files for each tweak in `docs/content/dev/tweaks/`.
   - Example file: `docs/content/dev/tweaks/CompactMode.md`
2. Commit the changes with a message referencing dev docs update.
   - Example commit: `chore: update dev docs for new tweaks`

## Testing Patterns

- Test files follow the pattern `*.test.*` (e.g., `PresetManager.test.ts`).
- The testing framework is not explicitly specified.
- Tests are colocated with the code or in a parallel structure.
- Example test file:
  ```typescript
  // PresetManager.test.ts
  import { getDefaultPreset } from './PresetManager';

  test('returns default preset', () => {
    expect(getDefaultPreset()).toBeDefined();
  });
  ```

## Commands

| Command            | Purpose                                                        |
|--------------------|----------------------------------------------------------------|
| /update-preset     | Update the application's preset configuration                  |
| /update-tweaks     | Update the tweaks configuration                                |
| /update-dev-docs   | Regenerate and update developer documentation for tweaks       |
```
