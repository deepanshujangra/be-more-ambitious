# be-more-ambitious

A skill for Claude that turns the request you typed into the one you meant to type.

Most prompts ask for the task: fix this test, fill in this template, summarize this sheet. This skill stretches the request along three axes, **Altitude**, **Depth** and **Range**, then insists the stretch is checked by something other than Claude's own opinion.

It is a practical version of Felix Rieseberg's essay [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/). Go read the essay; it is short and good. This repo is an unofficial skill built from its ideas, with original wording, and is not affiliated with the author or Anthropic.

## Before and after

**Before**

> The checkout test fails sometimes. Can you fix it?

**After** (what the skill steers toward)

> Checkout tests flake and I keep re-running CI by hand. Stop that from happening. Pull the last 60 days of CI results, rank tests by flake rate, reproduce the worst offender by running it 200 times, fix the root cause (no blind retries), and add a check that fails the build if any test's flake rate climbs above 0.5%. Target: no flaky failures across 1,000 consecutive runs. Ask before pushing anything.

More pairs (a launch post, learning Kubernetes, a job search, and one where the right answer is to stay small) are in [references/examples.md](references/examples.md).

## The three axes

| Axis | The move | Guide |
|---|---|---|
| **Altitude** | Go from the task to the outcome behind it, and own that outcome | [altitude.md](references/altitude.md) |
| **Depth** | Work like a field-leading expert: their instruments, raw data, outside validation | [depth.md](references/depth.md) |
| **Range** | Borrow methods from fields the task doesn't obviously need | [range.md](references/range.md) |

(The essay's fourth type, speed, needs no technique and is left out.)

## Install

**Claude Code**

```bash
git clone https://github.com/deepanshujangra/be-more-ambitious.git ~/.claude/skills/be-more-ambitious
```

**Claude.ai or the desktop app**: zip the `be-more-ambitious` folder (the one containing `SKILL.md`) and upload it in the skills settings.

## Use it

Ask in your own words, or call it directly with `/be-more-ambitious`:

- "Make this prompt more ambitious: *your prompt*"
- "Think bigger about this quarterly review. The data is in `q3.csv`."
- "What would a top expert do differently with this?"
- "Go deeper on this analysis."

You get one of three things, depending on what you asked: a rewritten prompt you can paste, the task done at the stretched level with a short header explaining what changed, or, if you did not ask for ambition, the original task plus a one-line offer.

## Guardrails built in

- **The original ask is the floor.** It is delivered in full; the stretch is added.
- **Honest results beat met targets.** Hard targets are for pushing, not pretending. A missed target is reported as missed.
- **Ambition is not permission.** It never sends, publishes, deletes, deploys or spends without a yes.
- **Methods, not costumes.** Bring in a "short seller" to do what a short seller does, not to talk like one.
- **Small stays small.** A birthday poem gets better craft, not a project plan.

## Does it work?

A small test, and it should be read as one. Three realistic requests were run with and without the skill, one run each:

1. A quarterly business review from a customer file, where leadership believes churn is a pricing problem (the data says otherwise).
2. Rewriting a weekly "summarize this feedback" prompt.
3. A birthday poem (a check that the skill does *not* inflate small tasks).

Outputs were graded against 18 pass/fail checks written in [evals/](evals/).

| | Checks passed |
|---|---|
| Claude without the skill | 13 of 18 |
| Claude with the skill | 17 of 18 (latest run of each test, after fixing three gaps the first round exposed) |

What I learned:

- **Claude without the skill is already good** when you say "as ambitious as possible". It tested the pricing belief against the raw data, found the real drivers, and wrote a solid prompt. The skill's gains are in the less obvious moves: checking findings on data the analysis hadn't seen, having an independent check recompute the numbers, bringing in outside methods and an adversarial role, redesigning the process behind the deliverable, giving every decision its own case for and against, and closing the loop on last cycle's advice.
- **Results vary run to run.** The "replace the quarterly deck with a better mechanism" check passed in one run and failed in the next. Treat the table as a signal, not a guarantee.
- **It costs more.** The with-skill runs used about 20% more tokens and took longer.
- **Not tested yet:** how reliably the description triggers the skill unprompted. PRs with trigger test cases are welcome.

The cases use the folder layout that `claude plugin eval` reads (Claude Code 2.1.269 or later), for example `claude plugin eval . --allow-tools Write,Edit,Bash --scaffold` from this folder. I ran them with subagents rather than that command, so treat the CLI route as untested.

## Contributing

Better examples, new domains and failing cases are the most useful contributions. Each test case is a folder in [evals/](evals/) with a prompt, an expected outcome and one-line graders.

## Credits

- **[Felix Rieseberg](https://felixrieseberg.com/)** for the essay this skill is built on: [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/) (13 Oct 2026). Altitude, Depth and Range, hard targets and the outside judge all come from it.
- **[RoboNuggets](https://github.com/robonuggets)** for [be-ambitious](https://github.com/robonuggets/be-ambitious), another skill built from the same essay that turns all three axes into step-by-step instructions. Worth comparing.
- **[DannyMac180](https://github.com/DannyMac180)** for [be-ambitious in DannyMac180/skills](https://github.com/DannyMac180/skills/tree/main/be-ambitious), an earlier, smaller skill that wraps Felix's "deeper, not bigger" prompt.

The wording, examples, tests and structure in this repo are original.

## License

MIT. See [LICENSE](LICENSE).
