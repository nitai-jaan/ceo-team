# CRM — contact state machines

Each contact (customer/design-partner or investor) is one markdown file with YAML front-matter that
encodes its state. The Chief of Staff is the only writer. The outreach agents propose changes by
returning updates; the Chief of Staff commits them.

```
memory/crm/
  customers/<slug>.md      # design partners / customers
  investors/<slug>.md      # pre-seed investors
  _templates/contact.md    # copy this to create a new contact
```

## State machine

```
queued → drafted → awaiting_approval → sent → awaiting_reply
  ├─ (reply received) → replied → [CEO takes over / next step defined]
  ├─ (no reply after next_action_date) → follow_up_drafted → awaiting_approval → ...
  ├─ closed_won
  ├─ closed_lost
  └─ do_not_contact
```

- `next_action_date` drives the sequencer: each run, the Chief of Staff finds contacts whose
  `next_action_date <= today` and has the relevant outreach agent draft the next step (still
  approval-gated).
- Follow-up cadence default: **+4 days**, then **+7 days**, then **+14 days**, then `closed_lost`
  (tune per segment). Never exceed 3–4 touches without a reply.
- A reply always pauses automation and routes to the CEO.

## Fields

See `_templates/contact.md`. Keep a dated `## Log` of every touch and response so history is
auditable and portable.
