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
- **ICP:** ~500 embodied-AI companies, filtered for large scale.
- **ACV:** $50–450k annual, priced as a fraction of in-house sim & eval engineering.
- **SAM (2026 baseline):** ~$90M annual serviceable market.
- **Category tags:** AI infrastructure · Physical AI · robotics · devtools · enterprise SaaS +
  usage-based compute.

## Team

- **Nitai — CEO.** Technion LAPIDIM alumni; high-performance distributed systems lead at a startup;
  B.Sc. CS (Technion), M.Sc. AI Research (Tel Aviv University). *(The CEO this team serves.)*
- **Alon — CTO.** Ex-technological researcher lead (Israeli Intelligence); former AWS platform and AI
  systems engineer; B.Sc. CS (Technion), M.Sc. AI Research (Tel Aviv University).

## Contact / links

- Site: https://jaan.world
- Email: nitai@jaan.world · WhatsApp: +972-54-5750446

## Current stage & priorities (keep updated)

- **Stage:** pre-seed. No customers/design partners yet, no investors yet, no other employees yet.
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
