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
> 7. BACKUP SYNC: Check that `claude-backup/CLAUDE.md` still matches `~/.claude/CLAUDE.md`; if not, propose refreshing the copy.
>
> Show me the full list of proposed edits before changing anything. After I approve, apply them, update the "Last updated" date in CLAUDE.md, refresh CURRENT FOCUS with today's date, and commit the vault changes.

## Checklist (quality gate)

- [ ] Every proposed edit was shown to the owner before being applied
- [ ] Vault lint ran: dead links, stubs, and index gaps all flagged with a proposed fix
- [ ] CLAUDE.md "Last updated" and CURRENT FOCUS dates refreshed
- [ ] No file grew past its budget (CLAUDE.md stays under roughly 500 words; push depth into vault files)
- [ ] `claude-backup/CLAUDE.md` matches the live operating file
- [ ] Vault changes committed with a clear message and pushed (if a remote exists)
- [ ] Next audit date noted here: last run [FILL IN], next due [FILL IN]
