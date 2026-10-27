# Depth: work like the best in the field

Asked to "act like an expert", a model often changes its vocabulary and keeps its method. Depth means changing the method: use the instruments, raw material and standards that top practitioners use, and keep going until even they might learn something.

## Moves

1. **Use the experts' instruments.** If you reach for a markdown table, ask whether a database query, a statistical model, a profiler, a solver or a proof assistant is what a professional would use. You do not need to know which: ask the model, it usually does.
2. **Set an unreasonable target and treat it as reasonable.** Not 5s load time instead of 10s but 200ms. When something seems impossible, say it is solvable and needs more persistence, then try other routes before concluding otherwise.
3. **Challenge what you know.** Hand over the raw data and ask for an adversarial check of a belief. "We think churn is a pricing problem. Try to reproduce that from the raw records, and try just as hard to break it."
4. **Produce new knowledge.** Once the known pattern is reproduced, look for the blind spot: "Find the earliest signal of this outcome we don't track yet, then show it predicts on data you did not use to find it."
5. **Use an outside judge.** Prefer something the model can run and get immediate feedback from: tests, a benchmark, a held-out set, a simulator, a compiler, a reference dataset, an independent reviewer who does not see your reasoning. A person's spot check counts too. Self-grading alone doesn't.

## Prompt: deeper, not bigger

> I want a deeper version of this task, not a bigger one. Before rewriting it, answer four things: what would a top professional here do that I haven't asked for; what is the rawest material they would start from, rather than what has already been digested for me; which specific methods and tools they would use; and what, other than you or me, could show the result is right. Then rewrite my request to ask for exactly that.

## Failure modes

- **Costume depth:** expert-sounding language over the same shallow method. Check that the *tools and data* changed.
- **Signal hunting without holdout:** search enough patterns and one will look real. Split the data first and test findings on the part you did not search.
- **Overclaiming:** when the data cannot answer the question (for example only one price point, so price sensitivity is unmeasurable), say so and name what data would settle it.

## Mini example

"Review this contract" becomes: extract every clause into a structured table, compare each against the standard terms the counterparty's other public filings use, flag deviations by risk, and list the questions only a lawyer can settle. Judge: a lawyer's review of the flagged clauses plus a spot check of 10 random extractions against the source text.
