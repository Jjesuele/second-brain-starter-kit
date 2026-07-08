# Directive: Update Skills from the Template

Fetch the latest shared Claude skills from the original template repo and refresh this vault's copies. Run when the owner says "update my skills" or hears the template has improved. Opt-in and manual; nothing about this runs on its own.

## What updates and what never does

- **Updates:** files under `dot-claude/skills/` and `dot-claude/optional-skills/`, and their installed copies in `~/.claude/skills/`.
- **Never touched:** `context/`, `brain/`, `sources/`, the vault's own `skills/` folder (the owner's expertise), `directives/` (self-annealing may have improved them locally), `claude-backup/`, and `~/.claude/CLAUDE.md`.

## Process

**Step 1: Fetch.** Download the current template from github.com/Jjesuele/second-brain-starter-kit (clone to a temporary folder, or download its ZIP). If it cannot be reached, stop and say so.

**Step 2: Diff.** Compare the template's `dot-claude/skills/` and `dot-claude/optional-skills/` against this vault's copies. Show the owner a plain-English summary of what changed per skill, plus the raw diff if they want it.

**Step 3: Apply with approval.** For each changed skill the owner approves: overwrite the copy in this vault's `dot-claude/`, and if that skill is installed in `~/.claude/skills/`, reinstall the new version there too. Skills the owner has deliberately customized locally: flag the conflict and let them choose keep, replace, or merge. Never silently clobber a local customization.

**Step 4: Note improved directives, hands off.** If the template's `directives/` also changed, list what changed and offer the diffs, but do not apply them automatically; the owner's local directives may have self-annealed past the template's version.

**Step 5: Clean up and commit.** Delete the temporary download. Commit the vault changes with the message "update skills from template" and push if a remote exists.

## Quality gates

- [ ] Every applied change was shown and approved first
- [ ] Nothing outside `dot-claude/` and `~/.claude/skills/` was modified
- [ ] Vault copy and installed copy of each updated skill match
- [ ] Temporary download deleted, changes committed
