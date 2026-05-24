---
type: framework
status: drafting
audience: internal
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [power-sector, sub-industry, power-technology, cii, dealos]
sub_industry: power_technology
sub_industry_index: 10
related_thesis: ["[[Strategy/Cantus-Framework]]", "[[Products/CII-Iteration-Document]]", "[[DealOS/README]]"]
related_pages: ["[[Strategy/Power-Sector/Power-Equipment]]", "[[Strategy/Power-Sector/Power-Markets]]"]
---

# Power Technology — Sub-Industry Specification

*Sub-industry 10 of 10 in the Power sector framework. Drafting. This is the sub-industry into which Cantus's CII and DealOS products fit, while Cantus avoids becoming a generalist Power Technology vendor.*

---

## 1. Definition

Power Technology is the **digital and software layer across the Power sector** — the data, analytics, control systems, and platforms that make every other Power sub-industry operate, optimize, and integrate. The unit of production is software, data products, services, and integrated digital systems sold or deployed across Power Assets, Power Equipment, Power Services, Power Land, Power Industries, Power Commodities, Power Capital, Power Markets, and Power Retail. The defining condition is that the value created sits in the digital layer — code, data, models, and integrated platforms — rather than in physical infrastructure, manufactured equipment, or labor-and-engineering services.

The boundary against adjacent Power sub-industries:

- **Power Equipment** is physical hardware manufactured in a factory. Power Technology is the software embedded in or running alongside that hardware. The line is structurally blurring — modern grid-forming inverters, BESS systems, smart switchgear, and turbine controls are software-defined products where the digital layer increasingly drives the value. The framework convention is to treat embedded firmware as part of Equipment, and external software (asset performance management, energy management systems, dispatch optimization) as Technology.
- **Power Services** performs physical and engineering work. Power Technology provides software tools and platforms that enable Services. The line blurs when an O&M provider offers a software platform; the convention is that the labor-and-engineering core is Services and the software product is Technology.
- **Power Markets** is the clearing mechanism. Power Technology builds the trading platforms, data feeds, optimization software, and analytics. Nodal Exchange is Power Markets (the exchange); Yes Energy is Power Technology (the data layer).
- **Power Retail** is the customer interface. Power Technology provides the billing, customer engagement, DR software, and DER management platforms used by Retail providers and their customers.

Within Power Technology, twelve structural sub-segments:

1. **Grid management software** — DERMS (distributed energy resource management), ADMS (advanced distribution management), EMS (energy management systems), WAMS (wide-area measurement).
2. **Asset performance management (APM)** — condition-based monitoring, predictive maintenance, digital twin, fleet-level dashboards.
3. **SCADA / industrial controls** — operational technology at the substation, generation plant, and balance-of-plant level.
4. **Energy trading and risk management (ETRM)** — trade capture, position management, risk reporting, settlement.
5. **Customer engagement** — billing, customer information systems (CIS), customer self-service portals, demand-side management programs.
6. **DR and DER management** — aggregation platforms, BTM optimization, virtual power plant (VPP) orchestration.
7. **Market data and analytics** — real-time grid data, market data, weather analytics, forecasting, integrated decision-support.
8. **DCIM (data center infrastructure management)** — building management, power monitoring, cooling optimization, capacity planning at the hyperscale and colo level.
9. **Power-sector AI and ML applications** — algorithmic dispatch, load forecasting, asset-failure prediction, grid optimization, market prediction.
10. **Grid-edge platforms** — vehicle-to-grid (V2G), behind-the-meter optimization, residential and small-C&I optimization.
11. **OT cybersecurity** — operational technology cybersecurity specifically for grid, generation, and BES infrastructure under NERC CIP and broader frameworks.
12. **Carbon and ESG accounting** — scope 1/2/3 accounting platforms, attribute tracking, supply-chain emissions reporting.

## 2. Deliverables

Power Technology produces four classes of deliverable:

**Software product (license or SaaS)** — the application sold under a subscription or perpetual license, deployed on-prem, in cloud, or hybrid. Recurring SaaS economics increasingly dominant.

**Data product and feed** — real-time or historical data feeds (Yes Energy LMP, Genscape outage data, Wood Mackenzie forward curves, BNEF data subscription). Subscription economics with high gross margin.

**Integrated platform** — multi-application platforms integrating data, control, analytics, and reporting (GE Vernova GridOS, Schneider EcoStruxure, AspenTech / AVEVA Operations Control). Higher-touch, higher-ticket, longer sales cycle.

**Algorithmic dispatch / optimization service** — software-as-an-operator services (Tesla Autobidder, Eolian, Plus Power) where the technology provider also operates the asset in real time. The deliverable is the dispatch decision and the resulting revenue stack.

The commercial instruments are typical software contracts: MSAs and order forms for SaaS, perpetual license + maintenance for legacy on-prem, professional services agreements for implementation, data subscription agreements for feeds, revenue-share for dispatch-as-a-service.

## 3. Major Players (US-Focused)

### Grid management software (DERMS, ADMS, EMS)

GE Vernova Digital (GridOS, formerly GE Digital + Predix energy applications); Siemens Energy Spectrum Power; Schneider Electric (EcoStruxure ADMS, EcoStruxure DERMS, AutoGrid-acquired DERMS); Hitachi Energy (formerly ABB) e-mesh, Asset Suite; AVEVA Operations Control (Schneider-owned); Itron (residential + grid software); Landis+Gyr; OSI Inc (now Open Systems International, acquired by Emerson); ETAP (operational technology consulting + software); Survalent.

### Asset performance management (APM)

Uptake (Cat-spinout, industrial APM); AspenTech (now Emerson-owned, includes IP21 and broader APM); C3 AI (energy vertical strong); AVEVA APM (Schneider); Bentley Systems (infrastructure-asset APM); Itron Field Asset Management; Hitachi Lumada (industrial APM); SparkCognition; Augury (industrial sensor + AI); Senseye (Siemens-owned).

### SCADA and industrial controls

Honeywell Process Solutions; Emerson Automation; Yokogawa; Rockwell Automation; Schneider Modicon; Siemens Process Automation; ABB Ability Process; Mitsubishi Electric. These vendors span Power, Oil & Gas, and broader process industries.

### Energy trading and risk management (ETRM)

Allegro Development (ION-owned, the dominant US Power ETRM); Openlink (ION-owned, Endur platform; combined with Aspect); Sapient Global Markets (Publicis-owned); ION Commodities (parent of multiple platforms); AspenTech ETRM; SAP Commodity Management; OATI (smaller market participants); Eka Software Solutions; ZE PowerGroup (data services adjacent).

### DCIM

Vertiv (NYSE: VRT; the largest pure-play); Schneider Electric EcoStruxure IT (DCIM market leader by share); Sunbird (DCIM specialist); Nlyte (DCIM specialist); Cormant; iTRACS (CommScope subsidiary); Modius; Device42. The DCIM market overlaps with Power Industries demand-side software at hyperscale and colo facilities.

### Power-sector AI and ML applications

C3 AI (broad energy applications); Palantir (energy practice with Constellation and others); Stem (AI-driven commercial storage; public NYSE: STEM); Tesla Energy Operations (Autobidder for BESS dispatch); Eolian (BESS dispatch AI); Plus Power (BESS dispatch); ABB Ability Energy Manager; GE Vernova GridOS AI; Octopus Energy Kraken (technology platform); SparkCognition.

### Customer engagement and CIS

Oracle Utilities (Customer Care & Billing, Meter Data Management — dominant US CIS); SAP IS-U for Utilities; Itron Customer Insights; Landis+Gyr software; Bidgely (residential analytics); AutoGrid (Schneider-owned, customer engagement); Uplight (residential engagement, recently public via SPAC merger then partial restructure); Sense (residential energy monitoring); Whisker Labs (Ting product); Centrica Hive (UK-origin, US presence).

### DR and DER management

Voltus (DR aggregation + technology); AutoGrid (Schneider Electric); Generac Grid Services; Octopus Energy Kraken (UK-origin tech platform); OPower (Oracle-owned residential engagement); Bidgely; Uplight; Tesla Energy (Autobidder + VPP); Stem (commercial); Sunrun (residential solar + storage + DR); Enchanted Rock (BTM gas dispatch); Camus Energy (grid management); Utilidata (grid edge); Singularity Energy (grid carbon analytics).

### Market data and analytics

Yes Energy (real-time settlement data); Genscape (Wood Mackenzie-owned, real-time market intelligence); Wood Mackenzie (analytics); S&P Global Commodity Insights (formerly Platts); BNEF (Bloomberg subsidiary); Argus; ICIS; Energy Acuity; LCG Consulting; ABB Velocity Suite; Hitachi Energy Ability; Modo Energy (UK-origin BESS analytics with US expansion).

### OT cybersecurity

Dragos (the dominant OT-cyber pure-play); Claroty; Nozomi Networks; Industrial Defender; Honeywell Forge OT Cyber; Mission Secure; OPSWAT; Tenable OT Security; Armis; Verve Industrial.

### Carbon and ESG accounting

Watershed (broad enterprise scope 1/2/3); Persefoni; Sweep; Position Green; Workiva ESG Reporting; Salesforce Net Zero Cloud; Climatiq; Carbon Trust services; Mainspring Energy (also generation); ClimeCo (advisory + technology); EcoVadis (supply chain); Onehouse (data engineering with ESG application).

### Hyperscalers as Power Technology providers

AWS Energy & Utilities (vertical practice, including AWS for Energy, recent GE Vernova partnership); Microsoft Energy Industry Cloud (Energy Data Services, Sustainability Manager); Google Cloud Energy Industry Solutions (carbon intelligence, energy demand forecasting); Oracle Utilities (CC&B, MDM, Network Management); Salesforce Energy & Utilities Cloud; ServiceNow Utilities. The hyperscalers are increasingly material as Power Technology vendors selling into the sector while also being Power Industries operators.

### Power-sector specialized startups (illustrative subset)

Camus Energy (grid management); Utilidata (grid edge analytics); Singularity Energy (carbon analytics); Span (electrical panel); Lunar Energy (residential + utility platform); Wallbox (EV charging); Optiwatt (EV charging optimization); Octopus Energy Kraken (US expansion); Switched Source (transformer monitoring); ev.energy (EV smart charging); WeaveGrid (utility EV integration); ChargeHub; Singularity Energy.

## 4. Capital Structures and Economics

Power Technology is **venture- and growth-equity-funded** at the early stages and **strategic-corporate or PE-owned** at maturity. Capital structure resembles enterprise software broadly, with sub-industry-specific overlays:

### Capital deployed by stage

| Stage | Capital model | Returns target |
|---|---|---|
| Early-stage venture (seed, Series A) | Venture equity | Power-law returns; 10x+ on winners |
| Growth-stage venture (Series B–D) | Growth equity | 3–10x on winners |
| Late-stage growth | Crossover capital, late venture | 2–5x on winners |
| Strategic acquisition (by Schneider, ABB, GE Vernova, Siemens, Honeywell, Emerson, Itron, Oracle) | Corporate balance sheet | Strategic ROI |
| Public market | Public equity | Market multiple |
| Private equity (mature) | LBO / growth buyout | 15–25% IRR |

### Margins (typical for SaaS / data businesses at scale)

| Metric | Range |
|---|---|
| Gross margin (SaaS, pure software) | 70–85% |
| Gross margin (data product) | 60–80% |
| Gross margin (platform with services) | 50–70% |
| EBITDA margin (at scale, mature SaaS) | 25–40% |
| R&D as % of revenue | 15–30% (still investing) |
| S&M as % of revenue | 25–45% (depends on go-to-market) |

### Valuation references

| Stage | EV/ARR multiple |
|---|---|
| Growth SaaS (Power-sector vertical) | 5–12x |
| Strategic acquisition by industrial prime | 4–10x |
| Public Power Tech (Itron, Vertiv) | 3–8x revenue depending on growth |
| Public utility-vertical SaaS (Stem) | Variable, currently distressed |

The capital structure of mature Power Technology businesses converges on strategic-acquirer ownership. Schneider Electric, ABB / Hitachi Energy, GE Vernova, Siemens Energy, Honeywell, Emerson (via AspenTech acquisition), Itron, Oracle, and the hyperscalers are the dominant acquirers. Recent transactions: Schneider's AutoGrid (2022); Emerson's AspenTech (2022, completed 2024); GE Digital reorganization into GE Vernova Digital (2024); Honeywell's industrial software focus.

### Recurring revenue economics

Power Technology businesses run on standard SaaS economics: annual contract value (ACV), gross dollar retention (GDR > 90% target), net dollar retention (NDR > 110% target for healthy businesses), customer acquisition cost payback (24-36 months typical for enterprise). The sub-industry-specific overlays are: long enterprise sales cycles (12-24 months for utility customers), heavy professional-services attach, multi-year contracts, and very-low churn once deployed (high switching cost in operational software).

## 5. Counterparty Universe

| Counterparty | Interaction |
|---|---|
| Power Assets (utilities, IPPs, infra-fund operators) | Primary buyer of grid management, APM, ETRM, OT cyber. |
| Power Equipment (OEMs) | Both partner (OEM-embedded software) and competitor (OEMs selling integrated software). |
| Power Services (EPCs, O&M) | Buyer of project software, commissioning tools, asset management. |
| Power Industries (hyperscalers, manufacturers, defense) | Buyer of DCIM, sustainability accounting, energy management. |
| Power Markets (ISOs, trading firms) | Buyer of ETRM, market data, dispatch optimization. |
| Power Retail (REPs, CCAs) | Buyer of CIS, customer engagement, DR aggregation. |
| Power Capital (infra funds, banks) | Buyer of analytics for portfolio management, ESG reporting. |
| Power Land (developers) | Buyer of geospatial analytics, site selection tools. |
| Power Commodities (trading houses, exchanges) | Buyer of market data, settlement systems. |
| Hyperscaler infrastructure (AWS, Azure, GCP) | Cloud hosting, partnership, and increasingly competitor in sector vertical software. |
| FERC / NERC | Cybersecurity standards (CIP), reliability data reporting requirements. |
| Standards bodies | IEEE 1547 (DER), IEC 61850 (substation automation), OpenADR, OpenFMB. |
| Investor base (VCs, growth equity, strategics) | Capital providers and acquirers. |

## 6. Regulatory Environment

Power Technology is regulated less by a single sectoral regulator and more by **the layered intersection** of OT-cybersecurity standards, data-privacy regulation, software-procurement standards at regulated utilities, and trade controls on certain advanced software.

**Federal**

- **NERC CIP (Critical Infrastructure Protection)** — cybersecurity standards for the Bulk Electric System; mandatory for entities operating BES assets; the dominant compliance framework for OT software in Power Assets.
- **FERC** — approves NERC standards; oversees software-related grid reliability through orders intersecting with cybersecurity (Order 887 on Bulk Electric System cyber systems; Order 829 on supply-chain cyber).
- **CISA (Cybersecurity and Infrastructure Security Agency)** — operational coordination for critical-infrastructure cybersecurity, including Power sector. CISA's Cybersecurity Performance Goals and sector-coordinated frameworks shape vendor and operator expectations.
- **NIST** — Cybersecurity Framework (CSF 2.0), NIST 800-53, NIST 800-82 (industrial control systems). Voluntary but de facto baseline.
- **DOE Cybersecurity, Energy Security, and Emergency Response (CESER)** — programs supporting sectoral cybersecurity.
- **BIS** — export controls on certain advanced software (AI for critical infrastructure, encryption above thresholds, cybersecurity software in some sub-categories).
- **FTC** — data privacy, deceptive practices in consumer-facing energy software.
- **SEC** — cybersecurity disclosure rules (2023 final rule); ESG reporting rule litigation and partial implementation.

**State**

- **State PUCs** — software procurement standards for regulated utilities (some states mandate competitive procurement above thresholds); customer-data privacy frameworks (California CPRA, Virginia VCDPA, others); CIS / billing system oversight.
- **State Attorneys General** — consumer data privacy enforcement.

**International / cross-border**

- **EU GDPR** — applies to US Power Technology vendors with EU customers; data privacy and cross-border data flow.
- **CFIUS** — foreign investment review of Power Technology acquisitions; recent activity around critical-infrastructure software acquisitions.

**Industry standards**

- IEEE 1547 (DER interconnection), IEC 61850 (substation automation communication), OpenADR (demand response), OpenFMB (field message bus), CIM (Common Information Model), Multispeak (utility-software integration), SunSpec (solar communications), MESA (modular energy storage).

## 7. Cantus's Relationship to Power Technology

The v2 framework places Power Technology inside the **Cantus Technology** vertical alongside Power Machines. Cantus Technology operates as **orchestrator + selective operator** across both sub-industries: orchestrating the Power Technology layer across all Cantus campuses, and selectively operating in specific Power Technology and Power Machine sub-segments where the integration economics justify principal capital. "Technology makes them productive" in the firm's value-creation sequence.

CII and DealOS — Cantus's proprietary integration intelligence and deal-level operating system — are explicitly placed as **Foundations** in the v2 architecture, cross-cutting all four verticals (Development, Infrastructure, Technology, Markets) rather than residing inside Cantus Technology. The Foundation framing reflects that CII compounds across the entire firm rather than being the property of any one vertical. See [[Products/CII-Iteration-Document]] and [[DealOS/README]].

### By role within Cantus Technology vertical

- **Power Technology orchestrator for Cantus campuses.** Cantus Technology selects, integrates, and operates the Power Technology stack across Cantus campuses — DCIM at tenant fence-line, BMS/EMS at campus level, DERMS for grid-edge optimization, OT cybersecurity for Facility infrastructure, ETRM for any market-facing activity, structured-product analytics for capital-partner reporting. External vendor selection (Vertiv, Schneider EcoStruxure, AutoGrid, Dragos, Honeywell Forge) is matched to campus needs.
- **Power Machines orchestrator and selective operator.** Per [[Strategy/Power-Sector/Power-Machines]], Cantus Technology specifies Machine deployment (GPUs, robotics, electrolyzers, bioreactors) for tenant campuses and selectively operates principal businesses in specific Machine sub-segments.
- **Cantus Compute as selective operator.** Hosted GPU compute on Cantus campuses (the Crusoe-style vertical-integration adjacent business, structurally differentiated by Cantus's integrated Land + Facility + Infrastructure stack). The scope and customer base are open questions for the business plan rewrite.
- **Possible Cantus Robotics (future selective operator).** Robotics-as-a-service for industrial tenants, particularly Advanced Manufacturing and Defense Industrial Base. Compounding-phase or later.
- **Power Technology software integrator, not Power Technology software vendor.** Cantus Technology does not build DERMS, ADMS, EMS, OT cyber, ETRM, or DCIM as standalone products to sell to the broader Power sector. The temptation to broaden into market-facing software is explicit and is explicitly rejected.

### By phase

**Building (Years 1–2) — current.** Power Technology vendor selection and OEM relationship-building for Cantus campuses. CII data asset construction and DealOS specification work (as cross-vertical Foundations). Cantus Compute concept articulation; initial GPU slot positions explored.

**Activation (Years 3–4) — modeled.** Cantus Technology vertical operational across Cantus campuses. Cantus Compute hosted-GPU pilot in one or two campuses. Fund I capital allocated. Selective Power Machine procurement aggregation across multi-campus pipeline.

**Compounding (Years 5–7) — modeled.** Cantus Compute at scale across multiple campuses; possibly external customer base beyond Cantus tenants. Cantus Robotics articulated and possibly initiating. Power Technology integration intelligence institutionalized.

**Mature platform (Years 8+).** Cantus Technology as a recognized vertical operating across all Cantus campuses, with Cantus Compute (and possibly Cantus Robotics) as identified principal businesses inside.

### CII and DealOS as Foundations (not inside Cantus Technology vertical)

CII and DealOS compound across all four verticals — Development, Infrastructure, Technology, Markets — rather than residing inside any one vertical. The Foundation framing parallels Labor/Community as a Foundation that flows across all four verticals. Specific Foundation-level capabilities:

- **CII data assets** — 23 data assets across parcel, tenant, capital, regulatory, and operational families, populating intelligence used by every vertical.
- **CII prediction-and-resolution loops** — site validation, tenant match, capital routing, regulatory intelligence — each loop runs across verticals.
- **DealOS** — deal-level operating system used by Development for site formation, Infrastructure for build orchestration, Technology for machine and software specification, Markets for capital and commercial structuring.
- **Parcel Registry** — geospatial parcel-scored database; primarily Development-facing but cross-referenced by Markets for commercial structuring.

### What Cantus does not become

Cantus does not become a Power Technology software vendor competing in DERMS, ADMS, ETRM, DCIM, OT cyber, or carbon accounting. Cantus does not compete with Schneider Electric, ABB / Hitachi Energy, GE Vernova, Siemens Energy, Honeywell, Emerson / AspenTech, Itron, Oracle, or the hyperscaler vertical software plays. The boundary is structural: Cantus's technology activity is *operational support to the integrated production*, not market product. The selective-operator role applies to specific Power Machine businesses (Cantus Compute, possibly Cantus Robotics) and to Foundation-level integration intelligence (CII, DealOS) — neither of which is a Power Technology software product competing for general utility-or-IPP customers.

### The integrated-tech claim

The structural claim Cantus Technology makes about Power Technology is that the integration of Machines + Software inside a Cantus campus is itself the product. The Power Technology vendor cohort (Schneider, ABB, Vertiv, etc.) sells point products; the hyperscaler vertical-software plays sell platform-as-a-service to existing utility customers. Neither delivers the *integrated* Machine + Software + Power + Land + Workforce platform that a Cantus Intelligent Campus combines. Cantus Technology's contribution is the integration; the selective operating businesses (Cantus Compute, etc.) sit on top of that integration as the principal layer where the integration creates structural advantage that justifies principal capital.

## 8. Key Trends and Structural Conditions (2026–2036)

**1. Grid-edge software explosion.** DERMS, DER aggregation, V2G, BTM optimization, and grid-edge platforms are the highest-growth subsegment of Power Technology. Utility adoption is uneven but accelerating; the AutoGrid / Schneider acquisition, Octopus Energy Kraken's US expansion, and the growth of David Energy / Voltus / Camus / Utilidata are the visible signals. The structural driver is the explosion of distributed resources and the inability of legacy grid software to manage them.

**2. AI and ML applied to grid optimization.** Algorithmic dispatch (Tesla Autobidder, Eolian, Plus Power, Stem) has matured into a structural feature of the BESS market. Load forecasting, asset-failure prediction, market prediction, and grid-state estimation are increasingly AI-driven. The hyperscaler vertical-software plays (AWS, Azure, GCP energy industry clouds) are explicitly betting on AI as the differentiator.

**3. Behind-the-meter platform consolidation.** Residential and small-commercial BTM platforms (Sunrun, Tesla Energy, Span, Lunar Energy, Sense, Bidgely, Uplight) have been through consolidation cycles. The structural pattern is convergence between solar installer, storage installer, and software platform — with the hyperscaler-as-customer relationship (Tesla, Apple, etc.) increasingly material.

**4. ETRM modernization.** Legacy ETRM systems (Allegro, Endur, AspenTech) are aging. ION's consolidation of multiple legacy platforms has slowed innovation. The structural opportunity for new entrants is real but the enterprise-software inertia is large.

**5. OT cybersecurity rising priority.** Dragos, Claroty, Nozomi, and Industrial Defender have built large pure-play OT cybersecurity businesses. NERC CIP requirements, increasing nation-state threats (Volt Typhoon, others), and CISA coordination are driving sustained OT-cyber investment from utility and IPP buyers. The sub-segment is one of the most defensible in Power Technology.

**6. Carbon accounting platform consolidation.** Watershed, Persefoni, Sweep, and the broader carbon-accounting cohort have been through a venture cycle. The integration of carbon accounting into core ERP (SAP, Oracle, Salesforce Net Zero Cloud, Workiva) is the structural endpoint. Standalone platforms are consolidating or becoming features inside ERP.

**7. Vehicle-to-grid (V2G) software emergence.** Bidirectional EV charging is moving from pilot to commercial. WeaveGrid, ev.energy, Wallbox, Optiwatt are scaling. The structural enabler is utility tariff design (more than the technology), but Power Technology vendors are building ahead of the demand.

**8. Compute as a grid asset.** AI compute can curtail, time-shift, and even respond to grid signals. The structural insight that compute workloads (especially training, which is more time-flexible than inference) can be treated as flexible grid load is being commercialized. This sits at the intersection of Power Industries, Power Markets, and Power Technology and is one of the more interesting strategic frontiers for Cantus's Compute-vector tenants.

**9. Data center operations AI.** DCIM is being reshaped by AI applied to cooling optimization, power management, capacity planning, and capacity scheduling. Hyperscaler-internal teams and Vertiv / Schneider EcoStruxure are the dominant developers. The implication for Cantus campus design is that the demand-side software stack is becoming as differentiated as the supply-side software stack.

**10. Power-sector vertical LLM applications.** Large language model deployment for sector-specific workflows (interconnection-process automation, regulatory-document review, market-rule analysis, integrated diligence on campus deals) is in early commercialization. The hyperscalers, sector-vertical AI startups (C3 AI, Palantir, several stealth-mode entrants), and internal teams at utilities and IPPs are building. CII has explicit LLM-augmented agent layers in the DealOS spec, fitting this trend.

## 9. Open Questions for the Framework Rewrite

To resolve as the framework matures:

- **CII boundary between internal capability and external product.** Under v2, CII is a Foundation cross-cutting all four verticals (decision locked in). The remaining question is whether selected CII surfaces externalize to capital partners, tenants, and co-development partners under controlled access — and the threshold criteria that gate each surface.
- **DealOS as a Cantus product vs. a Cantus internal system.** [[DealOS/README]] articulates DealOS as a deal operating system. The question is whether DealOS ever becomes a market-facing product (licensed to other integrators, capital partners) or remains a closed internal system. Strong default position is closed internal, but the framework should specify.
- **Cantus's posture on V2G, grid-edge, and BTM platforms for tenants.** Should Cantus campuses integrate external Power Technology vendors (Tesla Autobidder, Voltus DR, AutoGrid DERMS) or build the campus operating layer in-house under CII / DealOS? The make/buy decision needs an explicit framework.
- **OT cybersecurity for Cantus campus operations.** Campus operations include critical-infrastructure cybersecurity requirements. The framework should specify whether Cantus operates its own OT cyber capability or relies on contracted vendors (Dragos, Claroty, Honeywell Forge).
- **Compute-as-grid-asset as a Cantus strategic frontier.** This intersects Power Industries (Cantus Compute), Power Markets (ancillary participation), and Power Technology (the algorithmic dispatch software). The framework should specify whether Cantus actively develops this as a Cantus Compute / Cantus Edge offering, or whether it remains an integration the firm structures around external participants.

---

*Drafting. Final sub-industry page in the Power sector framework. All ten sub-industries are now drafted at depth; the framework is ready for the thesis and business plan rewrite.*

*Author of record: Dom Espinosa.*
