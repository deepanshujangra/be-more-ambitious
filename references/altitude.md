# Altitude: from the task to the outcome

Every task is someone's guess at how to get a result. Altitude asks what the result is and whether a better route exists. The question to keep asking: **what should be true after this is done, and who acts on it next?**

## Moves, from mild to bold

1. **Give context, not just a template.** Hand over every relevant dataset, doc and constraint. Ask the question the audience will actually ask. A quarterly review audience wants: what changed, why, and what should we do?
2. **Ask for decisions, not only findings.** "Work out the three most urgent decisions this raises and, for each, build the case for and against, with an owner and a date." Give every decision its own case; a single argument for the whole deck leaves most of them unexamined.
3. **Redesign the process the task serves.** State what the process is for, ask for a better mechanism, then test it against your own history (would it have caught last year's problems sooner?) and run it beside the old way for one cycle.
4. **Own the outcome.** Move from fixing instances to keeping a property true: from "fix this crash" to "keep the app crash-free", from "answer this ticket" to "keep first-response time under an hour". This only works after the loop exists, so build it first:
   - a way to read the signal (crash reports, logs, metrics)
   - a way to verify a fix independently (reproduce, run tests, check on every platform that matters)
   - a clear boundary on what you may do alone and what needs a human
   - a feedback step: each cycle starts by checking last cycle's recommendations against the results, so the loop learns whether its advice worked before it gives more. Design this in from the first version instead of listing it as a later phase.

## Signs it fits

- People would normally schedule a meeting about this.
- The task recurs, and you would like to stop being the person who feeds it.
- The deliverable is a means (a deck, a report, a fix) rather than the end.

## Signs it doesn't

- Creative or expressive work where the process is the point.
- Goals with no checkable result ("make the company succeed"). Go up one or two rungs, not ten. Test: can you name how you would know the outcome was reached? If not, come down a rung.

## Before you start

- Reversible vs irreversible: read, analyze, draft and simulate freely; confirm before sending, publishing, deleting, deploying or spending.
- Ask for the access the loop needs (data, credentials, machines) instead of working around its absence.

## Mini example

"Fix the failing test in checkout" becomes "stop checkout tests from flaking". Pull the last 60 days of CI runs, rank tests by flake rate, reproduce the worst one by running it 200 times, fix the cause rather than adding a retry, then report the flake rate before and after. Target: zero flaky failures across 1,000 consecutive runs. Judge: the repeated runs, not your reading of the code.
