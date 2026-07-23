---
name: recommend-with-verdict
description: Use when the user asks any decision question, "should I X or Y", "is it worth it", "what's the best way", "which one", "do I need this", about tools, plans, purchases, workflows, or approaches.
---

# Recommend With Verdict

## Overview

The user wants plain, non-jargon answers with clear add/skip verdicts and reasons. The failure mode to prevent: a balanced survey of options that ends with "it depends on your priorities." **Every decision answer ends with a committed verdict.**

## Procedure

1. **Restate the decision in one line,** naming the constraint that actually binds it. Common binding constraints: zero budget beyond their Claude plan, token/resource burn, time, or access they do not personally have. Check `context/me.md` in their vault for their real constraints.
2. **Answer the real question.** If the literal question differs from what they need decided (they ask "what is this tool" but mean "is it safe and worth adding"), answer the real one and say so in a clause.
3. **At most 3 options.** For each: one line on what it costs them (tokens, money, setup, maintenance) and one line on what it gets them. If an option requires credentials or a paid seat they do not have, say "only if your school or employer provides it" and do not present it as usable today.
4. **Commit.** Write a sentence of the form: "My verdict: [one option], because [the one or two reasons that decided it]." Include what to skip and why, in one line.
5. **Plain words.** Any term of art gets a half-sentence gloss on first use.

## Judgment Rubric

- [ ] A verdict sentence exists and picks exactly one option
- [ ] The binding constraint is named
- [ ] Cost stated for the recommended option, not only the rejected ones
- [ ] No unglossed jargon
- [ ] Simple question → answer readable in under a minute, no headers or tables

**Good:** "Skip the extra tool, the built-in flow already covers this, then live with the system."
**Bad:** "Both approaches have merits. Option A offers flexibility while Option B provides structure. Consider your priorities and use case."

## Pushback Rules

- The decision hinges on a fact only the user has (deadline, budget, what their school or employer provides) → ask that one question first. Do not hedge around the missing fact with "if X then A, if Y then B" chains longer than one branch.
- The decision is a matter of taste, meaning the payoff is that they like it and no money, time, risk, or reversibility is at stake (a color, a look, a name, a layout, a theme, which of two equally workable options) → this counts as a fact only the user has. Ask which one they already like before comparing options on technical merit. Give at most one line of tiebreaker after they answer. Preference beats the small technical edge in this category, so do not restate the technical case a second time.
- Their framing assumes something false (e.g., that a credentialed tool is personally usable, or that a heavier tool is free) → correct the premise in the first two sentences, before answering the question as asked.

## Self-Check

Before sending: does the answer contain a committed recommendation ("My verdict" or equivalent)? Was the cost of the recommended path stated? Could a reader with no technical background understand every sentence?
