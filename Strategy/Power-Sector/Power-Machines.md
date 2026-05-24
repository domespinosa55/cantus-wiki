---
type: framework
status: drafting
audience: internal
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
tags: [power-sector, sub-industry, power-machines, cantus-technology]
sub_industry: power_machines
sub_industry_index: 6
related_thesis: ["[[Strategy/Cantus-Framework]]"]
related_pages: ["[[Strategy/Power-Sector/Power-Facilities]]", "[[Strategy/Power-Sector/Power-Industries]]", "[[Strategy/Power-Sector/Power-Technology]]"]
---

# Power Machines — Sub-Industry Specification

*Sub-industry 6 of 10 in the Power sector framework v2. Drafting. Cantus Technology is the operating vertical for this sub-industry — orchestrator and, at selective scale, operator.*

---

## 1. Definition

Power Machines is the sub-industry of **productive machinery installed inside Power Facilities that converts electrons into industrial output**. The unit of production is a machine deployed in a Power Facility doing productive work: a GPU server cluster, a lithography stepper, a robot cell, a battery coater, an electrolyzer stack, a bioreactor, an automation island, a CNC machine, a process tool. The defining condition is that the machine consumes electricity to produce a unit of industrial output, and its productive capacity (chips per hour, cells per minute, tokens per second, vials per shift) is what the Power Industries operator sells.

The boundary against adjacent Power sub-industries:

- **Power Equipment** is the hardware that *enables* the Power sector — turbines, transformers, switchgear, BESS, inverters. It serves the **supply side** (Power Assets). Power Machines serves the **demand side** (Power Facilities and Power Industries). Same word ("equipment") sometimes used colloquially for both, but the supply chains, OEMs, capital sources, and economics are completely different. A Caterpillar reciprocating engine is Power Equipment; an NVIDIA H100 GPU is a Power Machine.
- **Power Facilities** is the building or campus that houses the Machines. The fab building is the Facility; the ASML lithography tools inside are Machines.
- **Power Industries** is the operator on the marquee. TSMC is Industries; the ASML tools they run are Machines. Microsoft is Industries; the GPUs they run are Machines.
- **Power Technology** is the software, control, analytics, and orchestration layer. Power Machines is the productive *hardware*. The line blurs because modern Machines are increasingly software-defined (NVIDIA's CUDA stack is the case study), and the framework treats embedded firmware as part of the Machine while external software (CUDA, DCIM, MES, robotic-operating-systems) is Technology.

Within Power Machines, fifteen structural sub-segments organized by Power Industries demand vector:

**Compute Machines (serve Compute vector):**

1. **AI accelerators** — GPUs, custom AI ASICs, wafer-scale, neuromorphic. NVIDIA-dominant; large captive cohort.
2. **AI compute systems** — servers, racks, networking, optical interconnect.
3. **Edge compute hardware** — smaller AI inference systems closer to consumption.

**Advanced manufacturing Machines (serve Advanced Manufacturing vector):**

4. **Semiconductor equipment** — lithography, etch, deposition, metrology, advanced packaging.
5. **Industrial robotics** — articulated industrial robots, SCARA, collaborative robots.
6. **Humanoid robotics** — emerging category; Tesla Optimus, Figure, Apptronik, Boston Dynamics, Agility, Unitree.
7. **Automation systems** — PLC, DCS, MES integration, machine vision, motion control.
8. **Additive manufacturing equipment** — industrial 3D printing across polymer, metal, ceramic.

**Supply chain manufacturing Machines (serve Supply Chain Manufacturing vector):**

9. **Battery manufacturing equipment** — mixing, coating, calendering, slitting, winding, formation, cell assembly, pack assembly.
10. **EV manufacturing equipment** — stamping, body-in-white, paint, general assembly, robotic cells.
11. **Solar manufacturing equipment** — cell, wafer, module assembly.
12. **Wind turbine manufacturing equipment** — blade molds, nacelle assembly tooling, gearbox machining.

**Energy transition Machines (serve Energy Transition Manufacturing vector):**

13. **Hydrogen electrolysis stacks** — PEM, alkaline, SOEC.
14. **Direct air capture equipment** — sorbent contactors, regenerators, liquid sorbent systems.

**Biomanufacturing and defense Machines:**

15. **Bioprocessing equipment** — bioreactors, downstream processing, fill-finish, cell therapy manufacturing.
16. **Defense manufacturing equipment** — large-scale CNC, additive manufacturing for defense components, energetics processing, missile body production, drone airframe assembly. (Numbered sixteenth but parallel to the others.)

Critical minerals processing equipment fits across categories — electrolysis cells, solvent extraction, smelting, milling. Treated as a sub-segment of Advanced Manufacturing / Critical Materials within this taxonomy.

## 2. Deliverables

Power Machines produces four classes of deliverable:

**The machine unit** — the manufactured productive equipment delivered, installed, and commissioned in a Power Facility. Specified by throughput (units/hour, tokens/sec, kg/day), precision (nanometer node, picometer placement), uptime (>95% standard at industrial scale), efficiency, and integration interfaces.

**Performance guarantees and service** — yield guarantees on semi tools, throughput guarantees on robotics, uptime guarantees on AI infrastructure, capacity factor on electrolyzers. Performance is often the contractual deliverable that monetizes the equipment.

**Software stack and orchestration** — the embedded firmware, control software, and increasingly the application-layer software that defines what the machine can do. NVIDIA's CUDA stack is the defining example — the GPU's productive value is inseparable from the CUDA software. ASML's computational lithography software is similarly integral to the lithography product. Modern industrial robots ship with vendor-locked operating systems.

**Long-term service agreements (LTSAs) and aftermarket** — multi-year service contracts, spare parts and consumables, retrofits, upgrades. For semiconductor and battery manufacturing equipment, the LTSA and aftermarket revenue is often comparable to the original sale.

The contractual instruments are: equipment supply contracts with milestone payments, performance guarantees, service contracts (LTSA), software license and subscription terms, vendor-financing or equipment-finance arrangements (especially for AI compute given NVIDIA paper and CoreWeave-style structures).

## 3. Major Players (US-Focused)

### AI accelerators (the dominant Power Machine sub-segment)

NVIDIA (NVDA — dominant; H100, H200, B100/B200, GB200 generations, full-stack from chip to system); AMD (MI300X, MI325X, MI350 series; ROCm software stack improving); Intel (Gaudi 3, future generations; Habana acquisition); Cerebras (wafer-scale); Groq (LPU for inference); SambaNova; Tenstorrent (Jim Keller; CPU + AI hybrid); Graphcore (UK; struggling commercially); Rivos (RISC-V AI). Custom captive silicon: Google TPU; AWS Trainium and Inferentia; Microsoft MAIA; Meta MTIA; Apple M-series and Apple Intelligence chips.

### AI compute systems

Dell Technologies; Hewlett Packard Enterprise (HPE); Lenovo; Super Micro Computer (Supermicro); Foxconn (Hon Hai — massive scale, manufactures for hyperscalers); Quanta Computer (Taiwan, dominant white-label); Wiwynn; Inventec; Gigabyte; ASRock Rack; NVIDIA reference systems (DGX, HGX); ODMs serving hyperscalers (Foxconn, Quanta, Wiwynn dominate this segment).

### Networking and interconnect

NVIDIA (Mellanox / Cumulus; NVLink for GPU-to-GPU); Broadcom (Tomahawk, Jericho switches); Arista Networks; Cisco; Marvell (custom silicon for hyperscalers); Astera Labs (PCIe and CXL silicon); Cornelis Networks. Optical interconnect: Coherent, Lumentum, Marvell Optical, NVIDIA InfiniBand.

### Semiconductor equipment

ASML (Dutch; dominant in lithography, the only EUV supplier globally — the binding constraint on leading-edge semi capacity); Applied Materials (AMAT; deposition, etch, ion implant, CMP); Lam Research (LRCX; etch and deposition); KLA Corporation (KLAC; metrology and process control); Tokyo Electron (TEL; etch, deposition, coater-developer); ASM International (ASMI; deposition); Onto Innovation; Disco Corporation (Japanese; dicing and grinding); Camtek; Veeco Instruments; Onto Innovation; FormFactor (probe cards); Teradyne (test).

### Industrial robotics

ABB Robotics; FANUC (Japanese); KUKA (Midea-owned, Chinese); Yaskawa Electric; Kawasaki Robotics; Stäubli; Universal Robots (Teradyne); Mitsubishi Electric; Epson Robots; Omron; Comau; Denso Robotics. The Big Four (ABB, FANUC, KUKA, Yaskawa) account for the majority of installed industrial robot base globally.

### Humanoid robotics (emerging category)

Tesla (Optimus); Figure AI (Microsoft / OpenAI / NVIDIA-backed); Apptronik (NASA partnership, Mercedes deployments); Boston Dynamics (Hyundai-owned, Atlas); Agility Robotics (Digit, Ford and Amazon deployments); 1X Technologies (OpenAI-backed); Sanctuary AI; Unitree (Chinese, lower-cost humanoid). The category is in early commercialization 2025–2027; large-scale industrial deployment is the inflection ahead.

### Automation systems

Siemens (Sinumerik CNC, TIA Portal automation, Simatic); Rockwell Automation (Allen-Bradley, FactoryTalk); Schneider Electric (Modicon, EcoStruxure Automation); Emerson Automation (DeltaV DCS, Ovation); ABB Ability Industrial Automation; Honeywell Process Solutions (Experion); Yokogawa Electric (Centum); Mitsubishi Electric (MELSEC); Beckhoff Automation. The Big Five (Siemens, Rockwell, Schneider, Emerson, ABB) dominate industrial automation.

### Battery manufacturing equipment

Wuxi Lead Intelligent (Chinese, dominant for global cell manufacturers); Hitachi High-Technologies (mixing, coating); Manz Group; Schuler Group (Andritz-owned; calendering, slitting, stamping); DÜRR Group (paint and coating, cell finishing); Sovema; Hibar Systems (DÜRR); KGM (Korean); Comau (formation cycling); Yinghe Technology (Chinese). Significant captive equipment by CATL, LG Energy Solution, Samsung SDI for proprietary lines.

### EV manufacturing equipment

KUKA, ABB Robotics, FANUC, Yaskawa (general robotics); Schuler Group (stamping); DÜRR (paint, coating); ATLAS COPCO (fastening, joining); Stäubli; Comau (Stellantis-owned); GROB-WERKE (machining); Heller (engine machining, less relevant for EV); Schaeffler (bearings, gearing).

### Solar manufacturing equipment

Centrotherm; Schmid Group; Despatch Industries (furnaces); Centrolite; Meyer Burger (equipment, distinct from struggling module business); Applied Materials (some solar tool integration); Singulus Technologies.

### Wind turbine manufacturing equipment

LM Wind Power (blade molds; GE Vernova subsidiary); TPI Composites; Schaeffler (bearings); ZF Wind Power (gearboxes); ABB and Siemens (generators); Vestas in-house (large-scale assembly).

### Hydrogen electrolysis stacks

Plug Power; NEL Hydrogen (Norwegian, US footprint); ITM Power (UK; US activity); Cummins (HyLYZER and Accelera segment); Nucera (thyssenkrupp-spinout); Topsoe (SOEC); Bloom Energy (SOEC fuel cells and electrolyzers); Ohmium; HyAxiom (Mitsubishi-owned); Ceres Power (UK); Verdagy.

### Direct air capture equipment

Climeworks (Swiss, US activity); 1PointFive (Occidental subsidiary using Carbon Engineering tech); Heirloom; Global Thermostat; Mosaic Materials; CarbonCapture Inc.; Avnos.

### Critical minerals processing equipment

Outotec / Metso (smelting, refining); FLSmidth; Mintek (South African); ALS Limited (process tech); various specialty lithium and rare-earth equipment vendors.

### Bioprocessing equipment

Sartorius (German; bioreactors, downstream); Thermo Fisher Scientific (instruments, bioprocessing); Cytiva (Danaher; bioprocessing equipment formerly GE Healthcare Life Sciences); Merck KGaA Millipore Sigma; Lonza Bioprocessing (Lonza-owned equipment for own facilities); Pall Corporation (Danaher); Repligen (downstream); Sartorius Stedim Biotech (single-use bioreactors).

### Additive manufacturing equipment

3D Systems; Stratasys; Desktop Metal; Markforged; Velo3D; Carbon; Formlabs; HP Industrial 3D (Multi Jet Fusion); EOS (German, industrial metal); SLM Solutions; Renishaw (UK, metal AM); Trumpf; Sintavia (service bureau).

### Defense manufacturing equipment

Hadrian (specialty CNC at scale for defense supplier modernization); 3D-printed defense components increasingly important (Anduril, Lockheed Martin use additive at scale); specialty energetics processing equipment; missile body production tooling.

## 4. Capital Structures and Economics

Power Machines is **highly capital-intensive on the OEM side**, with returns shaped by technology cycle position and end-customer mix. Buyer-side economics depend on the Power Industries vector being served.

### Capital structures by participant class

| Participant | Capital structure | Returns target |
|---|---|---|
| OEM (NVIDIA, ASML, AMAT, Lam, KLA) | Corporate balance sheet; high R&D burn | 30–60% gross margin; 20–40% operating margin at top of cycle |
| Captive (Google TPU, AWS Trainium, etc.) | Internal corporate capex | Strategic vs. third-party pricing |
| AI compute buyer (CoreWeave, Lambda, Crusoe) | Equipment finance + vendor paper + project finance | 12–25% IRR on AI-compute infrastructure |
| Semi fab buyer (TSMC, Intel) | Operator corporate + CHIPS grants + 48D ITC | 18–28% ROE through-cycle |
| Battery factory buyer | Sponsor + 45X credits + DOE LPO | Currently squeezed; 45X-supported |
| Robotics buyer (industrial customer) | Operator capex; sometimes leased | Productivity-driven payback |

### NVIDIA economics as the dominant case

NVIDIA's structural position in AI accelerators is the most consequential single fact about Power Machines economics in this cycle:

- Gross margin: ~75% data center segment
- Operating margin: ~60% at peak
- Pricing power: H100 systems priced $250K–$400K each; B200 systems $450K–$600K each
- Order book: 2026 capacity sold out; 2027 capacity partially allocated
- Software lock-in: CUDA stack effectively necessary for AI training at scale
- Customer base: heavily concentrated in hyperscalers + AI labs + neoclouds + sovereign AI initiatives
- Vendor financing: NVIDIA paper increasingly visible in AI compute build-outs; Coreweave, Crusoe and others use NVIDIA-collateralized debt and equipment finance

### ASML economics (lithography monopoly)

- EUV is the only path to leading-edge node (3nm and below); ASML is the sole EUV supplier
- High-NA EUV (next generation) at ~$370M per tool; standard EUV at ~$200M
- Order book extends 24+ months
- Export controls to China constrain shipments
- Gross margin ~50%; operating margin ~30% through-cycle
- The structural monopoly is one of the deepest in the Power sector

### Battery manufacturing equipment economics

- Capex per GWh of cell capacity: $80M–$150M for equipment (excluding building)
- Wuxi Lead Intelligent dominates the Chinese-influenced supply chain
- US-domestic battery equipment supply is structurally thin; the IRA 45X PTC supports buyers but does not directly subsidize equipment supply
- Equipment OEMs operate on 18–25% gross margin, lower operating margin

### Industrial robotics economics

- Industrial robot installed base globally ~3.5M units (IFR 2024 figures); growth driven by China + reshoring elsewhere
- Big Four (ABB, FANUC, KUKA, Yaskawa) hold ~60–65% combined market share
- ABB and FANUC operating margins 15–18% at industrial robot business level

### Humanoid robotics economics (emerging)

- Pre-commercial at industrial scale; pilot deployments only
- Tesla Optimus projected at $20–30K unit price at scale (Musk's stated target)
- Figure, Apptronik, Agility raising at $1–3B valuations on early production deployment
- The structural inflection is whether humanoids reach industrial-scale unit economics in 2026–2028

### Bioprocessing equipment economics

- Sartorius operating margin ~25–30%
- Single-use bioreactor systems dominant in new builds (>80% of new cell-culture capacity)
- COVID-era demand boom + post-COVID correction creates volatile cycle dynamics

## 5. Counterparty Universe

| Counterparty | Interaction |
|---|---|
| Power Industries (operators) | Primary buyer — hyperscalers buy GPUs, fabs buy litho, gigafactories buy cell equipment, defense primes buy CNC and additive. |
| Power Facilities (developers, owners) | Facility-level coordination on installation, MEP integration, cooling capacity, floor loading. |
| Power Technology (software vendors) | Embedded firmware and external software that runs Machines; bidirectional integration. |
| Power Capital (now part of Power Markets sub-industry) | Equipment finance, vendor paper, project finance for compute infrastructure, sponsor equity for fab and gigafactory operators. |
| Power Equipment (different supply chain) | Adjacent counterparty for shared upstream inputs (specialty materials, controls), but structurally distinct. |
| Tier-2 component suppliers | TSMC and Samsung Foundry (chip fabrication for AI accelerators); rare earth and magnet suppliers; specialty alloys; ASML supply chain (Zeiss optics, lasers, etc.). |
| Supply chain logistics | Highly sensitive for semiconductor equipment (ASML's air-freight, specialty handling) and large-tool moves. |
| BIS (Bureau of Industry and Security) | Export controls — most acute for semi equipment to China and for AI accelerators (Nvidia H20, etc.). |
| CFIUS | Foreign investment review of Power Machines OEMs and acquisitions. |
| DoD | Defense Machine procurement; DPA Title III for critical Machine supply (e.g., advanced fabrication for defense). |
| DOE | Hydrogen Hubs, ARPA-E, MESC (Manufacturing & Energy Supply Chains office) for Machine demand. |
| FDA | Bioprocessing Machine validation under cGMP. |
| Treasury | IRA 48D, 45X, 45V administration relevant to Machine purchases. |

## 6. Regulatory Environment

Power Machines is regulated heavily on the **export-control, trade, and technology-security** axis (especially for semi equipment and AI accelerators) and the **safety and standards** axis (across all Machine classes). Industrial-policy capital (CHIPS, IRA, DPA) shapes the buyer-side economics across most sub-segments.

**Federal — export controls and trade**

- **BIS** — Export controls on semi equipment (October 2022 rules, expanded 2023 and 2024) restrict shipments of advanced lithography, deposition, and EUV-related tools to China and entities-of-concern. Export controls on AI accelerators (Nvidia H100, H200, H20 variants; AMD MI series); chip-specific licensing.
- **Treasury / Commerce** — Outbound Investment Order (2024) restricts US investment in Chinese AI, quantum, and advanced-semi.
- **CFIUS** — review of foreign acquisitions of US Power Machines OEMs.
- **USTR / DOC** — Section 301 China tariffs on machinery and components; Section 232 considerations for specialty components.
- **DoD / DPA** — Title III grants and authorities for critical Machine supply chain (large CNC, additive at scale, specialty bioprocessing).

**Federal — industrial policy**

- **CHIPS Act** — $39B grants + $24B research + 48D 25% ITC for semiconductor manufacturing equipment purchases as well as facilities.
- **IRA Section 45X** — manufacturing PTC for solar wafer/cell/module equipment-supported manufacturing, battery cell/module manufacturing, wind components, critical minerals processing.
- **IRA Section 45V** — hydrogen production PTC; electrolyzer manufacturing affected indirectly through demand for electrolysis Machines.
- **DOE LPO** — financing for hydrogen production, battery manufacturing, critical minerals processing facilities — drives Machine demand.
- **DPA Title III** — defense Machine supply chain.

**Federal — sector-specific Machine regulation**

- **FDA** — bioprocessing Machine validation under cGMP (21 CFR Part 211, 600 series).
- **NRC** — Machines used in nuclear-adjacent processes.
- **EPA** — Machine-level emissions where relevant (e.g., chemical-processing Machines, electrolyzer balance-of-plant emissions).
- **OSHA** — Machine guarding, worker safety in industrial settings.

**Standards**

- IPC standards (electronics manufacturing)
- SEMI standards (semiconductor equipment)
- IEEE 754 (computing), IEEE 802 (networking)
- ISO 10218 (industrial robots), ISO 10218-2 (collaborative)
- ANSI/RIA R15.06 (industrial robot safety)
- ANSI/IES standards for automation
- cGMP (FDA)
- IEC 61131 (PLC), IEC 61850 (substation), MTConnect (machine tool data)

**International**

- WA (Wassenaar Arrangement) — multilateral export controls on dual-use Machines.
- EU AI Act — relevant for AI Machines deployed in EU contexts.
- China — domestic Machine supply chain prioritization under "Made in China 2025" and successors.

## 7. Cantus's Relationship to Power Machines

Cantus Technology is the operating vertical for Power Machines. Per the v2 framework architecture, Cantus Technology is **orchestrator and selective operator** — orchestrating across Power Machines + Power Technology for all Cantus campuses, and selectively operating in specific Power Machine sub-segments where the operating economics justify principal capital.

### By role

- **Machine selector and specifier for tenant campuses.** Cantus Technology specifies the Power Machine deployment in customer campuses — GPU architecture and density for AI compute tenants, robotics and automation systems for advanced manufacturing tenants, electrolyzer selection for hydrogen production tenants. The specification work is integration intelligence: matching Machine selection to Facility design, cooling capacity, power profile, and tenant operating envelope.
- **OEM relationship manager.** Long-tenor relationships with the primary Power Machine OEMs — NVIDIA, AMD, ASML (where relevant for tenant fab buildouts), the Big Four robotics (ABB, FANUC, KUKA, Yaskawa), the bioprocessing cohort (Sartorius, Cytiva, Thermo Fisher), the electrolysis cohort (Plug, NEL, Nucera, Bloom). Slot-holding and procurement-channel access analogous to the Cantus Infrastructure OEM relationships in [[Strategy/Power-Sector/Power-Equipment]].
- **Cantus Compute (selective operator role).** Cantus Compute is articulated in [[Strategy/Cantus-Framework]] as a hosted-compute operating business. The v2 framework places Cantus Compute inside Cantus Technology as a selective operator of AI compute Machines at scale — hosting GPU capacity for campus tenants and possibly for external customers. Structural reference points: Crusoe (vertically integrated with generation), CoreWeave (neocloud at scale), Lambda Labs (research-focused), Crusoe (vertically integrated). Cantus Compute differentiates via the integrated campus + power + cooling stack rather than via standalone neocloud economics.
- **Possible Cantus Robotics (future selective operator).** Robotics-as-a-Service for industrial tenants, particularly in advanced manufacturing and defense industrial base verticals. Speculative for now; the framework treats it as Compounding-phase or later.
- **Software platform integrator.** External Power Technology vendors (Tesla Autobidder for BESS dispatch, AutoGrid DERMS, Voltus DR, Vertiv DCIM) are orchestrated into the Cantus campus operating layer alongside Cantus's own CII and DealOS Foundation systems.
- **Not an OEM.** Cantus does not manufacture GPUs, lithography tools, robots, electrolyzers, or bioreactors. The Machine OEMs are counterparties, not businesses Cantus competes with.

### By phase

**Building (Years 1–2) — current.** OEM relationship-building across Machine cohorts. Specifying authority on Cantus-led campuses for tenant Machine deployment. CII data assets covering Machine supply chain, lead times, pricing, performance benchmarks. Cantus Compute concept articulation; initial GPU slot positions explored.

**Activation (Years 3–4) — modeled.** Cantus Compute hosted-GPU pilot operating in one or two Cantus campuses; Fund I capital allocated. Specifying authority extended across all four Cantus campus verticals. Machine-procurement aggregation across multi-campus pipeline reducing per-unit cost to tenants.

**Compounding (Years 5–7) — modeled.** Cantus Compute at scale; possibly hosted across multiple campuses; possible third-party customer base beyond Cantus tenants. Cantus Robotics articulated and possibly initiating selective operation. Machine intelligence layer institutionalized via CII.

**Mature platform (Years 8+).** Cantus Technology as a recognized integrated machine-and-software vertical operating across all Cantus campuses, with Cantus Compute and possibly Cantus Robotics as identified principal businesses inside.

### The orchestrator + selective operator claim

The strategic claim Cantus Technology makes about Power Machines is twofold:

First, **machine selection and integration is itself a deliverable**. The fragmented Machine OEM landscape (NVIDIA + AMD + ASML + the four robotics primaries + the bioprocessing cohort + the electrolysis cohort + multiple battery equipment vendors) cannot be navigated by the average Power Industries operator. Cantus Technology integrates across the OEM landscape and delivers Machine-specified campuses to tenants — an integration role analogous to Cantus Infrastructure's role on the supply side.

Second, **selective operation in specific Machine sub-segments creates structural advantage**. Cantus Compute as a hosted-GPU business sits on the Cantus campus power-and-cooling integration that no standalone neocloud can replicate. The integration advantage justifies principal capital in this Machine sub-segment. The same logic may extend to Cantus Robotics in time.

The structural difference between Cantus Technology and Crusoe / CoreWeave: Cantus operates *from the integrated campus outward*, while Crusoe and CoreWeave operate *from the compute infrastructure outward*. The two converge on similar product but diverge on origin point and on capital architecture.

## 8. Key Trends and Structural Conditions (2026–2036)

**1. AI compute supercycle.** NVIDIA's revenue trajectory (data center segment from ~$10B 2022 to >$100B 2024 to projected $150B+ 2025) is the dominant single fact about Power Machines. The supercycle runs through 2026–2028 at minimum, with B200/GB200 generations dominant and Rubin generation entering. Custom captive silicon (Google TPU, AWS Trainium, MS MAIA, Meta MTIA) is growing but does not displace NVIDIA at the high end.

**2. Custom AI silicon proliferation.** Every major hyperscaler is investing in custom silicon. The structural implication is that the AI compute Machine market segments into NVIDIA-dominant general-purpose (especially training) and captive-silicon optimized inference. CoreWeave-like neocloud operators sit in the NVIDIA segment; hyperscaler captives sit in the optimized segment.

**3. Liquid-cooled rack convergence.** The thermal envelope of B200, B100, GB200, and successor generations forces liquid cooling. Direct-to-chip and immersion cooling are the two competing approaches. Supply chain for cooling components is the binding constraint.

**4. Humanoid robotics commercialization 2025–2028 inflection.** Tesla Optimus, Figure, Apptronik, Agility, 1X are all in pilot deployment. The structural question is whether unit economics work for industrial deployment in 2026–2028. If yes, the humanoid robotics Machine class becomes a major Power Industries supply layer; if no, the category remains pre-commercial for another decade. Cantus Technology should track this trajectory closely.

**5. Battery manufacturing equipment localization.** The US battery manufacturing build-out is significantly equipment-constrained because the Chinese (Wuxi Lead) and Korean equipment supply dominates. US-domestic battery equipment buildout (with DPA Title III and DOE support) is the structural project.

**6. Bioprocessing equipment consolidation.** Sartorius, Cytiva (Danaher), Thermo Fisher, Merck KGaA have consolidated the bioprocessing Machine market. Single-use bioreactor systems are the dominant new-build technology. The implication for Cantus Markets vertical (biomanufacturing demand vector advisory) is that Machine selection is concentrating into a smaller cohort.

**7. Robotics-as-a-Service business model.** Industrial robotics increasingly delivered under capacity-based rather than capex-based commercial structures. Boston Dynamics, Universal Robots, Agility Robotics are all exploring RaaS. Cantus Robotics as a future Cantus Technology business sits in this commercial frame.

**8. Defense additive manufacturing.** Anduril, Hadrian, and the new defense-tech cohort are using additive manufacturing at industrial scale for missile, drone, and weapons subsystem production. The Machine supply chain for defense AM is critical-path; supply is structurally thin.

**9. ASML EUV constraint.** The single-supplier EUV bottleneck (and the parallel High-NA EUV constraint emerging) is the deepest supply chain constraint in Power Machines. TSMC and Samsung and Intel's leading-edge capacity is gated by ASML throughput.

**10. Industrial automation converging with AI.** Siemens, Rockwell, Schneider Electric, Emerson, ABB are integrating AI agents into PLC, DCS, and MES platforms. The line between Power Machines (the productive equipment) and Power Technology (the orchestration software) is blurring at the high end. For Cantus, the implication is that Machine specification carries software lock-in and platform-architecture decisions that affect tenant operations for decades.

## 9. Open Questions for the Framework Rewrite

To resolve as the framework matures:

- **Cantus Compute scope.** Hosted GPU for Cantus campus tenants only, or hosted GPU for external customers as well? If the latter, Cantus Compute is more like CoreWeave-with-integration-advantage; if the former, Cantus Compute is a campus-internal Machine layer that monetizes through tenant economics. The framework should specify.
- **Cantus Robotics priority and timeline.** Speculative in the current articulation. The framework should specify whether Cantus Robotics is an explicit Compounding-phase initiative or a "monitor and revisit" item.
- **NVIDIA relationship as Cantus's most strategic Power Machine relationship.** The OEM cohort in [[_parameters]] under Strategic OEM Relationships does not currently include NVIDIA. Given NVIDIA's central role in Power Machines and Cantus Compute, an explicit corporate relationship strategy should be specified.
- **Captive silicon relationship for hyperscale tenants.** When the tenant is Microsoft, Amazon, Google, or Meta, the Machine layer includes both NVIDIA-supplied accelerators and the tenant's captive silicon (TPU, Trainium, MAIA, MTIA). Cantus Technology's relationship to the captive silicon — does Cantus integrate it like any other Machine, or does the tenant manage the captive layer independently?
- **Software boundary between Machines and Power Technology.** Modern Machines ship with deep software stacks (CUDA, robot-OS, MES). The framework treats embedded firmware as Machine and external software as Technology, but the boundary is blurry. Specific cases to resolve: where does NVIDIA's CUDA stack sit (Machine? Technology?). Where does Siemens TIA Portal sit (Machine? Technology?). Consistent treatment needed.

---

*Drafting. Author of record: Dom Espinosa.*
