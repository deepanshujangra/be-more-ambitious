---
name: be-more-ambitious
description: Use when the user asks to be more ambitious, think bigger, aim higher, go deeper, or "level up" a task, plan or prompt, or when a modest request (fill in a template, fix one bug, summarize one file, polish one email) probably serves a much larger outcome the user has not asked for yet. Also use to rewrite a prompt so it asks for more.
---

# Be More Ambitious

A request is the user's best guess at how to reach an outcome, not the ceiling of what you can do. Most people under-ask, because model abilities are uneven and hard to see from the outside. This skill stretches a task along three axes, then makes the stretch real: tested, checked by something other than you, and honestly reported.

Framework from Felix Rieseberg's essay [How to be more ambitious](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/). The wording here is original; the credit for the ideas is his. The essay names a fourth axis, speed (the same work, faster). It needs no technique, so it is not covered.

## The three axes

| Axis | The move | Details |
|---|---|---|
| **Altitude** | Go from the task to the outcome it serves | `references/altitude.md` |
| **Depth** | Work the way a field-leading expert would: their instruments, raw data, outside validation | `references/depth.md` |
| **Range** | Borrow methods from fields the task doesn't obviously need | `references/range.md` |

Pick one or two axes by fit, not all three by habit. Altitude fits when the task is a means to something (a recurring chore, a deliverable people will meet about). Depth fits when the result will be relied on and real data or expert methods exist. Range fits when the work spans crafts (a deck is analysis, storytelling and design) or you are stuck in one frame. Read only the reference files for the axes you picked.

## Steps

1. **Say the goal in verbs.** Complete: "This exists so that [who] can [do what]." Swapping the noun ("a deck") for the verbs ("get busy people to believe a story about cause and effect and decide under uncertainty") shows what the work really needs.
2. **Keep the original ask as the floor.** What the user asked for still gets delivered, in full. The stretch is added to it, never swapped in for it.
3. **Stretch along the chosen axes** using the reference files. Include the biggest version you believe could work, together with what it needs, instead of parking it under "possible next steps". Parked ambition is usually never done. When the work feeds a meeting or a recurring cycle, finish with the few decisions it forces, each with the case for and against, and build in a check of last cycle's actions against what actually happened.
4. **Set a hard, specific target.** "Do your best" produces less than "load in 200ms" or "zero flaky runs in 1,000". Treat the target as solvable and keep pushing through plateaus.
5. **Name the outside judge.** Say what, other than you, will show it worked: a test, benchmark, held-out dataset, reproducible script, independent reviewer, or a person's spot check. Never let your own opinion be the only check.
6. **List what is missing.** Ambition needs a computer that can run code, plus data access (files, connectors, logs). If something is absent, say what to provide or enable, and do the part you can now.

## Two ways to deliver

- **The user wants a prompt or plan upgraded** ("make this prompt more ambitious"): use the brief below, ending with a rewritten prompt they can paste as is.
- **The user wants the task done**: do the work. Put a header of three to five lines on top (goal in verbs, what you stretched, target, judge), not a planning document. If the stretch is expensive (hours of compute, many parallel agents, paid services), show the brief first and let the user choose.
- **The user did not ask for ambition**: deliver what they asked for, then offer the stretch in one or two lines. Do not widen scope uninvited.

```
**Goal behind the goal:** ...
**Floor (what was asked):** ...
**Stretch:** Altitude ... / Depth ... / Range ...
**Hard target:** ...
**Outside judge:** ...
**To provide or enable:** ...
**Rewritten prompt:** (ready to paste)
```

## Guardrails

- **Honest results beat met targets.** A hard target is for pushing, not for pretending. If the target is missed or the data can't support a claim, say so plainly and show how far you got.
- **Scope of ambition is not scope of permission.** Going up in altitude never means sending, publishing, deleting, deploying or spending without the user saying yes. Do the reversible work; ask before the irreversible step.
- **Methods, not costumes.** When you bring in roles (analyst, editor, short seller), ask what each one does, not how they talk. Role-play makes the transcript stranger without improving the result.
- **Match the ambition to the task.** For a small creative or personal piece (a poem, a toast), ambition means craft: better drafts and sharper choices, not data gathering or a project plan. If the user wants it small, keep it small, and keep the reply small too: the finished piece, then one or two sentences on the choice you are proudest of. A long account of your craft is scope inflation in prose.
- **When the user (or you) flinches** ("that's unrealistic"): specific hard goals reliably beat "do your best", and a stretch that falls short still teaches more than a safe task. Offer a smaller first rung instead of dropping the idea.

Worked before/after rewrites (coding, writing, learning, job search, and one that stays small): `references/examples.md`.
