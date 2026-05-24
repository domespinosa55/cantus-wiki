---
type: framework
status: drafting
audience: internal
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [power-sector, sub-industry, power-facilities, cantus-development]
sub_industry: power_facilities
sub_industry_index: 5
related_thesis: ["[[Strategy/Cantus-Framework]]"]
related_pages: ["[[Strategy/Power-Sector/Power-Land]]", "[[Strategy/Power-Sector/Power-Industries]]", "[[Strategy/Power-Sector/Power-Machines]]"]
---

# Power Facilities — Sub-Industry Specification

*Sub-industry 5 of 10 in the Power sector framework v2. Drafting. Cantus Development is the direct-principal arm operating in this sub-industry alongside Power Land.*

---

## 1. Definition

Power Facilities is the **physical-load-center** sub-industry — the buildings, campuses, and built environments that convert power access into productive industrial capacity. The unit of production is the constructed facility: a hyperscale AI data center, a colocation data center, a semiconductor fab, a battery gigafactory, a defense manufacturing plant, a critical-materials processing facility, a CDMO biopharma plant, an advanced-manufacturing site. The defining condition is that the structure exists to convert sustained power input (typically tens to hundreds of megawatts continuous) into the productive output of a Power Industries operator.

The boundary against adjacent Power sub-industries:

- **Power Land** is the substrate — the assembled, entitled, interconnection-attached real estate. Facilities is the constructed building or campus that sits on the land. A 200-acre powered industrial tract is Power Land; the 1.5M sq ft data center sitting on it is Power Facilities.
- **Power Industries** is the operator on the marquee — Microsoft, TSMC, Tesla, Anduril, Lilly. Facilities is the building they operate inside. The same company often owns both layers (Microsoft builds and operates its data halls; TSMC builds and operates its fabs), but the Facility and the operation are different deliverables. The building is real estate plus base-building MEP; the operation is the workload, the production process, the commercial output.
- **Power Machines** is the productive equipment *inside* the Facility — the GPUs, the lithography tools, the battery cell lines, the robotics, the bioreactors. The Facility houses the Machines; the Machines convert the electrons into output.
- **Power Assets** is generation, transmission, substation, distribution — the supply side of the meter. Facility-level UPS, embedded BESS, and on-site emergency generation sit at the boundary; the framework convention is to treat dedicated demand-side power equipment serving a single Facility as part of that Facility's base-building MEP rather than as Power Assets.
- **Power Services** builds and operates Facilities through EPC and O&M. Services is the labor and engineering; Facilities is the constructed output.

Within Power Facilities, twelve structural sub-segments by industrial use class:

1. **Hyperscale AI campuses** — purpose-built for high-density AI training and inference; liquid-cooled increasingly default; 100–500MW per campus typical, growing toward 1GW+.
2. **Hyperscale traditional cloud data centers** — air-cooled, lower density, multi-tenant or single-tenant; 50–200MW per facility.
3. **Colocation data centers** — multi-tenant, retail-and-wholesale colo, Equinix and Digital Realty model.
4. **Edge data centers** — smaller, distributed, latency-sensitive workloads.
5. **Semiconductor fabs** — leading-edge ($15–25B per fab) and mature node ($3–6B per fab).
6. **Battery gigafactories** — cell, module, pack manufacturing; $1.5–3B per ~30GWh nameplate.
7. **EV assembly plants** — vehicle manufacturing; $1–3B per plant.
8. **Solar and wind manufacturing facilities** — module, wafer, cell, turbine component manufacturing.
9. **Hydrogen production facilities** — electrolysis, blue hydrogen, e-fuels production.
10. **Critical minerals processing facilities** — refining, separation, downstream chemistry; $0.5–2B per facility.
11. **Defense manufacturing facilities** — munitions, missiles, drones, aerospace structures, energetic materials, ship and submarine yards.
12. **Biomanufacturing facilities** — biopharma (large molecule, fill-finish, advanced therapy), bioindustrial, synthetic biology, CDMO.

## 2. Deliverables

Power Facilities produces four classes of deliverable, increasingly layered:

**Built shell and core** — the physical structure (concrete, steel, building envelope) and the base-building MEP (cooling, electrical distribution within the facility, fire suppression, security, vertical transportation). For data centers, this is typically delivered as "cold shell" (envelope + structure + utility tie-ins, no critical environment) or "warm shell" (shell + core MEP, ready for white-space fit-out).

**Critical environment fit-out** — for data centers, the UPS, generators, CRAH/CRAC cooling, PDU, raised floor or slab, and white-space layout. For fabs, the cleanroom (Class 1 / Class 10 / Class 100), the chemical and gas distribution, the wafer-handling layout, the bay-and-chase configuration. For gigafactories, the dry room, the coating line layout, the formation cycling. For biomanufacturing, the cleanroom classification and the suite layout.

**Operating systems for the facility** — building management systems (BMS), energy management systems, security systems, fire and life safety, access control, environmental monitoring. Increasingly software-defined and integrated with Power Technology layers.

**Commercial instruments** — the lease, build-to-suit (BTS) arrangement, ground lease + facility lease, sale-leaseback, condo structure (rare), or owner-occupier title that conveys facility access to the Power Industries operator. The standard data-center BTS arrangement and the standard fab/gigafactory owner-occupier model are the two dominant patterns.

## 3. Major Players (US-Focused)

### Hyperscale AI campus developers and operators (often the same entity)

Microsoft Azure, Amazon AWS, Google Cloud, Meta, Oracle Cloud, Apple — all build and operate at scale; some lease from BTS developers. xAI (Colossus). CoreWeave (lease-and-operate hybrid). The hyperscalers operate as both Industries (the workload) and Facilities (the building) at varying integration levels.

### BTS data center developers (build for hyperscale tenant lease)

Aligned Data Centers; Compass Datacenters; Stack Infrastructure; Vantage Data Centers; QTS Realty Trust (Blackstone-owned); T5 Data Centers; Stream Data Centers; NTT GDC; CyrusOne (KKR/GIP-owned); EdgeConneX (EQT-owned); Cologix. These firms develop facilities for hyperscaler tenants under multi-decade lease arrangements.

### Colocation developers and operators

Equinix (EQIX); Digital Realty (DLR); CyrusOne (overlapping with BTS); DataBank; Switch (DigitalBridge-owned); Iron Mountain (data center segment).

### Edge and specialty data center developers

EdgeConneX; American Tower (Edge); 365 Data Centers; DataBank Edge. Lower scale, geographically dispersed.

### Semiconductor fab developers/operators (typically the operator owns the facility)

TSMC (Arizona, multi-fab buildout); Intel (Ohio, Arizona, New Mexico); Samsung (Texas, Taylor); Micron (NY, ID); GlobalFoundries (NY); Texas Instruments (Texas, Utah); Wolfspeed (NC, NY). The fab building and the fab operation are typically combined under the operator's balance sheet.

### Battery gigafactory developers/operators

LG Energy Solution; Samsung SDI; SK On; Panasonic; CATL (limited US); BYD (limited US). Joint ventures with EV OEMs are common (LG-GM Ultium Cells; Ford-SK BlueOval City; Toyota-Panasonic; etc.) — the JV typically owns the facility.

### EV assembly plant developers

Tesla; Ford; GM; Rivian; Lucid; Hyundai (Metaplant Georgia); Toyota; Honda. The OEMs own the facilities.

### Defense manufacturing facility developers

Lockheed Martin; Raytheon (RTX); Northrop Grumman; General Dynamics; Boeing Defense; BAE Systems Inc.; HII (shipbuilding); L3Harris; Anduril (rapidly scaling). The defense prime typically owns the facility, sometimes with co-investment from DoD via DPA Title III.

### Biopharma facility developers

Eli Lilly; Merck; Pfizer; Moderna; Catalent (CDMO); Lonza (CDMO); Resilience; Samsung Biologics (announced US). Mix of owner-occupier (large pharma) and CDMO-developed (Lonza, Catalent build CDMO facilities for multiple customers).

### Critical materials processing facility developers

MP Materials (CA rare earth refining); Albemarle (lithium); Arcadium Lithium; IperionX (titanium); Energy Fuels (uranium + rare earths); USA Rare Earth; Westwin Elements (nickel + cobalt); Lynas (Texas project). DoD and DOE co-investment via DPA Title III and LPO is structurally significant.

### Specialty Facility EPC developers (build for operator-tenant)

Holder Construction (DC-heavy); Mortenson (DC + renewables); DPR Construction; Whiting-Turner; Skanska USA; AECOM Hunt; Turner Construction; McCarthy Building. These contractors build the facilities under EPC contracts; the operator is the principal. See [[Strategy/Power-Sector/Power-Services]] for the Services-side framing.

### Specialty cooling and critical environment vendors

Vertiv (NYSE: VRT) — racks, UPS, cooling, power distribution; Schneider Electric EcoStruxure (DCIM and critical environment); ABB; Eaton; Stulz; CoolIT (liquid cooling); CoolerMaster; Asetek (liquid cooling). The supply chain for liquid cooling has tightened significantly with the AI workload shift.

## 4. Capital Structures and Economics

Power Facilities is **highly capital-intensive** and the capital structure depends on whether the facility is operator-owned (corporate balance sheet) or BTS-developer-owned (real-estate-financed). The two patterns produce different economics.

### Capital intensity by Facility class

| Facility class | Capital intensity |
|---|---|
| Hyperscale AI data center (shell + critical env, ex-IT) | $10–15M / MW |
| Hyperscale AI data center (all-in, including Machines) | $25–40M / MW |
| Hyperscale traditional cloud DC (shell + critical env) | $7–12M / MW |
| Colocation data center | $8–13M / MW |
| Semiconductor fab (leading-edge) | $15–25B per fab |
| Semiconductor fab (mature node) | $3–6B per fab |
| Battery gigafactory | $1.5–3B per 30 GWh |
| EV assembly plant | $1–3B per plant |
| Solar PV manufacturing facility (cell + module) | $0.5–1.5B per GW |
| Hydrogen production facility (large electrolysis) | $1–2B per GW capacity |
| Critical minerals processing facility | $0.5–2B per facility |
| Defense manufacturing facility | $0.5–5B per facility |
| Biopharma large-molecule manufacturing | $1–4B per major facility |

### Capital structures by Facility type

**Hyperscale-owned data centers** — corporate balance sheet at Microsoft/Amazon/Google/Meta/Oracle; supplemented by sustainability bonds and increasingly by project-finance structures for $10B+ facilities. The shift from corporate-balance-sheet to project-financed at the largest scale is one of the most consequential capital-structure shifts of 2024–2026.

**BTS data centers** — real-estate-financed under sponsor + REIT + infra fund structures. Aligned, Compass, Stack, Vantage, QTS, T5, NTT GDC, CyrusOne operate on this model. Lease economics determine the financing: a 15–20 year triple-net BTS lease to a hyperscaler at IG covenant supports $1B+ of project finance at attractive cost. Cap rates 7–10% on stabilized lease.

**Colocation** — REIT-financed (Equinix, Digital Realty as public REITs); private REIT (CyrusOne, Switch); infrastructure-fund-financed (KKR-GIP owns CyrusOne, Blackstone owns QTS). Cap rates 5–7% on stabilized.

**Semiconductor fabs** — operator balance sheet + CHIPS Act grants + 48D ITC (25% Advanced Manufacturing Investment Credit) + Treasury direct-pay election. The CHIPS framework provides ~$39B of direct grants; the ITC layers on top.

**Battery gigafactories** — sponsor equity (typically a strategic OEM JV) + IRA 45X credits ($45/kWh integrated US production) + DOE LPO loans + state incentive packages.

**EV assembly plants** — corporate balance sheet, sometimes with state incentive package adding 5–15% of capex.

**Hydrogen production facilities** — IRA 45V (10-year PTC) + DOE Hydrogen Hubs program + sponsor equity + project finance. Pre-commercial at scale; underwriting carries 45V interpretation risk.

**Critical minerals facilities** — DPA Title III grants + DOE LPO loans + DoD IBAS + sovereign capital + corporate equity. Industrial-policy capital is structurally significant.

**Defense facilities** — corporate balance sheet + DPA Title III + cost-plus contracts that effectively amortize facility capex into product pricing.

**Biopharma facilities** — corporate equity (large pharma) + project finance (CDMOs) + BARDA contracts (biodefense-relevant).

### Returns

| Facility class | Return / yield reference |
|---|---|
| Hyperscale BTS lease (data center) | 7–10% cap rate on stabilized |
| Colocation (operator P&L) | 12–18% ROIC at top of cycle |
| Semiconductor fab (operator P&L) | 15–25% ROE through-cycle |
| Battery gigafactory (operator P&L) | Currently squeezed; supported by 45X |
| EV assembly (operator P&L) | -10% to 15% (Tesla profitable; legacy mixed) |
| Hydrogen production | Pre-commercial; modeled 8–14% with 45V |
| Critical minerals refining | Variable; supported by industrial-policy capital |
| Defense facilities (operator P&L) | 12–18% ROE (top primes) |
| Biopharma large-molecule | 20–35% ROIC branded pharma; 12–20% CDMO |

### Hyperscale BTS lease economics (the most active Facility sub-segment)

The triple-net BTS lease to a hyperscale tenant is one of the most active capital-structure categories in Power Facilities. Standard structure:

- 15–20 year initial term + multiple 5-year renewal options
- Triple-net (tenant pays opex, taxes, insurance)
- Annual escalators (CPI-linked or fixed 2–3%)
- Hyperscaler corporate guarantee (Microsoft, AWS, Google, Meta, Oracle IG credit)
- $80–120 per kW-month rent on shell-plus-critical-environment
- Capital partners: REIT capital, infra fund (Brookfield, BlackRock, Stonepeak, KKR), Canadian pension, sovereign wealth

### Lead times and supply chain constraints

The build cycle for a Facility is gated by:

- Concrete and steel supply (currently tight)
- Specialty MEP supply — UPS, generators, switchgear, large cooling units (extending 18–24 months for AI-grade equipment)
- Specialty cooling (liquid cooling supply chain newly constrained)
- Labor (the workforce constraint detailed in [[Strategy/Power-Sector/Power-Services]])
- Permitting and entitlement (Land-side; constraint precedes Facility)
- Interconnection energization (often the binding constraint on operational readiness rather than facility construction itself)

Typical Facility build cycle: 18–30 months from groundbreaking to substantial completion for data centers; 30–48 months for fabs; 24–36 months for gigafactories; 24–60 months for nuclear-adjacent facilities.

## 5. Counterparty Universe

| Counterparty | Interaction |
|---|---|
| Power Industries (operator) | The tenant or owner-occupier; the principal customer for the Facility. |
| Power Land (developer) | The substrate; assembled and entitled land where Facility sits. |
| Power Assets (utilities, IPPs) | Power supply to the Facility through grid + BTM arrangements. |
| Power Equipment (OEMs) | UPS, generators, substation equipment, large cooling units. |
| Power Machines (vendors) | Productive equipment installed inside the Facility (GPUs, lithography, robotics, bioreactors). |
| Power Services (EPC, O&M) | Construction, commissioning, ongoing operations. |
| Power Technology (DCIM, BMS, controls) | Software layer over Facility operations. |
| Power Markets (lease and capital structuring) | Lease structuring, project finance, capital deployment. |
| Local government (zoning, building permits, incentives) | Entitlement, building permits, incentive packages, infrastructure cost-sharing. |
| Utilities (TSPs / TDSPs) | Interconnection, large-load tariff structuring, water and gas service. |
| Insurance | Builder's risk, property insurance, business interruption. |
| Engineers and architects | Facility design (electrical, mechanical, structural, architectural). |
| Specialty consultants | Mission-critical design (HDR, kW Mission Critical, Syska Hennessy); cleanroom design; gigafactory layout; biopharma cGMP. |
| Cybersecurity | Both physical and OT cybersecurity for sensitive Facilities (defense, biopharma, critical minerals). |

## 6. Regulatory Environment

Power Facilities is regulated primarily at the **local and state level** (zoning, building permits, environmental review, water rights, fire and life safety), with federal overlays for specific facility classes (FDA for biopharma, NRC for nuclear-adjacent, ITAR/BIS for defense, EPA for emissions and waste).

**Federal — by Facility class**

- **EPA** — fab emissions (PFAS, VOC, GHG), battery facility waste, biomanufacturing solvent handling.
- **OSHA** — facility construction and operations safety.
- **FDA** — biopharma cGMP, food and drug facility regulation.
- **NRC** — nuclear-adjacent facilities (fuel handling, nuclear medicine).
- **ITAR / EAR / BIS** — defense and dual-use technology facilities.
- **CFIUS** — foreign investment review for sensitive Facility ownership.
- **CISA** — critical-infrastructure cyber for select Facility classes.
- **DoD** — facility security and IBAS for defense industrial base.
- **TSA / CBP** — for export-port-adjacent facilities.

**Federal — industrial policy**

- **IRA Section 48D** — 25% ITC for semiconductor manufacturing facilities (CHIPS Act).
- **IRA Section 45X** — manufacturing PTC for solar, battery, wind components.
- **IRA Section 45V** — hydrogen production PTC.
- **DPA Title III** — defense and critical materials.
- **CHIPS and Science Act** — semiconductor and research facility grants and ITCs.

**State and local**

- Zoning and ETJ — particularly Texas (limited zoning in unincorporated areas; ETJ overlay).
- Building permits — local jurisdiction.
- State environmental — TCEQ (Texas), CARB (California), DEEP (Connecticut), DEP (Pennsylvania).
- Water permits — increasingly material for cooling-water-intensive facilities; Texas groundwater districts, Arizona aquifer rules, California surface water rights.
- State incentive packages — property tax abatements (Texas HB 5), sales tax exemptions, infrastructure cost-sharing.
- Local fire codes — NFPA 855 for BESS, IBC for buildings, NFPA 75/76 for IT equipment, specialty codes for gas storage at hydrogen facilities.
- Water and sewer authorities — municipal infrastructure capacity.

**Specialty Facility class regulation**

- **Data center**: ASHRAE 90.4 (energy efficiency), Uptime Institute Tier certification (voluntary but commercial-standard), NFPA 75/76 (fire protection).
- **Fab**: SEMI standards, FFC (Facility Forecast Compatibility) standards.
- **BESS embedded**: NFPA 855 spacing and fire requirements.
- **Biopharma**: cGMP (21 CFR Part 211 and 600 series), FDA inspection regimes.
- **Defense**: NISPOM (National Industrial Security Program Operating Manual), CMMC, DFARS facility-clearance requirements.
- **Nuclear-adjacent**: NRC licensing tiers.

## 7. Cantus's Relationship to Power Facilities

Cantus Development is a direct principal in Power Facilities, in the same way Cantus Development is a direct principal in Power Land. The two sub-industries together constitute the Development vertical's value-creation territory: assemble Land + build Facility = create the productive site.

### By role

- **Facility developer and owner.** Cantus Development builds, owns, and leases Facilities to Power Industries operators (the hyperscaler tenant, the fab operator, the gigafactory operator, the defense prime, the CDMO). Facility ownership is held on firm balance sheet, through co-development partnerships, or through Cantus fund vehicles depending on transaction structure.
- **Master-developer for multi-tenant Intelligent Campuses.** A Cantus Intelligent Campus combines Land + multiple Facilities + shared infrastructure (substation, BTM generation, cooling, fiber, security, workforce-and-community function) into an integrated master-planned development. Cantus Development is the master-developer.
- **Build-to-suit (BTS) operator.** Cantus delivers BTS Facilities to specific Power Industries tenants under long-tenor lease arrangements. The Aligned / Compass / Stack / Vantage / QTS comp set is the structural reference, but with the Cantus integration overlay (workforce, BTM bridge, integrated dispatch).
- **Facility-design specifier.** Cantus specifies mission-critical design (data center critical environment, fab cleanroom layout, gigafactory dry room, biopharma cGMP suite) with consultants and EPC partners. The specification is part of what makes the Cantus Facility distinct from a generic developer's.
- **Brand owner of the Intelligent Campus.** Over time, the Cantus campus brand becomes a marketing and capital asset.
- **Direct principal — not just orchestrator.** This distinguishes Power Facilities + Power Land from sub-industries where Cantus is integrator-only (Assets, Equipment, Services) or advisor (Markets, Industries).

### By phase

**Building (Years 1–2) — current.** Initial Facility developments through JV with Tier-1 partners (Hillwood, Crow, Howard Hughes, Majestic per [[_parameters]]). CII data assets covering Facility design parameters, lease comps, BTS tenant covenants. Specific tenant engagements ramping (Foxconn, Tesla long-standing; T1 Energy active; hyperscaler discussions including Nebius on Joule).

**Activation (Years 3–4) — modeled.** Cantus-led Intelligent Campuses with principal Facility positions; Fund I capital ($250M–$500M per [[_parameters]]) deployed across Land + Facility positions. Multi-tenant Intelligent Campus deliveries begin.

**Compounding (Years 5–7) — modeled.** Multi-campus portfolio of Facilities with shared operating standards; brand recognition; Facility-class diversification (DC + fab-adjacent + gigafactory + critical minerals as the active mix).

**Mature platform (Years 8+).** Power Studio-scale platform across Facilities and Land; Cantus Intelligent Campus as recognized institutional product class with its own underwriting parameters.

### What Cantus Development is not

Not a colocation operator competing with Equinix or Digital Realty for individual cabinet sales. Not a fab operator. Not a gigafactory operator. Not a defense prime. Cantus Development *develops and owns the Facility*; the Power Industries operator runs the workload, the production process, the industrial mission.

### The principal claim

The structural claim Cantus makes about Power Facilities is that the sub-industry is fragmented across Facility class (data center vs. fab vs. gigafactory vs. defense vs. biopharma), capital structure (operator-balance-sheet vs. BTS-developer vs. REIT vs. co-investment), and design specialty (mission-critical electrical vs. cleanroom vs. dry room vs. cGMP). No single Facility developer operates across multiple classes at the integration level a multi-vector Cantus Intelligent Campus requires. Cantus Development's role is to construct the integrated multi-class Facility platform with the Power Land substrate, the Power Infrastructure energy backbone, the Power Technology operating systems, and the workforce-and-community function combined.

## 8. Key Trends and Structural Conditions (2026–2036)

**1. AI data center capex explosion.** Hyperscaler facility capex commitments are running $200B+/year across the top six firms (Microsoft, Amazon, Google, Meta, Oracle, Apple). Individual hyperscale AI campus capex routinely exceeds $5B. The volume of facility build required over the next 5–10 years is unprecedented.

**2. Liquid cooling as standard for AI workloads.** Air cooling is insufficient at the rack densities NVIDIA's H100, B100, and successor generations require (>50kW/rack and growing toward 250kW+). Direct-to-chip liquid cooling, immersion cooling, and rear-door heat exchangers are reshaping data center facility design. Supply chain for liquid cooling components (manifolds, CDUs, dielectric fluids) is tightening.

**3. Modular facility design.** Microsoft's modular data hall approach, Aligned's pre-fab data center pods, and similar approaches are accelerating facility delivery. The shift toward modular fab construction (TSMC's multi-fab Arizona buildout, Intel's Ohio campus) is parallel but slower because semiconductor manufacturing tolerances are tighter.

**4. Co-location of generation with Facility.** The Microsoft–Constellation TMI restart and similar arrangements demonstrate that direct on-site or adjacent-site generation is becoming a structural feature of large Facility deals. The campus model — Land + Facility + Generation under integrated control — is consistent with this trend and is the Cantus deliverable.

**5. Embedded BESS in Facility design.** UPS at scale, peak-shaving BESS, and grid-services BESS embedded in the Facility's electrical architecture rather than as a separate Power Asset. This blurs the Facilities / Assets boundary and is one of the structural reasons the framework treats demand-side BESS as Facility infrastructure rather than Power Assets.

**6. Site security as Facility differentiator.** Defense, advanced manufacturing, biopharma, and increasingly AI facilities require enhanced physical security and OT cybersecurity. Cleared-personnel facility design, controlled-access zoning, surveillance integration, and supply-chain integrity verification are becoming standard for sensitive Facility classes. The implication for Cantus is that Facility design needs to anticipate security requirements that didn't exist in standard industrial real estate.

**7. Modular fab construction acceleration.** TSMC, Intel, and Samsung are exploring more standardized fab module designs to shorten construction cycles. The structural barrier is process-tolerance — modular standardization is easier for mature-node fabs than for leading-edge. Cantus's potential role on the fab side is on the campus-and-infrastructure integration layer, not the cleanroom itself.

**8. Specialty cooling and MEP supply constraint.** UPS, generators, large cooling units, switchgear for AI-grade data centers are in 18–36 month lead times. The Power Equipment supply chain is the binding constraint on facility delivery schedule. Cantus's slot-holding role on the Power Equipment side ([[Strategy/Power-Sector/Power-Equipment]]) directly supports Facility delivery on the Power Facilities side.

**9. Concrete and steel constraint affecting Facility schedule.** Domestic concrete and structural steel supply, particularly for very large facilities, is currently tight. Specialty concrete (high-strength, lightweight, mass concrete) used in large data hall floor slabs is supply-constrained.

**10. Hyperscaler facility standardization.** Open Compute Project specs, hyperscaler-led design standards, and the convergence of hyperscale data center design across operators are creating a more commoditized base-building specification. The implication for Cantus Development is that differentiation moves from individual facility design to the integrated campus, the workforce-and-community function, and the multi-tenant orchestration.

## 9. Open Questions for the Framework Rewrite

To resolve as the framework matures:

- **Boundary treatment between Facility-embedded electrical infrastructure and Power Assets.** Facility-level UPS, embedded BESS, on-site emergency generation, internal substation. The framework convention treats these as Facility base-building MEP; should be made explicit and consistently applied across the framework.
- **How Cantus Development monetizes Facility ownership at scale.** Through stabilized BTS lease economics, through sale-leaseback to capital partners, through fund-level holding of Facility portfolios, or through some combination. The Capital Architecture (now folded into Power Markets sub-industry under Cantus Markets vertical) needs to specify the Facility-financing pattern.
- **Multi-class Facility integration on a single campus.** A Cantus Intelligent Campus may combine a hyperscale AI data center, a battery manufacturing facility, and a critical minerals processing facility on shared infrastructure. The framework should specify whether such multi-class campuses are the standard product or a special case.
- **Brand strategy across the Intelligent Campus product.** Master-branded (every Cantus Facility carries the Cantus name) or sub-branded (each campus has its own brand under a Cantus parent). Same question raised in [[Strategy/Power-Sector/Power-Land]]; needs consistent treatment.
- **BTS lease vs. owner-occupier sale.** For different Facility classes, the dominant commercial pattern differs (BTS lease for hyperscale DC; owner-occupier for fab and gigafactory). Cantus Development should specify the patterns it operates and the cases where it elects ownership vs. sale.

---

*Drafting. Author of record: Dom Espinosa.*
