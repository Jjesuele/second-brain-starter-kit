# Directive: Monthly Context Audit

Run this on the strongest model available, roughly monthly. It keeps `~/.claude/CLAUDE.md` and the vault's context files matched to reality so cheaper daily models inherit current rules, not stale ones.

## The prompt to paste

> Audit my context files against recent reality. Read `~/.claude/CLAUDE.md`, then this vault's `context/` (me.md, standards.md, voice.md, worked-examples.md), then skim my last month of conversation history or session transcripts if you have access to them.
>
> 1. STALE: Flag every dated fact that has passed or changed (courses, job status, CURRENT FOCUS items, open questions now answered). Propose the corrected line for each.
> 2. CONTRADICTIONS: Flag any two files that disagree. Name the winner and the edit to the loser.
> 3. RULE DRIFT: Find feedback I gave repeatedly this month that is not yet a written rule. Convert each into an if/then a literal-minded model can follow, and propose where it goes (HOW I WORK vs QUALITY BAR vs voice.md).
> 4. DEAD RULES: Flag any rule I overrode or ignored more than once this month. Ask me whether to delete or rewrite it.
> 5. EXAMPLES: If any output this month was clearly better than what worked-examples.md shows, propose swapping it in with a note on why.
> 6. VAULT LINT: Sweep every .md file in the vault. Flag (a) wikilinks that point to notes that do not exist, (b) stub or placeholder notes with little real content, (c) notes missing from brain/INDEX.md and index entries pointing at nothing. Skip links that sit inside code spans, quoted examples, or template files; those are illustrations, not real links. Propose a fix for each real hit: write the note, delete the link, or update the index. These go in the same approval list as everything else.
> 7. INTEGRITY: Check that `claude-backup/CLAUDE.md` still matches `~/.claude/CLAUDE.md`, and diff each installed skill in `~/.claude/skills/` against its copy in this vault's `dot-claude/skills/` (and `dot-claude/optional-skills/`); propose refreshing whichever side is stale. Also check every absolute path mentioned in each SKILL.md and in `~/.claude/CLAUDE.md` actually exists; a path that fails is a broken instruction. Flag every mismatch or dead path with a proposed fix.
> 8. SYMLINKS: Sweep `~/.claude/` and the vault for symlinks (`find <dir> -type l`). Any symlink whose target is missing is broken: flag it with a proposed restore from a real copy. Any symlink posing as a skill, backup, or config copy is a latent failure even if its target still exists: flag it for replacement with real files. Backups must be real copies; a symlink dies with its target and git stores only the pointer.
>
> Show me the full list of proposed edits before changing anything. After I approve, apply them, update the "Last updated" date in CLAUDE.md, refresh CURRENT FOCUS with today's date, and commit the vault changes.

## Checklist (quality gate)

- [ ] Every proposed edit was shown to the owner before being applied
- [ ] Vault lint ran: dead links, stubs, and index gaps all flagged with a proposed fix
- [ ] CLAUDE.md "Last updated" and CURRENT FOCUS dates refreshed
- [ ] No file grew past its budget (CLAUDE.md stays under roughly 500 words; push depth into vault files)
- [ ] `claude-backup/CLAUDE.md` matches the live operating file, and installed skills match their `dot-claude/` copies
- [ ] Symlink sweep ran: no broken symlinks, and no symlinks posing as skills, backups, or config copies
- [ ] Vault changes committed with a clear message and pushed (if a remote exists)
- [ ] Next audit date noted here: last run [FILL IN], next due [FILL IN]
