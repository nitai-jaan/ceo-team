# ICI Fund meeting prep — 2026-09-15 10:30 IL

**Where:** Landwer Coffee Sarona · 60 min · in person
**Who:** Nitai (accepted), Alon, Aviv Nizri (organizer, accepted), Gili Elkin (MP), Yaron Wolfsthal (Partner)
**This is:** second conversation after 2026-09-10 (Aviv + briefly Yaron). Deck already sent to Yaron today. Separate Tim Jones / Innosphere call **2026-09-24 17:00 IL** — do not treat tomorrow as that conversation.

Full market critique: `reports/daily/2026-09-14/market-model.md`.

---

## Room map

| Person | Role | What they will pressure-test | How to play |
|---|---|---|---|
| **Aviv Nizri** (`aviv@ici.fund`) | Principal; champion from Thu | That the second meeting converts Gili + Yaron. Process, founder quality. | Ally. Recap since Thu. Do not make him defend a sloppy TAM. Bio: [ici.fund](https://ici.fund/team-member/aviv-nizri/) |
| **Yaron Wolfsthal** (`yaron@ici.fund`) | Partner (joined Oct 2024). Founded IBM Cybersecurity CoE Israel; IBM Ventures Israel M&A liaison; BGU adjunct; 100+ pubs. | Eval validity, world models, sim-to-real, built vs slideware, “why not Isaac?” | Alon leads. Bounded claims. If he emailed questions overnight, *that* is the agenda. [bio](https://ici.fund/team-member/yaron-wolfsthal/) · [CTech appointment](https://www.calcalistech.com/ctechnews/article/bjjrogfca) |
| **Gili Elkin** (`gili@ici.fund`) | Co-founder & Managing Partner. Stanford MBA. Boards: Kando, Genda, Pelles.ai, Rangers.ai, illumex (NVIDIA, Feb 2026). | Israeli founder → US GTM, capital efficiency, first-check / lead / board, whether she wants jaan in the ICI community. | Nitai leads. Design-partner *search process*, not fake names. No US-office fantasy. [bio](https://ici.fund/team-member/gili-elkin/) |
| **Tim Jones** | Partner ICI + COO Innosphere (Colorado) | **Not in the room.** US scale-up. | One sentence: we speak on the 24th. [bio](https://ici.fund/team-member/tim-jones_/) |

**Thesis fit (honest):** Strong on paper — Israeli technical founders, pre-seed, B2B AI infra, Robotics + GenAI listed on [ici.fund](https://ici.fund/). Mild mismatch: ICI often backs AI sold into conservative industries (water, construction, healthcare). Frame jaan as **infra that makes Physical AI deployable**, not as a utility app.

**Gili’s own words (Jan 2026 CTech VC Survey):** “Autonomous physical systems like robotics, edge AI, and infrastructure safety are on track to be Israel’s next global export engine.” Buyers she named: US defense, logistics, energy. AUM stated **$50M**. [CTech](https://www.calcalistech.com/ctechnews/article/bywlipxiwl)

**Check size:** $250k–$1M documented in 2020 IIA Colorado–Israel guidelines; later directories ~$500k sweet spot. Fund II closed **$50M** (Jul 2025), 13 investments then, targeting ≥15 more by end-2026. [IIA PDF](https://innovationisrael.org.il/sites/default/files/Colorado-Israel%20Joint%20R&D%20and%20Pilot%20Programs%20%E2%80%93%20Guidelines.pdf) · [CTech Fund II](https://www.calcalistech.com/ctechnews/article/bklp9wbsgl)

**Adjacent portfolio (use lightly, do not pitch as customers):**
- Alta Grid — low-altitude autonomy data layer
- PLCs.ai — industrial automation intelligence
- Pelles.ai — generative MEP + path planning (physical-world generation, not policy eval)
- Insignito — drone acoustics (they use simulation language)
- **Rangers.ai is fintech scam-prevention. Do not analogize.**
- illumex → NVIDIA (Feb 2026). Congratulate if they bring it up. jaan is not an acquisition story.

---

## 60-minute agenda (coffee, deck already sent)

Do **not** restart from slide 1.

| Min | Who | What |
|---|---|---|
| 0–5 | Nitai | Thanks for looping Yaron/Gili. Since Thu: deck sent; Tim booked for the 24th. Ask if Yaron already has written questions — if yes, that becomes the agenda. |
| 5–15 | Nitai then Alon | **Lead with the job-to-be-done, not TAM.** Loop: policy in → site/edge-cases specified → closed-loop rollouts on generative worlds → failures/scores/videos/trajectories out. Why-now: VLAs raise eval complexity; generative worlds make diverse scenes possible; deploy pressure. |
| 15–35 | Alon | Yaron block. Architecture at the level of `company.md` only. What is built vs next 90 days (**confirm tonight**). Invite the attack on eval validity. |
| 35–50 | Nitai | Gili block. First design partners as a *search process*. US GTM: sell to AI-first robotics teams that already spend on sim; Innosphere is useful later, not a substitute for product proof. Two founders, no other employees, pre-seed. |
| 50–60 | Both | Their questions. Next step: Tim 2026-09-24; what they need before then. No term-sheet theater. |

If the coffee is noisy, skip any video demo unless it is rehearsed and honest about limitations.

---

## Say / don’t say

**Lead with**
- Evaluation is the bottleneck once policies leave the lab.
- jaan = evaluation layer for Physical AI. Custom worlds for the actual site, closed-loop rollouts, diagnostics.
- Team: Nitai (Technion LAPIDIM, distributed systems, BSc CS Technion, MSc AI TAU); Alon (ex-Israeli Intelligence research lead, AWS platform/AI, same degrees).
- Stage, said once: pre-seed. No customers, no design partners, no investors yet. We are here to see if this is worth continuing.
- Why ICI: Israeli deep-tech + US access + they already write first checks into physical-world AI. We want Yaron’s technical view, which is why he has the deck.

**Market, if asked (do not open with a number)**
> Robot software is a multi-billion-dollar category (Mordor ~$6–8B in 2025–26). Simulation is roughly a $1–2B slice. We are not claiming that slice. We size a standalone policy-eval layer at $15–40M today, with wide error bars, and we will win or lose on a beachhead of tens.

**Do not claim**
- Any customer, LOI, waitlist, paid pilot, or “in talks with [logo].”
- $90M SAM, ICP 300/330/500, ACV $50–450k, 36.5% CAGR, 2029 $340–420M, or “25% of senior engineer time” as facts.
- Sim-to-real percentages, eval–hardware correlation, or “minutes not weeks” as a measured SLA.
- A named world-model vendor, NVIDIA partnership, or Isaac/Cosmos integration unless you confirm it exists tonight.
- Raise size, valuation, other term sheets, “we’re oversubscribed.”
- That Rangers.ai / illumex / Pelles are jaan comps.
- That jaan is ready for an IIA Colorado bilateral pilot.

**If they quote the deck’s market slide:**
> That number is a 100% attach of an unsourced ICP. We would not defend it as SAM. Happy to walk a conservative three-layer version.

Overclaiming TAM/SAM is the #1 way this meeting dies with Yaron. Undersizing and being precise is the win.

---

## Anticipated questions (missing facts marked)

**Yaron — product**

| Question | Answer |
|---|---|
| What is jaan, one sentence? | Evaluation layer for Physical AI. Team brings a policy and the edge-cases they care about; we generate simulations and run evals so the policy is proven before hardware. |
| Walk the loop. | Integrate → specify scenarios → closed-loop rollouts on generative world models → diagnose (failures, scores, videos, trajectories). |
| What world model? | **Do not claim from memory.** Do not name Cosmos / a paper unless you confirm tonight. |
| How do custom worlds match a real site? | Intended: scenarios matched to the actual deployment site. Mechanism, data required (scans, video, CAD), fidelity: **do not invent.** |
| Why not Isaac / Gazebo / MuJoCo? | Those are simulators / engines. The wedge is *eval as the product* (generation + rollout + diagnostics), not another scene editor. Do not claim we beat Isaac on physics. |
| Sim-to-real validity? | **No correlation study in memory.** Honest: this is the hard problem; we will not fake a number; design partners exist to pressure-test it. |
| What’s built vs slideware? | **Confirm tonight.** Prefer: current / 90-day / later. |
| Minutes vs weeks? | Product copy. No measured cycle-time. Do not treat as SLA. |

**Gili — market / GTM / round**

| Question | Answer |
|---|---|
| Who is the customer? | AI-first robotics companies already spending on internal sim and validation. |
| How many / SAM? | We have not published a defensible census. Beachhead is well-funded teams evaluating learned policies. We size a standalone eval wedge at $15–40M with wide error bars (inference, not a counted SAM) and we win or lose on tens of high-fit teams — not $90M. |
| ACV? | Hypothesis $50–150k year-1, fraction of in-house eval. Not observed. Closest public analog: W&B median ~$48k. |
| Why US if you’re Israeli? | GTM is AI-first robotics teams already spending on sim; many of those budgets sit in the US. We have no US customers yet. Tim’s call on the 24th is the US-scale conversation. No US entity/office in memory — do not invent. |
| First design partners — names? | **Do not invent names.** Describe the filter. Landing first design partners is priority #1. |
| How will two people sell this? | Founder-led design-partner work, not a US sales team. ICI/Innosphere helps with intros *after* there is something to show. |
| How much are you raising? | **Not in memory.** If pressed: we will share a round sketch; we are not asking for a term sheet over coffee. Documented ICI check range is $250k–$1M (IIA Colorado–Israel guidelines, 2020) with a ~$500k sweet spot on [NFX Signal](https://signal.nfx.com/firms/ici-fund). Their stated model is lead + board. Do not commit to a board seat tonight. |
| Why you two? | Nitai: Technion LAPIDIM; distributed systems lead; BSc CS Technion; MSc AI TAU. Alon: Intelligence research lead; AWS platform/AI; same degrees. |

---

## Confirm tonight (otherwise Alon improvises)

1. What is actually built vs intended (world-model stack, policy interface, any internal demo).
2. Raise ask / round shape if asked (amount, lead vs syndicate, board).
3. Whether the deck they already have still shows $90M / 1,600 companies — if yes, verbally retire those slides rather than defend them.

---

## After the coffee

- Ingest notes into `memory/crm/investors/ici-fund.md` (questions, temperature, next step).
- Do not send a follow-up email unless you ask us to draft one.
- 2026-09-24 17:00 IL: Tim Jones — US footprint / Innosphere. Prep a one-pager before then.
