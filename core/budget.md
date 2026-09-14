# Budget & cost control

**Target: ≈ $10 / month.** This is tight for Cloud Agents, so the team is deliberately frugal. The
Chief of Staff enforces these rules and reports spend in the daily brief.

## Cadence

- **One consolidated daily run** (Chief of Staff orchestrates everything). Avoid multiple separate
  scheduled runs per agent — each run has fixed overhead.
- **On-demand runs** only when the HUMAN asks (e.g. "prep me for the 3pm").
- **Batch, don't stream.** Outreach drafting is rate-limited (see below), not a firehose.

## Skip idle work

- The Chief of Staff spawns a team member **only if it has pending work** this run. No speculative
  research, no "just checking" runs.
- If an agent has nothing to do, it returns `status: idle` cheaply and is skipped next time until a
  trigger appears.

## Model tiering

| Tier | Use for | Notes |
|---|---|---|
| **Fast/cheap** | inbox triage, summarizing, CRM updates, first-draft outreach | default for almost everything |
| **Strong** | daily synthesis/brief, strategy calls, Red Team review | use sparingly |

Pick the cheapest model that does the job. Reserve the strong tier for judgment-heavy steps.

## Rate limits (starting points — tune with real data)

- Customer outreach: draft up to **5 new/follow-up messages per run**.
- Investor outreach: draft up to **3 new/follow-up messages per run**.
- Research: **one focused task per run** (a target batch or one dossier), not open-ended crawling.

## Guardrails

- No subagent recursion beyond one level (Chief of Staff → team member → Red Team).
- Cap tool calls per subagent; stop and report `blocked` rather than looping.
- If a run trends expensive, the Chief of Staff finishes the essential work (brief + approvals) and
  defers non-urgent agents to the next run, noting this in the brief.

## Scaling up

Start with 3 agents live (Chief of Staff + Research Analyst + Customer Outreach). Watch real cost
for a week, then enable the rest via `team/roster.yaml`. Expect that running all agents daily may
push spend above $10; frequency is the main lever (fewer Automations = lower cost).
