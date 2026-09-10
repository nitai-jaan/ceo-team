# ceo-team

The agentic team for the CEO of **[jaan](https://jaan.world)** — the evaluation layer for Physical AI.

This repository **is** the team. Each "team member" is a role prompt (`agents/<role>/agent.md`),
scheduled as a [Cursor Cloud Agent](https://cursor.com/docs/cloud-agent) via
[Automations](https://cursor.com/docs/cloud-agent/automations). Their memory, reports, CRM,
and outbound message queue all live here as version-controlled files, so the whole operation is
documented in one place and is portable if we ever move off Cursor.

## How it works (in one picture)

```
Cursor Automation (daily) ──▶ Chief of Staff (cloud agent, single writer)
                                 │
                                 ├─ spawns subagents (Task tool), each a team member:
                                 │     Executive Assistant · Research Analyst
                                 │     Customer Outreach · Investor Outreach
                                 │
                                 ├─ Red Team subagent reviews every report + outbound draft
                                 │
                                 ├─ commits state → reports/ , memory/crm/ , outbox/
                                 │
                                 └─ pushes ONE daily brief + approvals → your Telegram
```

Key design rules:

- **Single writer.** Only the Chief of Staff commits shared state. Team members are stateless
  workers that *return* results. This avoids branch/merge chaos across isolated subagent worktrees.
- **External sends are approval-only.** No email/DM to any third party is ever sent without your
  explicit approval. Agents only ever produce *drafts* in `outbox/pending/`. See `core/approvals.md`.
- **One front door.** You talk to the Chief of Staff via Telegram, not to six bots. See `core/telegram.md`.
- **Budget-aware.** Target ≈ $10/month: one consolidated daily run, idle agents skipped, cheap
  models for routine work. See `core/budget.md`.
- **The repo is the control plane.** Adding/removing an agent = editing `team/roster.yaml` + a folder.
  Changing an agent's behaviour = a reviewable pull request.

## Repository layout

| Path | Purpose |
|---|---|
| `AGENTS.md` | Global operating rules every agent must follow. |
| `team/roster.yaml` | Registry of agents: active flag, cadence, model tier, budget. Add/remove here. |
| `agents/<role>/agent.md` | Each agent's "job description" (portable prompt). |
| `core/` | Shared conventions: Telegram, approvals, report schema, budget. |
| `memory/company.md` | Distilled jaan context (product, ICP, voice) — grounds every agent. |
| `memory/crm/` | Per-contact state machines for customers + investors. |
| `memory/decisions/` | Decision log. |
| `reports/daily/YYYY-MM-DD/` | Each agent's report + the consolidated CEO brief. |
| `outbox/{pending,approved,sent,rejected}/` | Approval-gated outbound messages. |
| `.cursor/environment.json` | Cloud Agent environment definition. |

## Active roster

See `team/roster.yaml`. Current phase-1 squad:

- **Chief of Staff** — orchestrator, single writer, Telegram front door, budget cop.
- **Executive Assistant** (lean) — Gmail triage + draft replies.
- **Research Analyst** — ICP / market / competitor research feeding outreach.
- **Customer Outreach** — design-partner sourcing + sequenced, approval-gated outreach.
- **Investor Outreach** — pre-seed investor research + sequenced, approval-gated outreach.
- **Red Team** — reviews every report and outbound draft before it reaches you.

## Setup (one-time, done by the CEO)

1. **Telegram secrets** — add `TELEGRAM_BOT_TOKEN` and `TELEGRAM_CHAT_ID` in the Cloud Agent
   **Secrets** panel (see `core/telegram.md`).
2. **Authorize MCPs** — Gmail, Google Drive, Google Calendar, GitHub for your account.
3. **Create Automations** — one daily schedule running the Chief of Staff (prompt in
   `agents/chief-of-staff/agent.md`). Turn on more agents by flipping `active: true` in the roster.

## Status

Phase 1 (this scaffold): structure, prompts, and conventions. **No external actions are performed.**
Phase 2 wires Telegram + a live Chief-of-Staff daily brief. Phase 3 turns on the remaining agents.
