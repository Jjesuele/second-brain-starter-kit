# Second Brain Starter Kit

One folder that holds who you are, how you work, what you know, and what you have decided. Claude Code reads it to do work your way. You read it in Obsidian (optional) to think.

This kit ships as blank scaffolding plus a guided setup. You answer an interview once, and Claude writes all your personal files for you. You never hand-edit anything to get started.

## What you need first

1. **Claude Code** installed and working. That is the app this kit runs on. If you do not have it, install it from Anthropic first.
2. **A free GitHub account** (recommended, not required). With one, your whole brain gets a private online backup and version history. Without one, everything still works, it just lives only on your computer.

## Get your copy

**With GitHub (recommended):**

1. On this repo's page, click **Use this template → Create a new repository**.
2. Name it whatever you like and set it to **Private**. Private matters: this folder will hold your personal notes.
3. Get it onto your computer: `git clone <your new repo URL>`, or use the GitHub Desktop app if you prefer clicking to typing.

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

## Getting updates

This copy is independent of the original template. If the template improves later, run the recipe in `directives/update_skills.md`. It fetches the latest skills from the template repo (github.com/Jjesuele/second-brain-starter-kit), shows you what changed, and refreshes only shared skill files. Your personal files are never touched by updates.

## Ground rules

- Everything is plain markdown. No apps that can die, no lock-in, no API keys, no costs beyond your Claude plan.
- Git tracks every change (if you set up the backup). Anything can be undone.
- Claude never invents facts. Placeholders and questions beat confident fiction.
