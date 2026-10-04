# Scoring Rubric

Score each answer 1-5 against four dimensions. The score itself is less important than the
notes you take per dimension — those notes are what make the final report specific instead of
generic. Weight the dimensions differently depending on difficulty (see below).

## Dimensions

1. **Correctness** — Is the core technical approach sound? Would it actually work, or does it
   contain a factual error or a step that would fail in practice?
2. **Scenario reasoning / trade-offs** — Did the candidate reason about *this specific
   situation* (constraints, scale, risk) rather than reciting a generic textbook answer? Did
   they weigh alternatives, or jump to one answer without considering why?
3. **Completeness** — Did they cover the edge cases and failure modes a real incident/rollout
   would hit, or only the happy path?
4. **Communication clarity** — Could a teammate or on-call partner actually follow their plan?
   Structured and sequenced, or a scattered list of keywords?

## Difficulty weighting

- **Beginner**: Correctness and clarity matter most. Don't penalize heavily for shallow
  trade-off discussion — that's not expected yet.
- **Intermediate**: All four dimensions roughly equal weight.
- **Advanced**: Scenario reasoning and completeness matter most. A technically correct but
  one-dimensional answer that ignores the ambiguity in the prompt should score no higher than a
  3, even if nothing in it is factually wrong — advanced interviews are testing judgment under
  ambiguity, not textbook recall.

## Score bands

- **5 — Strong hire signal**: Correct, reasons explicitly about trade-offs/edge cases
  appropriate to the difficulty level, and communicates it clearly enough to execute on.
- **4 — Solid**: Correct and clear, but trade-off reasoning or edge-case coverage is thinner
  than a 5.
- **3 — Borderline**: Right general direction, but either a meaningful gap (missed a major edge
  case, chose a reasonable-but-not-great approach without acknowledging the trade-off) or
  communication was hard to follow.
- **2 — Weak**: Significant technical gap or the answer doesn't actually address the scenario
  asked (e.g. answers a different, easier question than the one posed).
- **1 — Missing the mark**: Factually wrong in a way that would cause real harm (e.g. would
  make an outage worse), or no real attempt at reasoning through the scenario.

## Notes to capture per question (for the report)

- One line on what the answer got right.
- One line on the single most important thing it missed — be specific (not "needs more depth,"
  but "didn't mention checking recent deploys before concluding it was a cert expiry").
- Whether this gap is a knowledge gap (doesn't know the concept) or a reasoning/habit gap
  (knows the concept but doesn't reach for it under pressure) — these need different prep.
