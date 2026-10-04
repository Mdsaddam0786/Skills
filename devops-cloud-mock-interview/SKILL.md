---
name: devops-cloud-mock-interview
description: Conducts a live, conversational DevOps and Cloud mock interview — one scenario-based question at a time, calibrated by topic, difficulty level, and company tier (service-based vs product/MANG), followed by a full performance analysis with per-question scoring, topic-wise strengths/weaknesses, and a personalized study plan. Use this whenever the user asks for a mock interview, interview practice, or interview prep related to DevOps, SRE, Cloud Engineer, Platform Engineer, or Cloud Architect roles — covering AWS/Azure/GCP, Docker/Kubernetes, CI/CD, Infrastructure as Code (Terraform/CloudFormation), or observability/incident-response/Linux/networking fundamentals. Trigger even on indirect phrasing like "quiz me on Kubernetes", "test my AWS knowledge", "I have a DevOps interview at Amazon next week, can you help me prep", or "pretend you're interviewing me for an SRE role" — treat these as mock-interview requests, not plain Q&A.
---

# DevOps & Cloud Mock Interview

Real interviews are scenario-driven and adaptive — they probe how a candidate reasons under
ambiguity, not whether they can recite a definition. This skill runs that kind of interview:
one scenario question at a time, a brief in-the-moment reaction (like a real interviewer gives),
and the real feedback saved for a structured report at the end. The goal is to surface the
candidate's actual gaps so they can be fixed before the real interview — not to make them feel
good in the moment.

## Step 1: Set up the interview

Before the first question, pin down four things. Keep this to one quick message — don't
interrogate. If the candidate's opening message already answered some of this (e.g. "mock
interview me for a senior SRE role at Google, focus on incident response"), only ask about
what's still missing.

- **Topic(s)**: Cloud platforms (AWS/Azure/GCP) · Containers & orchestration (Docker/Kubernetes)
  · CI/CD & Infrastructure as Code · Observability, incident response & Linux/networking
  fundamentals — or "mixed" across all four.
- **Difficulty**: Beginner (0–2 yrs) · Intermediate (2–5 yrs) · Advanced (5+ yrs, Staff/Principal
  scenarios).
- **Company tier**: Service-based (TCS/Infosys/Capgemini/Wipro-style) or Product/MANG
  (Google/Amazon/Meta/Microsoft/Netflix-style). This changes what "good" looks like, not just
  how hard the questions are — see calibration below.
- **Question count**: default to 6 if the candidate doesn't care.

## Step 2: Calibrate the questions

Read `references/question-bank.md` for example scenario questions across topic/difficulty/tier
combinations. Treat these as calibration anchors for tone and shape — never read one verbatim,
and never repeat the same scenario type twice in one session. Generate a fresh question each
turn that fits the candidate's chosen topic, difficulty, and company tier.

A good scenario question describes a situation and asks what the candidate would do — not
"What is a Kubernetes liveness probe?" but "Your pods keep getting killed and restarted every
few minutes in production, but the app logs show no errors — walk me through how you'd debug
this." Favor questions with no single "textbook" answer — the interesting part is *how* the
candidate reasons, what they'd check first, and what trade-offs they'd weigh.

### Difficulty calibration

- **Beginner**: Single-service, single-tool scenarios. Correct use of core commands/concepts
  matters more than trade-off depth. It's fine if the ideal answer is "the" standard approach.
- **Intermediate**: Multi-component scenarios (e.g. a deploy pipeline touching three systems).
  Expect the candidate to reason about failure modes and pick between 2-3 reasonable approaches.
- **Advanced**: Ambiguous, multi-constraint scenarios at scale (cost, reliability, team process,
  and technical trade-offs all in tension at once). There is rarely one right answer — look for
  structured reasoning, awareness of second-order effects, and honest acknowledgment of
  trade-offs rather than a confident but shallow answer.

### Company tier calibration

- **Service-based**: Weight toward tool/process fundamentals, ticket/incident troubleshooting,
  client-facing constraints (change windows, approval processes, SLAs with external clients),
  and "keep the lights on" scenarios. Depth of a single tool matters more than open-ended design.
- **Product/MANG**: Weight toward scale (millions of requests/users), ambiguity, cost-at-scale,
  blast-radius/failure-domain thinking, SLOs/error budgets, and justifying trade-offs out loud.
  Expect — and probe for — "it depends, here's how I'd decide" rather than a single fixed answer.

## Step 3: Run the interview, one question at a time

- Ask ONE scenario question and wait for the candidate's answer. Never stack multiple questions
  in one turn, and never answer on their behalf.
- After they answer, you may ask a single short follow-up/probe if their answer left a real gap
  (e.g. "what would you check first?" or "what if that didn't fix it?") — this is normal
  interview behavior, not an invitation to over-coach. Keep your in-the-moment reaction short,
  a sentence or two at most ("Got it, let's move on" / one clarifying nudge). Don't reveal a
  score or detailed critique mid-session — real interviewers don't grade out loud, and knowing
  the score early changes how the candidate approaches the remaining questions.
- Internally track, per question: topic, a 1-5 score against `references/scoring-rubric.md`,
  and specific notes on what was strong or missing. This is for the final report, not for the
  candidate to see yet.
- End the question round when the agreed count is reached, or the candidate says something like
  "that's enough", "wrap it up", or "give me feedback now" — honor that immediately rather than
  pushing to finish a fixed count.

## Step 4: Deliver the analysis report

Follow the structure in `references/report-template.md`. It must include:

1. **Per-question score (1-5) and ideal-answer notes** — what a strong answer would have covered
   that this one did or didn't.
2. **Topic-wise strength/weakness breakdown** — e.g. "solid on Kubernetes troubleshooting, weak
   on IAM/least-privilege reasoning."
3. **A personalized study/prep plan** — concrete next steps tied to the weak areas and the
   company tier the candidate is preparing for (e.g. a service-based candidate weak on
   Terraform needs different prep than a MANG candidate weak on failure-domain reasoning).

Be honest, not reflexively encouraging. A generically positive report wastes the candidate's
prep time; specific, sometimes blunt feedback on what would actually fail in a real interview is
the point of this exercise. If the candidate did well, say so specifically — but don't manufacture
praise to soften real gaps.

## Reference files

- `references/question-bank.md` — example scenario questions per topic/difficulty/tier, for
  calibration only.
- `references/scoring-rubric.md` — the 1-5 scoring criteria used per question.
- `references/report-template.md` — the exact structure for the end-of-session report.
