---
name: vet-tool-before-adopting
description: Use when the user asks whether to install, keep, trust, or evaluate any Claude Code skill, plugin, MCP server, connector, or GitHub repo, "is this safe", "should I add this", "what does this skill do", "my friend uses X".
---

# Vet Tool Before Adopting

## Overview

Tools get adopted carefully: token burn and background-server dependencies are the usual reasons to reject one. A vetting answer based on a README is worthless; the value comes from reading the actual artifact and committing to a verdict. **Never vouch for code you did not open.**

## Procedure

1. **Fetch and read the actual artifact.** For a skill: SKILL.md plus every file in its folder. For a plugin: the manifest plus any scripts. For a repo: the files that execute, not the README. List which files contain executable code (`.py`, `.sh`, `.js`, hooks) versus pure markdown.
2. **Fill the audit table** — one row per component, answering from opened files only:

   | Component | Runs commands? | Network access? | Touches files outside its folder? | Auto-triggers? | Injects context every session? |
   |---|---|---|---|---|---|

   For auto-trigger, check for model-invocation flags (e.g. `disable-model-invocation`) and hook registrations.
3. **Cost pass.** State what it burns in plain terms: per-session context injection ("adds roughly Xk tokens to every session"), background processes, per-commit AI calls, auto-installed runtimes. Recurring costs must be labeled recurring. State the cost even when the verdict is ADD.
4. **Access pass.** If it needs credentials or a paid seat the user does not personally have, lead with that before discussing features, and frame it as "ask your school or employer for access."
5. **Overlap pass.** Name any already-installed skill or tool that covers the same need.
6. **Verdict.** Exactly one of **ADD / SKIP / ADD-BUT** (with the single condition). One sentence per factor that decided it. No "it depends" ending.

## Judgment Rubric

- [ ] Every claim about the tool cites the filename it came from
- [ ] Audit table complete, from opened files, not inference
- [ ] Token/resource cost stated regardless of verdict
- [ ] Overlap with existing tools checked and named
- [ ] Exactly one verdict

**Good:** "Safe: pure markdown, no code, no network (checked all 4 files). But it runs a full audit pass plus a second rewrite of your text every use, so real token burn. SKIP unless you hit its exact use case weekly."
**Bad:** "Looks useful! It has good reviews and could help with your essays."

## Pushback Rules

- Source cannot be fetched or read → say the review is limited to the description, downgrade confidence explicitly, and do not vouch. Offer to review properly if the user can provide the files.
- The tool requires a paid seat they do not have → that fact leads the answer; do not bury it under features.
- They are excited about it but it duplicates something installed → name the duplicate before the verdict.

## Self-Check

Confirm each audit-table cell traces to a file opened this session; confirm the verdict line exists and is singular; confirm cost was stated in concrete terms, not "some overhead."
