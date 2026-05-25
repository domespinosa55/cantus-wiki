---
type: framework
status: active
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [prospecting, tenant-scoring, partner-scoring, six-demand-vectors, cantus-markets, v2]
related_thesis: ["[[Strategy/Cantus-Power-Sector-Thesis]]"]
related_pages: ["[[Strategy/Cantus-Business-Plan]]", "[[Strategy/Cantus-Markets]]", "[[Strategy/Power-Sector/Power-Industries]]", "[[Strategy/Cantus-Customer-Category]]", "[[Strategy/Prospecting/Cantus-Prospecting-Playbook]]"]
supersedes: ["Box v0.1 Tenant Targeting Framework", "Box v0.1 Supply Chain Tenant Framework", "Box v1.0 Partner Framework"]
---

# The Cantus Prospecting Framework v2.0

*The operational scoring system for identifying and prioritizing Cantus tenants and partners. v2.0 supersedes the v0.1 Tenant Targeting Framework, v0.1 Supply Chain Tenant Framework, and v1.0 Partner Framework — preserving their operational discipline and restructuring around the Power Sector framework v2 (10 sub-industries, four operating verticals, two Foundations).*

*Sits under the Cantus Markets vertical as the institutional discipline for sourcing and qualifying engagements across the six Power Industries demand vectors. The companion sourcing manual is [[Strategy/Prospecting/Cantus-Prospecting-Playbook]].*

---

## I. What This Framework Is

The Cantus business model depends on integrating supply and demand intelligence across the ten Power sub-industries. The Prospecting Framework is how that intelligence becomes operational at the firm level — a structured scoring discipline that converts publicly observable signals into a defensible read on which companies Cantus should engage with, at what priority, in what role, and within what timing window.

The framework scores two structurally distinct populations:

- **Tenants** — Power Industries operators that occupy a Cantus Intelligent Campus (or commission Cantus to advise on their own site selection). The demand side. Scored across the six demand vectors articulated in [[Strategy/Power-Sector/Power-Industries]].
- **Partners** — Power-sector counterparties that supply, build, equip, or capitalize the Cantus platform. The supply side. Scored across four partner classes (generation, transmission, EPC/services, equipment OEM) plus capital partners (sovereign wealth, infrastructure funds, family offices, federal program capital).

Single-sided developers see one half of every deal. Cantus is constructed to see both, and the matching of qualified demand to qualified supply is where the integrated platform monetizes. The Prospecting Framework is the discipline that makes that matching reproducible rather than founder-dependent.

The framework's anchoring claim aligns with [[Strategy/Cantus-Power-Sector-Thesis]]: the most important companies of the next decade are moving vertically across the Power stack — becoming selectively asset-heavy because control of power, machines, facilities, and software now determines strategic advantage. **The highest-value Cantus prospects are the firms executing that vertical integration**, because they need more of the integrated platform per dollar of capex than single-sub-industry operators do. This claim shapes the scoring mechanic below.

## II. The Two Scored Populations

### A. Tenants — the demand side

Tenants are Power Industries operators consuming electricity at industrial scale to produce strategic outputs. The Cantus Customer Category in [[Strategy/Cantus-Customer-Category]] articulates the unified category; the six demand vectors in [[Strategy/Power-Sector/Power-Industries]] are the canonical taxonomy. Each tenant prospect is scored under one or more of these vectors:

1. **Compute** — hyperscale AI training and inference, traditional hyperscale cloud, neoclouds, HPC, colocation customers, crypto.
2. **Supply Chain Manufacturing** — EV manufacturing, battery cell and pack assembly, heavy industrial, chemicals.
3. **Advanced Manufacturing** — semiconductor fabrication and advanced packaging, specialty chemicals, aerospace structures, robotics manufacturing, AI server assembly and burn-in.
4. **Defense Industrial Base** — munitions, missiles, drones, energetic materials, shipbuilding, large naval structures.
5. **Biomanufacturing and Critical Materials** — biopharma, bioindustrial, refined critical minerals, specialty chemicals, synthetic biology, cell therapy.
6. **Energy Transition Manufacturing** — solar PV manufacturing (ingot, wafer, cell, module), wind turbine manufacturing, hydrogen electrolyzer production, direct hydrogen production, e-fuels, direct air capture.

Important v2 change from the v0.1 framework: a firm can be (and increasingly is) scored under multiple vectors simultaneously. The v0.1 framework forced single-archetype classification; v2.0 explicitly permits and rewards multi-vector exposure (see §IV.A below).

### B. Partners — the supply side

Partners are Power-sector counterparties Cantus co-develops with, contracts from, procures from, or invests alongside. Under v2, Partners are organized by the supply-side Power sub-industries plus capital:

1. **Power Assets** partners — Generation Developers & IPPs; Transmission & Grid Developers.
2. **Power Equipment** partners — Equipment OEMs (turbines, transformers, switchgear, BESS, inverters).
3. **Power Services** partners — EPC, specialty contractors, O&M providers.
4. **Power Markets / Capital** partners — sovereign wealth, infrastructure funds, insurance-funded platforms, family offices, federal program capital. See [[Strategy/Cantus-Markets]] and [[_parameters]] Capital Partner Categories.

The Partner-side scoring discipline preserved from v1.0 carries forward intact (Delivery Capability / Strategic Alignment / Financial Strength / Regulatory Density / Commercial Flexibility) with sub-category-specific weight adjustments. See §VII below.

## III. Tenant Scoring — Standard Rubric

V2.0 replaces the v0.1 archetype-specific scoring rubrics (one for DC, one for Manufacturing, one for Supply Chain) with a **standardized four-dimension rubric applied per vector**, with vector-specific signal calibrations. The standardization makes multi-vector scoring tractable.

### Standard Tenant Scoring Dimensions

| Dimension | Weight | Core question |
|---|---|---|
| **Power Pull** | 40% | Does this firm have observable demand for Cantus-grade Power infrastructure (power, land, facilities, machines, integration)? Signals are vector-specific (see §III.B). |
| **Timing** | 25% | How proximate is the decision window? Active site search = high; budgeting cycle = medium; 36+ month horizon = low. |
| **Counterparty Strength** | 20% | Credit, contractual reliability. IG direct or look-through to IG customer concentration. |
| **Geographic & Site Fit** | 15% | Does the Cantus pipeline include candidate sites that match the firm's needs (MW envelope, water, fiber, workforce, incentives, security)? |

Each dimension is scored 0–5; the composite is the weighted sum, on the same 0–5 scale.

### A. Tier bands (preserved from v0.1)

| Composite score | Tier | Action |
|---|---|---|
| ≥ 4.0 | **A** | Immediate outreach. High conviction; 24-month decision window. |
| 3.0–3.9 | **B** | Cultivate. Strong signals on multiple dimensions; timing or fit gap to resolve. |
| 2.0–2.9 | **C** | Monitor. Quarterly revisit cadence. |
| < 2.0 | **D** | Deprioritize. Insufficient signal density. |

### B. Per-vector signal calibrations for the Power Pull dimension

The Power Pull (40%) dimension is the most vector-sensitive. Specific signals by vector:

#### Compute vector — Power Pull signals

- Cloud purchase obligations (3-year CAGR); absolute cloud spend (>$500M flags candidacy). MW heuristic: **$1B annual cloud spend ≈ 50–100 MW equivalent if repatriated**.
- Disclosed GPU procurement (10-K, 8-K, earnings call references to H100/H200/B200/GB200 orders).
- AI/ML headcount as % of engineering; R&D as % of revenue.
- MD&A mentions of "training," "inference," "GPU," "AI infrastructure," "compute capacity," "data center expansion."
- Disclosed hyperscaler / generation co-location deals (Microsoft–Constellation TMI pattern; Amazon–Talen; Meta–Calpine).
- API / inference volume disclosed in investor materials.
- Rack power density trajectory: assume **80–130 kW/rack for training-heavy**, **15–40 kW/rack for inference**, with default mix 60% inference / 40% training. **Power density has compressed in 2024–2026 with the NVIDIA roadmap and continues to escalate** — track quarterly.

#### Supply Chain Manufacturing vector — Power Pull signals

- Announced capex for new gigafactories, EV plants, battery assembly facilities.
- IRA Section 45X credits captured or modeled (battery components $35–45/kWh; solar components by part).
- IRA Section 30D / 25E vehicle credits driving downstream demand.
- FEOC compliance posture (Chinese-supply-chain exposure dictates plant location).
- Hyperscaler-supplier disclosures (EMS firms supplying AI servers — Celestica HPS, Jabil Cloud, Flex, Foxconn, Quanta, Wiwynn, Supermicro).
- Backlog and lead-time disclosures (>12 months = acute capacity expansion signal).
- Customer concentration footnote indicating hyperscaler-anchored revenue (look-through credit).

#### Advanced Manufacturing vector — Power Pull signals

- CHIPS Act Section 48D ITC announcements (25% ITC for semi manufacturing).
- CHIPS direct grants (TSMC AZ, Intel OH, Samsung TX, Micron NY/ID, GlobalFoundries NY, Wolfspeed NC/NY).
- Announced fab capex; advanced-node vs. mature-node mix.
- Domestic content compliance posture (BABA, FEOC).
- Robotics manufacturing announcements (Tesla Optimus, Figure, Apptronik, Agility, Boston Dynamics, 1X scaling).
- Aerospace structures and defense-adjacent advanced manufacturing.

#### Defense Industrial Base vector — Power Pull signals

- DPA Title III grant recipients (DoD Industrial Base Analysis and Sustainment).
- DoD multi-year procurement contracts under DFARS (munitions, missiles, drones).
- IBAS award announcements.
- New defense-tech cohort capex (Anduril, Shield AI, Saronic, Hadrian, AeroVironment, Skydio).
- Shipbuilding capacity expansion (Electric Boat, HII, Austal).
- Energetic materials and critical-component production reshoring.
- ITAR / CMMC certification posture (high-trust environment requirement).
- Security clearance workforce density and pipeline.

#### Biomanufacturing and Critical Materials vector — Power Pull signals

- BIOSECURE Act (2026 implementation) driving US-domestic CDMO buildout (Lonza, Catalent, Resilience, Samsung Biologics US, others).
- FDA inspection regime exposure (cGMP, advanced therapy MFRs).
- BARDA contract awards (biodefense-relevant manufacturing).
- DPA Title III for critical materials (lithium, cobalt, nickel, graphite, rare earths, gallium, germanium, antimony).
- DOE Critical Materials Office program participation.
- Refined-mineral capacity announcements (MP Materials, Albemarle, Arcadium, IperionX, Energy Fuels, USA Rare Earth, Westwin Elements).
- Sovereign capital pairing (Saudi PIF, Australian Future Fund, allied government partnerships).

#### Energy Transition Manufacturing vector — Power Pull signals

- IRA Section 45V hydrogen production tax credit (PTC for 10 years, $0.60–$3.00/kg by GHG intensity).
- IRA Section 45X component PTC for solar, battery, wind, critical minerals processing components.
- DOE Hydrogen Hubs program participation.
- DOE Industrial Decarbonization Hubs.
- Solar vertical integration announcements — **ingot → wafer → cell → module** capacity (Tesla, First Solar buildout, Hanwha Qcells, Meyer Burger).
- Wind turbine component manufacturing footprint expansion.
- Direct air capture commercialization (Climeworks, Heirloom, 1PointFive, Carbon Engineering, Mosaic Materials).
- E-fuels and SAF capacity announcements (HIF Global, Infinium).

### C. Standard signals for the other three dimensions

The Timing, Counterparty Strength, and Geographic & Site Fit dimensions use largely vector-agnostic signals:

#### Timing (25%)

- Active site selection underway (announced or disclosed)
- Budgeting cycle position (capex authorization completed vs. pending)
- Board-level capital project approval
- Existing facility expansion or relocation triggers
- Lease expiration or major contract renewal triggers
- Federal program capital deployment timing (LPO, DPA, CHIPS)

#### Counterparty Strength (20%)

- S&P / Moody's / Fitch issuer credit rating
- For private firms: parent support, capital structure, sponsor equity
- Customer concentration look-through (e.g., EMS firm with IG hyperscaler customer revenue)
- Free cash flow coverage for 10–15 year commitments
- Federal-program-backed financing capacity (DOE LPO loan guarantees, DPA Title III)

#### Geographic & Site Fit (15%)

- Match to Cantus pipeline sites (ERCOT primary; PJM, MISO, Western, Southeast as extension)
- MW envelope match to candidate Cantus parcels
- Water-intensity match (semi 3–10 MGD; battery 1–3 MGD; pharma 0.5–2 MGD)
- Workforce density and skilled-labor radius
- Logistics requirements (rail, port, interstate)
- Sustainability and regulatory environment fit
- Security or clearance environment match (for defense, biopharma, critical materials)

## IV. Two v2-Native Multipliers

The base score (§III) captures vector-specific demand and standard counterparty/fit dimensions. V2.0 adds two firm-level multipliers that reflect strategic observations from the Power Sector Thesis.

### A. Multi-Vector Exposure Multiplier

A firm scoring under multiple demand vectors needs more of the Cantus integrated platform than a single-vector operator. Tesla (Compute via Dojo + Supply Chain Manufacturing via gigafactories + Energy Transition Manufacturing via solar vertical integration) is the canonical case. NVIDIA-customer hyperscalers spanning training and inference and proprietary silicon manufacturing are another.

| Vectors scored ≥3.0 (Tier C or better) | Multiplier |
|---|---|
| 1 vector | 1.00 |
| 2 vectors | 1.10 |
| 3 vectors | 1.20 |
| 4+ vectors | 1.30 |

Apply the multiplier to the highest-scoring primary vector. The result is the firm's **Composite Tenant Score**. A Tier B (3.5) under one vector who also scores Tier C (2.5) under a second vector becomes 3.5 × 1.10 = 3.85 — still Tier B but closer to A. A firm with three Tier B scores becomes a structural Tier A even if no single vector clears the bar.

### B. Vertical-Integration Trajectory Multiplier

The thesis observation: frontier companies are becoming selectively asset-heavy because control of power, machines, facilities, and software determines strategic advantage. Firms executing that vertical integration across the Power stack are structurally higher-value Cantus prospects.

| Vertical-integration posture | Multiplier |
|---|---|
| Not vertically integrating (pure operator) | 1.00 |
| Stated strategy to vertically integrate, no execution yet | 1.05 |
| Active vertical integration in 2–3 sub-industries | 1.15 |
| Aggressive vertical integration across 4+ sub-industries | 1.25 |

Signals of vertical integration:

- Owns or is acquiring generation (Microsoft–Constellation TMI; Amazon–Talen; Meta–Calpine)
- Manufactures or commissions captive Machines (Google TPU, AWS Trainium, Microsoft MAIA, Meta MTIA, Apple M-series, Tesla Dojo + Optimus)
- Builds proprietary Facilities at scale (hyperscaler self-developed data halls; Tesla gigafactories)
- Operates owned Land aggregation teams (hyperscaler direct site assemblers)
- Operates direct PPA and capital teams (large hyperscalers; Crusoe; Constellation customer side)
- Operates software platform vertically integrated with hardware (NVIDIA CUDA; Tesla full-stack; Anduril Lattice)

### C. Composite formula

```
Composite Tenant Score = Primary Vector Score × Multi-Vector Multiplier × Vertical-Integration Multiplier
```

Tier banding applies to the Composite, not the base. The multipliers can push a Tier B firm into Tier A (and vice versa, though that direction is bounded since multipliers are ≥1.0).

## V. MW Translation Heuristics by Vector

Updated for the 2024–2026 power-density escalation and the Celestica calibration:

### Compute vector

| Workload class | Density |
|---|---|
| Hyperscale AI training (B200/GB200 era) | **100–150 kW/rack** (revised up from v0.1 80–130 kW) |
| Hyperscale AI training (legacy H100/H200) | 70–100 kW/rack |
| AI inference | 20–50 kW/rack (revised up from v0.1 15–40 kW) |
| Traditional cloud / enterprise IT | 8–20 kW/rack |
| Crypto mining (interruptible) | 12–30 kW/rack |

Cloud-spend-to-MW translation: $1B annual cloud spend ≈ **50–100 MW** if repatriated as mixed training/inference; **75–150 MW** if heavily training-tilted.

### Supply Chain Manufacturing vector

| Sub-segment | MW per facility |
|---|---|
| Battery cell gigafactory | 30 GWh nameplate → **80–150 MW** load |
| EV assembly | **30–100 MW** |
| EMS / AI server assembly + burn-in | **40–300+ MW** ← *revised up significantly from v0.1 40–120 MW per Celestica engagement reality; burn-in testing power scales with GPU TDP* |
| Heavy industrial (steel arc, aluminum, chemical) | 50–500 MW |

### Advanced Manufacturing vector

| Sub-segment | MW per facility |
|---|---|
| Semiconductor fab (leading edge, ~3nm) | **200–500 MW** |
| Semiconductor fab (mature node) | 80–200 MW |
| Advanced packaging | 30–80 MW |
| Aerospace structures | 20–60 MW |
| Robotics manufacturing | 30–120 MW |

### Defense Industrial Base vector

| Sub-segment | MW per facility |
|---|---|
| Munitions / energetic materials | 20–80 MW |
| Missile / drone production | 15–60 MW |
| Shipbuilding | 50–200 MW |
| Defense electronics | 30–100 MW |

### Biomanufacturing and Critical Materials vector

| Sub-segment | MW per facility |
|---|---|
| Biopharma large-molecule | 30–80 MW |
| CDMO fill-finish | 15–50 MW |
| Critical minerals processing (Li, Co, Ni, graphite, REE) | 50–200 MW |
| Specialty chemical processing | 30–150 MW |

### Energy Transition Manufacturing vector

| Sub-segment | MW per facility |
|---|---|
| Solar PV manufacturing (cell + module, US, 45X-supported) | 50–150 MW per GW capacity |
| Solar vertical integration (ingot + wafer + cell + module, full stack) | **300–1,000+ MW** ← *Tesla solar engagement scale* |
| Wind turbine component manufacturing | 30–100 MW |
| Hydrogen electrolysis production (1 GW capacity) | 200–500 MW continuous load |
| Direct air capture (commercial scale) | 50–200 MW |
| E-fuels / SAF | 100–400 MW |

## VI. Calibration Anchors

Two current Cantus engagements anchor the v2.0 framework. The framework was developed in part to fit these engagements; ongoing scoring should be validated against them.

### A. Tesla — multi-vector vertical integrator (the canonical case)

Tesla scores under multiple demand vectors simultaneously:

| Vector | Tesla activity | Score range |
|---|---|---|
| Compute | Dojo training, Optimus inference, FSD inference at scale | 3.5–4.0 |
| Supply Chain Manufacturing | Gigafactories (Austin, Reno, Berlin, Shanghai) | 4.0–4.5 |
| Advanced Manufacturing | Robotics manufacturing (Optimus production lines) | 3.5–4.0 |
| **Energy Transition Manufacturing** | **Solar vertical integration: ingot → wafer → cell → panel. Gigawatts of power demand. *Current Cantus engagement.*** | **4.5–5.0** |

Primary vector (highest score): Energy Transition Manufacturing at 4.5–5.0 (Tier A).
Multi-Vector Multiplier: 1.30 (4+ vectors at Tier C or better).
Vertical-Integration Trajectory: 1.25 (aggressive vertical integration across 4+ sub-industries — owns generation infrastructure via Megapack deployment + Facilities + Machines + Software via Tesla full-stack).

**Composite Tenant Score (Tesla)**: 4.75 × 1.30 × 1.25 = **7.7 normalized → Tier A++ (cap at 5.0, the firm is structurally a Tier A anchor across the portfolio).**

The v0.1 framework scored Tesla at 3.9 (Tier B, 150–300 MW) under the Compute archetype alone — missing the solar engagement entirely. The v2.0 mechanic surfaces the actual firm-level strategic position.

### B. Celestica — Supply Chain Manufacturing Tier A near-term (with updated power density)

Celestica was scored 4.4 (Tier A) under the v0.1 Supply Chain Framework with a 50–100 MW estimate. The current Cantus engagement is **300+ MW for AI server assembly and burn-in testing** — 3–6x the v0.1 estimate.

| Vector | Celestica activity | Score range |
|---|---|---|
| Supply Chain Manufacturing | HPS segment: AI server assembly + burn-in testing | **4.5–5.0** |
| Compute | Adjacent / customer-facing only | 1.0–2.0 |

Primary vector: Supply Chain Manufacturing at 4.5–5.0 (Tier A).
Multi-Vector Multiplier: 1.00 (effectively single-vector).
Vertical-Integration Trajectory: 1.05 (stated co-location strategy, growing AI infrastructure positioning).

**Composite Tenant Score (Celestica)**: 4.75 × 1.00 × 1.05 = **4.99 → Tier A.**

MW reality: 300+ MW per facility, driven by power-density compression from H100 (~700W) to B200 (~1000W) and the burn-in testing requirement to draw rated power across the entire GPU population being qualified. The v0.1 MW table (40–120 MW for EMS) understated the current power-density profile; the v2.0 table above (40–300+ MW for EMS / AI server assembly + burn-in) reflects the engagement reality.

### C. What the calibration anchors imply

- The Tesla anchor implies multi-vector multipliers materially change firm rankings. Any prospect operating across three or more demand vectors is structurally a Tier A even if individual vector scores are mid-B.
- The Celestica anchor implies the supply-chain manufacturing power-density assumption needs to **track the NVIDIA roadmap quarterly**. Power density for AI-adjacent manufacturing is a leading indicator, not a static parameter. See [[Strategy/Prospecting/Cantus-Prospecting-Playbook]] §III for the NVIDIA / GPU power-density signal tracker.
- Both anchors imply the Power Pull dimension's signal set is the most time-sensitive component of the framework. Other dimensions (Counterparty Strength, Geographic Fit) are more stable.

## VII. Partner Scoring — Preserved with v2 Restructure

The Partner Framework v1.0 scoring discipline is preserved intact, restructured around v2 sub-industries:

### Standard Partner Scoring Dimensions

| Dimension | Default weight | Core question |
|---|---|---|
| Delivery Capability | 25% | Can this partner deliver at the scale, quality, and pace Cantus requires? |
| Strategic Alignment | 20% | Does the partner's strategy align with Cantus's geographies, technologies, timeline? |
| Financial & Counterparty Strength | 20% | Balance sheet, credit, bonding capacity, long-tenor durability. |
| Regulatory & Relationship Density | 20% | Working relationships with utilities, ISOs, regulators, permitting bodies. |
| Commercial Terms & Flexibility | 15% | Pricing posture, structure creativity, co-investment openness. |

Same 0–5 scoring, same Tier A/B/C/D bands.

### Partner Sub-Categories (mapped to v2 Power sub-industries)

| Partner sub-category | Maps to v2 sub-industry | Reweighted dimensions |
|---|---|---|
| Generation Developers & IPPs | Power Assets | Delivery 30% / Strategic 20% / Financial 20% / Regulatory 15% / Commercial 15% |
| Transmission & Grid Developers | Power Assets (transmission) | Delivery 30% / Strategic 15% / Financial 20% / Regulatory 25% / Commercial 10% |
| Equipment OEMs (turbines, transformers, switchgear, BESS) | Power Equipment | Delivery 35% / Strategic 20% / Financial 15% / Regulatory 10% / Commercial 20% |
| Machine OEMs (GPUs, semi equipment, robotics, electrolyzers, bioreactors) | Power Machines | Delivery 30% / Strategic 25% / Financial 15% / Regulatory 10% / Commercial 20% |
| EPC & Construction Partners | Power Services | Delivery 35% / Strategic 15% / Financial 20% / Regulatory 10% / Commercial 20% |
| Specialty Mission-Critical Consultants | Power Services | Delivery 30% / Strategic 20% / Financial 10% / Regulatory 10% / Commercial 30% |
| Capital Partners | Power Markets (Capital sub-segment) | See [[Strategy/Cantus-Markets]] Capital Partner Categories for separate evaluation rubric |

**New in v2.0:** Machine OEMs (NVIDIA, AMD, ASML, robotics primaries, bioprocessing cohort, electrolysis cohort) are now a partner sub-category. The v1.0 framework had no Machine OEM scoring because v1 didn't recognize Power Machines as a distinct sub-industry. Today, **NVIDIA is the most strategically consequential single Machine OEM relationship for Cantus** and should be scored as Tier A even though it's not yet captured in [[_parameters]] Strategic OEM Relationships. This is one of the framework's immediate outputs.

### Reference Partner Cohort

| Sub-category | Reference partners |
|---|---|
| Generation IPPs | NextEra, Vistra, Constellation, Talen, AES, RWE, Engie, Invenergy, EDP, Pattern, Calpine |
| Transmission | Pattern Energy, Grain Belt Express, Invenergy Transmission, NextEra Energy Transmission, Berkshire Hathaway Energy Transmission; Oncor, CenterPoint, AEP (ERCOT) |
| Equipment OEMs (Power Equipment) | GE Vernova, Siemens Energy, Mitsubishi Power, Caterpillar, Cummins, Wärtsilä, Baker Hughes, Solar Turbines, Kawasaki, Doosan, Hitachi Energy, Hyundai HD, Prolec GE, ABB, Schneider, Tesla, Fluence, Powin |
| Machine OEMs (Power Machines) | **NVIDIA (priority gap)**, AMD, Intel, ASML, Applied Materials, Lam, KLA, Tokyo Electron, Wuxi Lead, DÜRR, Schuler, Sartorius, Cytiva, Thermo Fisher, ABB Robotics, FANUC, KUKA, Yaskawa, Tesla (Optimus + Dojo), Figure, Apptronik, Plug Power, NEL, Nucera, Bloom |
| EPC & Construction | Bechtel, Fluor, Black & Veatch, Burns & McDonnell, Kiewit, Zachry, Quanta, MasTec, MYR Group, Primoris, Mortenson, Holder, DPR, Whiting-Turner, Skanska USA |
| Mission-Critical Consultants | HDR, kW Mission Critical, Syska Hennessy, Burns & McDonnell consulting |

## VIII. Integrated Supply–Demand Matching

The Tenant Framework identifies who absorbs Cantus's powered land. The Partner Framework identifies who Cantus builds it with. The value comes from the integration. For any active Cantus site engagement, the matching exercise asks:

1. **What is the tenant configuration?** Single hyperscale anchor (400 MW+)? Multi-tenant Intelligent Campus (anchor + 2–4 supply chain manufacturers + 1 advanced manufacturer)? Specialty sovereign or defense configuration?
2. **What generation and infrastructure stack does that configuration require?** 24/7 baseload? Renewables + storage? Behind-the-meter bridge? Grid-tied? Mixed?
3. **Which Tier A Partners are aligned with that configuration?** Cross-reference §VII partner scoring against the technology and timing needs.
4. **Where do relationship paths already exist?** Newmark + Cantus + founder networks. Where do new introductions need to be built?

### Three integrated-matching use cases (preserved from Partner Framework v1.0, restated under v2)

**Use case 1 — Hyperscaler Anchor + ERCOT Site (400 MW).** Tenant: Tier A hyperscaler under Compute vector (OpenAI / Anthropic / Meta / xAI / Oracle / CoreWeave). Generation: Vistra (ERCOT-native commercial flexibility + gas baseload). EPC: Quanta or Kiewit for transmission + substation. Equipment OEMs: GE Vernova or Mitsubishi Power for turbines; Hitachi Energy or Siemens for substation transformers. Machine OEMs: NVIDIA for GPU layer (direct hyperscaler procurement, but Cantus coordinates installation timing). Capital: Brookfield / BlackRock-GIP / Stonepeak for principal positions; strategic corporate LP from the hyperscaler.

**Use case 2 — Multi-tenant Intelligent Campus (500 MW).** Anchor: AI compute tenant (300 MW). Co-tenants: one Energy Transition Manufacturing tenant (solar — 100 MW), one Supply Chain Manufacturing tenant (EMS / AI server assembly — 50 MW, scaling up with NVIDIA roadmap), one Defense Industrial Base tenant (drone production — 50 MW). Generation: BTM gas bridge from Cantus Infrastructure (Caterpillar or Wärtsilä reciprocating + Mitsubishi or GE Vernova aeroderivative) plus grid-tied solar + BESS. EPC: Burns & McDonnell engineering; Mortenson or Holder for facility build; Rosendin or Sundt for specialty trades. Workforce: Texas A&M + UT + Texas Tech R1 partnerships; IBEW JATC pipeline; Labor/Community Foundation orchestration. Capital: Fund I principal positions + DOE LPO + Texas Energy Fund.

**Use case 3 — Solar Vertical Integration (Tesla / equivalent, 800 MW).** Tenant: Energy Transition Manufacturing vertical integrator, full ingot-to-panel stack. Generation: substantial owned solar buildout co-located (where the operator itself becomes a hybrid Power Assets + Power Industries entity); grid-tied complement for non-daylight load. Equipment OEMs: Centrotherm + Schmid + Despatch for solar manufacturing equipment; specialty wafer/ingot equipment; Tesla Megapack for BESS. EPC: Mortenson or Burns & McDonnell. Capital: IRA 45X anchor + DOE LPO for facility + strategic corporate Tesla balance sheet.

## IX. Tier-A Initial Outreach Roster

Drawn from the calibrated v2.0 framework. To be expanded and re-scored quarterly.

### Tenants — Tier A by vector (illustrative; analyst-scored, not committed)

| Vector | Tier A prospects |
|---|---|
| Compute | OpenAI (4.8), Anthropic (4.7), Meta (4.7), xAI (4.5), Oracle (4.4), Microsoft Azure, AWS, Google Cloud (multi-vector + vertical-integration multipliers push to Tier A++) |
| Supply Chain Manufacturing | Tesla (cross-vector anchor), LG Energy Solution, SK On, Panasonic, Samsung SDI, Celestica (active engagement, 300+ MW), Jabil Cloud, Foxconn (active relationship), Quanta, Wiwynn |
| Advanced Manufacturing | Samsung Taylor (4.9), TSMC US (4.8), Intel Foundry (4.4), Micron (4.3), Wolfspeed (4.0), GlobalFoundries, T1 Energy (active engagement) |
| Defense Industrial Base | Anduril (rapidly scaling), Lockheed Martin, Raytheon, Northrop Grumman, General Dynamics, HII, Shield AI, Saronic, Hadrian |
| Biomanufacturing / Critical Materials | Eli Lilly, Merck, Pfizer, Moderna, Lonza, Catalent, Resilience, MP Materials, Albemarle, Arcadium Lithium, IperionX, USA Rare Earth |
| Energy Transition Manufacturing | Tesla (active engagement, ~800 MW solar buildout), First Solar, Plug Power, Air Products, Linde, Bloom Energy, 1PointFive |

### Partners — Tier A by sub-category (illustrative)

| Sub-category | Tier A partners |
|---|---|
| Generation IPPs | NextEra, Vistra, Constellation, Talen, AES |
| Transmission (ERCOT) | Oncor, CenterPoint (active C-suite engagement), AEP |
| Power Equipment OEMs | GE Vernova, Mitsubishi Power, Siemens Energy, Caterpillar, Cummins, Wärtsilä, Hitachi Energy, ABB, Tesla (Megapack), Fluence |
| Power Machines OEMs | **NVIDIA (priority gap — corporate-level relationship needed)**, AMD, ASML, Sartorius, ABB Robotics, FANUC |
| EPC | Bechtel, Kiewit, Quanta, Mortenson, Burns & McDonnell, Black & Veatch, Holder, DPR |
| Capital Partners | Blue Owl (active relationship), Brookfield, BlackRock-GIP, Stonepeak, KKR, IFM, sovereign wealth (PIF, GIC, NBIM, Mubadala) |

## X. How to Operate the Framework

1. **Quarterly scoring refresh.** Every 90 days, the active pipeline plus the Tier A prospect list gets re-scored. Power Pull signals are most volatile and drive most score changes.
2. **Tier A immediate outreach.** Within 30 days of identification, outreach is initiated. Tier A is binding on the firm's calendar.
3. **Tier B cultivation cadence.** Quarterly check-in; signal-tracking via CII data assets.
4. **Tier C monitor.** Semi-annual review; pulled into Tier B only on a material signal shift.
5. **Tier D deprioritize.** Removed from active tracking unless a category-level shift surfaces them.
6. **Multi-vector firms get cross-arm engagement.** A Tier A firm scoring under three or more vectors is managed by the Cantus Markets vertical with explicit coordination across Cantus Development (site fit), Cantus Infrastructure (power program), and Cantus Technology (machines and software).
7. **Calibration runs against active engagements.** Every Tier A engagement Cantus closes (Tesla, Celestica, future) gets a calibration write-up that updates the framework's signal calibrations and MW heuristics.

## XI. Cross-References

| Page | Relationship |
|---|---|
| [[Strategy/Cantus-Power-Sector-Thesis]] | Foundational thesis anchor; the multi-vector + vertical-integration multipliers operationalize the "frontier company becoming selectively asset-heavy" claim |
| [[Strategy/Cantus-Business-Plan]] | The Prospecting Framework operates inside the firm's Building / Activation / Compounding phasing |
| [[Strategy/Cantus-Markets]] | Operating vertical that runs the Prospecting Framework |
| [[Strategy/Power-Sector/Power-Industries]] | Canonical taxonomy of the six demand vectors |
| [[Strategy/Cantus-Customer-Category]] | Customer category articulation; Two Customer Stacks as Tier-1 simplification |
| [[Strategy/Prospecting/Cantus-Prospecting-Playbook]] | Operational sourcing manual; where each signal comes from |
| [[Products/CII-Iteration-Document]] | Tenant + Capital data asset families feed and consume framework outputs |
| [[Strategy/Foundations/CII-DealOS-Foundation]] | Prospect Tracker as a CII data asset compounds across the firm |
| [[_parameters]] | Tenant Power Price Tolerance Spectrum; Capital Partner Categories; OEM relationships; active pipeline projects |

## XII. Open Questions

To resolve through iteration:

- **NVIDIA strategic relationship architecture.** Most consequential Machine OEM relationship for Cantus; priority gap in [[_parameters]] Strategic OEM Relationships. Should be elevated to corporate-level relationship inside Cantus Technology.
- **Multi-vector score weighting curve.** The current multiplier curve (1.00 / 1.10 / 1.20 / 1.30) is a first calibration. After 2–3 quarters of scoring runs, the curve may need re-fitting against observed outcomes.
- **Vertical-integration signal automation.** Hand-scoring the integration trajectory across each prospect is analyst-intensive. CII / DealOS Foundation should automate the signal harvesting (announced vertical-integration moves, generation acquisitions, captive silicon, vertical software stacks).
- **Sovereign Compute prospect class.** Foreign-government / sovereign-wealth-backed compute deployments are emerging (Saudi, UAE, Korea, India). Currently under-scored in the v2.0 framework. May need its own vector or a calibration overlay on Compute vector.
- **Workforce-and-Community Foundation as a Tier-A enabler.** PWA compliance and skilled-labor pipeline can disqualify a high-scoring tenant for a specific site. The framework should explicitly flag Labor/Community readiness alongside the Geographic & Site Fit dimension.
- **Cantus Compute self-tenant treatment.** When Cantus Compute (selective operator inside Cantus Technology vertical) occupies a Cantus campus, the firm is both Partner (Cantus operating business) and Tenant (campus occupier). The framework should specify how this internal counterparty is scored or excluded.

## XIII. Closing

The Prospecting Framework v2.0 is the institutional discipline by which Cantus turns the Power Sector thesis into specific client engagements. The framework is operational; the scoring is reproducible; the calibration anchors (Tesla, Celestica) make it concrete. The intent is that any analyst inside Cantus can apply the framework to a candidate firm and arrive at the same tier within a half-point band.

The framework lives inside the Cantus Markets vertical and is consumed by every operating vertical. Cantus Development uses it to know which tenants fit which sites. Cantus Infrastructure uses it to align supply-side OEM and EPC relationships against tenant cohorts. Cantus Technology uses it to time Machine procurement and Cantus Compute deployment. Cantus Markets runs it as the firm's institutional process.

The compounding asset is the data: every prospect scored, every engagement closed, every calibration run improves the firm's read on the next prospect. That compounding sits in the CII/DealOS Foundation. The framework is the structured prompt; CII is the memory.

---

> *Single-sided developers see one half of every deal. Cantus sees both, and the integrated supply-demand matching is where the integrated platform monetizes.*

*Operational scoring system, v2.0 canonical. Anchored to the Cantus Power Sector Thesis. Companion sourcing manual: [[Strategy/Prospecting/Cantus-Prospecting-Playbook]]. Author of record: Dom Espinosa.*
