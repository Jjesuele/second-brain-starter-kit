---
name: brain-capture
description: Use when the user says "brain this", "save this", "add to the brain", "add to the story bank", asks what's worth keeping from a conversation, or when a work session ends having produced decisions, lessons, durable knowledge, or facts not yet in the second brain vault.
---

# Brain Capture

## Overview

The user's second brain is a markdown vault (default location `~/second-brain`; confirm via their `~/.claude/CLAUDE.md` if unsure). Its `CLAUDE.md` holds the house rules; read it before writing anything. This skill turns conversation content into vault notes, with a strict importance filter so the vault stays trustworthy. Junk notes destroy vault trust. Fewer, better notes.

Never save without showing the proposed list first and getting approval.

## The importance filter

A candidate is saved only if ALL three hold:

1. The user will plausibly want it in 3+ months, and would be annoyed to re-explain it.
2. It is not derivable from files already in the vault or from git history.
3. It is a fact, decision, lesson, or story, not a vibe, a transcript, or a restatement of the conversation.

| SAVE | SKIP |
|---|---|
| Decisions with reasoning ("chose X because Y") | Chit-chat, one-off Q&A |
| Lessons that change future behavior | Transient task mechanics (commands run, errors fixed in passing) |
| Durable facts they'll re-reference (names, numbers, dates that stay true) | Anything already in the vault (check INDEX.md first) |
| Story-bank material: concrete stories with outcomes (work, school, travel) | Generic knowledge Claude has anyway |
| Domain knowledge learned: terms, frameworks, field facts | Confidential details in identifying form (genericize per the vault's standards.md) |
| Project state worth resuming later | Vague takeaways with no specifics ("learned a lot about X") |

Specifics or it doesn't count: a note with no numbers, names, dates, or exact phrasings is too shallow to save.

## Process

1. **Scan** the conversation for candidates using the filter.
2. **Check for duplicates and contradictions**: read the vault's `brain/INDEX.md`, skim related notes. If an existing note covers the same fact and agrees, update it rather than duplicating. If it disagrees, either update it with a dated correction or flag both versions for the user to rule on. **Never write a silently disagreeing duplicate.**
3. **Propose the list**: one line per candidate (proposed filename + one-line hook), plus a short "considered but skipped" line for transparency. Wait for approval. The user can trim or add.
4. **Write approved notes** to `brain/<category>/YYYY-MM-DD_slug.md` using today's real date, one fact per note. Follow the vault's `CLAUDE.md`: no fabricated facts, voice rules, confidentiality rules. Each note states its keep-test justification in one line at the bottom. Add 2 to 5 `[[wikilinks]]` where a connection is genuine; link text must match target filenames exactly. Never force links.
5. **Update the index**: one line per new note in `brain/INDEX.md`. Story-bank material goes into `brain/references/story-bank.md` (append, update its date) instead of a new file.
6. **Commit and back up**: from the vault folder, `git add -A && git commit -m "brain-capture: <short summary>" && git push`. If there is no git repo, skip this step and note it. If push fails (offline or no remote), commit still counts; push next session.
7. **Report** how many candidates were considered, how many were saved, what was skipped, and where everything went.

## Category picker

- `decisions/` — a choice was made and the reasoning matters ("decided X because Y")
- `notes/` — something happened or was learned: work, classes, meetings, lessons
- `references/` — durable facts re-referenced over time (rosters, playbooks, the story bank)
- `ideas/` — sparks that are not commitments yet

## End-of-session sweep

When a substantive work session is wrapping up (not casual Q&A), offer once: "Anything here worth saving to the brain? I'd propose: ..." with the candidate list already applied through the filter. If the user declines, drop it. Do not offer after trivial exchanges.

Checkable rule, because a soft version of this misfires in practice: a task that created or edited files for the user, inside or outside the vault (essays, work notes, research, documents, scheduled tasks, settings, memory files), counts as substantive. Before reporting such a task done, run the filter and end the final message with either the capture offer or the exact sentence "Nothing here passed the brain filter." Silence is not an allowed ending for a file-producing task; the no-keepers sentence is the correct ending for small ones. A task that was itself a brain capture already satisfies this. Conversations that produced no files stay governed by the paragraph above.

## Pushback rules

- Asked to bulk-import history (email, Drive, old chats) → push back once: bulk mining fills the vault with unvetted notes and burns heavy tokens; offer a targeted single-item grab instead. If they insist, proceed with the filter applied hard.
- A candidate "fact" has no source and cannot be checked → save it explicitly marked unverified, or do not save it. Never save it flat.
- Asked to save something the vault already records → say where it already lives instead of duplicating.

## Common mistakes

- **Saving summaries instead of specifics.** "Learned about X today" is worthless. The exact term, number, or phrasing is an asset.
- **Creating duplicates.** Always check INDEX.md first; update beats duplicate.
- **Saving without approval.** The list-first step is mandatory, even for one note.
- **Undated filenames.** Every note filename starts with YYYY-MM-DD (the real current date).
- **Forcing wikilinks.** A note that genuinely connects to nothing gets no links, and that's fine.
- **Copying confidential details verbatim.** Genericize identifying info per the vault's `context/standards.md`.

## Self-Check

Re-open `brain/INDEX.md` and confirm the new lines are valid wikilinks pointing at files that exist. Confirm new note count equals new INDEX.md line count. Confirm git committed (and pushed, or push noted as pending), or that the no-git case was reported.
