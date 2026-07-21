# Second Brain Starter Kit

One folder that holds who you are, how you work, what you know, and what you have decided. Claude Code reads it to do work your way. You read it in Obsidian (optional) to think.

This kit ships as blank scaffolding plus a guided setup. You answer an interview once, and Claude writes all your personal files for you. You never hand-edit anything to get started.

## What you need first

1. **Claude Code** installed and working. That is the app this kit runs on. If you do not have it, install it from Anthropic first.
2. **A free GitHub account** (recommended, not required). With one, your whole brain gets a private online backup and version history. Without one, everything still works, it just lives only on your computer.

### Starting from scratch

If Claude Code is not on the machine yet, these two steps are the same on any computer:

1. You need a Claude account with a paid plan (Pro or Max) at claude.ai. Claude Code runs on that plan; there is no separate cost.
2. Install Claude Code: download the desktop app from claude.com/claude-code, or if you prefer the terminal, follow the install instructions at docs.anthropic.com/en/docs/claude-code. Either works with this kit. Open it once and sign in with your Claude account. If it can answer "hello", you are ready.

Then get git, which differs by machine:

**On a Mac:** git ships with macOS. The first time you run a git command, the Mac may offer to install the command line tools; accept.

**On a Windows PC:** git does NOT ship with Windows. The easy path is **GitHub Desktop** (desktop.github.com), which includes git and handles sign-in; the next section recommends it anyway. If you prefer the command line, install **Git for Windows** from git-scm.com instead. Either one is enough.

## Get your copy

**With GitHub (recommended):**

1. On this repo's page, click **Use this template → Create a new repository**.
2. Name it whatever you like and set it to **Private**. Private matters: this folder will hold your personal notes.
3. Get it onto your computer. The smoothest path is the free **GitHub Desktop** app (desktop.github.com): install it, sign in through your browser, click **Clone a repository**, pick your new repo, and choose where it lands. This also stores your GitHub credentials on the machine, so every backup after this pushes without prompts.
4. Terminal alternative, only if git is already set up to talk to GitHub: `git clone <your new repo URL>`. Heads up: GitHub no longer accepts your account password for git commands, so a fresh machine will fail here with "password authentication is not supported" until you set up a personal access token or SSH key. If you hit that, use GitHub Desktop instead; it is the two-minute fix on Mac and Windows alike.

**Without GitHub:** click **Code → Download ZIP** on this page, unzip it, and you have the same folder. You can add the backup later.

Either way, consider moving or renaming the folder to `second-brain` in your home folder. The setup will ask.

## Set it up (one time, about 10 to 15 minutes)

1. Open Claude Code in this folder.
2. Paste this line:

```
Read directives/onboarding_setup.md and follow it exactly to set up my second brain.
```

3. Answer the interview: who you are, what you are working on, how you like to write, and one or two samples of your real writing. Claude writes your personal files, installs the skills, and saves the first backup.

That is the whole setup.

## Try this first

Right after setup, test the system with one real task. Think of something you decided recently, anything at all, and tell Claude:

```
Save this to my brain: [what you decided and why]
```

Claude will propose a dated note, ask your approval, file it, and back it up. If that works, everything works.

## What's where

| Folder | What it holds |
|---|---|
| `context/` | Who you are, your writing voice, your hard rules |
| `directives/` | Step-by-step recipes for repeated tasks |
| `skills/` | Frameworks and expertise you extract from courses, work, and books |
| `brain/` | Dated, linked notes: decisions, references, ideas, everything worth remembering |
| `sources/` | Raw material (transcripts, exports, documents) waiting to be turned into notes |
| `claude-backup/` | A copy of your personal Claude operating file, kept here so git backs it up |
| `dot-claude/` | The install source for your Claude skills. Setup copies from here. Keep it. |

## Optional modules

Two extras ship in `dot-claude/optional-skills/` and `directives/optional/`, switched off by default:

- **Commercial real estate deal notes**: turn offering memos and deal material into structured teardown notes.
- **Recruiting prep**: firm research, coffee chat prep, interview prep, and a story bank.

If either fits your life, tell Claude: "install the optional [real estate / recruiting] module" and it will copy the skill into place.

## Optional add-ons

Setup offers these once (Step 8 of the onboarding directive); all are free and all are skippable:

- **Superpowers plugin** — structured workflows for building and debugging with Claude Code.
- **Security-guidance plugin** — warnings about risky commands and code.
- **Obsidian** (obsidian.md) — a beautiful way to read the vault; wikilinks become clickable and the note graph is visible.
- **Obsidian CLI and Defuddle CLI** — small command line helpers two of the skills use; each skill names its own install command.

**How to install the two plugins.** In Claude Code, type `/plugin` to open the plugin manager. Add the two sources once:

```
/plugin marketplace add obra/superpowers
/plugin marketplace add anthropics/claude-code
```

Then pick **superpowers** and **security-guidance** from the menu and install them. Both are free and run on your Claude plan; nothing here costs extra. You can skip either and add it later the same way.

### Connect your Google account (optional)

If you use claude.ai with the same account, you can connect Google Drive, Gmail, and Calendar so Claude can pull your documents (class readings, syllabi, exports) into `sources/` for mining into the brain:

1. In your browser, go to claude.ai → **Settings** → **Connectors**.
2. Click **Connect** next to Google Drive (and Gmail or Google Calendar if you want them).
3. Complete the normal Google sign-in and consent screen.

These authorizations live on your Claude account, not in this folder. Nothing about them is stored in the vault, and you can disconnect them any time from the same settings page. Skipping this changes nothing else; you can always drag files into `sources/` by hand.

## Getting updates

This copy is independent of the original template. If the template improves later, run the recipe in `directives/update_skills.md`. It fetches the latest skills from the template repo (github.com/Jjesuele/second-brain-starter-kit), shows you what changed, and refreshes only shared skill files. Your personal files are never touched by updates.

## Ground rules

- Everything is plain markdown. No apps that can die, no lock-in, no API keys, no costs beyond your Claude plan.
- Git tracks every change (if you set up the backup). Anything can be undone.
- Claude never invents facts. Placeholders and questions beat confident fiction.
