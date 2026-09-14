# Report schema

One format for every agent so the Chief of Staff can merge them into a single, skimmable HUMAN brief.

## Per-agent report (returned by each team member)

Agents **return** this to the Chief of Staff; the Chief of Staff writes it to
`reports/daily/<date>/<agent-id>.md`.

```markdown
---
agent: research-analyst
date: 2026-09-10
status: ok            # ok | blocked | idle
cost_tier: fast       # fast | strong
---

## Summary
<= 3 sentences on what was done and why it matters.

## Actions taken
- <internal action> (no external sends — those are drafts only)

## Needs HUMAN
- [ ] <decision or approval needed, referencing outbox [id] if applicable>

## Drafts queued
- [id] <one-line description> → outbox/pending/<id>.md

## Findings / state changes
- <fact discovered, CRM update, etc. — grounded, with source>

## Next
- <what this agent will do next run>

## Flags
- <risks, missing info, anything the Red Team or HUMAN should know>
```

## Consolidated HUMAN brief (`reports/daily/<date>/brief.md`, also sent to Telegram)

```markdown
# jaan daily brief — 2026-09-10

**TL;DR:** <2–3 lines: the single most important things + what needs you.>

## Needs your decision (N)
1. [id] <recipient> — <purpose>  → reply `approve <id>` / `reject <id>: reason`
...

## Highlights
- <cross-agent highlights, deduplicated>

## Pipeline
- Customers: <counts by stage> · Investors: <counts by stage>

## Inbox & calendar
- <EA + Scheduler summary: what needs you today>

## Housekeeping
- Agents run: <list> · skipped (idle): <list>
- Est. spend today: <if known> / budget notes
```

Keep the brief tight. If nothing needs the HUMAN, say so in one line rather than padding.
