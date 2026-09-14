# jaan — company context (shared memory)

Every agent reads this before acting. Keep it accurate and current; if something changes, update it
here (via PR) so the whole team stays grounded. Do not invent facts beyond what is written here.

## One-liner

**jaan is the evaluation layer for Physical AI.** A cloud platform for continuous robot-AI
evaluation: teams bring a policy and the edge-cases they care about; jaan generates the simulations
and runs the evals, so a policy is proven before it ever touches hardware.

## The problem

Robotic deployment hinges on one question: *how do we know this policy will work in real life?*

- The long tail stays uncovered — unseen layouts, lighting, and obstacles are hard to simulate
  before deployment.
- Physical testing doesn't scale — slow, expensive, risks hardware, and can't safely recreate rare
  failures.
- Simulators require manual building — weeks of engineering and asset work still miss real-world
  diversity.

## The solution / product

jaan generates custom edge-case simulations so robotics teams can evaluate policies against their
exact deployment sites — turning evaluation cycles from weeks into minutes.

- **Custom worlds** — scenarios matched to the actual deployment site.
- **Closed-loop rollouts** — policies run against generative world models.
- **Actionable diagnostics** — failures, scores, videos, and trajectories.

Customer process: **1) Integrate** (plug in the robot's AI policy) → **2) Specify** (define target
scenarios/edge-cases) → **3) Evaluate** (closed-loop rollouts on generative world models) →
**4) Diagnose** (failures, scores, videos, trajectories).

## Why now

1. **Foundation models in robotics** — VLAs raise policy capability and evaluation complexity at once.
2. **Generative world models** — realistic, diverse environments can be synthesized without
   hand-building every scene.
3. **Speed-to-market pressure** — teams racing to deploy need scalable proof that policies work
   beyond the lab.

## Market

- **GTM:** AI-first robotics companies already spending heavily on internal simulation and validation.
- **Category tags:** AI infrastructure · Physical AI · robotics · devtools · enterprise SaaS +
  usage-based compute.

Working hypothesis (original bottoms-up, under revision after the 2026-09-14 critique —
see `reports/daily/2026-09-14/market-model.md` and
`memory/decisions/2026-09-14-market-model-revision.md`; CEO has not yet adopted the revision):

- **ICP (original):** ~500 embodied-AI companies, filtered for large scale. Internally inconsistent
  with the 300 / 330 headline counts used in the same model.
- **ACV (hypothesis, not observed):** $50–450k annual, priced as a fraction of in-house sim & eval
  engineering. No jaan contracts exist.
- **SAM (original, 100% attach):** ~$90M / yr. This is every listed ICP buying at hypothesized
  price — a theoretical max, not a diligence-grade SAM.

Proposed investor-safe framing (2026-09-14 research — **pending CEO adoption**; not standing
orders for external conversations until the CEO confirms):

- **TAM:** robotic software platforms ~$6.07B (2025) / $7.58B (2026) (Mordor). Simulation +
  digital-twin slice ~26.5% in 2025 ≈ $1.6B. jaan is a wedge inside that slice, not the slice.
- **SAM (INFERENCE — no census, no contracts):** $15–40M today for a standalone policy-eval layer
  (~200–350 reachable AI-robotics teams × $75–150k hypothesized ACV). Base single number if forced:
  $25M.
- **Beachhead / SOM:** tens of high-fit teams (humanoid + VLA manipulation with a real site), not
  500 logos. 24-month ambition is design partners, not a % of $90M.
- **ACV (hypothesis):** $50–150k year-1 land. $450k is not a current price card.
- **Do not cite:** 1,600-company TAM, 36.5% CAGR, 2029 SAM $340–420M, or “25% of senior engineer
  time” — those are unsourced or internally contradictory.

## Team

- **Nitai — CEO.** Technion LAPIDIM alumni; high-performance distributed systems lead at a startup;
  B.Sc. CS (Technion), M.Sc. AI Research (Tel Aviv University). *(The CEO this team serves.)*
- **Alon — CTO.** Ex-technological researcher lead (Israeli Intelligence); former AWS platform and AI
  systems engineer; B.Sc. CS (Technion), M.Sc. AI Research (Tel Aviv University).

## Contact / links

- Site: https://jaan.world
- Email: nitai@jaan.world · WhatsApp: +972-54-5750446

## Current stage & priorities (keep updated)

- **Stage:** pre-seed. No committed customers, design partners, or investors. No other employees yet.
- **Live threads (none committed; as of 2026-09-14, from inbox — not traction):**
  - Impact Labs / Idan Keisar — exploratory conversation; site visit offered; CEO-owned. Not a design partner.
  - ICI Fund — deck sent; Yaron time not confirmed.
  - Innosphere / Tim Jones — 2026-09-24 17:00 IL email-accepted (ICI intro); not a standalone raise.
  - Horizon Capital / Tom Kaverman — stay-in-touch + deck after HaRetzif; not a formal process.
- **Top priorities for the team right now:**
  1. Land the first **design partners** from the embodied-AI ICP.
  2. Open the first **pre-seed investor** conversations.
  3. Keep the founders' inbox/calendar/knowledge under control with minimal overhead.

## Voice & positioning (for any drafting)

- Technical, precise, credible to robotics/ML engineers and deep-tech investors. No hype, no fluff.
- Lead with the concrete pain (weeks-long, hardware-risking eval) and the concrete payoff
  (edge-case sim + closed-loop eval in minutes; failures/scores/videos/trajectories).
- Short, specific, respectful of the reader's time. Founder-to-expert tone.

## Do-not

- Do not overstate traction (we have none yet) or invent customer names, metrics, or endorsements.
- Do not make technical claims beyond this document without CEO confirmation.
