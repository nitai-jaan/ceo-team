# Outbox — approval-gated outbound messages

Every third-party communication lives here as a file and moves between states. See
`core/approvals.md` for the item format and the full protocol.

```
pending/    drafted + Red-Team-passed, waiting for HUMAN approval
approved/   HUMAN approved; not yet sent
sent/       actually sent (records timestamp + provider message id)
rejected/   HUMAN rejected (records reason)
```

Nothing in `pending/` is ever sent automatically. Only the Chief of Staff performs an approved send.
