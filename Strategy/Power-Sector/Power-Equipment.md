---
type: framework
status: drafting
audience: internal
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [power-sector, sub-industry, power-equipment, cantus-infrastructure]
sub_industry: power_equipment
sub_industry_index: 2
related_thesis: ["[[Strategy/Bridge-to-Grid-Thesis]]", "[[Strategy/Cantus-Framework]]"]
related_pages: ["[[Strategy/Power-Sector/Power-Assets]]"]
---

# Power Equipment — Sub-Industry Specification

*Sub-industry 2 of 10 in the Power sector framework. Drafting.*

---

## 1. Definition

Power Equipment is the **industrial manufacturing** sub-industry that produces the physical hardware deployed into Power Assets. The unit of production is a manufactured product — a turbine, transformer, switchgear lineup, inverter, battery system, or specialty component — delivered to a project site, a distributor, or an EPC contractor under a supply contract.

The boundary against adjacent Power sub-industries:

- **Power Assets** owns and operates the equipment once installed and energized. The OEM is not the asset owner unless a BOOM or tolling arrangement keeps title at the manufacturer — rare at industrial scale, more common at distributed scale.
- **Power Machines** (v2 framework) is the productive machinery installed *inside* Power Facilities — GPUs, semi tools, robotics, electrolyzers, bioreactors. Power Equipment serves the supply side; Power Machines serves the demand side. Same word ("equipment") is sometimes used colloquially for both, but the supply chains, OEMs, capital sources, and economics are completely different. A Caterpillar reciprocating engine is Equipment; an NVIDIA H100 is a Machine. The v2 framework makes this distinction explicit.
- **Power Services** installs, commissions, and maintains the equipment. The line is blurring as OEMs forward-integrate into EPC and Long-Term Service Agreements (LTSAs), but the structural distinction holds: Equipment is what is made in a factory; Services is what is done in the field.
- **Power Commodities** is the output of Power Industries — refined minerals, battery cells when traded as a commodity, semiconductor wafers, refined hydrogen. The boundary with Equipment requires care: a battery cell is a *commodity* when traded into the cell market, and *equipment* when integrated into a BESS system sold to a project. The framework convention adopted here is that the **end use determines classification at the point of sale.** A cell sold to a BESS integrator is a Commodity; the integrated BESS sold to a Power Asset is Equipment.
- **Power Industries** consumes power to make industrial commodities. The same entity can be a Power Industries operator and a Power Equipment supplier (a battery factory producing cells), but the framework treats the *primary commercial product* as the classifier. A battery cell factory is Power Industries when its output is sold into general commodity markets; a BESS integrator is Power Equipment because its output is a capital good installed in a Power Asset.

Within Power Equipment, nine structural sub-segments:

1. **Rotating machinery** — gas turbines (heavy frame, aeroderivative, mid-block, industrial), steam turbines, reciprocating engines (gas, diesel), wind turbines (onshore, offshore), hydro turbines, generators.
2. **Power conversion** — large power transformers (LPT, >100 MVA), distribution transformers, substation transformers, HVDC converters, solar inverters, BESS inverters, wind turbine converters.
3. **Switching and protection** — HV switchgear (>72.5 kV), MV switchgear, LV switchgear, protective relays, reclosers, fuses, surge arresters, GIS and AIS lineups.
4. **Storage systems (integrated)** — lithium-ion BESS containers, flow battery systems, emerging long-duration (iron-air, compressed-air, gravity).
5. **Power electronics** — FACTS devices, STATCOMs, SVCs, grid-forming inverters, custom power electronics.
6. **Solar PV** — modules, trackers, inverters (modules increasingly behaving as a Power Commodity in pricing dynamics — see boundary discussion above).
7. **Transmission hardware** — conductors, towers, insulators, hardware fittings.
8. **Substation balance-of-plant** — control houses, GIS, AIS auxiliary equipment, station service.
9. **Nuclear-specific** — reactor pressure vessels, steam generators, fuel assemblies, control rod drive systems, nuclear-rated I&C.

## 2. Deliverables

Power Equipment produces four classes of deliverable, increasingly interlocked:

**The unit product** — the manufactured turbine, transformer, switchgear assembly, BESS container, module set. Performance specified in nameplate (MW, kV, MVA, kWh), with performance guarantees on heat rate, efficiency, availability, and capacity factor.

**Equipment supply contracts** — commercial instruments with delivery schedules, milestone payments, performance guarantees, warranty terms (typically 2–5 years standard, extended via LTSA). Order-book position is a tradeable asset given current lead times.

**Long-Term Service Agreements (LTSAs)** — multi-decade service contracts that monetize the manufacturer's installed base. GE Vernova, Siemens Energy, and Mitsubishi Power have all restructured around LTSA capture; the service revenue tail now drives a majority of the OEM's profit on heavy-frame and aero gas turbines. The deliverable is contractual: a commitment to keep the equipment performing to spec for 10–25 years.

**Spare parts and consumables** — turbine hot section components, transformer bushings, BESS replacement modules, switchgear contacts. Lifetime revenue per unit is often comparable to the original sale.

Beneath these sit two operating instruments that the sub-industry treats as products in their own right: **manufacturing slot allocation** (which has become a tradeable position) and **inventory of long-lead items** (large forgings, LPT cores, GOES coils).

## 3. Major Players (US-Focused)

### Gas turbines — heavy frame and aeroderivative

GE Vernova (spun from GE April 2024; the largest US player by installed base); Siemens Energy (spun from Siemens; second-largest globally); Mitsubishi Power (largest globally for heavy-duty frames); Solar Turbines (Caterpillar subsidiary, small-to-mid industrial); Baker Hughes (industrial / oil & gas heritage frames); Kawasaki (smaller industrial); Doosan (Korean); Pratt & Whitney (Mitsubishi-licensed aero derivatives).

The OEM list in [[_parameters]] under Strategic OEM Relationships maps directly onto this segment: Mitsubishi Power and GE Vernova as aeroderivative bridge providers, Baker Hughes / Solar Turbines / Kawasaki / Doosan as permanent generation.

### Reciprocating engines

Caterpillar (CAT, including the Solar Turbines unit for smaller frames); Cummins; Wärtsilä (Finnish; the dominant grid-scale reciprocating player); MAN Energy Solutions; Rolls-Royce Power Systems (MTU brand); INNIO (formerly GE Distributed Power; now ADQ / I Squared-owned; Jenbacher and Waukesha brands).

All five of Caterpillar, Cummins, and Wärtsilä are in [[_parameters]] as Cantus OEM partners for bridge BTM generation.

### Wind turbines

GE Vernova (US leader by installed base); Vestas (Danish, global #1); Siemens Gamesa (struggling commercially); Nordex; Goldwind, Envision, Mingyang (Chinese — restricted US market access via trade and Section 301 considerations).

### Solar PV modules

Tier-1 Chinese: LONGi, JinkoSolar, Trina Solar, JA Solar, Canadian Solar, Tongwei. Korean: Hanwha Q CELLS. US/Western: First Solar (the IRA 45X primary beneficiary), Maxeon, Meyer Burger (struggling). US production capacity is expanding rapidly under 45X; the binding constraint is upstream (wafer, cell capacity).

### Solar and storage inverters

SMA Solar Technology (German); Sungrow (Chinese); Power Electronics (Spanish); TMEIC (Toshiba-Mitsubishi); Huawei (limited US market access); Enphase and SolarEdge (residential-focused).

### Battery storage systems (BESS, integrated)

Tesla (Megapack); Fluence (Siemens Energy / AES JV; publicly traded); Powin (US, near-bankruptcy filing in 2024–2025; emerging restructure); Wärtsilä Energy Storage; Hitachi Energy; Saft (TotalEnergies subsidiary); LG Energy Solution; Samsung SDI (integrating downstream); CATL EnerC platform; BYD (limited US); IHI Terrasun; Sungrow (with module-level offer).

Tesla, Fluence, and Powin are the three named in [[_parameters]] as Cantus BESS partners.

### Battery cells

CATL (global leader); BYD; LG Energy Solution; Samsung SDI; SK On; Panasonic; Northvolt (Sweden, distressed); ACC (Stellantis/Mercedes/TotalEnergies European JV). US-domestic cell capacity standing up under IRA 45X, dominated by Korean and Japanese partners with US footprint (LG, SK On, Panasonic, Samsung) and a smaller domestic-only cohort.

### Transformers — large and substation

Hitachi Energy (formerly ABB Power Grids); Siemens Energy; GE Prolec (JV); WEG (Brazilian); Hyundai Heavy; Hyosung; Mitsubishi Electric; SPX Transformer Solutions / Waukesha; Howard Industries (US distribution); ERMCO (US distribution).

LPT capacity is structurally constrained. Hitachi Energy and Siemens Energy in [[_parameters]] are Cantus procurement counterparties.

### Switchgear and protection

ABB (now Hitachi Energy for HV); Siemens Energy; Schneider Electric; Eaton; GE Vernova (Grid Solutions); S&C Electric; Mitsubishi Electric; Toshiba; Powell Industries (US-listed; HV/MV custom switchgear).

### HVDC converters

Hitachi Energy; Siemens Energy; GE Vernova; Mitsubishi Electric; Toshiba.

### Nuclear equipment

Westinghouse (Brookfield/Cameco-owned); BWX Technologies (US naval + commercial); GE Hitachi Nuclear Energy (boiling water reactors, SMR via BWRX-300); Curtiss-Wright (controls and instrumentation); Holtec (storage casks, SMR-300); Framatome (French; large-component supplier to US fleet); Japan Steel Works (the single dominant ultra-large forging supplier globally); Doosan Heavy Industries (large forgings).

### Steam turbines

GE Vernova; Siemens Energy; Mitsubishi Power; Toshiba; Doosan Škoda Power.

## 4. Capital Structures and Economics

Power Equipment is structurally different from Power Assets — capital-intensive industrial manufacturing rather than long-tenor infrastructure ownership. The economics are cyclical, supply-constrained at present, and increasingly bifurcated between the unit-product margin and the service revenue tail.

### Cost structure of an OEM (heavy-frame turbine reference)

Roughly indicative; real disclosures vary:

| Component | Share of cost of goods sold |
|---|---|
| Raw materials (steel forgings, specialty alloys, electrical steel) | 35–45% |
| Components from tier-2 suppliers (controls, ancillary systems) | 20–30% |
| Direct labor | 10–15% |
| Plant overhead and depreciation | 10–15% |
| Logistics (specialty heavy haul) | 3–7% |

R&D is 4–7% of revenue for major OEMs; warranty reserves run 2–4% of revenue.

### Margins and returns

Power Equipment margins are heavily dependent on cycle position and product mix:

| Segment | Operating margin (current cycle) |
|---|---|
| Heavy-frame and aeroderivative gas turbines (unit sales) | 8–14% |
| LTSA revenue (services tail) | 18–25% |
| Large power transformers | 12–18% (supply-constrained pricing power) |
| Switchgear and protection | 10–16% |
| Solar modules (commodified) | -5% to 12% (highly variable by manufacturer; First Solar elevated by 45X) |
| BESS integrated systems | 0–8% (caught between cell price volatility and project pricing pressure) |
| Battery cells | -5% to 15% (Chinese players currently squeezed by overcapacity; US 45X-eligible players elevated by credit) |
| Reciprocating engines | 8–14% |
| Nuclear equipment | 6–12% (long-tail business; project-by-project) |

Return on invested capital: 8–15% at top of cycle for major OEMs; 5–10% at trough. Recent cycle (2024–2026) is at the top.

### Working capital structure

The OEM business model runs on milestone payments rather than upfront cash:

- 10–30% down payment at order
- 30–60% progress payments through manufacturing milestones
- 10–20% on factory acceptance test
- 5–10% retention released on commissioning and performance

Receivables and inventory often exceed annual revenue at major OEMs given multi-year build cycles. Working capital is the binding cash constraint; the unit economics of growth are gated by financing capacity for in-process inventory.

### Lead times (the critical sub-industry parameter)

| Equipment category | Lead time, mid-2026 |
|---|---|
| Large power transformer (>100 MVA, US) | 130+ weeks (3–4 yr) |
| Heavy-frame gas turbine (F-class, H-class) | 3–5 yr |
| Aeroderivative gas turbine | 24–36 mo |
| Reciprocating gas engine (industrial) | 24–36 mo |
| Mid-voltage GIS switchgear | 18–24 mo |
| BESS integrated container | 12–18 mo |
| HVDC converter station | 30–48 mo |
| Solar inverter (utility-scale) | 6–12 mo |
| Solar module | 3–6 mo (commodified) |
| Reactor pressure vessel (large LWR or SMR) | 5–7 yr (single-digit global suppliers) |
| Wind turbine (onshore, large) | 18–30 mo |

These lead times are the chokepoints that define Time-to-Operational across every Cantus campus. Cross-reference: [[_parameters]] BTM lead times of 18–36 months align with the aeroderivative and reciprocating engine rows; LPT lead times exceed any Cantus-controllable schedule.

### OEM business model bifurcation

The Power Equipment sub-industry has restructured around four commercial patterns:

- **Pure equipment sale** — declining as standalone strategy; margin pressure from commoditization.
- **Equipment + LTSA** — the GE/Siemens/Mitsubishi default. The majority of new heavy-frame turbines sell with multi-decade service contracts attached; the service tail is the profit center.
- **Equipment + EPC + LTSA** — the integrated wrap. Mitsubishi Power has done this with select customers; Wärtsilä has done it for grid-scale BESS.
- **Equipment + financing** — vendor financing is uncommon in the US at large-frame scale but more common in BESS and reciprocating-engine sales.

## 5. Counterparty Universe

| Counterparty | Interaction |
|---|---|
| Power Assets (IPPs, IOUs, infra funds) | Primary buyer of equipment. Procurement specifications, EPC selection drives equipment selection. |
| Power Services (EPC contractors) | Both an intermediary buyer (EPC procures on behalf of project owner) and a partner in integrated wraps (EPC + equipment + LTSA). |
| Power Industries (industrial customers) | Direct buyer when industrial customer self-procures BTM equipment (the Cantus campus pattern). Customer-owned generation arrangements. |
| Distributors and channel partners | Distribution-scale equipment moves through electrical distributors (Graybar, Rexel, WESCO, Sonepar) and specialty channels. |
| Tier-2 component suppliers | Steel forgings (Japan Steel Works, Doosan Heavy), specialty alloys, GOES (Cleveland-Cliffs in US), semiconductors (SiC and GaN for power electronics — Wolfspeed, Onsemi, STMicro), rare-earth magnets (largely China), controls and I&C. |
| Specialty input suppliers | The structural chokepoints — single-source forging suppliers, single-source GOES, single-source rare-earth refining. |
| Logistics counterparties | Specialty heavy haul (rail, barge, dimensional trucking) for transformers, turbine components, wind blades. |
| Trade authorities | Commerce (ITA), USTR, ITC — for AD/CVD investigations, Section 301, Section 232. |
| Standards bodies | IEEE, IEC, NEMA, ANSI, UL — equipment standards, interconnection requirements. |
| Customs and brokers | Increasingly significant given tariff regime. |

## 6. Regulatory Environment

Power Equipment is regulated less by FERC and more by the **trade, industrial policy, and standards regime**. Federal regulators include:

- **DOE** — equipment efficiency standards (the distribution transformer efficiency rule has been a multi-year fight); ARPA-E and EERE manufacturing R&D; Hubs (Hydrogen, Industrial Decarbonization) that pull equipment demand.
- **DOC and USTR** — antidumping and countervailing duty (AD/CVD) actions, Section 301 tariffs, Section 232 national security tariffs, BIS export controls. The solar AD/CVD circumvention investigations on Southeast Asian transshipment have repeatedly disrupted module supply.
- **EPA** — manufacturing emissions, hazardous waste (battery manufacturing in particular), RCRA, TSCA (PFAS rules increasingly relevant to electronics).
- **CPSC and OSHA** — product safety and worker safety in manufacturing.
- **DOD / DPA** — Defense Production Act authority invoked for transformer manufacturing, large-frame castings, and select critical components. DOD also runs the Industrial Base Analysis and Sustainment program.

**Industrial policy framework**

- **IRA Section 45X (Advanced Manufacturing PTC)** — credit per unit of US production for solar wafers, cells, modules, polysilicon, battery cells, battery modules, critical minerals processing, wind turbine components, inverters. Has driven roughly $100B+ of announced US manufacturing investment since 2022. The 45X credit is the dominant economic factor reshaping the US side of the sub-industry.
- **IRA domestic content bonus** — ITC bonus for projects using US-made equipment; threshold escalates from 40% to 55% by 2027.
- **Build America Buy America (BABA)** — federal infrastructure procurement requirements; applies indirectly via federal financing programs.
- **CHIPS Act** — semiconductor manufacturing incentives, relevant for SiC/GaN power electronics and BESS controls.
- **Critical Minerals lists (DOE and Department of Interior)** — rare earths, lithium, cobalt, nickel, graphite, etc.
- **Defense Production Act Title III invocations** — used to incentivize US transformer manufacturing capacity build-out.

**Trade actions affecting current equipment sourcing**

- Solar AD/CVD on Chinese and circumventing Southeast Asian imports — ongoing.
- LPT AD/CVD on Korean producers — active.
- Section 301 China tariffs — broad; 25% on most electrical equipment.
- Section 232 steel and aluminum — affects forgings, conductors, structural components.
- 2025+ administration tariff actions — additional layers under reconsideration; remains the largest policy uncertainty in the sub-industry.

**Standards**

- IEEE 519 (harmonics), 1547 (interconnection of distributed resources), 1815 (DNP3 controls)
- IEC 61850 (substation automation)
- NEMA distribution and switchgear standards
- UL 9540 / 9540A (BESS safety)
- IEC TS 62933 series (electrical energy storage systems)
- NERC CIP (cyber-security; bears on equipment with software interfaces)

## 7. Cantus's Relationship to Power Equipment

Cantus does not manufacture equipment. Cantus's relationship is procurement-side and orchestration-side, executed through the **Cantus Infrastructure** vertical in the v2 four-vertical architecture. Cantus Infrastructure spans Power Assets, Power Equipment, and Power Services together as the unified supply-side integration vertical — "Infrastructure powers them" in the firm's value-creation sequence.

### By role

- **Procurement counterparty and specifier.** Cantus Infrastructure structures equipment selection for campuses, specifies equipment in CCN filings and IRPs, and manages OEM relationships at the corporate level. The OEM cohort in [[_parameters]] — Caterpillar, Cummins, Wärtsilä, Mitsubishi Power, GE Vernova, Baker Hughes, Solar Turbines, Kawasaki, Doosan, Hitachi Energy, Siemens Energy, ABB, Tesla, Fluence, Powin — is the counterparty universe.
- **Order-slot holder.** Given current lead times, manufacturing slots have become a tradeable asset. Cantus's structural advantage in the bridge-BTM use case is the ability to hold and assign slots that competitors cannot get on short notice. This is not theoretical; it is the operating reason the firm can promise a Time-to-Operational that downstream tenants cannot replicate on their own.
- **Integrator across OEMs.** A Cantus campus typically combines equipment from multiple OEMs — a Wärtsilä or Caterpillar bridge plant, a Mitsubishi or GE Vernova aeroderivative for the next tranche, Tesla or Fluence BESS, Hitachi Energy or Siemens transformers, ABB or Schneider switchgear. The integration across OEMs is part of what the campus deliverable is.
- **Intelligence source.** Capacity, lead time, and pricing intelligence on Power Equipment is one of the CII data assets that compounds — see [[Products/CII-Iteration-Document]]. The Cantus relationship with OEMs feeds market intelligence that downstream Cantus customers and capital partners do not have direct access to.
- **Not an EPC, not an OEM, not an O&M provider.**

### By phase

**Building (Years 1–2) — current.** Procurement relationships at the OEM corporate level. Specifying authority on Cantus-led sites. Slot-holding for bridge generation. Equipment intelligence feeding CII.

**Activation (Years 3–4) — modeled.** Pre-purchase agreements at corporate level, possibly with cash deposits funded by Fund I. Warehoused slots for fund pipeline. Direct relationships with Tier-1 component suppliers (Japan Steel Works, Doosan Heavy, Cleveland-Cliffs) where binding constraints emerge.

**Compounding (Years 5–7) — modeled.** Possible strategic equity stakes in critical OEMs where supply constraints persist (a Brookfield-Westinghouse pattern at smaller scale). Potential in-house assembly capability for highly customized integration — microgrid control, storage-plus-generation hybrid skids — only where the integration is inseparable from the campus operating envelope.

**Mature platform (Years 8+).** Cantus would likely remain a procurement-and-integration counterparty rather than a manufacturer, with selective principal equity in critical supply nodes.

### The integration claim against Power Equipment

The structural claim Cantus makes about Power Equipment is that the OEM landscape is consolidating (GE Vernova, Siemens Energy, Mitsubishi Power, Wärtsilä, CAT, Cummins as the dominant primary movers), supply-constrained (multi-year lead times), and forward-integrating into LTSAs and EPC. The demand-side operator therefore needs a counterparty that can navigate OEM slot allocation across multiple suppliers, hedge against forward-integration capture by any single OEM, and combine equipment into integrated campus deliverables. That is Cantus Infrastructure's role against this sub-industry.

## 8. Key Trends and Structural Conditions (2026–2036)

**1. Large power transformer crisis.** Domestic US LPT manufacturing capacity is insufficient for replacement plus growth demand. Lead times at 130+ weeks. The binding upstream constraint is grain-oriented electrical steel (GOES) — Cleveland-Cliffs is the single domestic supplier — and large-forging capacity, where Japan Steel Works and Doosan Heavy dominate globally. DOE and DOC have invoked Defense Production Act authority and stood up capacity expansion programs; the build-out runs years.

**2. OEM consolidation and order-book scarcity.** GE Vernova (spun April 2024) and Siemens Energy (spun September 2020) are now publicly traded pure-play OEMs with rising market capitalization, growing order books, and restored pricing power after a decade of weakness. Mitsubishi Power, Wärtsilä, and Caterpillar are running at peak utilization. The OEM cohort has been pricing capacity up consistently through 2025–2026.

**3. Domestic content premium.** IRA bonus ITC for 40%+ domestic content (escalating to 55% by 2027) has created a two-tier market — buyers paying domestic premium versus importers gambling on AD/CVD outcomes. The 2025+ tariff regime has compounded the differential. First Solar is the most visible beneficiary on solar; US transformer manufacturing buildout is the slower-developing parallel.

**4. Battery cell supply bifurcation.** Chinese cell manufacturers (CATL, BYD) dominate global supply at structurally lower cost but face US tariff and security restrictions, including Foreign Entity of Concern (FEOC) rules that exclude their cells from IRA-eligible projects. The IRA-eligible alternatives are Korean (LG Energy Solution, Samsung SDI, SK On) and Japanese (Panasonic) cell makers with US footprint. Domestic-only US cell capacity is still ramping. BESS integrators are caught in the middle and must navigate sourcing rules carefully.

**5. Critical materials constraints.** Wind turbine permanent magnets (NdFeB, Chinese-dominated), EV motor magnets, electrical-steel GOES, large forgings, SiC/GaN power semiconductor wafers, lithium and graphite for batteries. The US/allied supply chain remains thin; the China dependency is the durable risk in the sub-industry.

**6. Slot-holding as a strategy.** Manufacturing slots have become a tradeable asset class. Some developers and capital partners hold speculative slots for resale. Cantus's OEM corporate-level relationships position the firm as a primary slot-holder rather than a secondary-market slot-buyer.

**7. OEM forward integration into Services.** GE Vernova, Siemens Energy, Mitsubishi Power, and Wärtsilä are all increasing their EPC and LTSA capture. The boundary between Power Equipment and Power Services is blurring at the heavy-frame end. For Cantus, this matters because the equipment counterparty is becoming the construction and operations counterparty, which raises counterparty concentration risk and makes integrator-side hedging across OEMs more strategically valuable.

**8. BESS integration vs. cell commoditization.** Cells are commoditizing under Chinese overcapacity; integrated BESS systems are differentiating on software, control, and warranty. Tesla, Fluence, and Powin compete on integration rather than chemistry. The strategic implication: BESS as a Power Equipment product is increasingly a *software-plus-warranty* product wrapped around commoditized cells.

**9. Nuclear equipment capability rebuild.** The US has lost most of its large-forging capability for reactor pressure vessels and steam generators. Japan Steel Works and Doosan Heavy supply the few global forging facilities at the relevant scale. SMR developers (NuScale, X-energy, Kairos, Oklo, BWX, Westinghouse AP300) depend on a small number of qualified suppliers. The capability rebuild is a 10–15 year project at minimum; near-term, the global supply chain is the constraint.

**10. Software content rising across all equipment.** Increasingly, the differentiator in Power Equipment is the embedded software — grid-forming inverter algorithms, BESS energy management systems, turbine combustion control, smart switchgear, asset performance management. This is the structural bridge into Power Technology, and the place where Power Equipment OEMs are protecting margin against commoditization. The implication for Cantus is that equipment selection increasingly carries software lock-in; integration choices need to be made with software interoperability in mind.

## 9. Open Questions for the Framework Rewrite

To resolve as the framework matures:

- **Where exactly does the boundary between Power Equipment and Power Commodities sit?** Battery cells, polysilicon, semiconductor wafers, and refined critical minerals all sit at the boundary. The convention adopted here (end-use at point of sale determines classification) is defensible but should be tested against all 10 sub-industries before locking in.
- **Where does software-content equipment sit at the Power Equipment / Power Technology boundary?** A BESS integrator selling an asset on its software stack is increasingly a Power Technology counterparty as much as a Power Equipment counterparty. The framework needs a treatment that does not double-count. The v2 distinction between Power Equipment (supply-side hardware) and Power Machines (demand-side productive hardware) does not eliminate this question — it just contains it within Equipment.
- **Should Cantus take strategic equity in any OEM during the Compounding phase?** Brookfield's stake in Westinghouse is the reference precedent. The question is whether Cantus's structural value in equipment is large enough to justify principal capital, or whether the procurement-and-integration position is the durable winning posture.
- **How does the framework treat OEM-financed BTM equipment?** When an OEM finances the BTM plant (Wärtsilä has done this; reciprocating-engine vendors do this at smaller scale), the equipment counterparty is also a capital provider. This blurs Equipment, Services, and Markets (now containing Capital) simultaneously and needs explicit treatment.

---

*Drafting. Companion sub-industry pages forthcoming. Author of record: Dom Espinosa.*
