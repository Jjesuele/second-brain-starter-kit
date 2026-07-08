---
name: scope-before-spending
description: Use before starting any action with material token or resource cost, deep research, multi-agent workflows, reading many or large files, web-fetch sweeps, or before recommending anything that runs in the background, runs on a schedule, or injects context into every session.
---

# Scope Before Spending

## Overview

The user runs on a fixed Claude plan with a zero-spend-beyond-it constraint. **Heavy work gets a cost line and a choice first. Trivial work gets no cost theater.**

## Procedure

1. **Classify the task.** If the cheapest sufficient path is fewer than ~5 file reads, no subagents, no web sweep: just do it. Do not narrate cost for trivial work; asking permission to read one file is its own failure.
2. **If heavier:** before starting, state in one or two sentences roughly what it costs (many file reads, N subagents, ~N web fetches, a long-running process) and the cheaper alternative if one exists, then ask which they want. Example: "Deep research here means ~15 web fetches and a few subagents. A single targeted search probably answers it. Want the cheap pass first?"
3. **Recurring costs always labeled recurring.** For anything that repeats (hooks, background servers, scheduled agents, per-session context injection, per-commit AI calls), the cost statement is mandatory and must say "every session" / "every commit" / "runs continuously", never just "some overhead."
4. **Never without asking:** auto-install runtimes, start persistent background services, create scheduled/recurring agents, or add per-session context injection.

## Judgment Rubric

- [ ] Heavy work was preceded by a cost line plus a choice
- [ ] Trivial work was NOT preceded by cost narration
- [ ] Every recurring cost labeled as recurring with its cadence
- [ ] Estimates in plain concrete terms ("adds roughly 2k tokens to every session"), not vague ("may use some resources")

**Good:** "This audit skill reruns a full pass plus a rewrite of your text every use, so real token burn each time."
**Bad:** silently spawning 10 subagents; or, at the other end, asking permission before a single grep.

## Pushback Rules

- The request implies a recurring cost that contradicts the user's own lightweight, zero-added-spend constraint → flag the contradiction once, plainly, then follow their call without relitigating.
- A tool they want requires installing a runtime or server → name that dependency before installing, not after.

## Self-Check

Before launching any subagent, background task, or scheduled job: confirm the cost line was shown and answered this session. After finishing heavy work: if the actual cost blew past the estimate, say so.
