# Approvals — nothing reaches a third party without the CEO

**Rule:** every communication or commitment directed at anyone other than the CEO is
**approval-gated**. Agents only ever produce drafts. The Chief of Staff is the only component that
performs an approved send.

## What requires approval

- Any email, Telegram/WhatsApp/LinkedIn message, or DM to a third party (customer, design partner,
  investor, candidate, vendor, journalist — anyone).
- Any commitment on the CEO's behalf (scheduling with an external party, promises, pricing).
- Any spend, any public post, any legal/contractual action.

## What does NOT require approval

- Internal work: research, drafting, CRM updates, organizing Drive, composing the CEO's brief.
- Messages to the CEO's own Telegram.

## The outbox state machine

Each outbound item is a single markdown file that moves between folders:

```
outbox/pending/    drafted + Red-Team-passed, waiting for the CEO
outbox/approved/   CEO approved; not yet sent
outbox/sent/       actually sent (records timestamp + provider message id)
outbox/rejected/   CEO rejected (records reason → feeds learning)
```

### Outbox item format (`outbox/pending/<id>.md`)

```markdown
---
id: 2026-09-10-cust-0001
type: customer_outreach        # customer_outreach | investor_outreach | ea_reply | other
channel: email                 # email | telegram | linkedin(draft-only)
to_name: Jane Doe
to_handle: jane@robotco.ai
contact_ref: memory/crm/customers/robotco.md
step: initial                  # initial | follow_up_1 | follow_up_2 ...
red_team: pass                 # pass | flagged (with notes below)
created_by: customer-outreach
created_at: 2026-09-10T12:00:00Z
---

**Subject:** Proving your policy before it hits hardware

Hi Jane,
<the drafted message body>

---
Red Team notes: <tone/accuracy/brand/privacy notes, or "none">
Why now / rationale: <one line the CEO can sanity-check>
```

## Approval protocol (per run)

1. Chief of Staff sends the CEO a numbered approval request per pending item, each tagged `[id]`,
   showing: recipient, channel, purpose, the full draft, and the Red Team note.
2. The CEO replies via Telegram using a decision keyword:
   - `approve <id>` — send as-is.
   - `approve <id>: <edits>` — apply the edits, then send.
   - `reject <id>: <reason>` — do not send; log the reason.
   - `hold <id>` — leave pending.
   - `approve all` — approve every currently pending item (use sparingly).
3. On the next run, the Chief of Staff:
   - moves approved items to `outbox/approved/`, performs the send (Gmail MCP for email, Telegram
     API for Telegram), records the provider result, moves to `outbox/sent/`, and updates the
     contact's CRM state to `sent` / `awaiting_reply` with a `next_action_date`.
   - moves rejected items to `outbox/rejected/` with the reason and updates CRM accordingly.

## Safety defaults

- If a decision is ambiguous, treat it as `hold`.
- Never auto-send on the same run an item was drafted; the CEO must see it first.
- Never send outside a contact's stated preferences or after `do_not_contact`.
