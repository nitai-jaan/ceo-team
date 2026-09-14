# jaan market model — critique and rebuild (ICI Fund, 2026-09-15)

**Status:** research critique. Not customer evidence. No jaan ACV has been observed.
**For:** in-person ICI Fund meeting, 2026-09-15 10:30 IL (Landwer Coffee Sarona).
**How to read:** FACT = published number + URL. INFERENCE = jaan interpretation. UNKNOWN = do not fill in the room.

---

## Investor-safe numbers (use these tomorrow)

| Layer | Status | Say this | Do not say |
|---|---|---|---|
| **TAM** | FACT (Mordor) + scoped INFERENCE (jaan is a wedge) | Robotic *software platforms* ~$6.07B (2025) / $7.58B (2026). Simulation + digital-twin slice ~26.5% of that in 2025 ≈ **$1.6B**. jaan is a wedge inside that slice. | “TAM is 1,600 robotic companies.” |
| **SAM** | **INFERENCE** — no census, no contracts | **$15–40M** for a standalone policy-eval layer (~200–350 reachable AI-robotics teams × $75–150k hypothesized ACV). Use **$25M** if forced to one number. Wide error bars. | **$90M / $91M** as a fact. That is 100% attach of an unsourced list. |
| **2029** | **INFERENCE** | If learned-policy adoption continues: maybe **$50–75M**. Robot-sim syndicators grow mid-teens, not 55–68%. | **$340–420M** and **36.5% CAGR** in the same breath (they contradict). |
| **ICP** | FACT anchors + INFERENCE filter | **Tens** of high-fit teams now (humanoid + VLA manipulation with a real site). **Low hundreds** if learned policies keep spreading. Anchors: 45–53 humanoid OEMs; 480 Series A+ autonomous-robotics as an *upper bound*, not a buyer list. | ICP = 300 or 330 or 500 as one sourced fact. |
| **ACV** | **INFERENCE** (W&B analog is FACT) | **Hypothesis $50–150k** year-1 land. Analog: W&B median ~$48k (n=65). $450k is not a current price card. | Proven $100–400k or Tier-1 $450k. |
| **SOM (24 mo)** | **INFERENCE** — ambition, not a forecast | 3–8 design partners, 1–4 paying if the product works. Do not quote an ARR number. | Any % of $91M, or a 24-month ARR target. |

**One-breath version if pressed:**
> Robot software is a multi-billion-dollar category. Simulation is roughly a $1–2B slice. We are not claiming that slice. We can reach a few hundred AI-first robotics teams that might buy a standalone eval layer; we size that at $15–40M today, with wide error bars, and we will win or lose on a beachhead of tens, not 1,600 logos.

---

## What is wrong with the previous model

Headline you gave: TAM 1,600 companies · ICP 300 · ACV $100–400k · SAM $90M · 3-year CAGR 36.5%.
Full write-up: 90 + 240 + 170 = 500 logos · ACV $50–450k · SAM $91.0M · 2029 $340–420M.

| # | Failure | Why it dies in this room |
|---|---|---|
| 1 | **TAM is a company count** | TAM is dollars. “1,600 companies” is a logo universe. IFR itself excludes software bots, remote drones, and autonomous cars from “robot.” [IFR 2025 press deck](https://ifr.org/downloads/press_docs/PressConference2025_presentation.pdf) |
| 2 | **1,600 is unsourced** | Segment bins (60–80 / 120–150 / 180–220 / 90–110 / 1,100+) have no methodology. Public anchors disagree: IFR 944 service-robot *makers*; Tracxn 2,053 active autonomous-robotics; 45–53 humanoid OEMs — not 60–80 “embodied AI.” |
| 3 | **Architectural filter never applied** | You require neural policies / VLA / world models, then count everyone who passes a *scale* filter. Most industrial cells and many AMRs still run classical motion planning. They are not jaan buyers. |
| 4 | **ICP is three numbers** | Headline 300 · funnel 330 · SAM table 500 · `memory/company.md` ~500. An investor will notice. |
| 5 | **ACV is two ranges** | Headline $100–400k vs table $50–450k. No jaan contract exists. $450k reads as Applied-Intuition OEM pricing, not a 2-person pre-seed land. |
| 6 | **SAM = 100% of ICP × list price** | 90×$450k + 240×$175k + 170×$50k = $91M. That is a theoretical max, not SAM. No competitive loss, no in-house build, no China/export cut, no “already on Applied.” |
| 7 | **CAGR contradicts the 2029 number** | $91M → $340–420M in 3 years is **55–66% CAGR**, not 36.5%. At 36.5% for 3 years: $91M × 1.365³ ≈ **$231M**. 36.5% is also unsourced (nearest syndicated figure is MarketIntelo 38% on a *different* category). |
| 8 | **2029 double-counts growth** | 500 → 650 logos *and* blended ACV $182k → $523–646k, then labeled with 36.5%. That is company-count growth + 3× ACV expansion, not a category CAGR. |
| 9 | **Sensitivity matrix is internally inconsistent** | First row ($350k / $125k) should be 90×350 + 240×125 + 170×50 = **$70.0M**, not $68.5M. Other cells mix whether Tier 3 is included. |
| 10 | **“25%+ of senior engineer time”** | Invented. No study, survey, or customer quote. If Yaron asks for the source, the answer is “we made it up.” |
| 11 | **$5–7.5k/mo/engineer tooling** | Unsourced. Mixes GPU training spend with eval-tooling spend. Do not repeat. |
| 12 | **$220k fully loaded** | Low for US senior robotics/ML. KORE1 puts mid-to-senior ML fully loaded year-1 at $210–370k. Use as a range, not a point. [KORE1](https://www.kore1.com/cost-to-hire-ml-engineer-2026/) |
| 13 | **Category pollution** | Viam is a robot data/fleet platform, not AV. Covariant’s founders joined Amazon (Aug 2024). Boston Dynamics appears in two segments. |
| 14 | **No beachhead / SOM** | ICI is a $50M AUM pre-seed/seed fund ([CTech Jan 2026](https://www.calcalistech.com/ctechnews/article/bywlipxiwl)). They underwrite who you sell to in 24 months, not a 1,600-logo boil-the-ocean. |
| 15 | **No competitors** | Silence on Applied Intuition, NVIDIA Isaac/Cosmos, in-house stacks, Gazebo/MuJoCo, W&B, and Scale reads as naivety. |

The bottoms-up *structure* (universe → scale filter → ACV from build-vs-buy → sum) is the right shape. The execution treated every assumption as a fact and never applied the product filter.

---

## Sourced universe (inputs — never add these)

These databases overlap. **Do not sum them.**

| Universe | Number | As-of | What it is | Source |
|---|---|---|---|---|
| IFR industrial robot installations | 542,000 units; stock 4.66M | 2024 | Units, not companies. Mostly programmed arms. | [IFR WR 2025](https://ifr.org/ifr-press-releases/news/global-robot-demand-in-factories-doubles-over-10-years) |
| IFR service-robot manufacturers | **944** (80% SMEs ≤500). Sample of 293/944, not projected. | 2024/25 | Closest official “who makes service robots.” Includes many non-learned-policy firms. Excludes AV. | [IFR Service Robots 2025](https://ifr.org/img/worldrobotics/Executive_Summary_WR_2025_Service_Robots.pdf) |
| Tracxn Industrial Robotics | 2,568 / **2,302 active** / 860 funded / **438 Series A+** | Aug 2026 | Broad industrial taxonomy. | [Tracxn](https://tracxn.com/d/sectors/industrial-robotics/__8YzlIwdZtVDpzlzTadeYnqjdh1suJksuE5MDB89oZiU) |
| Tracxn Autonomous Robotics | 2,365 / **2,053 active** / 945 funded / **480 Series A+** | Aug 2026 | Closest “autonomous robots” count. Overlaps industrial + AV. | [Tracxn](https://tracxn.com/d/sectors/autonomous-robotics/__CCq4CQiwNC1b6bYQMhwu5b9O0n0hzUT3OCOfhcSHYEo) |
| Tracxn Autonomous Vehicles | 1,327 / **1,145 active** / 690 funded / **408 Series A+** | Aug 2026 | Many already buy Applied Intuition. | [Tracxn](https://tracxn.com/d/sectors/autonomous-vehicles/__lKXOKEcD9v8_QkVgJB6zssX4fym2wDECLdcAPpIfXnU) |
| Humanoid directories | **45** (humanoidintel) · **53** (RoboZaps, Jul 2026) | 2026 | Not “60–80 embodied AI.” Model labs (π, Skild) are not OEMs. | [humanoidintel](https://humanoidintel.ai/humanoid-robot-companies-complete-list/) · [RoboZaps](https://blog.robozaps.com/b/humanoid-robot-companies) |
| Robotics venture funding | **$15B** (2025) · **$18.8B YTD** (to 22 Jun 2026) | 2025–26 | Capital *into* labs, not eval-software spend. Concentrated in mega-rounds. | [Crunchbase](https://news.crunchbase.com/robotics/startup-venture-funding-surges-2026-data/) |

**Segment rewrite (INFERENCE):** “embodied AI 60–80” is high vs 45–53 humanoid OEMs and low vs “anyone training a robot policy.” AV 120–150 undercounts Tracxn’s 1,145 active AV firms and overcounts jaan-reachable buyers. AMR 180–220 and defense 90–110 are unsourced. Legacy 1,100+ looks like the leftover after forcing the total to 1,600.

---

## Rebuilt three-layer model

### A. TAM — dollar category, not logos

jaan sits in **robot / Physical-AI software**, specifically the **simulation + evaluation** slice — not hardware, not foundation-model training, not the entire “Physical AI platform.”

| Category (do not mix) | 2025 | 2026 | CAGR | Use | Source |
|---|---|---|---|---|---|
| Robotic **software platforms** | **$6.07B** | **$7.58B** | 24.93% (2026–31) to $23.07B | Broadest credible software TAM. Sim/digital-twin **26.5%** in 2025 ≈ **$1.61B**. | [Mordor](https://www.mordorintelligence.com/industry-reports/robotic-software-platforms-market) |
| Industrial robot *intelligence* software | $1.83B | $2.04B | 9.83% to 2031 | Narrower industrial slice. | [Mordor](https://www.mordorintelligence.com/industry-reports/industrial-robot-intelligence-software-market) |
| Physical AI + embodied intelligence software | $4.50B | $6.21B | **38.0%** to $67.8B (2034) | **Directional only.** Includes training, nav, HRI — not jaan’s SKU. | [MarketIntelo](https://marketintelo.com/report/physical-ai-and-embodied-intelligence-software-market) |
| Physical AI **Platform** | $0.32B | — | **47%** to $5.5B (2032) | **Different definition. Do not average with $4.50B.** | [MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/physical-ai-platform-market-11457300.html) |

**Do not give ICI a single-point TAM.** Give a range and a definition. The old “36.5% Physical AI tooling CAGR” is an unsourced blend of the 38% / 47% syndicated figures, applied to the wrong (company-count) TAM.

Applied Intuition is the existence proof that autonomy eval/sim is a real software business: official **$15B Series F / $600M** (Jun 2025), **18 of top 20 automakers**. Sacra *estimates* $830M 2025 ARR — say “Sacra estimates,” not “they do $830M.” [Applied PR](https://www.appliedintuition.com/press-releases/series-f) · [Sacra](https://sacra.com/c/applied-intuition/)

### B. SAM — who can buy a standalone eval layer

**Filter (from product, not from a census):**
1. Deploys a **learned policy** on real hardware.
2. Already spends on sim / validation (or is hitting the hardware-eval wall).
3. Can buy a **standalone** cloud eval layer (not Tesla / Amazon Robotics / Waymo-class captive).
4. Budget that can support $50k+ software (proxy: Series A+ / specialized lab).
5. Can integrate their policy for closed-loop rollouts.

| Step | Count | Status |
|---|---|---|
| Tracxn Autonomous Robotics Series A+ | **480** | FACT |
| Minus AV programs standardized on Applied / OEM toolchains | unknown unique set | Tracxn AV Series A+ = 408; intersection unpublished |
| Architectural cut: learned policy vs classical / teleop | unknown % | No public split |
| Willing to buy third-party eval | unknown % | Captive majors often build |
| **Working SAM buyer set** | **~200–350** | INFERENCE: start from 480, do not add industrial+AV, apply a ~50–70% “has a learned policy and could buy standalone” cut. Humanoid 45–53 sit *inside* this. |

**ACV (hypothesis, not realized):**

| Analog | Number | Status | Source |
|---|---|---|---|
| W&B median contract | **$47,625 / yr** (n=65); range $11k–$107k | FACT | [Vendr](https://www.vendr.com/marketplace/weights-biases) |
| W&B enterprise seats (buyer-reported) | ~$315–400 / seat / month | FACT (anecdote) | same |
| jaan year-1 land | **$50–150k** | INFERENCE | Fraction of 0.5–1.5 eval FTE, or W&B-like land. **No contracts.** |
| jaan expand | **$150–400k** | INFERENCE | Only if usage grows. Do not quote $450k as list. |

Build-vs-buy (label as hypothesis): US mid/senior ML fully loaded ~$210–370k. Two eval-adjacent FTE ≈ $0.4–0.7M before GPUs. A $50–150k eval product is a *credible fraction*. It is not evidence they will pay it.

| Case | Buyers | Blended ACV | 100% theoretical max |
|---|---|---|---|
| Conservative | 200 | $75k | **$15M** |
| Base | 250 | $100k | **$25M** |
| Stretch | 350 | $150k | **$52.5M** |

**Investor-safe SAM 2026: $15–40M** (base $25M). This replaces $91M.

**2029 (INFERENCE):** reachable buyer set 1.5–2.0× and ACV 1.3–1.5× → $25M → **~$50–75M**. Do not say $340–420M.

### C. SOM / beachhead — first 24 months

**FACT:** $0 revenue, 0 design partners, 2 founders, pre-seed (`memory/company.md`).

**Beachhead (who, not 1,600):**
- AI-first teams that already train/deploy a policy (VLA / learned manipulation / learned mobility).
- A **named real deployment site** — this is the custom-world wedge.
- English-speaking / cloud-OK GTM (US, Israel, selected EU).
- **Not** passenger-AV OEMs (Applied fortress). **Not** FANUC-style programmed cells. **Not** Amazon/Tesla/Waymo as first logos.

**24-month ambition (not a forecast):** outreach 15–30 high-fit logos · design partners 3–8 · paying 1–4 if the product works. Do not quote a 24-month ARR target.

---

## Competitors jaan must name

Differentiate only with `memory/company.md`: custom worlds matched to the **actual deployment site**, closed-loop policy rollouts, diagnostics (failures, scores, videos, trajectories). Do not claim data-engine, fleet OS, AV safety-case, or a jaan foundation model.

| Name | What they are | jaan wedge |
|---|---|---|
| **Applied Intuition** | Vehicle-intelligence toolchain. Series F $600M @ $15B. Official: 18/20 top automakers + major DoD. Sacra est. $830M 2025 ARR. Expanding into trucking, construction, mining, agriculture, defense. | They sell a *vehicle* toolchain. Year-1 beachhead is not OEM AV validation. |
| **NVIDIA Isaac / Cosmos** | Isaac Sim (Omniverse), Isaac Lab (train/eval), Isaac Lab-Arena (policy evaluation), Cosmos world models. Default stack, often free at the toolkit layer. | NVIDIA sells infrastructure and models. Our bet is a *hosted, site-matched eval layer*, not beating Isaac on physics. [Isaac Lab-Arena](https://developer.nvidia.com/isaac/lab-arena) |
| **In-house stacks** | Every serious lab has internal sim/eval. This is the real incumbent. | Buy-vs-build for *site-specific long-tail eval*, not a replacement for their training loop. Captive majors are not the beachhead. |
| **Gazebo / MuJoCo / Isaac Lab** | Open engines. | Engines, not a productized eval service that generates a customer’s site and returns a diagnostic pack. |
| **Weights & Biases** | Experiment tracking / eval *logging*. Median ACV ~$48k. | Logs runs. Does not generate site-matched worlds or closed-loop robot rollouts. Complementary. |
| **Scale** | Physical AI *data engine* (collection, annotation). Partners include Physical Intelligence; UR + Isaac Sim flywheel. | Scale industrializes demonstration data. jaan industrializes policy evaluation in custom sims. Adjacent budget line. [Scale Physical AI](https://scale.com/physical-ai) |

If asked, also: Foretellix / dSPACE / Ansys / Siemens (AV & industrial incumbents). Same rule: no invented jaan capabilities.

---

## What is still UNKNOWN

1. Unique, deduplicated count of companies that ship a learned policy *and* would buy third-party eval.
2. jaan willingness-to-pay. Zero customers. All ACVs are hypotheses.
3. Share of senior engineering time spent on sim/eval. The 25% figure is invented; no replacement study.
4. $5–7.5k/mo/engineer tooling cost.
5. What was committed in the 2026-09-10 ICI meeting (no notes in memory).
6. Whether Applied’s robotics/warehouse expansion becomes a 2027+ direct competitor.
7. Export-control / on-prem / air-gap demand. `company.md` describes a **cloud** platform.
8. Shipped product status (world-model vendor, policy API, any internal demo). Memory describes the product, not what is built.

---

## If they quote the old model back

> That 1,600 / $91M build counted companies, assumed 100% of them buy, mixed ACV bands, and implied a 55–68% SAM CAGR while citing 36.5%. We threw it out. The conservative version is a $1–2B sim-software category, a $15–40M serviceable eval wedge, and a beachhead of tens.
