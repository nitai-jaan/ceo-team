# Telegram — the HUMAN's front door

The HUMAN interacts with the whole team through a single Telegram bot. Only the **Chief of Staff**
talks to Telegram. All other agents route messages to the HUMAN through the Chief of Staff.

## Secrets (environment variables)

| Variable | What it is |
|---|---|
| `TELEGRAM_BOT_TOKEN` | Bot token from @BotFather, e.g. `123456:ABC-DEF...`. |
| `TELEGRAM_CHAT_ID` | The HUMAN's personal chat id with the bot (a number, sometimes negative for groups). |

These are added in the Cloud Agent **Secrets** panel and injected as env vars. Never print them.

### How the HUMAN adds them
1. In Telegram, create a bot with **@BotFather** → copy the token.
2. Get the chat id: message the bot once, then open
   `https://api.telegram.org/bot<TOKEN>/getUpdates` and read `result[].message.chat.id`
   (or use **@userinfobot**).
3. In Cursor, open the Cloud Agent **Secrets** panel (right-hand side, next to the chat) and add
   `TELEGRAM_BOT_TOKEN` and `TELEGRAM_CHAT_ID`. Secrets persist across runs and are injected into
   new Cloud Agent VMs (so they apply to the next run, not the currently running one).

## Outbound — send a message to the HUMAN

```bash
curl -s "https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/sendMessage" \
  --data-urlencode "chat_id=${TELEGRAM_CHAT_ID}" \
  --data-urlencode "parse_mode=Markdown" \
  --data-urlencode "text=${MESSAGE}"
```

Keep messages skimmable. Long briefs should lead with a TL;DR and use short sections.

## Inbound — read the HUMAN's messages (poll-within-run, option "a")

At the **start** of every run, the Chief of Staff reads new messages and treats them as
instructions + approval decisions:

```bash
# Read the last acknowledged update id from state (default 0)
OFFSET=$(cat memory/telegram_offset 2>/dev/null || echo 0)
curl -s "https://api.telegram.org/bot${TELEGRAM_BOT_TOKEN}/getUpdates?offset=$((OFFSET+1))&timeout=10"
```

After processing, persist the highest `update_id + 1` to `memory/telegram_offset` and commit it, so
the same message is never processed twice. Latency of this design = time until the next scheduled
run; this is the accepted tradeoff of option (a). Option (b) — an always-on relay that triggers a
run instantly — is a future upgrade.

## Approval requests

Approval requests are sent as normal Telegram messages that reference an outbox item id. The HUMAN
replies with a decision keyword (see `core/approvals.md`). Inline keyboard buttons are a future
enhancement that pairs with option (b).

## Message conventions

- One consolidated **daily brief** per run (not one message per agent).
- Separate, clearly-numbered **approval requests** for anything awaiting a decision.
- Use `[id]` tags so the HUMAN can approve by referencing the id.
