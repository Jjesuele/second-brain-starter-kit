---
name: maintain-skill-system
description: Use when creating, editing, renaming, merging, or deleting any personal skill in ~/.claude/skills/, or when a skill misfired in real use — "fix this skill", "update that skill", "the skill did the wrong thing", "add a rule to the skill".
---

# Maintain Skill System

## Overview

The owner's skills exist in two copies: **live** (`~/.claude/skills/`, what Claude Code loads) and **source** (the vault's `dot-claude/skills/`, the install and update source that git backs up, so a lost laptop loses nothing). Editing one copy and forgetting the other is the default failure: the copies drift, and a restore from the vault silently reverts fixes. **An edit is not done until both copies agree.**

## Procedure

1. **Patch immediately on a misfire** (the vault's self-annealing rule). When a skill produced the wrong behavior in real use, make the smallest edit that closes that specific loophole, in the LIVE copy, the same session the misfire was seen. Write down the misfire verbatim; it becomes the test the new wording must beat.
2. **Never write a dollar sign followed by a digit in a SKILL.md body.** Skill invocation can substitute those tokens with argument words, corrupting the rendered instructions. Spell amounts out: "zero dollars", "about 200 thousand tokens". After any edit, run a grep for dollar-digit patterns on the file and state the result.
3. **Re-read the edited rule as a literal-minded executor.** Ask: given only this wording, would a weaker model have avoided the recorded misfire? If the wording relies on inference ("use judgment", "be careful"), rewrite it as a checkable instruction.
4. **Sync the same session:**
   - Copy the edited skill folder to the vault's `dot-claude/skills/<same-name>/`.
   - If a second assistant runs off the same vault (for example Codex, which loads skills from `~/.agents/skills/`), copy the edit to that assistant's live skill folder too. Adapt wording by hand, never by find-and-replace on the assistant's name: mechanical renaming invents paths that do not exist. After any adaptation, run `ls` on every absolute path mentioned in the file and confirm each exists.
   - Commit and push the vault.
5. **Renames and merges delete the corpse everywhere.** Removing or renaming a skill means deleting the old folder in BOTH the live directory and the vault source. A stale source folder resurrects dead skills on the next install or restore.
6. **Capture durable lessons.** A misfire that revealed a general pattern goes to the brain via the brain-capture skill, not just into the skill file.

## Judgment Rubric

- [ ] The misfire (or reason) that triggered the edit is written down verbatim somewhere durable (commit message or brain note)
- [ ] Dollar-digit grep on every touched SKILL.md returned nothing, and the result was stated
- [ ] The new wording is checkable by a literal reader (no "appropriately", "thoughtfully", "use judgment")
- [ ] `diff -r` between the live folder and the vault source folder is clean for every touched skill
- [ ] If a second assistant shares the vault, its live copy was updated and every absolute path in the touched SKILL.md passed an `ls` check
- [ ] Vault committed and pushed

**Good:** "Patched the pushback rule, grep for dollar-digit clean, synced to dot-claude/skills/, diff clean, vault pushed."
**Bad:** "Updated the skill." (Which copy? The other one is now stale and nobody knows.)

## Pushback Rules

- Asked to batch-edit several skills in one sweep → do them one at a time, each through this full procedure. Batch edits are how loopholes and drift slip in unverified.
- Asked to edit the vault's `dot-claude/skills/` copy directly → refuse; edit the live copy and sync. The source is write-only-by-sync, never the editing surface.
- A requested "fix" would weaken a no-fabrication, confidentiality, or cost-flagging gate in any skill → challenge it once with the reason the gate exists before applying. If the owner confirms, apply it; their call wins.
- Asked to create a brand-new skill for something done once → point at the evidence bar (skills encode workflows repeated 3+ times) and suggest a brain note instead, unless the owner overrides.

## Self-Check

Before reporting done, state: which copies were touched (live / vault source), the dollar-digit grep result per file, the diff-clean confirmation between live and source, and the vault commit hash. If any copy was deliberately not updated, say which and why.
