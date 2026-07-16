---
name: edit-into-voice
description: Use when any text will carry the user's name, essay drafts, emails, cover letters, LinkedIn messages, memos, application paragraphs, after drafting and before showing them. Also use when asked to "polish", "make professional", "humanize", or "clean up" their writing.
---

# Edit Into the User's Voice

## Overview

The user's voice is defined in their vault at `context/voice.md`, calibrated from their real writing. The default output of a language model fails almost anyone's voice test. This skill is the mandatory editing pass that fixes that. The core principle: **the voice file is law; plain words, concrete details kept, zero chatbot register.**

**"More professional" never means more inflated.** A person's plain register IS their professional version. If asked to polish, polish within their rules.

## The Procedure (run every step, in order)

1. **Read the vault's `context/voice.md` in full first.** Do not edit from memory of it. If the file is missing or still contains unfilled placeholders, stop and say so; do not improvise a voice.
2. **Hard-rules scan (mechanical).** Apply every hard rule in their voice.md as a literal search-and-fix pass. If their rules ban dashes as punctuation, search the draft for `—`, `–`, and ` - ` and rewrite every hit. Whatever their rules are, enforce them by search, not by feel.
3. **Banned-word scan.** The canonical banned list lives in their voice.md; scan against that full list. Universal AI tells are banned even if their file omits them: delve, landscape, tapestry, multifaceted, leverage (as a verb), Moreover, Furthermore, "In today's". No exceptions, even in quotes you wrote.
4. **Pattern scan, one pass each:**
   - Rule-of-three padding ("clear, concise, and compelling") → cut to the one word that matters
   - Hedging stacks ("arguably one of the most significant") → one plain claim
   - Short dramatic fragments ("And that matters. A lot.") → fold into a full sentence, unless their voice.md says fragments are their register
   - Staccato widening ("It's not just X. It's Y.") → fold into one flowing sentence, and keep any widening move to at most once per page; a closer used in every paragraph stops being a closer
   - Inflated register ("developed financial models", "gained valuable insight", "eager to deepen my understanding") → what they'd actually say ("built Excel models", "what stayed with me was")
5. **Positive-voice pass.** Match the draft to what their voice.md says they DO: their sentence rhythm, their habitual transitions, their signature moves, their hedging style. Do not import moves their file does not describe.
6. **Concreteness check.** Find the most specific, personal detail in the original draft. It must survive into the final version. If a sentence could appear in any candidate's email or any student's essay, rewrite it around a real detail from the draft's subject. If no real detail exists, ask the user for one. Never invent one.

## Judgment Rubric (all must pass before showing them)

- [ ] Every hard rule in their voice.md verified by search, with the count stated (e.g. "dash count: 0")
- [ ] Banned words: 0 (their list plus the universal tells)
- [ ] No sentence fragments added for drama (unless their voice.md endorses them)
- [ ] The original draft's most concrete detail is still present
- [ ] No facts, numbers, or claims added that were not in the original draft

## Worked Example 1 — a recruiting email (a real cheap-model failure, then the fix)

**The user's draft:**
> I'm a junior studying econ. This summer I interned at a real estate firm where I worked on excel models and read offering memos for office deals. I liked seeing how the numbers actually decide whether a deal happens. I want to learn more about how your firm thinks about acquisitions.

**FAIL (what "make it professional" produces by default):**
> I'm a junior studying economics with a strong interest in real estate investment. This summer, I interned at a commercial real estate firm, where I developed financial models and analyzed offering memoranda for office properties. Through this experience, I gained valuable insight into how rigorous quantitative analysis directly informs acquisition decisions. I'm eager to deepen my understanding of your firm's investment thesis and approach to deal evaluation.

Why it fails: inflated register throughout, generic ambition ("strong interest"), chatbot closer ("eager to deepen my understanding"), and the one genuinely personal line (numbers deciding the deal) got erased.

**PASS (the correct edit):**
> I'm a junior studying economics. This summer I interned at a real estate firm, where I built Excel models and read offering memos for office deals. What stayed with me was how directly the numbers decide whether a deal happens, and I would like to hear how your team makes that judgment on the acquisitions side.

Why it passes: plain register, the writer's concrete observation kept and sharpened, nothing invented.

## Worked Example 2 — essay register (the same tells in academic clothing)

**FAIL:**
> Federal grazing policy represents a multifaceted challenge. Ranchers depend on public lands. Environmentalists want them protected. Moreover, climate change is intensifying these tensions, making it arguably one of the most significant land-use debates in the American West.

**PASS:**
> Federal grazing policy asks the government to serve two groups that want opposite things from the same land. Ranchers depend on public grazing allotments to stay solvent, while environmental groups see those same allotments as degraded habitat that may not recover. In this sense, the debate is not just about cattle, but about who public land is actually for.

Why it passes: the banned words and hedging stack are gone, the staccato fragments are folded into flowing sentences, the claims got specific, and the one widening move sits in the closer where it belongs. Adjust the pass version to whatever the user's own voice.md prescribes; the fail version is wrong for everyone.

## Rationalizations — all of these mean go back and rewrite

| Excuse | Reality |
|--------|---------|
| "This phrasing reads better" | Their voice.md defines better. Follow it. |
| "Professional tone needs elevated diction" | Their plain register is the professional version. Inflation is the failure. |
| "I only added a small supporting fact" | Adding facts is fabrication. Only rearrange what the draft contains. |
| "The draft was too thin, so I generalized" | Generic filler is worse than thin. Ask them for a real detail. |
| "I remember what voice.md says" | Read the file this session. It may have changed. |

## Self-Check (do this, then report it)

Before delivering, state in one line: each hard-rule count from the final scan, banned-word count (must be 0), and confirmation that no new facts were introduced. If any check fails, fix and re-scan before showing the text.
