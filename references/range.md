# Range: borrow from other fields

Doing good work used to mean a small team with a few specialties. Cheap parallel agents and a computer with software make it affordable to consult many more fields, so ask which fields would see this problem differently and what they would actually do.

## Moves

1. **Swap nouns for verbs.** "A quarterly review" is a noun. "Help busy people believe a story about cause and effect, and decide under uncertainty, in thirty minutes" is a set of verbs, and each verb points at fields that are good at it (persuasion, statistics, visual design, decision theory). Write the verb version, then ask which fields own each verb.
2. **Assemble the crew.** Pretend the stakes are absurdly high and ask who you would recruit. For a report: an analyst, a journalist, an editor; for a live presentation, add a motion or audio designer; for an adversarial pass, a short seller and a forensic accountant.
3. **Make each role do work.** The point is to extract methods. Do not ask the model to *write like* a short seller; ask it to do what a short seller does: hunt for the strongest evidence against the thesis. Do not ask for a forensic accountant's *tone*; ask for the totals to be re-added and the sources reconciled.
4. **Use software from other worlds.** Rendering interiors in Blender, audio in ffmpeg, routes in a solver, maps in a GIS library. Let the model install what it needs (it needs a computer that allows this).

## Running the crew

- With subagents or parallel threads: one per role, each with its own method and output, then one pass that reconciles them.
- Without: run the roles as sequential passes over the same material, each starting from the raw input rather than from the previous role's opinion.

## Keep it useful

- Choose roles whose output would change the work. Three sharp roles beat ten vague ones.
- The adversarial role is the most commonly skipped and the most valuable. Always include one when the result will be relied on.
- If the transcript reads like theater, you drifted into role-play. Go back to "what does this person do on Monday morning?"

## Prompt

> Rewrite what this deliverable does as verbs, not nouns. Then name five fields that are good at those verbs, say what a practitioner in each would actually do with our material (methods and tools, not tone), and run the two most useful ones. Include one adversarial role whose job is to break the conclusion.

## Mini example

"Write a launch post for our new feature" becomes "get the people who have the problem to try the thing in under five minutes". Crew: a support analyst who mines ticket history for the exact words customers use, a journalist who finds the lede, an editor who cuts, and a skeptical customer who tries to stop reading after paragraph one.
