---
type: framework
status: drafting
audience: internal
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [power-sector, sub-industry, power-industries, cantus-markets]
sub_industry: power_industries
sub_industry_index: 7
related_thesis: ["[[Strategy/Cantus-Framework]]", "[[Strategy/Cantus-Customer-Category]]"]
related_pages: ["[[Strategy/Power-Sector/Power-Facilities]]", "[[Strategy/Power-Sector/Power-Machines]]", "[[Strategy/Power-Sector/Power-Commodities]]"]
---

# Power Industries — Sub-Industry Specification

*Sub-industry 7 of 10 in the Power sector framework v2. Drafting. Narrowed to the operator-only definition; Facility content is now in [[Strategy/Power-Sector/Power-Facilities]] and Machine content in [[Strategy/Power-Sector/Power-Machines]]. Cantus Markets is the operating vertical for this sub-industry.*

---

## 1. Definition

Power Industries is the **operator** sub-industry — the demand-side firms that consume electricity at industrial scale, operate Power Facilities, run Power Machines, and produce strategic outputs that become Power Commodities. The unit of production is the operating enterprise itself: Microsoft running Azure AI infrastructure, TSMC running fabs, Tesla running gigafactories, Anduril running munitions and drone production, Lilly running biopharma manufacturing. The defining condition is operational control of the industrial process that converts power into output, regardless of whether the operator owns the Facility, the Machines, or the Land underneath.

The boundary against adjacent Power sub-industries:

- **Power Facilities** is the constructed building or campus. Power Industries is the *operator* of the industrial process inside the building. Same firm can own both layers (Microsoft owns the data hall + runs Azure), but they are different deliverables on different counterparty stacks. A BTS-leased hyperscale facility is a Power Facility owned by Aligned or Vantage; the workload running inside is the Power Industries operation by Microsoft or AWS.
- **Power Machines** is the productive equipment installed in the Facility. Industries operates the Machines; it does not manufacture them. TSMC is Industries; ASML is Power Machines.
- **Power Commodities** is the output the operator produces (chips, cells, compute capacity, refined critical minerals, biologics, munitions). Industries is the operator; Commodities is what flows out the door for sale or for captive use.
- **Power Land** is the substrate. Industries operates on it.
- **Power Markets** (under the v2 broad-allocation framing) is the layer that finances and commercializes the operator's output. Cantus Markets vertical contains Industries, Commodities, and Markets-broad together, because the value chain from operator → output → commercialization runs through one vertical.

The boundary against the **broader industrial economy** is structural rather than nominal. Many industries consume power. Power Industries is the cohort for whom power has become the binding operating constraint, the primary site-selection driver, and the dominant capital-allocation question. Empirical threshold: 50MW+ sustained continuous load. Beneath that threshold, the firm is a standard industrial operator with power as a routine input.

### The six demand vectors

Power Industries comprises six structurally distinct demand vectors. Each has its own operator profile, capital structure, regulatory regime, and counterparty universe. The framework treats the six vectors as the canonical taxonomy of the customer category; the Two Customer Stacks framing in [[Strategy/Cantus-Customer-Category]] is the Tier-1 simplification of vectors 1 and 2 plus elements of 3 and 4.

1. **Compute** — hyperscale AI training and inference, traditional hyperscale cloud, HPC, colocation customer base, crypto mining (interruptible).
2. **Supply chain manufacturing** — EV manufacturing, battery cell and pack assembly, heavy industrial (steel, aluminum), chemicals, petrochemicals.
3. **Energy transition manufacturing** — solar PV operating, wind turbine operating-side, hydrogen production operations, e-fuels production, direct air capture operations.
4. **Advanced manufacturing** — semiconductor fabrication, advanced packaging, specialty chemicals, aerospace structures manufacturing, robotics manufacturing.
5. **Defense industrial base** — munitions production, missile production, energetic materials, ship and submarine production, aircraft, drones, large naval structures.
6. **Biomanufacturing and critical materials** — biopharma manufacturing, bioindustrial, refined critical minerals processing, specialty chemical processing, synthetic biology, cell therapy manufacturing.

## 2. Deliverables

Power Industries does not produce a single homogeneous deliverable. The operator's deliverable is the operating enterprise itself; the financial and operational measures by which that enterprise is evaluated are:

**Operational capability** — running an industrial process at design capacity, with the trained workforce, the supply chain, the certifications, and the commercial relationships required for sustained production.

**Output throughput** — the volumetric performance of the operator's industrial process: tokens generated, GPUs operated, wafers produced, cells assembled, missiles produced, vials shipped. The output volume is what becomes Power Commodities or captive consumption.

**Sustained load profile** — the power-consumption envelope the operator presents to the grid: peak MW, average MW, capacity factor, ramp behavior, interruptibility, time-of-use pattern. This is itself a deliverable in the sense that the grid, capital partners, and the Facility owner underwrite against it.

**Tenant covenant strength** — the credit, contractual reliability, and operational covenant the operator brings as a counterparty to ground lease, build-to-suit lease, PPA, tolling, equipment supply, and service agreements. Tenant covenant is the primary input to Power Land underwriting and to Power Facilities lease pricing.

The contractual instruments by which Power Industries transacts with the rest of the Power sector: ground lease or build-to-suit lease with Power Land and Power Facilities; PPA, tolling agreement, or behind-the-meter offtake with Power Assets; equipment supply with Power Equipment; machine supply with Power Machines; EPC and O&M with Power Services; capital with Power Markets (the now-broad allocation sub-industry); commodity offtake with Power Commodities; software and data services with Power Technology.

## 3. Major Players (US-Focused)

### Compute — hyperscale AI

Microsoft (Azure + OpenAI infrastructure); Amazon AWS (also Anthropic infrastructure); Google Cloud / Alphabet; Meta (Llama infrastructure); xAI (Colossus in Memphis); Oracle Cloud Infrastructure; CoreWeave; Lambda Labs; Crusoe (vertically integrated with generation); IREN; Applied Digital; Hut 8.

Nebius is named in [[_parameters]] as pre-approved cooperating broker on Project Joule.

### Compute — hyperscale traditional cloud

AWS, Microsoft Azure, Google Cloud, Oracle Cloud, IBM Cloud. Overlapping operators with the AI cohort; the power profile of traditional cloud workloads differs (lower density, less ramp, higher mix of inference and storage).

### Compute — colocation customer base

Equinix and Digital Realty are typically *Power Facilities* operators rather than the demand-side operator; their colocation customers are the actual Power Industries operators using the space. The Cantus framework convention places the colocation customer (the financial firm running its trading infrastructure, the enterprise running its IT, the AI company renting AI compute capacity) in Power Industries; the colo facility itself is Power Facilities.

### Compute — crypto (interruptible class)

Marathon Digital, Riot Platforms, CleanSpark, Hut 8, Bitfarms, Cipher Mining. Per [[_parameters]] tenant tolerance, crypto operates at $30–45/MWh with 60–80% of OpEx as power. Interruptibility makes this cohort a distinct sub-class with different campus economics.

### Supply chain manufacturing — EV operators

Tesla (Austin, Reno, Berlin, Shanghai); Ford (Michigan, Tennessee BlueOval City); GM (Michigan, Tennessee, Ohio); Rivian (Illinois, Georgia announced); Lucid (Arizona); Hyundai (Georgia Metaplant); Toyota (Kentucky, Tennessee, North Carolina).

Tesla and Foxconn are named in [[_parameters]] as long-standing Cantus customer relationships.

### Supply chain manufacturing — battery cell operators

LG Energy Solution; Samsung SDI; SK On; Panasonic; CATL (limited US, FEOC-restricted); BYD (limited US, FEOC-restricted); domestic-only ventures.

### Supply chain manufacturing — heavy industrial

Nucor, Steel Dynamics, Cleveland-Cliffs, US Steel (Nippon Steel acquisition pending) — steel; Alcoa, Century Aluminum — aluminum; Dow, BASF, LyondellBasell, Eastman Chemical — chemicals; Cemex, Holcim, Eagle Materials — cement.

### Energy transition manufacturing — operators

Solar production: First Solar, Hanwha Qcells, Maxeon, Meyer Burger (distressed). Wind turbine operating-side: GE Vernova, Vestas, Siemens Gamesa. Hydrogen production: Air Products, Linde, Plug Power, ExxonMobil (Baytown blue H2), Chevron, BP. Direct air capture: Climeworks, Heirloom, 1PointFive. E-fuels / SAF: HIF Global, Infinium.

### Advanced manufacturing — semiconductor operators

TSMC (Arizona); Intel (Ohio Silicon Heartland, Arizona, New Mexico); Samsung (Texas Austin + Taylor); Micron (NY, ID); GlobalFoundries (NY Malta); Texas Instruments (Texas Sherman, Utah Lehi); Wolfspeed (NC, NY Mohawk Valley); Onsemi (Vermont, NH); Analog Devices.

T1 Energy is named in [[_parameters]] as active engagement and analyzed pipeline.

### Advanced manufacturing — other

Boeing, Lockheed Martin, Northrop Grumman (aerospace structures); Raytheon RTX; Hadrian (advanced manufacturing services); robotics manufacturing operators (Boston Dynamics, Agility Robotics, Apptronik, Figure).

### Defense industrial base

Lockheed Martin; Raytheon RTX; Northrop Grumman; General Dynamics; Boeing Defense, Space and Security; BAE Systems Inc.; HII; L3Harris; Anduril (rapidly scaling); Shield AI; AeroVironment; Palantir (software but defense-platform-adjacent); Hadrian; Saronic and Saildrone (maritime autonomy).

### Biomanufacturing and critical materials — biopharma operators

Eli Lilly; Merck; Pfizer; Moderna; Novavax; Catalent; Lonza; Resilience; Samsung Biologics (planned US); WuXi Biologics and WuXi AppTec (CFIUS and BIOSECURE Act-sensitive).

### Critical minerals operators

MP Materials; Albemarle; Arcadium Lithium; IperionX; Energy Fuels; USA Rare Earth; Westwin Elements; Lynas Rare Earths (Texas project).

### Cross-vector platforms

Several entities operate across multiple vectors and complicate clean classification: Tesla (EV + battery + storage + compute via Dojo), Crusoe (compute + generation), Constellation (Power Assets + hydrogen + co-located AI offtake). The convention is to classify at the business-unit level (the Tesla compute business is Compute-vector; the Tesla gigafactory is Supply Chain Manufacturing-vector) rather than at corporate level.

## 4. Capital Structures and Economics

Power Industries does not have a single capital-structure pattern. The six demand vectors operate with distinct capital architectures, tax-and-incentive frameworks, and return profiles. The unifying feature is that all six absorb very large capital relative to broader industrial norms, and that capital architecture for the operator increasingly intersects with industrial policy.

### Operator capital architecture by vector

**Hyperscale compute operators** — corporate balance sheet at Microsoft, Amazon, Google, Meta, Oracle. CoreWeave, Crusoe, and the smaller AI compute cohort use a mix of venture capital, infrastructure debt, vendor financing (NVIDIA paper), and structured asset-level finance. Hyperscaler operator capex commitments running $200B+/year across the top six firms.

**Semiconductor fab operators** — corporate equity + CHIPS Act grants + Section 48D Advanced Manufacturing Investment Credit (25% ITC) + Treasury direct-pay election.

**Battery manufacturing operators** — sponsor equity (typically a strategic OEM JV) + IRA Section 45X credits + DOE LPO loans + state incentive packages. Some plants are nearly fully credit-financed once 45X credits are factored.

**Energy transition manufacturing operators** — IRA 45X (component-by-component for solar wafers, cells, modules, polysilicon; inverters; wind turbine components), DOE LPO, state incentives, sponsor equity. Hydrogen production additionally accesses 45V ($0.60–$3.00/kg PTC for ten years depending on lifecycle GHG).

**Defense industrial base operators** — DoD contracts (cost-plus, fixed-price, OTAs) + corporate balance sheet + DPA Title III grants + working-capital structures backed by progress payments. Capital structure is structurally different because the customer is the federal government.

**Biomanufacturing operators** — corporate equity (large pharma) or venture capital + project finance (CDMOs) + BARDA contracts (biodefense-relevant).

**Critical minerals operators** — DPA Title III grants, DOE LPO loans, DoD IBAS funds, sovereign capital (Australian, Saudi, Canadian government partners), corporate equity. Capital architecture mixes industrial-policy and private capital in operationally complex ways.

### Returns by operator vector

| Vector | ROIC / ROE band |
|---|---|
| Hyperscale compute | 15–25% ROIC (Microsoft, Amazon AWS at top) |
| Semiconductor (TSMC, top players) | 18–28% ROE through-cycle |
| Battery manufacturing | -5% to 10% (currently squeezed; US plants supported by 45X) |
| EV manufacturing | -10% to 15% (Tesla profitable; legacy auto mixed) |
| Solar PV manufacturing (US, 45X-supported) | 12–18% |
| Hydrogen production | Pre-commercial at scale; modeled 8–14% with 45V |
| Defense | 12–18% ROE (top primes) |
| Biopharma (branded) | 20–35% ROIC; CDMOs 12–20% |
| Critical minerals refining | Highly variable; supported by industrial-policy capital |

### Power-cost tolerance (cross-reference)

[[_parameters]] documents Tenant Power Price Tolerance Spectrum:

| Vector | $/MWh tolerance | Power % of OpEx |
|---|---|---|
| Hyperscale AI compute | 80–110 | 15–25% |
| Hyperscale traditional cloud | 60–85 | 8–15% |
| Battery / EV manufacturing | 45–65 | 8–18% |
| Semiconductor / advanced manufacturing | 50–70 | 4–8% |
| Traditional manufacturing / industrial | 35–55 | 5–15% |
| Crypto / Bitcoin mining (interruptible) | 30–45 | 60–80% |
| Hydrogen production (electrolysis) | 20–40 | 50–70% (Tier 2, pending validation) |
| Direct air capture | 25–45 | 40–60% (Tier 2, pending validation) |
| E-fuels | 25–40 | 40–60% (Tier 2, pending validation) |

The variance in power-cost tolerance across operator classes drives the multi-tenant Cantus Intelligent Campus economics. Mixed-Tenant Campus Economics per [[_parameters]]: 300 MW anchor at $90/MWh + 150 MW co-tenant at $55/MWh + 50 MW curtailable.

## 5. Counterparty Universe

| Counterparty | Interaction |
|---|---|
| Power Facilities (developers, owners) | Lease, BTS, ownership of the operating site. |
| Power Land (developers) | Substrate underneath the facility. |
| Power Assets (utilities, IPPs, infra funds) | Power supply via PPA, tolling, BTM, retail. |
| Power Equipment (OEMs) | BTM equipment, substation, cooling, generation hardware. |
| Power Machines (OEMs) | Productive equipment — GPUs, semi tools, robotics, bioreactors, electrolyzers. |
| Power Services (EPC, O&M) | Facility build-out, equipment installation, ongoing operations. |
| Power Markets (the broad allocation layer) | Capital, project finance, PPAs, customer contracts, commodity offtake, hedging. |
| Power Commodities (downstream output markets) | Where the operator's output is sold. |
| Power Technology (DCIM, MES, controls, AI ops software) | Operating systems for the industrial process. |
| Federal government — DoD | Defense industrial base contracts, DPA Title III, IBAS. |
| Federal government — DOE | LPO, ARDP, hydrogen hubs, industrial decarbonization. |
| Federal government — DoC | CHIPS Act, AD/CVD, Section 232. |
| Federal government — Treasury | IRA tax credit administration. |
| State governments | Incentive packages, infrastructure cost-sharing, regulatory streamlining. |
| Workforce institutions | Community colleges, R1 universities, building trades councils, military-to-civilian pipelines. |
| Foreign sovereigns | Capital and supply chain relationships (Korean and Japanese battery; Taiwanese semi; allied critical minerals). |

## 6. Regulatory Environment

Power Industries is regulated **vector-by-vector** more than as a unified sub-industry. Each demand vector has its own federal agency lead, its own industrial-policy framework, and its own state-level regulatory overlay.

**Compute**

FERC/NERC where the operator reaches the BES via direct interconnection; state PUCs on large-load tariffs and retail service; local zoning, water rights, cooling water permits; ERCOT large-load registration (SB 6); CFIUS for foreign data center ownership.

**Supply chain manufacturing**

EPA on emissions and waste; OSHA on safety; DOC/USTR on AD/CVD and tariffs; IRA Section 45X on battery, solar, wind components; IRA Section 48D for semi-adjacent; IRA Section 30D/25E vehicle credits; FEOC rules restricting Chinese-linked supply chain access.

**Energy transition manufacturing**

IRA 45X, 45V, 45Q; DOE Hydrogen Hubs, Industrial Decarbonization Hubs; EPA on emissions; FERC where the operation interconnects to grid.

**Advanced manufacturing — semiconductors**

CHIPS Act grants and research; 48D ITC (25% Advanced Manufacturing Investment Credit); BIS export controls (chip equipment to China); CFIUS; EPA fab emissions (PFAS, VOC, GHG); state environmental.

**Defense industrial base**

DoD acquisition regulation (DFARS, FAR); DPA Title III; IBAS; CMMC; ITAR; EAR; CFIUS; BARDA, DTRA, JPEO-CBRND (biodefense-adjacent).

**Biomanufacturing and critical materials**

FDA on biopharma cGMP (large molecule, fill-finish, cell therapy); DEA on controlled substances; DoC + DoD + DOE on critical minerals industrial policy; DPA Title III for critical materials; BIOSECURE Act (US federal procurement restrictions on certain Chinese biotech firms); BIS export controls; USDA for agricultural bioindustrial.

**Industrial policy framework as the dominant regulatory force**

The IRA, CHIPS Act, BIL, and DPA Title III together constitute the largest federal industrial-policy intervention in US power-consuming industry since World War II. Aggregate announced capex committed to Power Industries operations through 2024–2026 exceeds $1 trillion. Industrial-policy capital reshapes operator underwriting; underwriting Power Industries operators without modeling the federal-policy stack misprices most projects by 15–40%.

## 7. Cantus's Relationship to Power Industries

Cantus Markets is the operating vertical for Power Industries (alongside Power Commodities and Power Markets-broad). The vertical's role with respect to Power Industries is **advisory, orchestration, and commercial structuring** — Cantus does not operate Power Industries facilities, but provides the integrated production deliverable that lets the operator focus on its industrial mission while Cantus handles the integration across Land, Facilities, Infrastructure, and Machines.

### By role

- **Tenant covenant and demand-vector advisor.** Cantus Markets identifies the demand-side operator's site needs (MW envelope, water, fiber, labor, incentives, schedule, security clearance level for defense) and orchestrates the campus deliverable. The covenant strength of the tenant is the primary input to the Cantus Development underwrite; making that covenant legible to capital partners is part of the advisory deliverable.
- **Capital partnership orchestrator.** The operator's capital architecture, the project's capital structure, and the matchmaking with Cantus capital partners (per [[_parameters]] Capital Partner Categories) is part of the integrated production. With Capital folded into Power Markets sub-industry under the v2 framework, this is a coherent Cantus Markets function.
- **Permitting and incentive navigator.** The IRA, CHIPS, DPA, BIL stack interacts with state and local incentive packages in ways that require explicit underwriting. Cantus Markets provides this navigation.
- **Direct-PPA architect.** For Cantus tenants at sufficient scale, direct PPAs with Power Assets operators (the Microsoft–Constellation TMI pattern) bypass the Retail relationship entirely. Cantus Markets structures these direct-PPA arrangements as part of the integrated production.
- **Not the industrial operator.** Cantus does not run semiconductor fabs, battery gigafactories, hyperscale compute workloads, biomanufacturing plants, defense facilities, or critical minerals refineries. The Power Industries operator is the customer.

### Cantus Markets full scope (cross-reference)

Cantus Markets vertical covers three sub-industries: Power Industries (the operator advisory work described here), Power Commodities (output structuring), and Power Markets-broad (capital allocation, customer contracts, commercial structuring). The vertical's integrated function: monetize the platform and allocate capital, power, output, and risk across the Cantus campus portfolio.

### By demand vector

The Cantus Markets engagement varies by demand vector. Current concentration: Compute (hyperscale AI training and inference) and Supply Chain Manufacturing (battery and EV manufacturing). Next-priority engagement track: Advanced Manufacturing (semiconductors). Explicit growth tracks with thinner current pipeline: Defense Industrial Base, Biomanufacturing and Critical Materials, Energy Transition Manufacturing.

The framework rewrite should explicitly prioritize across the six vectors and specify conditions under which Cantus engages each.

### By phase

**Building (Years 1–2) — current.** Advisory engagements with Compute and Supply Chain Manufacturing tenants. Tenant pipeline at 200–300 MW manufacturing per [[_parameters]]. Foxconn and Tesla long-standing relationships.

**Activation (Years 3–4) — modeled.** Multiple advisory mandates active across at least three of the six vectors. Defense Industrial Base and Critical Minerals engagements active.

**Compounding (Years 5–7) — modeled.** All six vectors active. Cantus Markets operating as the recognized integrator-of-record for multi-vector campus development.

**Mature platform (Years 8+).** Cantus Markets operating across all six vectors as the institutional advisor and orchestrator of integrated productions.

### What Cantus does not become

Cantus does not become a hyperscaler. Does not become a fab operator. Does not become a battery manufacturer. Does not become a defense prime. Does not become a CDMO. The integrator posture is durable specifically because Cantus does not compete with the operator on the operator's primary business.

## 8. Key Trends and Structural Conditions (2026–2036)

**1. AI compute as foundational demand vector.** The training and inference build-out is the largest single demand-vector driver of Power sector growth, with hyperscaler capex commitments running $200B+/year across the top six firms.

**2. Reshoring acceleration under CHIPS / IRA / Section 232.** Federal industrial policy driving the largest US manufacturing reshoring in 40+ years. 2024–2026 announced capex pipeline exceeds $1 trillion across semiconductors, batteries, solar, EV, hydrogen, and critical minerals.

**3. Battery overcapacity globally with US carve-outs.** Chinese cell capacity built ahead of demand; cell prices collapsed. US-domestic carve-out (FEOC-compliant, 45X-eligible) protected by tariffs, IRA credits, and Korean/Japanese partner sourcing.

**4. Defense industrial base reconstruction.** Russia-Ukraine, China-Pacific tensions, recognition that US munitions and shipbuilding capacity is insufficient for sustained great-power competition. New defense-tech cohort (Anduril, Shield AI, Saronic, Hadrian) scaling alongside primes.

**5. Critical minerals as national security priority.** Federal capital deploying to reshore refining of rare earths, lithium, cobalt, nickel, graphite, gallium, germanium, antimony.

**6. Hydrogen at inflection point.** 45V framework, DOE Hydrogen Hubs, and underlying economics finding equilibrium. Vector is real but underwriting carries explicit policy risk.

**7. Bio CDMO sector reshaping.** BIOSECURE Act creating structural demand for US-domestic CDMO capacity. Lonza, Catalent, Resilience, Samsung Biologics scaling.

**8. Co-location with generation becoming standard for AI.** Microsoft–Constellation TMI, Amazon–Talen Susquehanna, Meta–Calpine, and the broader pattern shift the offtake counterparty for large generation from IOUs to industrial demand operators.

**9. Water cooling at scale for AI.** Texas groundwater, Arizona aquifer, and similar constraints reshaping site selection.

**10. Workforce constraints across all six vectors.** Skilled labor shortage constrains every demand vector; trained operators, technicians, engineers in tight supply.

## 9. Open Questions for the Framework Rewrite

To resolve as the framework matures:

- **Mapping from six vectors to Two Customer Stacks.** [[Strategy/Cantus-Customer-Category]] currently frames the customer as Two Customer Stacks (AI Factory + Manufacturing Factory). The six-vector framing here is more complete. Reconciliation needed: are the Two Stacks a Tier-1 simplified articulation with the six vectors as the underlying taxonomy, or are the Two Stacks superseded?
- **Vector prioritization.** Compute, Supply Chain Manufacturing, Advanced Manufacturing are clearly active; Defense, Critical Minerals, Biomanufacturing, Energy Transition Manufacturing need explicit treatment.
- **Crusoe-style vertical integration competitive class.** Crusoe operates as Power Assets (generation) + Power Facilities (data center) + Power Machines (compute) + Power Industries (compute operation). The Cantus Markets vertical needs to specify how Cantus competes with this vertically integrated competitor class on the multi-tenant Intelligent Campus alternative.
- **Hyperscaler self-orchestration treatment.** Hyperscalers are increasingly direct land assemblers, direct PPA counterparties, and direct EPC contractors. Framework should specify what Cantus offers a hyperscaler that the hyperscaler's internal team cannot replicate.
- **Tenant covenant underwriting as a constituent product.** Operator covenant is the primary input to Cantus Development underwriting. Framework should make covenant underwriting an explicit Cantus Markets product, articulated to capital partners.

---

*Drafting. Author of record: Dom Espinosa.*
