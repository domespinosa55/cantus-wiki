---
type: strategy
status: active
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
strategy_area: gtm
tags: [prospecting, sourcing, playbook, signals, v2, cantus-markets]
related_framework: ["[[Strategy/Prospecting/Cantus-Prospecting-Framework]]", "[[Strategy/Cantus-Power-Sector-Thesis]]", "[[Strategy/Cantus-Markets]]"]
applies_to_phase: building
supersedes: ["Box v0.1 Tenant Targeting Sourcing Playbook", "Box v0.1 Supply Chain Sourcing Playbook"]
---

# The Cantus Prospecting Playbook v2.0

*Operational sourcing manual for the [[Strategy/Prospecting/Cantus-Prospecting-Framework]]. Documents where each scoring signal is sourced, which databases and trade publications drive each vector, and how to run a prospect from initial screen to outreach decision. The Framework defines the discipline; the Playbook makes the discipline executable.*

*Sits under the Cantus Markets vertical as the analyst-facing operational manual. Companion to the foundational discipline in [[Strategy/Prospecting/Cantus-Prospecting-Framework]].*

---

## I. Purpose

The Prospecting Framework defines what to score. The Playbook defines where each input comes from, how to interpret it, and how to operate the scoring exercise at firm scale across hundreds of prospects. The objective is reproducibility — any Cantus analyst applying the Playbook to a candidate firm should produce the same tier band within a half-point variance.

Three operational claims anchor the Playbook:

1. **Segment-level data does more work than consolidated data.** The Cantus-relevant exposure of most prospects is concentrated in one or two reportable segments and is masked at the consolidated level. Pull segment data first.
2. **Trade press and industry-analyst sources are more reliable than usual for Power-sector prospects.** Hyperscaler co-location plans, OEM-customer relationships, and capacity expansion commitments are routinely surfaced through Data Center Dynamics, Mission Critical, Light Reading, Synergy Research, Dell'Oro, Omdia, BloombergNEF, and adjacent trade publications. Filings often confirm rather than reveal.
3. **Lead-time disclosures are leading indicators.** Companies disclosing 60+ week lead times on critical equipment are in acute capacity-expansion mode and become Tier B/A prospects before the consensus market knows.

## II. Source Hierarchy by Signal Class

Every scoring signal in the Framework maps to one or more sources in the hierarchy below. The hierarchy is structured by signal class, not by vector — most sources are vector-agnostic, with vector-specific overlays in §III.

### A. SEC filings

Primary source for any publicly traded prospect. Specific sections to prioritize:

| Filing section | What to look for | Scores it feeds |
|---|---|---|
| **10-K segment reporting** (Notes 12–15 typically) | Segment revenue, growth rate, segment-specific commentary | Power Pull (all vectors) |
| **10-K customer concentration footnote** (Notes 1–3 typically) | Any customer >10% of revenue, named or described | Power Pull + Counterparty Strength |
| **10-K Properties section** | Facility list by location | Geographic & Site Fit; Multi-Vector Exposure |
| **10-K Risk Factors** | Geographic concentration, supply chain, customer dependence | Counterparty Strength; Site Fit |
| **10-K MD&A** | Backlog, lead times, capacity utilization, capex trajectory | Power Pull + Timing |
| **10-Q updates** | Quarter-over-quarter changes in the above | All dimensions, freshness |
| **8-K filings** | Material expansion announcements, customer wins, executive changes | Timing |
| **Proxy / DEF 14A** | Executive compensation tied to capacity expansion or revenue growth | Timing (board-level alignment) |
| **S-1 / S-3 / S-4** | Capital raise filings; new vehicle structures | Counterparty Strength |
| **Sustainability reports** | Scope 2 disclosures (sometimes broken out by facility); future capacity intent | Power Pull + Site Fit |

### B. Earnings calls and investor materials

| Source | What to look for | Scores it feeds |
|---|---|---|
| **Earnings call transcripts** (Bloomberg, FactSet, Sentieo, Seeking Alpha) | Management commentary on backlog, lead times, customer mentions, capacity expansion | Power Pull + Timing |
| **Earnings call Q&A specifically** | Analyst questions on backlog, AI capex, power equipment lead times often draw unprompted disclosures | Power Pull + Timing |
| **Investor day decks** | Multi-year capex roadmap, backlog charts, customer concentration | Power Pull + Timing |
| **Management interviews** (CNBC, Bloomberg TV, podcast circuits) | Strategy posture on vertical integration, proximity-to-customer, AI infrastructure | Vertical-Integration Trajectory multiplier |

### C. Federal program databases

| Database | What to query | Scores it feeds |
|---|---|---|
| **DOE Loan Programs Office (LPO)** awards | Loan guarantees, conditional commitments, applications | Power Pull (especially Energy Transition, Critical Materials, Advanced Manufacturing) |
| **CHIPS Act award database** (commerce.gov / CHIPS Program Office) | Direct grants, 48D ITC announcements | Power Pull (Advanced Manufacturing vector) |
| **DPA Title III awards** (DoD Industrial Base Policy) | Defense-base capacity grants, critical materials grants | Power Pull (Defense + Critical Materials) |
| **IBAS (Industrial Base Analysis & Sustainment)** awards | Defense supplier modernization | Power Pull (Defense, Advanced Manufacturing) |
| **BARDA contract database** | Biodefense-adjacent manufacturing contracts | Power Pull (Biomanufacturing) |
| **USDA Rural Development** | Rural energy program capital | Power Pull (Energy Transition, certain Manufacturing) |
| **EXIM Bank** disclosures | Export-finance support for US-domestic manufacturing build-out | Counterparty Strength |
| **IRA tax credit transferability marketplace** (Crux, Reunion, Basis Climate) | Credit prices, buyer cohort, project-by-project flow | Counterparty Strength (look-through credit) |

### D. Trade press and industry analyst sources

| Source | Coverage strength | Best used for |
|---|---|---|
| **Data Center Dynamics** | Facility announcements, hyperscaler-supplier relationships, capacity reporting | Compute + Supply Chain Manufacturing |
| **Data Center Knowledge** | Operations focus; DC industry news | Compute + Supply Chain Manufacturing |
| **Mission Critical Magazine** | Power, cooling, electrical infrastructure | Supply Chain Manufacturing (power & grid equipment, cooling) |
| **Light Reading** | Networking and optical hardware | Supply Chain Manufacturing (networking) |
| **The Information** | Hyperscaler procurement decisions, AI lab strategy | Compute |
| **The Register** | Global OEM-hyperscaler relationships | Compute + Supply Chain Manufacturing |
| **BloombergNEF (BNEF)** | Energy transition, battery, hydrogen, sustainability | Energy Transition Manufacturing + Supply Chain Manufacturing |
| **Synergy Research Group** | Hyperscaler capex tracking by region | Compute + Power Land / Facilities mapping |
| **Dell'Oro Group** | Networking, DC infrastructure market share | Supply Chain Manufacturing (networking, optical) |
| **Omdia / DCD Intelligence** | DC market sizing, supply chain analysis | Compute + Supply Chain Manufacturing |
| **LightCounting** | Optical communications | Supply Chain Manufacturing (optical) |
| **Wood Mackenzie** | Power, energy, metals, hydrogen | Energy Transition Mfg + Critical Materials |
| **S&P Global Commodity Insights (Platts)** | Power, gas, hydrogen, critical minerals | All Power-side and several demand vectors |
| **Argus / ICIS** | Hydrogen, e-fuels, specialty chemicals | Energy Transition Mfg, Biomanufacturing |
| **Benchmark Mineral Intelligence / Fastmarkets** | Battery materials, rare earths, lithium | Critical Materials |
| **DigiTimes / Trendforce / IDC / Gartner** | Semiconductors, AI compute, advanced packaging | Compute + Advanced Manufacturing |
| **Janes / Defense News / Breaking Defense** | Defense industrial base | Defense |
| **STAT News / Endpoints / FierceBiotech** | Biopharma manufacturing | Biomanufacturing |
| **Aviation Week / Space News** | Aerospace structures, space manufacturing | Advanced Manufacturing |

### E. Regulatory and government data

| Source | What to query | Scores it feeds |
|---|---|---|
| **ERCOT large-load registration** (SB 6 framework, 2023 Texas legislation) | Registered industrial loads, generators, customer applications | Timing + Power Pull (acute ERCOT activity) |
| **ISO/RTO interconnection queues** (ERCOT GINR, PJM Cluster Studies, MISO DPP, CAISO QC) | Queue position, study status, COD targets | Power Pull (supply-side and demand-side BTM) |
| **State PUC dockets** | CCN / CON filings, IRP filings, large-customer tariff filings | Power Pull + Timing + Site Fit |
| **Texas Comptroller franchise tax records** | Entities operating in Texas (proxy for footprint) | Geographic & Site Fit |
| **State EDC announcements** | Incentive package disclosures, named-project filings | Power Pull + Timing + Site Fit |
| **US Census Bureau Manufacturing Survey** | Quarterly state-level new orders / shipments by NAICS | Power Pull (Supply Chain + Advanced Mfg) |
| **US ITC DataWeb** | Import/export data; supply chain repositioning | Vertical-Integration Trajectory multiplier |
| **EPA / TCEQ permit databases** | Air, water, waste permit filings (industrial facility proxy) | Power Pull (Manufacturing vectors) + Site Fit |
| **USACE Section 404 permits** | Wetlands permits indicating major industrial development | Site Fit |
| **FAA filings** | Wind turbine height clearances; airspace impact assessments | Power Pull (Energy Transition specific cases) |

### F. Workforce and economic data

| Source | What to query | Scores it feeds |
|---|---|---|
| **BLS state and metro employment data** | Skilled-trades headcount; R1 university proximity; labor radius | Geographic & Site Fit (workforce) |
| **LinkedIn headcount and job posting data** | AI/ML headcount growth, manufacturing engineer hiring | Power Pull + Vertical-Integration Trajectory |
| **IBEW Local district data** | JATC enrollment, journeyman availability by geography | Site Fit (Labor/Community Foundation) |
| **Building trades council disclosures** | Project labor agreements, regional capacity | Site Fit |
| **University R1 partnership data** | Sponsored research, talent pipeline programs | Site Fit (Labor/Community Foundation) |

### G. Capital partner and fund data

| Source | What to query | Scores it feeds |
|---|---|---|
| **Form PF and Form ADV filings** (SEC EDGAR) | Private fund adviser disclosures, AUM, strategy descriptions | Partner Scoring (Capital) |
| **PERE / Infrastructure Investor / Preqin** | Infrastructure fund tracking, capital raises, deployment | Partner Scoring (Capital) |
| **ILPA Principles disclosures** | LP-GP transparency standards adherence | Partner Scoring (Capital) |
| **Public fund disclosures** (sovereign wealth annual reports — NBIM, GIC, ADIA, PIF) | Strategy, allocation, recent positions | Partner Scoring (Capital) |
| **Canadian pension annual reports** (CPP, CDPQ, OMERS, OTPP) | Infrastructure allocations, US deployment patterns | Partner Scoring (Capital) |
| **Tax-equity transferability marketplaces** (Crux, Reunion, Basis) | Credit buyer cohort, prices | Counterparty Strength + Capital Partner Scoring |

## III. Per-Vector Signal Sourcing Index

The Power Pull dimension's signal set is the most vector-sensitive. The Framework defines the signals; this section maps each signal to its primary source.

### A. Compute vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| Cloud purchase obligations (3-yr CAGR) | 10-K MD&A commitments table; CFO commentary | Earnings calls Q&A |
| Absolute cloud spend (>$500M flag) | 10-K MD&A; investor day | Synergy Research |
| Disclosed GPU procurement (H100/H200/B200/GB200) | 8-K, 10-K, earnings transcript keyword search | The Information, The Register |
| AI/ML headcount % of engineering | LinkedIn headcount + 10-K total | Investor decks |
| R&D % of revenue | 10-K income statement | Bloomberg / FactSet |
| MD&A AI-keyword density | Direct 10-K read | Earnings call transcripts |
| Hyperscaler-generation co-location deals | 8-K material agreements; trade press | Data Center Dynamics, The Information |
| API / inference volume | Investor day, blog posts, S-1 (if applicable) | Sentieo |
| **Rack power density trajectory** | NVIDIA roadmap (see §V.A); investor day decks; trade press | Mission Critical; Dell'Oro |
| **NVIDIA-driven escalation factor** | NVIDIA quarterly earnings; CES / GTC keynotes; analyst coverage | TrendForce; DigiTimes |

### B. Supply Chain Manufacturing vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| Announced capex (gigafactories, EV, battery) | 8-K; press releases; state EDC announcements | Reuters, Bloomberg |
| IRA Section 45X credit capture | IRS / Treasury filings; CHIPS Office releases | BNEF, Wood Mackenzie |
| FEOC compliance posture | 10-K Risk Factors; Treasury final rules | Trade press |
| Hyperscaler-supplier disclosures (EMS firms) | 10-K customer concentration; trade press | Data Center Dynamics, The Information |
| Backlog and lead-time disclosures | Earnings call MD&A; investor day | Mission Critical, The Register |
| Customer concentration look-through | 10-K Notes 1–3 | Sell-side equity research |
| Power-density trajectory (AI server assembly) | NVIDIA roadmap; OEM customer disclosures | Mission Critical; Dell'Oro |

### C. Advanced Manufacturing vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| CHIPS Act 48D ITC announcements | CHIPS Office press releases; Treasury Section 48D guidance | Reuters, Bloomberg, SemiWiki |
| CHIPS direct grants | CHIPS Office award database (commerce.gov) | DigiTimes, TrendForce |
| Announced fab capex (advanced vs. mature node) | 8-K, 10-K, investor day | SemiAnalysis, TrendForce |
| Robotics manufacturing scaling | 8-K; trade press | The Information, IEEE Spectrum |
| BABA / domestic content compliance | 10-K Risk Factors; OEM disclosures | Trade press |

### D. Defense Industrial Base vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| DPA Title III grant recipients | DoD Industrial Base Policy releases; Federal Register | Janes, Defense News |
| DoD multi-year procurement contracts | DoD contract awards database (defense.gov); 10-K backlog | Breaking Defense |
| IBAS awards | DoD Manufacturing Innovation Institute releases | Janes |
| Defense-tech cohort capex (Anduril etc.) | Press releases; private company disclosures via journalism | The Information, Forbes, Bloomberg |
| Shipbuilding capacity | Navy budget submissions; HII / Electric Boat investor materials | Defense News |
| ITAR / CMMC certification posture | Company disclosures; Federal contractor registries | Breaking Defense |

### E. Biomanufacturing and Critical Materials vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| BIOSECURE Act compliance / opportunity | Company disclosures; Treasury and Commerce releases | STAT News, Endpoints |
| FDA inspection regime | FDA inspection database; company 10-K Risk Factors | STAT News, FiercePharma |
| BARDA contract awards | HHS / ASPR press releases; defense.gov | STAT News, Endpoints |
| DPA Title III for critical materials | DoD releases; DOE Critical Materials Office | Mining.com, Wood Mackenzie |
| Refined-mineral capacity announcements | 8-K; state EDC; mining trade press | Benchmark Mineral Intelligence, Fastmarkets |
| Sovereign capital pairing | Sovereign wealth annual reports; investor announcements | Bloomberg, FT |

### F. Energy Transition Manufacturing vector — sourcing index

| Signal | Primary source | Secondary / cross-check |
|---|---|---|
| IRA Section 45V hydrogen PTC | IRS final rules; DOE Hydrogen Hubs | BNEF, Argus, Platts |
| IRA Section 45X component PTC | IRS / Treasury filings | BNEF, PV InfoLink |
| DOE Hydrogen Hubs program | DOE releases; awarded hub consortium disclosures | Argus Hydrogen Index |
| Industrial Decarbonization Hubs | DOE OCED releases | BNEF |
| Solar vertical integration (ingot → panel) | Company 8-K and press releases; trade press | PV InfoLink, BNEF |
| Wind turbine component footprint | 10-K Properties; press releases | BNEF, Wood Mackenzie |
| Direct air capture commercialization | Company disclosures; DOE CDR programs | CDR.fyi, Cipher |
| E-fuels / SAF capacity | Company disclosures; SAF Coalition | Argus, ICIS |

## IV. Per-Partner-Class Signal Sourcing Index

The Partner Framework dimensions and their sourcing — preserved from v1.0 with v2 sub-industry alignment.

### A. Generation Developers & IPPs (Power Assets)

| Signal | Source |
|---|---|
| MW of operating capacity by technology | EIA Form 860; company 10-K Properties |
| Recent COD performance | Press releases; ISO interconnection databases |
| Queue position in target ISOs | ERCOT, PJM, MISO, CAISO queue dashboards |
| PPA structure flexibility | Recent project announcements; structured products trade press |
| Credit profile | S&P, Moody's, Fitch |
| Project finance capacity | Recent issuances; bank LP-side |

### B. Transmission & Grid Developers

| Signal | Source |
|---|---|
| Miles completed by voltage class | FERC Form 1 filings; company reports |
| HVDC capability | Project disclosures; ABB / Hitachi / Siemens HVDC project portfolios |
| ISO transmission planning involvement | ISO planning documents; FERC dockets |
| FERC CWIP / CPCN track record | FERC dockets |

### C. Equipment OEMs (Power Equipment)

| Signal | Source |
|---|---|
| Current lead times for critical equipment | Earnings calls; trade press (Mission Critical, T&D World) |
| Manufacturing capacity and expansion plans | 8-K, 10-K, press releases |
| Slot availability for Cantus orders | Direct OEM corporate-level conversations |
| US manufacturing footprint (IRA / BABA compliance) | 10-K Properties; sustainability reports |
| Long-term service agreement capability | Standard contract templates; existing customer disclosures |

### D. Machine OEMs (Power Machines, new in v2.0)

| Signal | Source |
|---|---|
| **NVIDIA**: GPU roadmap, allocation, partner program | NVIDIA quarterly earnings; GTC keynote; NVIDIA Partner Network |
| ASML: EUV / High-NA capacity, export restrictions | ASML quarterly; BIS export rule updates |
| Robotics (ABB, FANUC, KUKA, Yaskawa): installed base, capacity | IFR World Robotics Reports; OEM quarterly |
| Battery equipment (Wuxi Lead, DÜRR, Schuler, Manz): order backlog | Trade press; OEM disclosures |
| Bioprocessing (Sartorius, Cytiva, Thermo Fisher): order book | OEM quarterly; trade press |
| Electrolysis (Plug, NEL, Nucera, Bloom): capacity backlog | OEM quarterly; BNEF |

### E. EPC & Construction Partners (Power Services)

| Signal | Source |
|---|---|
| Completed projects last 36 months | Company project portfolios; trade press |
| Bonding capacity | Surety market disclosures (Liberty Mutual, Travelers, Zurich, Chubb) |
| Hyperscaler client list | Project announcements; data center trade press |
| Schedule and budget track record | Industry surveys (ENR Top 400); third-party studies |
| OSHA safety record | OSHA database |

### F. Specialty Mission-Critical Consultants (Power Services)

| Signal | Source |
|---|---|
| Project portfolio | Firm websites and case studies |
| Hyperscaler relationships | Project disclosures; DCD speaker rosters |
| In-house engineering depth | Firm headcount via LinkedIn; published technical content |

### G. Capital Partners

See [[Strategy/Cantus-Markets]] §III for capital partner sourcing; the standard tools are Form PF, Form ADV, PERE / Infrastructure Investor / Preqin, sovereign wealth annual reports, and Canadian pension annual reports.

## V. New v2 Signal Sources

Three signal sources are net-new in v2.0 and weren't present in the v0.1 Playbook. These should be standing data feeds rather than one-off lookups.

### A. NVIDIA Roadmap and GPU Power-Density Tracker

The NVIDIA roadmap is the most consequential single external signal for the Compute, Supply Chain Manufacturing (AI server assembly + burn-in), and Advanced Manufacturing (robotics) vectors.

Tracking inputs (quarterly cadence):

| Input | Source | Cadence |
|---|---|---|
| NVIDIA quarterly earnings | NVIDIA IR site | Quarterly |
| GTC keynote announcements | NVIDIA GTC; YouTube | Annual (spring + fall) |
| CES keynote | NVIDIA CES; YouTube | Annual (January) |
| Computex Taiwan keynote | NVIDIA / Computex | Annual (May/June) |
| Analyst coverage (sell-side) | Morgan Stanley, JPM, BAML, Goldman semiconductor desks | Continuous |
| Independent analyst (SemiAnalysis, Dylan Patel) | semianalysis.com | Continuous |
| Hyperscaler procurement disclosures | Microsoft, AWS, Google, Meta, Oracle earnings calls | Quarterly |
| Custom silicon roadmaps (Google TPU, AWS Trainium, MS MAIA, Meta MTIA) | Hyperscaler events (re:Invent, Build, I/O, Connect) | Annual+ |

Output: a structured tracker mapping GPU generation → TDP → estimated rack density → estimated MW per 10,000 GPU cluster → implied MW per AI server assembly facility (for the EMS vector).

Reference progression:

| Generation | Per-GPU TDP | Rack density (8x) | MW per 100k-GPU cluster |
|---|---|---|---|
| A100 (2020) | 400 W | ~10 kW/rack | ~50 MW |
| H100 (2022) | 700 W | ~30 kW/rack | ~90 MW |
| H200 (2024) | 700 W (improved memory) | ~30 kW/rack | ~90 MW |
| B100 (2024) | 1000 W | ~80 kW/rack (NVL36/72) | ~140 MW |
| B200 (2025) | 1000 W | ~120 kW/rack | ~150 MW |
| GB200 NVL72 (2025) | ~1200 W effective | ~120 kW/rack | ~160 MW |
| Rubin (modeled 2026/27) | ~1500–1800 W (modeled) | ~150+ kW/rack | ~200 MW+ |

The trajectory matters because **burn-in testing at scale draws power proportional to the GPU population under test multiplied by the GPU's rated TDP**. The Celestica 300+ MW is consistent with this trajectory; future engagements should be calibrated against forward GPU generations, not legacy ones.

### B. IRA / CHIPS / DPA / DOE LPO Award Tracker

The industrial-policy stack is consequential across multiple vectors. Cantus should maintain a unified tracker that pulls from each program's award database.

| Program | Database | Cadence | Vectors most affected |
|---|---|---|---|
| **IRA Section 48D ITC** | Treasury elections; CHIPS Office | Continuous | Advanced Manufacturing (semis) |
| **IRA Section 45X** | IRS filings; trade press | Continuous | Supply Chain Mfg, Energy Transition Mfg |
| **IRA Section 45V** | Treasury final rules + project disclosures | Continuous | Energy Transition Mfg (hydrogen) |
| **IRA Section 45U** | Treasury; nuclear fleet operators | Continuous | Power Assets (operating nuclear) |
| **CHIPS direct grants** | CHIPS Program Office releases | Continuous | Advanced Manufacturing |
| **DPA Title III grants** | DoD Industrial Base Policy releases | Continuous | Defense, Critical Materials |
| **DOE LPO loan guarantees** | LPO website; conditional commitments | Continuous | Energy Transition, Critical Materials, Advanced Manufacturing |
| **DOE Hydrogen Hubs** | DOE OCED | Continuous | Energy Transition Mfg |
| **DOE Industrial Decarbonization Hubs** | DOE OCED | Continuous | Energy Transition Mfg, Heavy Industrial |
| **DOE Critical Materials Office** | DOE releases | Continuous | Critical Materials |
| **DoD IBAS** | DoD Manufacturing Innovation Institute | Continuous | Defense, Advanced Manufacturing |
| **BARDA contracts** | HHS / ASPR | Continuous | Biomanufacturing |
| **Texas Energy Fund** | Texas PUC; TXEF program updates | Continuous | Power Assets (ERCOT gas dispatchable) |
| **State EDC packages** | State EDC websites; Site Selection Magazine | Continuous | All vectors with site-specific incentives |

Output: a structured tracker of every announced award above a materiality threshold (e.g., $50M for grants, $100M for loans), tied to a candidate prospect record in CII.

### C. ERCOT SB 6 Large-Load Registration Tracker (Texas-specific)

Texas SB 6 (2023 session) created a large-load registration framework that requires industrial loads above thresholds to register with ERCOT. The registration data, once consistently published, becomes a high-signal Texas-specific prospecting feed.

| Input | Source | Cadence |
|---|---|---|
| ERCOT GINR queue position | ERCOT (Generation Information by Resource) | Monthly |
| Large-load registration filings | ERCOT (post-SB 6 implementation) | Continuous |
| Texas PUC large-customer tariff filings | Texas PUC docket system | Continuous |
| Texas Comptroller franchise tax registrations | Texas Comptroller | Quarterly (proxy for new entity activity) |
| Texas EDC project announcements | Texas EDC; Site Selection Magazine | Continuous |

Output: a Texas-specific large-load prospect list synced to the broader prospect tracker.

### D. Solar / Battery / Semi Vertical-Integration Announcement Tracker

The Tesla solar engagement is the canonical case but not unique. Multiple firms are executing or announcing vertical integration across the Power stack. The framework's Vertical-Integration Trajectory multiplier requires this signal to be tracked systematically.

| Input | Source | Cadence |
|---|---|---|
| Solar manufacturing capacity announcements (ingot, wafer, cell, module) | BNEF, PV InfoLink, Wood Mackenzie | Continuous |
| Battery cell + module + pack vertical integration | BNEF, Benchmark Mineral Intelligence | Continuous |
| Semi-adjacent vertical integration (advanced packaging, substrate, EDA tools) | SemiAnalysis, TrendForce, DigiTimes | Continuous |
| Hyperscaler captive silicon roadmaps | Hyperscaler events; sell-side semiconductor desks | Annual+ |
| Hyperscaler generation acquisitions / direct PPAs | 8-K, trade press | Continuous |
| Robotics vertical integration (chip → robot → software stack) | The Information, IEEE Spectrum, hyperscaler events | Continuous |

Output: a structured roster of firms executing vertical integration across two or more Power sub-industries, with the integration vector(s) tagged. This populates the Vertical-Integration Trajectory multiplier scoring across the prospect base.

## VI. Diligence Protocols — From Initial Screen to Outreach Decision

The Framework defines scoring; the Playbook defines the workflow that produces a scored prospect. Standard analyst workflow:

### A. Initial screen (Day 1, ~2 hours per prospect)

1. **Identify the candidate firm and primary vector(s).** Public ticker if listed; sector classification; first-pass demand vector assignment.
2. **Pull 10-K segment data.** Identify the Cantus-relevant segment. Note revenue %, growth rate, customer concentration footnote.
3. **Pull most-recent earnings call transcript.** Search keywords by vector (Compute: "GPU," "AI infrastructure," "data center"; Supply Chain Mfg: "capacity," "backlog," "lead time"; etc.).
4. **Quick LinkedIn headcount check.** AI/ML, engineering, manufacturing engineering headcount and growth.
5. **Quick federal-program-database scan.** Has the firm received CHIPS, IRA, DPA awards? At what scale?
6. **First-pass score.** Apply the Framework's standard four-dimension rubric to assign a tier. Note primary vector + any secondary vectors.

Output: a single-page Tier A/B/C/D classification with primary vector, estimated MW, and a confidence band.

### B. Deep dive (Days 2–5, if Tier A or strong Tier B emerges from initial screen)

1. **Full 10-K read.** Properties section (geographic fit); Risk Factors (constraint flags); MD&A (capex, backlog, growth posture).
2. **2–4 prior earnings calls.** Trend in lead times, backlog, customer concentration.
3. **Investor day deck review.** Multi-year capex roadmap; capacity expansion intent.
4. **Industry analyst coverage.** Sell-side equity research; specialist firms (Synergy, Dell'Oro, BNEF, Benchmark, etc.) for the relevant vector.
5. **Trade press archive search.** Last 18 months of trade-press coverage of the firm — facility announcements, customer wins, executive comments.
6. **Customer concentration look-through.** If the firm has IG-hyperscaler customer concentration, evaluate the look-through credit for power financing.
7. **Multi-vector and vertical-integration assessment.** Score the firm under each demand vector it touches; assess vertical-integration trajectory.
8. **Geographic fit specifics.** Match against Cantus active pipeline. Identify candidate sites by name (Mathis McDonald, GoodPeak, Joule, Palangana, Wilmer, T1, Singleton).
9. **Tier-A scoring write-up.** Structured memo with the four-dimension scoring, multipliers applied, composite, estimated MW, and a candidate Cantus engagement framing.

Output: a 2–4 page Tier A scoring memo, saved to CII as a tenant data asset, with a recommended outreach approach.

### C. Outreach prep (Days 5–10, if Tier A confirmed)

1. **Relationship-path mapping.** Existing Cantus / Newmark / founder-network paths to the firm. Warm intros prioritized.
2. **Cantus value proposition framing.** Vector-specific articulation of what Cantus delivers — site, infrastructure, machines, capital, workforce — sized to the firm's expected MW envelope.
3. **Pipeline-site framing.** Specific candidate Cantus sites with site-level economics presented.
4. **Capital architecture framing.** Indicative capital structure (Fund I principal position, REIT take-out path, federal program capital, IRA credit monetization).
5. **Workforce-and-community framing.** Labor/Community Foundation positioning per [[Strategy/Foundations/Labor-Community-Foundation]].
6. **Outreach kickoff.** Initial conversation; mutual NDA where appropriate; follow-up site visit scheduling.

Output: a structured outreach package per prospect; a CII Outreach record initiated.

### D. Engagement progression (post-outreach)

Standard milestones (per engagement):

1. Initial conversation completed.
2. Mutual NDA executed.
3. Site visit completed.
4. Term sheet / advisory engagement letter executed.
5. Capital partner introduction(s).
6. Definitive agreement.
7. Closing / COD.

Each milestone advances the prospect's record in CII / DealOS. Stale records (no milestone advance in 90 days) trigger an analyst review.

## VII. Cross-References to CII Data Assets

The Prospecting Framework and Playbook feed and consume specific CII data assets per [[Products/CII-Iteration-Document]] and [[Strategy/Foundations/CII-DealOS-Foundation]].

| CII data asset family | Role in prospecting |
|---|---|
| **Parcel family** (geospatial site scoring, Parcel Registry) | Geographic & Site Fit dimension; matching exercise (§V Framework) |
| **Tenant family** (covenant analysis, demand-vector intelligence, customer-category mapping) | All four scoring dimensions; calibration anchor maintenance |
| **Capital family** (capital partner mandates, federal-program eligibility, fund vehicle structures) | Partner Scoring (Capital); composite financing capability |
| **Regulatory family** (interconnection queues, IRA/CHIPS/DPA stack modeling, state incentives) | Power Pull (federal-program-driven signals); Timing |
| **Operational family** (campus operating metrics, equipment lead times, market dynamics) | Power Pull (Supply Chain power density); Timing (equipment lead times) |

The four prediction-and-resolution loops in CII also intersect:

| CII loop | Prospecting use |
|---|---|
| **Site validation loop** | Geographic & Site Fit; integrated underwrite of a candidate site against a prospect |
| **Tenant match loop** | Multi-vector scoring; matching exercise across the prospect base |
| **Capital routing loop** | Partner Scoring (Capital); matching prospect to capital partner |
| **Regulatory intelligence loop** | Power Pull (federal program signals); Timing |

## VIII. Operational Checklists

### A. Prospect Tracker (Excel workbook spec)

The v0.1 Box Tenant Framework named "Excel scoring workbook" as a next step. Under v2.0, the workbook is a CII Tenant-family data asset feeding the Tenant match loop. Spec:

**Sheet 1: Prospect Universe**
- Columns: Firm Name | Public/Private | Primary Vector | Secondary Vector(s) | Power Pull score | Timing score | Counterparty Strength score | Site Fit score | Base Composite | Multi-Vector Multiplier | Vertical-Integration Multiplier | Final Composite | Tier (A/B/C/D) | Estimated MW | Active Pipeline Site Match | Outreach Status | Last Scored | Next Review

**Sheet 2: Per-Prospect Detail**
- One sheet per Tier A and B prospect
- Sourcing notes by signal (cite filing section, page, or trade press URL)
- Multi-vector breakdown
- Vertical-integration assessment
- Engagement history log

**Sheet 3: Vector Roll-up**
- Counts and total estimated MW by vector
- Tier distribution by vector
- Active pipeline coverage by vector

**Sheet 4: Partner Roster**
- Same structure for Partner scoring across sub-categories

**Sheet 5: Calibration anchors**
- Tesla and Celestica scoring detail
- Any future calibration-anchor engagements added

The workbook is the operational tool; CII is the institutional memory; DealOS is the deal-execution engine. The three together constitute the firm's prospecting operating system.

### B. Per-engagement diligence checklist

For each Tier A engagement reaching the deep-dive stage, the analyst completes:

1. [ ] 10-K segment data pulled and tabulated (revenue, growth, customer concentration)
2. [ ] 4 most-recent earnings call transcripts scanned by keyword
3. [ ] Investor day deck reviewed and capex roadmap noted
4. [ ] LinkedIn headcount delta over 24 months recorded
5. [ ] Federal-program-database scan complete (CHIPS, IRA, DPA, LPO, BARDA, IBAS)
6. [ ] Sell-side equity research pulled (2+ analyst notes minimum)
7. [ ] Specialist industry research pulled (1+ from Synergy / Dell'Oro / BNEF / Benchmark / Wood Mackenzie / etc., per vector)
8. [ ] Trade press archive scanned (18-month look-back)
9. [ ] Customer concentration look-through assessed; IG anchor identified
10. [ ] Vector(s) and multipliers assigned with sourcing notes
11. [ ] Site fit assessed against active Cantus pipeline (named sites)
12. [ ] Constraint flags checked (water, workforce, permitting)
13. [ ] Relationship-path map drafted (Cantus / Newmark / founder networks)
14. [ ] Scoring memo (2–4 pages) drafted
15. [ ] Memo reviewed by founder / vertical head
16. [ ] CII Tenant record populated
17. [ ] Outreach package drafted
18. [ ] Outreach kickoff completed

### C. Quarterly framework calibration

Every 90 days, the analyst team and founder review:

1. New engagements closed since last calibration → calibration write-ups
2. New industry signal changes (NVIDIA roadmap movement, IRA/CHIPS administrative changes, ERCOT SB 6 implementation milestones)
3. Score delta across the Tier A and B roster → updated rankings
4. Multi-vector multiplier curve fit against observed outcomes
5. Vertical-integration trajectory signals updated
6. Open questions in [[Strategy/Prospecting/Cantus-Prospecting-Framework]] §XII status

Output: a quarterly Prospecting Calibration Memo logged to the wiki.

## IX. What This Playbook Replaces

The v0.1 Box Tenant Targeting Sourcing Playbook and v0.1 Supply Chain Sourcing Playbook are superseded by this document. The v0.1 sourcing discipline is preserved; the structure is updated to fit the v2 six-vector taxonomy and the v2 sub-industry partner categories.

Specific carry-forwards from the v0.1 work:

- 10-K segment reporting as primary source (preserved and emphasized).
- Customer concentration footnote analysis (preserved).
- Trade press source list (expanded with vector-specific overlays).
- Industry analyst source list (expanded).
- ERCOT-specific data emphasis (preserved and extended with SB 6 framework).
- Texas-specific regulatory data (Comptroller, EDC, PUC; preserved).

Specific net-new additions in v2.0:

- NVIDIA roadmap / GPU power-density tracker.
- Vertical-integration announcement tracker.
- BIOSECURE Act / FEOC posture tracking.
- DPA Title III / IBAS / DOE LPO unified tracking.
- Texas Energy Fund tracking.
- CII data asset and prediction-and-resolution loop integration.

## X. Closing

The Framework and Playbook are the operational pair that makes Cantus prospecting reproducible. The Framework defines what to score; the Playbook defines how to source the inputs. Together they constitute the institutional discipline by which the firm converts the Power Sector thesis into specific Tier A engagements.

The compounding value sits in the data. Every prospect scored, every engagement closed, every calibration run improves the next scoring exercise. The CII / DealOS Foundation is where that compounding lives institutionally; this Playbook is how analysts feed the Foundation with quality inputs.

The work is not to score every Power-sector firm; it's to identify the highest-conviction prospects within Cantus's pipeline window and convert them to engagements. The Playbook should be applied to the prospect universe weekly, with calibration runs quarterly and full framework refresh annually.

---

*Operational sourcing manual, v2.0 canonical. Companion to [[Strategy/Prospecting/Cantus-Prospecting-Framework]]. Anchored to the Cantus Power Sector Thesis. Author of record: Dom Espinosa.*
