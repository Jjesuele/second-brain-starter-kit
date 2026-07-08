# Skills: Your Extracted Expertise

This folder holds frameworks and knowledge YOU extract from courses, work, books, and experience. It starts empty on purpose; it fills as you learn.

This is different from the Claude skills in `dot-claude/skills/` (those change how the AI behaves; these store what you know).

## How a skill file gets made

When you learn something durable, tell Claude: "turn this into a skill file" and give it the source material. It writes a markdown file here with the source and date at the top.

## Conventions

- Organize by area with subfolders as they earn their existence (for example `school/`, `investing/`, `cooking/`). One or two files do not need a subfolder yet.
- Each file carries its source and date at the top, per `context/standards.md`.
- Each area with multiple files gets a short `README.md` listing what is inside.
- These files are load-on-demand: the AI reads the relevant ones when a task touches that area, per the vault `CLAUDE.md`.
