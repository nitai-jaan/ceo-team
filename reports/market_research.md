# jaan market research — evaluation layer for Physical AI

**Date:** 2026-09-14  
**Purpose:** Investor-grade bottoms-up market model. Same structure as the deck already sent to ICI Fund (universe → ICP → ACV → SAM), rebuilt on public sources.  
**Stage constraint:** jaan is pre-seed. No customers, no design partners, no realized ACV (`memory/company.md`). Every ACV and attach rate below is a **hypothesis**, not a measured contract.

**How to read**

| Tag | Meaning |
|---|---|
| **FACT** | Published number, with a source in §9 |
| **INFERENCE** | jaan interpretation of those facts. Labeled wherever it drives a dollar figure. |
| **UNKNOWN** | Not evidenced. Not filled in. |

Optimistic cases are the high end of a sourced range, not a new invention.

---

## 0. Headline vs the slides already sent

The deck ICI has uses: **universe ~1,600 companies · ICP ~500 (core ~300) · ACV $50–450k · SAM ~$90M · 3-year CAGR 36.5% · 2029 SAM $340–420M.**

| Metric | Slides (sent) | This research | How far? |
|---|---|---|---|
| Company universe | 1,600 | **2,000–2,500** physical-AI / autonomous-robotics companies **[FACT]** | Slides are **20–35% low**. Directionally right. |
| Dollar TAM | not stated (count used as TAM) | Robotic **software** **$6.1B (2025) / $7.6B (2026)**; sim + digital-twin slice **~$1.6–2.3B** **[FACT]** | Missing from the slides. This is the real TAM conversation. |
| Core ICP | 300–330 | **310–370** learned-policy teams at Series A+ scale **[INFERENCE on 480 FACT]** | **On top of the number.** |
| ICP + pipeline | 500 | **460–570** **[INFERENCE]** | **On top of the number.** 500 is a fair qualified-universe figure. |
| ACV band | $100–400k headline / $50–450k table | Land **$50–150k**; expand **$150–400k** **[INFERENCE]**; W&B median **$48k** **[FACT]** | Band is plausible. Mix is too top-heavy ($450k as the Tier-1 *average*). |
| SAM 2026 | $90–91M | Serviceable **$35–60M**; fully-penetrated ceiling **$75–95M** **[INFERENCE]** | **$90M is the ceiling, not the 2026 SAM.** About **1.5–2.5×** a fair serviceable number. |
| Category CAGR | 36.5% (unsourced) | Sim software **16.3%**; robotic software platforms **24.9%**; Physical AI software syndicators **38%** (different SKU) **[FACT]** | 36.5% matches the *Physical AI software* neighborhood. It does **not** apply to a 100%-attach SAM. |
| 2029 SAM | $340–420M | **$90–160M** base-to-optimistic; stretch **~$200M** if industrial OEMs convert **[INFERENCE]** | Slides are **2–4× high.** This is the number that needs retiring. |

**The one-line reconciliation:** the ICP count on the slides is roughly right. The $90M is a fully-penetrated *ceiling* that can be defended as a 3-year ambition, not as 2026 SAM. The 2029 $340–420M is the part that is too far from reality.

**One-breath version for the room**

> Robot software is a multi-billion-dollar category — about $7.6B in 2026. Simulation is a $1.6–2.3B slice of that. We are a wedge inside the slice. There are a few hundred AI-first robotics teams that could buy a standalone eval layer; we size that at $35–60M today, with a $75–95M ceiling if nearly every qualified team buys. The 500 / $90M on the deck is that ceiling, not a 2026 forecast. We win or lose on a beachhead of tens.

---

## Step 1 — Target universe

### 1.1 Dollar TAM (use this, not a logo count)

jaan sells **policy evaluation on generated worlds** — a slice of robot / Physical-AI *software*, not robot hardware and not foundation-model training.

| Category | 2025 | 2026 | Forward CAGR | What it includes | Use for jaan |
|---|---|---|---|---|---|
| Robotic **software platforms** | **$6.07B** | **$7.58B** | **24.93%** to $23.07B (2031) | Perception, sim/twins, fleet, safety, control plane | Broadest credible software TAM |
| ↳ of which **sim + digital twin** | **~$1.61B** (26.50% of $6.07B) | — | — | Offline programming, virtual commissioning, twins, validation tooling | Closest published slice |
| Dedicated **robot simulation software** | **$1.94B** | **$2.25B** | **16.3%** to $4.11B (2030) | Broader sim SKU (still includes OEM/OLP tools jaan is not) | Cross-check on the sim slice |
| Industrial robot **intelligence** software | $1.83B | $2.04B | 9.83% to 2031 | Factory programming, validation, monitoring | Lower-bound industrial-only |
| Physical AI + embodied intelligence **software** | $4.50B | $6.21B | **38.0%** to $67.8B (2034) | Training, nav, HRI, multi-robot, sim-to-real | **Directional only.** Different SKU. |
| Physical AI **platform** | $0.32B | — | **47%** to $5.5B (2032) | Narrower “platform” definition | **Do not average with $4.50B.** |

Sources: Mordor robotic software platforms; Mordor industrial robot intelligence software; The Business Research Company / Research and Markets robot simulation; MarketIntelo; MarketsandMarkets. Full URLs in §9.

**INFERENCE — jaan TAM statement:** the category we sit in is a **$1.6–2.3B** simulation / validation software market in 2025–26, itself inside a **$6–8B** robotic software-platform market. We do not claim either number as jaan revenue. We claim the right to take a wedge of the sim/eval slice.

**Existence proof that this is a real software business (FACT):**

- Applied Intuition: official **$600M Series F at $15B** (Jun 2025); official **18 of the top 20 global automakers** plus major DoD programs. Sacra *estimates* **$830M 2025 ARR** (estimate — say “Sacra estimates”).
- Foretellix (Israeli V&V analog): official **$85M Series C**, **$135M** total raised (Dec 2023); named customers include Volvo, Torc / Daimler Truck, Mazda, Woven by Toyota, Nuro, Isuzu. Third-party revenue figures ($26–32M) are unverified — do not quote as theirs.
- NVIDIA is productizing the same job: Isaac Sim, Isaac Lab, Isaac Lab-Arena (open policy-evaluation framework), Cosmos world models.

### 1.2 Company universe (inputs — never add these rows)

These databases **overlap**. Summing them double-counts Waymo-class, Amazon Robotics, and half the AMR field.

| Universe | Count | As-of | What it is | Source |
|---|---|---|---|---|
| Physical-AI companies, 24 use cases | **~2,500** | May 2026 | Best-effort census; English-web bias; long tail undercounted | npow |
| Tracxn **Autonomous Robotics** | 2,365 founded / **2,053 active** / 945 funded / **480 Series A+** | Aug 2026 | Closest “autonomous robots” count | Tracxn |
| Tracxn **Industrial Robotics** | 2,568 / **2,302 active** / 860 funded / **438 Series A+** | Aug 2026 | Includes classical arms + integrators | Tracxn |
| Tracxn **Autonomous Vehicles** | 1,327 / **1,145 active** / 690 funded / **408 Series A+** | Aug 2026 | Overlaps Autonomous Robotics; many already on Applied | Tracxn |
| IFR service-robot **manufacturers** | **944** (80% SMEs ≤500). Unit stats from a sample of 293/944, not projected | 2024 / WR 2025 | Official “who makes service robots.” Excludes AV. | IFR |
| IFR industrial robot **installations** | **542,000** units; stock **4.66M** | 2024 | Units, not companies. Mostly programmed arms. | IFR |
| StartUs **embodied AI** startups | **400+** | 2026 | Startup/scaleup filter, not all robotics | StartUs Insights |
| Humanoid OEMs | **45** (humanoidintel) · **53** (RoboZaps, Jul 2026) | 2026 | Bodies, not “embodied AI brains” (π, Skild) | directories |
| China embodied-AI **startups** | **425** (75% founded 2023–26) | Aug 2026 | China-only; do not add to global Tracxn | IT Juzi / HTX |
| China embodied-AI **value chain** | **10,000+** (components + integration + apps) | May 2026 | Supply chain, not ICP. Ignore for SAM. | Qixinbao / Embodied Global |
| Tracxn **Logistics Robotics** | 609 / **526 active** / 240 funded / **137 Series A+** | Aug 2026 | AMR / warehouse / delivery. Overlaps AR. | Tracxn |
| Tracxn **AI in logistics robotics** | 56 / 50 funded / **36 Series A+** | Jul 2026 | The AI-first subset | Tracxn |
| Tracxn **AI in drones** | 100 / 53 funded / **26 Series A+** | Jan 2026 | Not the 5,757-company consumer-drone dump | Tracxn |
| Tracxn **UAV** (narrow) | 193 / 176 active / 56 funded / **27 Series A+** | Aug 2026 | Skydio-class, not DJI long tail | Tracxn |

**INFERENCE — universe vs the slides:** a 1,600-company “robotics + autonomy” universe is **conservative** against 2,053 active autonomous-robotics firms and ~2,500 physical-AI firms. It is **aggressive** against IFR’s 944 service-robot makers. The honest sentence is: *there are a couple of thousand companies in the physical-AI / autonomous-robotics orbit; about a thousand of those are funded; a few hundred are at the scale where a standalone eval layer is a real budget line.*

### 1.3 Segment map (rebuilt)

The original five bins were the right *shape*. The counts were unsourced. Rebuilt from the tables above. **Do not add the five bins to invent a new TAM** — they overlap (Boston Dynamics, Agility, Skydio all sit in more than one mental bucket).

```
Physical-AI / autonomous-robotics orbit     ~2,000 – 2,500 companies
        │
        ├── 1. Embodied AI, humanoids, robot brains
        ├── 2. AV, trucking, off-highway autonomy
        ├── 3. Logistics, AMR, mobile manipulation
        ├── 4. Defense, aerial, maritime autonomy
        └── 5. Legacy industrial & service (long tail)
                        │
              [ scale + learned-policy filters ]
```

| Segment | Original slides | Sourced anchor | Rebuilt range (INFERENCE) | Notes |
|---|---|---|---|---|
| 1. Embodied AI & humanoids | 60–80 | 45–53 humanoid OEMs; 400+ embodied-AI startups (StartUs); plus brain labs (Physical Intelligence, Skild, Flexion, …) | **70–90 core** (OEM + brain). 400+ is the wide net. | Original 60–80 is fair for *core*, not for StartUs’s 400. Extreme eval need: VLA, RL, world models, site-specific long tail. |
| 2. AV, heavy machinery, off-highway | 120–150 | 408 Series A+ AV (Tracxn); 1,145 active | **100–150 jaan-reachable** | Original count matches *reachable*, not *total*. Passenger OEM AV is Applied Intuition’s fortress — bad beachhead, real later expansion. |
| 3. Logistics, AMR, mobile manipulation | 180–220 | 137 Series A+ logistics robotics; 36 Series A+ *AI* in logistics robotics; 240 funded | **80–140 AI-first**; 180–240 if you count all funded logistics robotics | Original 180–220 ≈ funded logistics robotics, **before** the neural-policy filter. The eval-layer ICP is the AI-first subset. |
| 4. Defense, aerial, maritime | 90–110 | 26 Series A+ AI-in-drones; 27 Series A+ UAV; defense-tech VC **$12.3B in H1 2026** (PitchBook/FT) | **50–90** AI-first aerial / defense / marine | Original 90–110 is the optimistic high end. Willingness to pay is high; air-gap / ITAR is a product question (jaan is described as cloud). |
| 5. Legacy industrial & service | 1,100+ | 2,302 active industrial robotics; IFR 944 service-robot makers | **Long tail. Not 2026 ICP.** | Conversion to learned grasping / adaptive motion is the 2028–30 expansion, not the beachhead. |

**Why now (FACT, not a TAM):** robotics startups raised **$15B in 2025** and **$18.8B YTD by 22 Jun 2026** (Crunchbase) — already above the 2021 peak. That is capital *into labs*, not eval-software spend. It is why those labs will need eval.

---

## Step 2 — ICP criteria and funnel

Not every robotics company can or should buy a standalone world-model evaluation layer. Two filters, applied in order.

1. **Scale & capital.** Enough budget for $50k+ software. Proxy: Series A+ **or** the original >$10M raised / >50 FTE rule. Tracxn publishes the Series A+ cut; FTE is not in public databases.
2. **Architecture.** Deploying (or imminently deploying) a **non-deterministic learned policy** — VLA, end-to-end RL, neural mobility — that needs edge-case scenario testing. Scripted / teach-pendant / classical motion-planning cells are not ICP.

The original model stated filter 2 and then counted everyone who passed filter 1. That is the main inflation in the $91M identity.

### ICP qualification funnel

```
Physical-AI / autonomous-robotics orbit
┌────────────────────────────────────────────────────────┐  ~2,050 – 2,500     FACT (Tracxn AR active / npow)
│ Filter 1a: funded                                      │  ~945               FACT (Tracxn AR funded)
│ Filter 1b: Series A+  (≈ >$10M / scale)                │  ~480               FACT (Tracxn AR Series A+)
│ Filter 2:  learned-policy architecture (65–75%)        │  ~310 – 370         INFERENCE
│ Pipeline: funded, pre-A, AI-policy (Tier 3)            │  ~150 – 200         INFERENCE
├────────────────────────────────────────────────────────┤
│ Qualified ICP + pipeline                               │  ~460 – 570         INFERENCE
│   Tier 1  Anchor  (>$50M or >150 FTE)                  │  ~80 – 100
│   Tier 2  Mid-market core                              │  ~200 – 250
│   Tier 3  Emerging pipeline                            │  ~150 – 200
└────────────────────────────────────────────────────────┘
```

**Why 65–75% on filter 2 (INFERENCE):** there is no public split of “has a learned policy.” The 2025–26 capital shift *into* embodied brains (China deal-mix already has “AI brain” deals ahead of humanoid-body deals; Crunchbase’s 2026 robotics narrative is explicitly embodied-AI) makes a majority cut at Series A+ defensible. A 50% cut is the conservative bound (240 of 480). A 75% cut is the optimistic bound (360). We use **70% → 336** as the point estimate for core ICP.

**Why the slides’ 500 survives:** 336 core + ~170 pipeline = **~506**. The 500 on the deck is a fair **qualified-universe** number once the architectural filter is actually applied to Tracxn’s 480 and a pipeline is added. It is **not** “every robotics company with 50 employees.”

### ICP tier breakdown

Keep the original three-tier story; retune the pain and the ACV (step 3).

**Tier 1 — Anchor (~90 companies)**  
Foundation-model / humanoid scaleups and Tier-1 AV / defense programs. >$50M raised or >150 FTE. 40–250 AI / robotics / sim engineers.  
Pain: in-house eval exists and is brittle; the question is buy-vs-build for *site-specific long-tail*, not “do we evaluate.”  
Examples (public, not jaan relationships): Figure, Apptronik, Agility, 1X, Skild, Physical Intelligence, Shield AI, Skydio, Anduril, Waymo-class (often captive).

**Tier 2 — Mid-market core (~240 companies)**  
Commercial physical-AI companies, 50–150 FTE, $10–50M raised, 12–40 AI / robotics engineers.  
Pain: cannot staff a 2–4 person eval-platform team. This is the volume ICP.  
Examples: ANYbotics, Collaborative Robotics, Sereact, specialist AMRs and mobile manipulators that have crossed onto neural policies.

**Tier 3 — Emerging pipeline (~170 companies)**  
Seed / Series A labs, 15–50 FTE, $3–10M, 5–12 AI engineers.  
Pain: need a credible eval story for the next round and the first pilot customer. Lower ACV, higher volume, longer to cash.

---

## Step 3 — Engineering economics and ACV

No jaan contract exists. ACV is derived from (a) replacement cost of in-house eval and (b) public analogs. Label both as hypotheses.

### Cost benchmarks (FACT)

| Input | Figure | Source |
|---|---|---|
| US mid-to-senior ML engineer, **fully loaded year-1** | **$210,000 – $370,000** | KORE1, 2026 (base + payroll tax + benefits + compute/tooling + recruiting) |
| US senior AI engineer, fully loaded | **$300,000 – $460,000** | AY Automate, 2026 |
| US robotics-AI engineer, average **base / total comp** | **$175,000 / $254,000** | Orbyt, Jun 2026 (81 cities) |
| Original model’s $220k “fully loaded” | too low for US senior robotics/ML | Closer to a mid-level *base* than a loaded senior seat |
| W&B median annual contract | **$47,625** (n=65); range $11,160 – $107,440 | Vendr, 2025 procurement |
| W&B enterprise seats (buyer-reported) | **~$315 – $400 / seat / month** | Vendr |
| W&B large-team enterprise analog | **~$360,000 / yr** (500+ ML engineers, crowdsourced) | Zendikt |

The original “$5,000–$7,500 per engineer per month on sim/tooling” and “25%+ of senior engineer time” are **UNKNOWN**. They are not used below.

### Build-vs-buy (INFERENCE)

| | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| Eval-adjacent FTE (sim + safety + eval harness) | 3–5 | 1–2 | 0.5–1 |
| Loaded labor (use $250k mid / $320k senior blend) | $750k – $1.6M | $250k – $640k | $105k – $250k |
| Value capture we can defend | 15–25% of labor | 20–30% | 20–30% |
| Implied ACV | **$110k – $400k** | **$50k – $190k** | **$20k – $75k** |
| **Point ACV used below** | **$300k** | **$150k** | **$60k** |
| Original slide ACV | $450k | $175k | $50k |

**Why this is still optimistic:** $300k / $150k / $60k sits at the *high* end of W&B-like land and the *middle* of build-vs-buy. It assumes jaan is priced as a real eval platform, not a $20k plugin. It does **not** assume Applied-Intuition OEM contracts.

**Land vs expand (INFERENCE):** year-1 land **$50–150k** (W&B-like + 0.5–1.5 FTE). Expand **$150–400k** as seats, sites, and usage-based compute grow. $450k is an expand outcome for a Tier-1 account, not the average new logo.

---

## Step 4 — Bottom-up SAM

$$\text{SAM}_{\text{theoretical}} = \sum_i N_i \times \text{ACV}_i$$

That identity is a **ceiling** (every qualified logo buys at list, every year). Serviceable SAM applies an attach rate for “would buy a standalone cloud eval layer vs build / vs Applied / vs Isaac-only.”

### 4.1 Theoretical max — same N as the slides, retuned ACV

| ICP tier | N | This research ACV | Subtotal | Original ACV | Original subtotal |
|---|---|---|---|---|---|
| Tier 1 | 90 | $300,000 | **$27.0M** | $450,000 | $40.5M |
| Tier 2 | 240 | $150,000 | **$36.0M** | $175,000 | $42.0M |
| Tier 3 | 170 | $60,000 | **$10.2M** | $50,000 | $8.5M |
| **Total (100% attach)** | **500** | blended **$146k** | **$73.2M** | blended ~$182k | **$91.0M** |

The slides’ $91.0M is **24% above** a sourced-ACV theoretical max on the same 500 logos. Most of the gap is the $450k Tier-1 average ($40.5M vs $27.0M).

### 4.2 Serviceable SAM 2026 — attach rates (INFERENCE)

Not every qualified team buys. Captive stacks (Tesla, Amazon Robotics, Waymo), Applied-standardized AV programs, air-gapped defense, and “Isaac + grad students” all leak.

| Case | Attach of the 500 | Effective N | Blended ACV | SAM | Read as |
|---|---|---|---|---|---|
| Conservative | 40% | 200 | $90k | **$18M** | Year-1 land, tight filter |
| Base | 55% | 275 | $120k | **$33M** | Default serviceable |
| **Optimistic (recommended)** | **70%** | **350** | **$160k** | **$56M** | High attach + expand mix |
| Ceiling (slides method, our ACV) | 100% | 500 | $146k | **$73M** | Everyone buys |
| Ceiling (slides method, slides ACV) | 100% | 500 | $182k | **$91M** | What ICI already has |

**Recommended 2026 SAM to defend:** **$35–60M** (base → optimistic).  
**Recommended ceiling to keep the deck honest:** **$75–95M** — “if we penetrate the qualified 500 at mid-to-high ACV.” That is how $90M stays in the conversation without being a 2026 forecast.

Weighted ACV at the optimistic serviceable case: $56M / 350 ≈ **$160k**, inside the slide headline band of $100–400k.

### 4.3 Sensitivity (theoretical max, $M)

Tier 3 held at 170 × $60k = $10.2M. N_T1 = 90, N_T2 = 240.

| T2 ACV \ T1 ACV | $250k | $300k (base) | $400k |
|---|---|---|---|
| $120k | 22.5 + 28.8 + 10.2 = **$61.5M** | 27.0 + 28.8 + 10.2 = **$66.0M** | 36.0 + 28.8 + 10.2 = **$75.0M** |
| $150k (base) | 22.5 + 36.0 + 10.2 = **$68.7M** | 27.0 + 36.0 + 10.2 = **$73.2M** | 36.0 + 36.0 + 10.2 = **$82.2M** |
| $200k | 22.5 + 48.0 + 10.2 = **$80.7M** | 27.0 + 48.0 + 10.2 = **$85.2M** | 36.0 + 48.0 + 10.2 = **$94.2M** |

The $91M slide sits just above the top-right of this grid — reachable only with **$400k Tier-1 and $200k Tier-2 at 100% attach**. That is the optimistic ceiling, not the base.

Arithmetic check on the *original* sensitivity (for the record): 90×350 + 240×125 + 170×50 = 31.5 + 30.0 + 8.5 = **$70.0M**, not the $68.5M printed on the old matrix. The old first row was wrong.

---

## Step 5 — Three-year expansion (2026 → 2029)

Growth has to come from named drivers, and the CAGR on the *output* must match the CAGR you cite.

### Drivers (FACT + inference)

1. **Learned-policy conversion of the long tail.** Industrial and AMR stacks are adding neural grasping / adaptive navigation. Mordor notes ABB and FANUC integrating NVIDIA Omniverse / Isaac in 2026 — the OEM software stack is moving toward sim-to-real validation as a buying criterion.
2. **New embodied-AI labs.** StartUs 400+ embodied-AI startups; China 425 embodied startups, 75% founded since 2023; Crunchbase robotics capital at records. The buyer set grows.
3. **Land-and-expand ACV.** Usage-based compute + more sites. W&B shows the pattern (median $48k → large-team analog $360k).
4. **Regulatory / safety pressure.** ISO 10218-1/2:2025 updates functional-safety expectations that flow into simulation and validation tooling (Mordor). Defense and AV already pay for scenario coverage (Foretellix, Applied).

### What CAGR applies to what

| If you are growing… | Use | 3-year multiple |
|---|---|---|
| Dedicated robot-sim software | **16.3%** (TBRC) | × **1.57** |
| Robotic software platforms | **24.93%** (Mordor) | × **1.95** |
| “Physical AI software” syndicators | **38.0%** (MarketIntelo) | × **2.63** |
| Original slide SAM $91M → $340–420M | **55–66%** implied | × **3.7–4.6** |

$91M × 1.365³ = **$231M**, not $340–420M. The old 36.5% and the old 2029 number cannot be used together.

### 2029 SAM (INFERENCE, internally consistent)

Start from optimistic 2026 serviceable **$56M** (350 × $160k).

| Path | Buyers 2029 | Blended ACV 2029 | SAM 2029 | Implied 3-yr CAGR |
|---|---|---|---|---|
| Sim-category only (16.3% on dollars, mix held) | 350 | $160k × 1.57 | **$88M** | 16.3% |
| Platform-category (24.9%) | 350 | $160k × 1.95 | **$109M** | 24.9% |
| **Base optimistic (buyers + ACV)** | **500** | **$200k** | **$100M** | **21%** |
| **Optimistic (conversion + expand)** | **600** | **$250k** | **$150M** | **39%** |
| Stretch (industrial OEM conversion) | 750 | $270k | **$203M** | 54% |
| Original slides | 650+ | ~$523–646k | $340–420M | 55–66% |

**Recommended 2029 range: $90–160M.**  
That lets you say, honestly and optimistically: *the $90M on the deck is what we believe the market is worth by the end of the decade if we execute — not what it is worth on day one.*  
Do not say $340–420M.

---

## Step 6 — Beachhead (SOM), because pre-seed lives here

**FACT:** $0 revenue, 0 design partners, 2 founders.

**Beachhead filter (who, not 1,600):**

- Already trains / deploys a learned policy (VLA, RL, neural mobility).
- Has a **named real deployment site** — the custom-world wedge.
- Cloud-OK, English-speaking GTM (US, Israel, selected EU).
- **Not** passenger-AV OEMs (Applied). **Not** FANUC-style programmed cells. **Not** Amazon / Tesla / Waymo as first logos.

**24-month ambition (not a forecast):** 15–30 high-fit logos in outreach · 3–8 design partners · 1–4 paying if the product works. Do not quote a 24-month ARR to ICI.

This is where the meeting is won. The $56M SAM is the *shape of the prize*. The next two design partners are the *proof*.

---

## Step 7 — Competitive set (must name)

Differentiate only with the product in `memory/company.md`: custom worlds matched to the **actual deployment site**, closed-loop policy rollouts, diagnostics (failures, scores, videos, trajectories).

| Name | What they are (FACT) | jaan wedge (INFERENCE) |
|---|---|---|
| **Applied Intuition** | Vehicle-intelligence toolchain. Series F $600M @ $15B. 18/20 top automakers + DoD. Sacra est. $830M 2025 ARR. Expanding into trucking, mining, agriculture, defense. | They own **vehicle** validation. Year-1 beachhead is robot-policy eval at a site, not ISO-26262 OEM programs. |
| **NVIDIA Isaac / Cosmos** | Isaac Sim, Isaac Lab, Isaac Lab-Arena (policy evaluation), Cosmos world models. Default stack. | NVIDIA sells infrastructure and models. Our bet is a **hosted, site-matched eval layer**, not beating Isaac on physics. |
| **In-house stacks** | Every serious lab has internal sim/eval. The real incumbent. | Buy-vs-build for long-tail *site* eval. Captive majors are not the beachhead. |
| **Gazebo / MuJoCo / Isaac Lab** | Open engines. | Engines, not a productized eval service. |
| **Weights & Biases** | Experiment tracking / eval *logging*. Median ACV ~$48k. | Logs runs. Does not generate site-matched worlds. Complementary. Closest **devtools ACV** analog. |
| **Scale** | Physical AI **data engine**. Partners include Physical Intelligence; UR + Isaac Sim flywheel. | They industrialize demonstration data. We industrialize **policy evaluation**. Adjacent budget. |
| **Foretellix** | Israeli AV/ADAS V&V + scenario coverage. $85M Series C, $135M total. Volvo, Torc, Mazda, Toyota, Nuro, Isuzu. | Closest **category analog** (eval as the product). Different domain (vehicles vs robot policies / sites). Useful proof that Israeli eval tooling can sell to US/EU OEMs. |

Also if asked: dSPACE, Ansys, Siemens, Cognata (AV / industrial incumbents). Same rule: no invented jaan capabilities.

---

## Step 8 — What is still UNKNOWN

1. Unique, deduplicated count of companies that both ship a learned policy **and** would buy third-party eval. Tracxn sectors overlap; IFR is units + 944 makers.
2. jaan willingness-to-pay. Zero contracts. All ACVs are hypotheses.
3. Share of engineering time spent on sim/eval. The old 25% figure stays retired; no replacement study.
4. Export-control / on-prem / air-gap share (defense, some industrial, China). Product is described as cloud.
5. Whether Applied Intuition’s robotics / warehouse expansion becomes a 2027+ direct competitor in this exact wedge.
6. What is built vs intended (world-model vendor, policy API, any internal demo). Memory describes the product, not shipped status.

---

## Step 9 — Sources

Every number in this memo traces to one of these. Syndicated TAM figures (Mordor, TBRC, MarketIntelo, MarketsandMarkets) are third-party models, not primary filings — treat as directional and do not blend definitions.

### Company and universe counts

1. Tracxn, *Autonomous Robotics — 2026 Market & Investments Trends* (Aug 2026): 2,365 / 2,053 active / 945 funded / 480 Series A+. https://tracxn.com/d/sectors/autonomous-robotics/__CCq4CQiwNC1b6bYQMhwu5b9O0n0hzUT3OCOfhcSHYEo
2. Tracxn, *Industrial Robotics — 2026* (Aug 2026): 2,568 / 2,302 active / 860 funded / 438 Series A+. https://tracxn.com/d/sectors/industrial-robotics/__8YzlIwdZtVDpzlzTadeYnqjdh1suJksuE5MDB89oZiU
3. Tracxn, *Autonomous Vehicles — 2026* (Aug 2026): 1,327 / 1,145 active / 690 funded / 408 Series A+. https://tracxn.com/d/sectors/autonomous-vehicles/__lKXOKEcD9v8_QkVgJB6zssX4fym2wDECLdcAPpIfXnU
4. Tracxn, *Logistics Robotics* (Aug 2026): 609 / 526 active / 240 funded / 137 Series A+. https://tracxn.com/d/trending-business-models/startups-in-logistics-robotics/__xG-czeq6am0YNeqmMlYyWY0LIXBcZp5kmfk3-LpjzVE
5. Tracxn, *Artificial Intelligence in Robotics in Logistics* (Jul 2026): 56 / 50 funded / 36 Series A+. https://tracxn.com/d/artificial-intelligence/ai-startups-in-robotics-in-logistics/__aAw4_BG5LGCSDDrmVuVmarI9XOSU6m3h8VTNjQ3RiHc
6. Tracxn, *Artificial Intelligence in Drones* (Jan 2026): 100 / 53 funded / 26 Series A+. https://tracxn.com/d/artificial-intelligence/ai-startups-in-drones/__ECpOl2FjqxCchFGSbU1chvLy7OuBiOIo-XDM473ESIo
7. Tracxn, *UAV* (Aug 2026): 193 / 176 active / 56 funded / 27 Series A+. https://tracxn.com/d/trending-business-models/startups-in-uav/__cV8f8l14dm1GZOzhCj1drelYAarohdS5BDP6Kl2NcC0
8. Tracxn, *Drones* sector (Jul 2026): 5,757 / 4,255 active / 1,434 funded / 553 Series A+ — **too broad for ICP** (includes consumer). https://tracxn.com/d/sectors/drones/__OXaRFvb8e22bXRzPql68ayvrBeJqfgZ2Z7EKgGsCSxE
9. npow, *The State of Robotics (May 2026)*: ~2,500 physical-AI companies across 24 use cases; best-effort, English-web bias. https://npow.github.io/posts/state-of-robotics-2026/
10. StartUs Insights, *10 Embodied AI Startups to Watch in 2026*: 400+ embodied-AI startups/scaleups identified. https://www.startus-insights.com/innovators-guide/embodied-ai-startups/
11. humanoidintel.ai, *Every Humanoid Robot Company in 2026*: 45 active companies, $15.1B+ disclosed funding (through Apr 2026). https://humanoidintel.ai/humanoid-robot-companies-complete-list/
12. RoboZaps, *53 Humanoid Robot Companies Compared* (30 Jul 2026). https://blog.robozaps.com/b/humanoid-robot-companies
13. International Federation of Robotics, *World Robotics 2025* press presentation: 542,000 industrial installations (2024); 944 service-robot manufacturers; definition excludes software bots, remote drones, UAV/UGV/UUV, autonomous cars. https://ifr.org/downloads/press_docs/PressConference2025_presentation.pdf
14. IFR, *World Robotics 2025 — Industrial Robots* executive summary / press: 542,000 installations; 4.66M operational stock. https://ifr.org/ifr-press-releases/news/global-robot-demand-in-factories-doubles-over-10-years
15. IFR, *World Robotics 2025 — Service Robots* executive summary: 944 manufacturers; 199,000 professional service robots sold (+9%); sample of 293/944. https://ifr.org/img/worldrobotics/Executive_Summary_WR_2025_Service_Robots.pdf
16. Crunchbase News, *Sector Snapshot: Robotics Startups…* (22 Jun 2026): $15B robotics startup funding in 2025; $18.8B YTD 2026. https://news.crunchbase.com/robotics/startup-venture-funding-surges-2026-data/
17. HTX Insights / IT Juzi, *From Building the Body to Building the Brain* (Aug 2026): 425 Chinese embodied-AI startups; 75% founded 2023–26. https://www.htx.com/news/from-building-the-body-to-building-the-brain-the-key-shift-i-vvWqcFUB/
18. Embodied Global / Qixinbao, *China Embodied AI Industry Surpasses 10,000 Companies* (May 2026): value-chain count, not ICP. https://embodiedglobal.com/en/article/china-embodied-ai-industry-10000-companies-report-2026

### Dollar TAM and growth

19. Mordor Intelligence, *Robotic Software Platforms Market*: $6.07B (2025), $7.58B (2026), $23.07B (2031), 24.93% CAGR; sim + digital twin **26.50%** of 2025 revenue. https://www.mordorintelligence.com/industry-reports/robotic-software-platforms-market
20. Mordor Intelligence, *Industrial Robot Intelligence Software Market*: $1.83B (2025), $2.04B (2026), $3.26B (2031), 9.83% CAGR. https://www.mordorintelligence.com/industry-reports/industrial-robot-intelligence-software-market
21. The Business Research Company / Research and Markets, *Robot Simulation Software Global Market Report 2026*: $1.94B (2025), $2.25B (2026), $4.11B (2030), 16.3% CAGR. https://www.thebusinessresearchcompany.com/report/robot-simulation-software-market-report · https://www.researchandmarkets.com/reports/6241507/robot-simulation-software-global-market-report
22. ABI Research, robotics simulation software to **$1.4B by 2030**; design/development sim 21.6% CAGR (narrower definition than TBRC). https://www.abiresearch.com/press/rapid-prototyping-training-and-product-testing-drive-a-us14-billion-robotics-simulation-software-market-by-2030
23. MarketIntelo, *Physical AI and Embodied Intelligence Software*: $4.50B (2025), $6.21B (2026), $67.8B (2034), 38.0% CAGR — **directional, different SKU**. https://marketintelo.com/report/physical-ai-and-embodied-intelligence-software-market
24. MarketsandMarkets, *Physical AI Platform Market*: $0.32B (2025) → $5.5B (2032), ~47% CAGR — **different definition, do not blend**. https://www.marketsandmarkets.com/Market-Reports/physical-ai-platform-market-11457300.html

### Comparables, ACV, and engineering cost

25. Applied Intuition, Series F press release (17 Jun 2025): $600M at $15B; 18 of top 20 global automakers; major DoD programs. https://www.appliedintuition.com/press-releases/series-f
26. Sacra, Applied Intuition profile: *estimated* $830M 2025 ARR (estimate, not company-reported). https://sacra.com/c/applied-intuition/
27. Foretellix, Series C close (5 Dec 2023): $85M round, $135M total; 83North, Temasek, Isuzu, Woven Capital, NVIDIA. https://www.foretellix.com/foretellix-raises-85-million-in-series-c-closing/
28. PR Newswire, Foretellix Foretify expansion (21 May 2025): customers Torc, Volvo, Mazda, Woven by Toyota, Nuro; Omniverse / Cosmos integration. https://www.prnewswire.com/news-releases/foretellix-accelerates-ai-powered-autonomous-vehicles-with-data-driven-development-toolchain-and-safety-evaluation-302461702.html
29. Vendr, *Weights & Biases Software Pricing* (2025): median buyer **$47,625 / yr** (n=65); range $11,160–$107,440; enterprise seats ~$315–400/mo. https://www.vendr.com/marketplace/weights-biases
30. Zendikt, Weights & Biases pricing intelligence: large-team enterprise analog ~$360,000 / yr (crowdsourced). https://www.zendikt.com/product/weights-and-biases
31. KORE1, *How Much Does It Cost to Hire an ML Engineer? (2026)*: US mid-to-senior fully loaded year-1 **$210k–$370k**. https://www.kore1.com/cost-to-hire-ml-engineer-2026/
32. AY Automate, *AI Engineer Cost (2026)*: US senior fully loaded **$300k–$460k**. https://www.ayautomate.com/blog/hire-ai-engineers-cost-guide
33. Orbyt, *Robotics AI Engineer Salary Data* (Jun 2026): US average base $175k, total comp $254k. https://www.orbytjobs.ai/salaries/robotics-ai-engineer

### Stack, capital, and adjacent markets

34. NVIDIA, Isaac Sim (Omniverse robotics simulation and synthetic data). https://developer.nvidia.com/isaac/sim
35. NVIDIA, Isaac Lab-Arena (policy evaluation framework). https://developer.nvidia.com/isaac/lab-arena
36. Scale, Physical AI data engine. https://scale.com/physical-ai
37. TechCrunch / Reuters, Shield AI Series G (26 Mar 2026): $1.5–2B at **$12.7B** valuation. https://techcrunch.com/2026/03/26/defense-startup-shield-ai-lands-12-7b-valuation-up-140-after-u-s-air-force-deal/ · https://www.reuters.com/business/aerospace-defense/defense-technology-startup-shield-ai-valued-127-billion-latest-funding-round-2026-03-26/
38. TechCrunch, Anduril (24 Jul 2026): $5B raise at $61B (May 2026); reported talks at ~$100B. Defense-tech VC **>$12B in H1 2026**. https://techcrunch.com/2026/07/24/anduril-reportedly-in-talks-to-raise-funding-at-100b-valuation-more-than-3x-last-years-mark/
39. Amazon, Covariant (Aug 2024): founders joined Amazon; models licensed — not a clean independent ICP logo. https://www.aboutamazon.com/news/company-news/amazon-covariant-ai-robots

### Product and company (jaan)

40. jaan site. https://jaan.world
41. Internal company memory (stage, product loop, no traction). `memory/company.md` in this repository.

---

*Arithmetic in §§4–5 was checked against the identities 90×300k + 240×150k + 170×60k = 73.2M and 350×160k = 56.0M. The original slide identity 90×450k + 240×175k + 170×50k = 91.0M is arithmetically correct; it is the attach-rate and Tier-1 ACV that overstate 2026 SAM.*
