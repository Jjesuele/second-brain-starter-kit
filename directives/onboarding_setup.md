# Directive: Onboarding Setup (run once)

Turn this blank starter kit into the owner's personalized second brain. Claude runs this; the owner just answers questions. Follow every step in order. Do not skip the interview and do not invent answers the owner did not give.

Before anything else, tell the owner in one sentence what this setup will do: interview them, write their personal files, install the Claude skills, and save a first backup. Then begin.

## Step 1: Confirm locations

1. Confirm the vault location: the folder this file lives in. If it is not already at `~/second-brain`, offer to move or rename it there (a short, stable path keeps every other instruction simple). Follow the owner's preference; any location works.
2. Confirm `~/.claude/` exists (Claude Code creates it). On Windows, `~` means the user's home folder, `C:\Users\<name>`.

## Step 2: Install the Claude skills

1. Copy every folder from `dot-claude/skills/` into `~/.claude/skills/` (on Windows that resolves to `C:\Users\<name>\.claude\skills`).
2. Do NOT copy `dot-claude/optional-skills/` unless the owner asks for those modules (offer them once, in one sentence: real estate deal analysis and recruiting prep exist as opt-ins).
3. If a skill folder with the same name already exists in `~/.claude/skills/`, ask before overwriting.
4. Keep the `dot-claude/` folder in the vault. It is the install and update source.

## Step 3: The interview

Ask conversationally, a few questions at a time, not as one giant form. Gather:

1. **Basics:** name, school or job, year or role, where they are based.
2. **Right now:** what they are currently doing and actively learning or building.
3. **Direction:** what they are working toward, and how settled that is.
4. **Outside work:** hobbies and background that show up in their writing and life.
5. **Strengths and gaps:** where they do their best work, and what takes deliberate effort. Explain why honest gaps make the AI more useful.
6. **Writing preferences:** ask whether they want these defaults, individually, explaining each in one line:
   - No em dashes or hyphens as punctuation (some writers never use them; keep only if true of them).
   - Plain language over jargon.
   - Verdict-first answers to decision questions.
7. **Writing samples:** ask for one or two pieces of their real writing (an email, an essay paragraph, a post). This matters more than the stated preferences; real text is what the voice file gets calibrated from. If they truly have nothing at hand, note in `voice.md` that it is uncalibrated and should be updated when a sample exists.
8. **Confidentiality:** what stays private (employer material, family matters, anything else), and how to genericize it when writing for the outside world. "Nothing yet" is a valid answer.

## Step 4: Write the context files

Using the interview answers and writing samples, fill in all four files, replacing every [FILL IN] marker:

1. `context/me.md` with today's real date on the "Last confirmed" line.
2. `context/standards.md` (only rule 3, confidentiality, needs their input; the rest ships final).
3. `context/voice.md` calibrated from the samples: observed sentence rhythm, habitual transitions, signature moves, hedging style, concrete detail types. Note which samples it was calibrated from. Keep the banned AI-tells list.
4. `context/worked-examples.md` with three examples matched to their life, the voice example built from their actual samples.

Show the owner each file after writing it, and adjust until they say it sounds like them. Do not proceed while any [FILL IN] marker survives in these four files.

## Step 5: Generate their personal Claude operating file

1. Read `dot-claude/CLAUDE.md.template`.
2. Fill its placeholders from the interview, and wire every vault path in it to the real vault location from Step 1.
3. **If `~/.claude/CLAUDE.md` already exists**, do not overwrite it. Copy the existing file to `~/.claude/CLAUDE.md.bak`, show the owner a diff between theirs and the new one, and merge with their approval. Only a missing or empty file gets written directly.
4. Write the result to `~/.claude/CLAUDE.md`.
5. **Windows fallback if the write to `~/.claude/CLAUDE.md` is blocked.** Claude Code guards writes outside the open project folder, and on Windows approving the prompt does not always clear it. If the write comes back blocked, write the finished operating file to `claude-backup/CLAUDE.md` inside the vault instead (writes inside the project folder are never blocked), then tell the owner to copy that file by hand into `%USERPROFILE%\.claude\CLAUDE.md` using File Explorer. Reach the folder by typing `%USERPROFILE%\.claude` into the Explorer address bar; create it if it is missing. The manual copy has no permission wall.

## Step 6: Back up the operating file into the vault

Copy the finished `~/.claude/CLAUDE.md` into `claude-backup/CLAUDE.md` so the git backup covers it. (The installed skills need no copy; they are identical to `dot-claude/skills/`.)

## Step 7: Save the first backup

1. Check whether `git` is available and this folder is a git repository.
2. **If they cloned their own private repo** (the recommended path): set their git identity if unset (ask for the name and email to use), then commit everything with the message "initial personalized setup" and push.
3. **If there is no git or no GitHub:** offer `git init` for local-only version history (still worthwhile). If they decline or git is absent, skip cleanly and add a line at the top of their `README.md`: "Backup not set up yet. To add it later: create a private GitHub repo and push this folder to it."
4. Never block setup on this step. A working brain without a backup beats no brain.

## Step 8: Optional add-ons (offer once, install only what the owner wants)

None of these are required; the brain works without all of them. Present the list in a few lines, name what each one is and costs (all are free; the only cost is installation and, for plugins, extra instructions loaded into sessions), and install only what the owner picks. Skipping all of them is a fine answer.

1. **Superpowers plugin** — adds structured workflows (brainstorming before building, systematic debugging, test-driven development). In Claude Code run `/plugin marketplace add obra/superpowers`, then `/plugin install superpowers`.
2. **Security-guidance plugin** — warns about risky commands and code patterns. Run `/plugin marketplace add anthropics/claude-code`, then `/plugin install security-guidance`.
3. **Obsidian** (free app, obsidian.md) — a nice way to read and browse the vault: the wikilinks become clickable and the note graph is visible. Download it, then "Open folder as vault" pointing at this folder. The json-canvas, obsidian-markdown, and obsidian-bases skills produce files that shine in it.
4. **Obsidian CLI** — lets Claude Code control the Obsidian app directly (only useful if Obsidian is installed and open). Setup instructions: help.obsidian.md/cli. The obsidian-cli skill works without any other part of this kit changing.
5. **Defuddle CLI** — cleaner, cheaper web page reading for the defuddle skill. Requires Node.js (nodejs.org). Install with `npm install -g defuddle`. Until it is installed, that one skill simply won't work; nothing else is affected.
6. **claude.ai connectors (Google Drive, Gmail, Calendar)** — connect the owner's own Google account so documents can flow into `sources/` for mining. Done in the browser at claude.ai → Settings → Connectors → Connect, then the normal Google sign-in. These are per-account authorizations; nothing is stored in this vault.

## Step 9: Verify, then hand over

1. Ask the owner to start a **new** Claude Code session in the vault and ask it: "Who am I and how do I like to write?" It should answer from their files, not generically.
2. In that new session, have it draft two sentences on any topic in their voice, and check the draft against `voice.md` together.
3. If either check fails, find which file is wrong or unread and fix it before declaring setup done.
4. Point them at the "Try this first" task in `README.md`.

## Quality gates

- [ ] Every [FILL IN] marker in the four context files is gone
- [ ] Voice file cites the real samples it was calibrated from (or is marked uncalibrated)
- [ ] `~/.claude/CLAUDE.md` written, with the pre-existing-file case handled by backup and merge, never silent overwrite
- [ ] `claude-backup/CLAUDE.md` matches `~/.claude/CLAUDE.md`
- [ ] First commit made and pushed, or the no-backup note added to README
- [ ] Fresh-session verification passed
