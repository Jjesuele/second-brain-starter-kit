# Second Brain: Operating Manual

This folder is the owner's second brain. Read this file first, every session.

**If `context/me.md` still contains [FILL IN] placeholders, setup has not run yet. Stop and follow `directives/onboarding_setup.md` before doing any other work here.**

## How this system works

Three layers, adapted from the DOE pattern (Directive, Orchestration, Execution):

- **Directives** (`directives/`): step-by-step workflows in plain English. When the owner asks for something repeatable, check here first for a matching SOP.
- **Orchestration** (you, the AI): read the right context, follow the SOP, apply judgment, check quality before delivering.
- **Execution**: there are no scripts in this system by design. Everything runs through Claude Code on the owner's plan. Do not add scripts, API integrations, or anything requiring API keys without asking first and flagging any cost.

## Directory map

- `context/` — who the owner is, how they write, and the hard rules. Load before any work.
- `directives/` — SOPs for repeated workflows. One file per workflow.
- `skills/` — the owner's extracted expertise, organized by area. Load relevant files for related work.
- `brain/` — dated, wiki-linked notes: decisions, notes, references, ideas. `INDEX.md` is the map; read it first, then open only what is relevant.
- `sources/` — raw material (transcripts, exports, documents) waiting to be mined into brain notes.
- `claude-backup/` — a mirror of the owner's personal `~/.claude/CLAUDE.md`, kept here so git backs it up. When that file changes, refresh the copy here.
- `dot-claude/` — the install and update source for Claude skills. Not read during normal work.
- `.tmp/` — scratch space for drafts. Never committed.

## Context loading priority

1. `context/me.md` — always first (who the owner is)
2. `context/standards.md` — always (hard rules; check work against them)
3. `context/voice.md` and `context/worked-examples.md` — for any writing
4. `skills/` relevant files — domain expertise for the task
5. `directives/` the matching SOP — the workflow itself
6. `brain/INDEX.md` — when the task touches past decisions, notes, or ongoing threads

## Standing rules

1. **Never fabricate.** No invented numbers, results, citations, names, or facts. Use a clearly labeled placeholder and ask.
2. **Date everything.** Brain notes are named `YYYY-MM-DD_short-slug.md`. An undated fact becomes a landmine when things change.
3. **Cite sources.** Skill files carry their source and date at the top. Claims in notes say where they came from.
4. **Write in the owner's voice.** Voice rules live in `context/voice.md`. Anything carrying their name gets checked against that file.
5. **Confidentiality.** Whatever the owner marked private in `context/standards.md` stays inside the vault. When in doubt, genericize.
6. **This vault can be read in Obsidian.** Use `[[wikilinks]]` between brain notes, with link text matching the target filename exactly so links resolve.
7. **End file-producing tasks with a capture check.** Any task that created or edited files for the owner, inside or outside this vault (scheduled tasks, settings, memory files all count), ends with either a brain capture offer or the exact sentence "Nothing here passed the brain filter." Never silence. A task that was itself a brain capture already satisfies this.

## Self-annealing protocol

After every task: if a step in a directive was wrong or missing, update the directive. If a better approach was found, update the relevant skill file. If a new edge case appeared, add it to the SOP. If a fact in the brain turned out stale or wrong, correct the note and record the correction with a date. Small edits, made immediately, are how this system compounds.

## Maintenance

- After adding brain notes, add one line each to `brain/INDEX.md`.
- If a task creates a new top-level folder in this vault, offer to add a matching Obsidian graph color rule (Graph view → Groups, a `path:` filter per folder) so its notes are not gray dots.
- Every few weeks, run the audit in `directives/monthly_context_audit.md`.
- If the owner's `~/.claude/CLAUDE.md` changed, refresh the copy in `claude-backup/`.
- Git tracks everything. Commit after meaningful changes with a clear message, then push if a remote is set up. If push fails (offline), commit anyway and push next time.
