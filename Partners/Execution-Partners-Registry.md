---
type: registry
status: draft
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-06-05
updated: 2026-06-06
strategy_area: energy
related_framework: ["[[Strategy/Cantus-Infrastructure]]", "[[Strategy/Cantus-Power-Sector-Thesis]]"]
related_pages: ["[[Strategy/Batch-Zero-Power-Strategy-Playbook]]", "[[Strategy/Cantus-Execution-Operating-Model]]"]
working_files:
  - "~/Documents/Cantus/Cantus/Execution-Model/Cantus-Execution-Operating-Model-v0.1.xlsx"
applies_to_phase: building
tags: [execution-partners, registry, batch-zero, ercot, btm, wlpun, pclr, generation, storage, interconnection]
---

# Cantus Execution Partners Registry

*The named partner roster for delivering a Cantus development. Each partner is slotted into a seat from the Batch Zero Power Strategy Playbook and the execution model. Partner facts marked "per public reporting" are unverified web sources (dated) and need confirmation in diligence; Greenflash facts are from its December 2025 intro deck (confidential).*

> Draft / advisory — not legal or engineering advice. Author of record: Dom Espinosa. 2026-06-05.

---

## How to read this

Cantus holds the **A (Accountable) — orchestrator / power-strategy** seat across the development and keeps the energy-management and back-end-PPA economics (see [[Strategy/Cantus-Execution-Operating-Model]]). **Every partner below is R (Responsible) under that A.** The recurring discipline: engage each partner on a structure that leaves ownership, energy management, and the PPA back-end with Cantus, defended by Cantus's control of the site/interconnection and the equipment slots.

## Partner-to-seat map

| Partner | Path / seat | RACI vs Cantus | Engage as | Core strength | Watch-item |
|---|---|---|---|---|---|
| **Greenflash Infrastructure** | Battery / **PCLR** — BESS, EMS/controls, power quality | R | Build-Transfer-Operate (not BOOM) | 4.5 GW BESS delivered; ERCOT/Houston footprint; NVIDIA 800VDC architecture | Full-stack "Own + Manage" model collides with Cantus economics; FEOC/China cells |
| **Thunderhead Energy Solutions** | Generation / **WLPUN** — funded BTM IPP (owns/operates) | R | Cantus-originated PPA with back-end participation; bridge→permanent rights | Harbert-funded balance sheet; recip+turbine hybrid; bridge or permanent | As owner/operator it competes for the same back-end Cantus wants — structure it |
| **Turbine-X Energy** | Generation / **WLPUN** — turbine packages + CCGT leg | R | Equipment/package supply; pair under Thunderhead or stand-alone | Baker Hughes NovaLT, quick-start, multi-fuel/H₂; simple→combined cycle | Default Eos storage pairing overlaps Greenflash; confirm slot lead times |
| **Splight** | Load study & **interconnection intelligence** | R (study) / advisor | Load-study resource for July 10 + capacity-unlock lever | AI electrical studies; claims 2–3x usable transmission capacity | Studies still require TSP/ERCOT acceptance — augments, not replaces, TSP process |

---

## 1. Greenflash Infrastructure — Battery / PCLR partner

**Snapshot.** Battery/microgrid developer-integrator for data centers; US- and China-based engineering team; 50+ microgrid projects across 6 continents; states ~4.5 GW of BESS delivered in the US and mechanical completion of an initial 1 GWh project in South Houston; commercial models from Build-Transfer up to Build-Own-Operate-Manage (BOOM); Texas / New Mexico / California microgrid footprint; architecture aligned to NVIDIA's 800VDC AI-factory roadmap. *(Source: Greenflash intro deck, Dec 2025.)*

**Seat fit.** Collapses most of the **PCLR path** into one firm — the BESS, the EMS/controls, telemetry, and the power-quality layer (BESS-UPS at MV, AI load smoothing, LVRT ride-through). The power-quality value holds across *every* posture (Base/Studied Firm/PCLR/WLPUN): AI training loads swinging 20–100% within 1–10s need battery-backed active power compensation regardless of how grid capacity is allocated.

**Strengths.** Real ERCOT/Houston track record; deep supplier relationships that feed the equipment-slot lock; credible co-pitch partner whose thesis (SB-6, speed-to-power, reserve margin negative by 2027) mirrors Cantus's own.

**Engagement structure (guardrail).** Engage at **Build / Build-Transfer-Operate**, not BOOM. Their top tier bundles Ownership + Energy Management (price/risk optimization, hedging) — exactly where Cantus's back-end-PPA participation lives. Greenflash builds and operates; Cantus or the capital partner owns; Cantus retains energy management and the PPA override. In RACI: R under Cantus Prime's A.

**Gaps / diligence.** FEOC / China supply chain (verify the "FEOC-compliant LTSA/O&M" claim — China cells can blow the storage ITC and disqualify defense/critical-materials tenants); confirm true PCLR regulatory mechanics (QSE coordination, Form W, telemetry to ERCOT spec, not just power-quality BESS); balance sheet if any ownership tier is used; no exclusivity — deck was built for Crusoe, a Cantus reference competitor.

## 2. Thunderhead Energy Solutions — Generation / WLPUN (funded IPP)

**Snapshot.** Founded 2024, Austin TX. Funds, develops, and operates **behind-the-meter baseload** power for data centers; solutions are either permanent or **relocatable "bridge"** plants after the primary term; uses a hybrid of reciprocating engines and turbines. Signed a ~250 MW BTM gas deal with Texas Critical Data Centers (Ector County / Permian), scalable to 1 GW. Secured a funding partnership with **Harbert Management Corporation** to develop up to ~1.5 GW. *(Per public reporting, Sep 2025 / May 2025 — unverified.)*

**Seat fit.** The **WLPUN generation-developer / IPP** seat — and the exact "bring in the best operator, Cantus keeps the back-end" partner from the seat memo. Funded balance sheet means the equipment is off the offtaker's books; the offtaker signs a PPA (transcript reference ~$100/MWh all-in). Bridge-or-permanent flexibility maps directly to the **20-year PPA / 5-year off-ramp** structure.

**Strengths.** Capital (Harbert) + owns/operates + recip-and-turbine hybrid + Texas/Permian execution; relocatable bridge model fits speed-to-power then transition.

**Engagement structure (guardrail).** Because Thunderhead *owns and operates*, structure deliberately so Cantus originates the deal, controls the site/interconnection and equipment slots, and **holds the PPA back-end participation + energy-management role** — otherwise Cantus is the finder. Secure the bridge→permanent off-ramp and the grid-asset transition rights in the term sheet.

**Gaps / diligence.** Harbert funding capacity and terms; firm gas supply + midstream/transport firmness; air-permit class sized to continuous-duty run hours (not emergency standby); queue path for the eventual grid-asset transition.

## 3. Turbine-X Energy — Generation / WLPUN (turbine packages + CCGT leg)

**Snapshot.** Behind-the-meter gas-fired power-infrastructure / energy-technology firm for data centers. Contracted **Baker Hughes NovaLT** gas turbines (5.5–17.5 MW, quick-start, multi-fuel — gas, H₂ blends, 100% H₂); supplies industrial gas-turbine packages in **combined-cycle** configuration. Joint development agreement with **Eos Energy** for up to 2 GWh of zinc storage paired with simple-cycle turbines for constrained high-load AI campuses, all BTM. *(Per public reporting, 2025 — unverified.)*

**Seat fit.** The **prime-mover / turbine-package** seat, and specifically the partner for the **combined-cycle → grid-asset** leg of the bridge (simple-cycle for speed, CCGT for the permanent asset that points back to the TSP). Multi-fuel/H₂ capability adds energy-transition optionality.

**Strengths.** Tier-1 turbine technology (Baker Hughes NovaLT); simple-and-combined-cycle in one partner; H₂-ready; can deliver the permanent/grid-asset leg that simple-cycle packagers cannot.

**Engagement structure (guardrail).** Two clean options: (a) Turbine-X supplies the turbines **under Thunderhead's funded/operated structure** (Thunderhead funds+operates, Turbine-X equipment, Greenflash BESS, Cantus orchestrates) — the strongest combined stack; or (b) stand-alone package supply. Either way, **decouple Turbine-X's default Eos storage pairing** where Greenflash is the chosen BESS — Cantus picks the stack. Confirm Baker Hughes NovaLT slot availability against the ~30-day designation rush flagged in the playbook.

**Gaps / diligence.** Slot lead times and reservation terms; whether they take development/ownership risk or are equipment-only; corporate maturity (newer, listed entity); interplay with Thunderhead on who owns the operating asset.

## 4. Splight — Load study & interconnection intelligence

**Snapshot.** AI-enabled transmission/interconnection platform (offices San Francisco + **Austin, TX** + Santiago + Madrid). Runs next-generation electrical studies ("Grid Online AI"), navigates large-load interconnection, and claims to unlock **2–3x usable transmission capacity** on existing infrastructure using real-time grid data; rapidly deployed by the load operator. *(Source: splight.com, fetched 2026-06-05.)*

**Seat fit.** The **load-study / interconnection-engineering resource** — runs the electrical studies the July 10 eligibility deadline requires and provides hands-on interconnection navigation.

**Engagement structure / caveat.** Splight's studies still have to be **accepted by the TSP and ERCOT** — the studies are TSP-led under Batch Zero, so Splight *augments* the process, it doesn't replace it. Confirm ERCOT/TSP acceptance of its methodology and its track record of approved large-load studies before relying on it for the deadline.

### What else Splight can do for Cantus (commentary)

- **Attack the "one number" directly.** The whole Studied-Load decision turns on how much firm grid capacity ERCOT allocates. If Splight can genuinely unlock 2–3x usable transmission capacity, it can *raise the firm allocation* — shrinking the shortfall that PCLR demand-flex or WLPUN generation has to carry. That changes posture economics in Cantus's favor and reduces the generation/storage capex on every deal.
- **Portfolio site-screening.** Run Splight across the CII Parcel Registry to score candidate sites by *true* available transmission capacity, not just nameplate queue data — a direct upgrade to Cantus Development's interconnection-rights aggregation and the brownfield-with-transferable-rights thesis.
- **Generation interconnection for the grid-asset transition.** When the Thunderhead/Turbine-X CCGT leg points back to the TSP, Splight's generation-interconnection use case can accelerate that step.
- **Curtailment reduction** on any Cantus on-campus renewables/BESS, and **real-time grid monitoring/reliability** that can feed the CII/DealOS data flywheel and the campus EMS.
- **Strategic note:** Splight is an information/optionality layer, not a contractor — its highest value to Cantus may be as a *standing capability across the pipeline* (site screening + capacity unlock), not just a per-deal study vendor.

---

## The combined stack (one campus)

For a Studied site, the partners compose cleanly:

1. **Splight** first maximizes the firm grid allocation (shrinks the shortfall) and runs the load studies for July 10.
2. The residual shortfall is carried by **Thunderhead**-funded generation (**Turbine-X** turbines + recip hybrid) under **WLPUN** for sustained load — simple-cycle for speed, transitioning to CCGT and ultimately a grid asset.
3. **Greenflash** BESS carries **PCLR** ride-through plus the power quality / LVRT / AI-load-smoothing that gas alone cannot deliver.
4. **Cantus** quarterbacks the whole engagement, holds the site/interconnection and equipment slots, and keeps the energy-management role and the back-end PPA participation.

This is the full PCLR + WLPUN + interconnection coverage of the playbook in four partners, with Cantus accountable across all of it.

## Open seats still to fill

From the playbook's team list, still to assign for a live development: ERCOT regulatory/energy counsel; the interconnecting TSP/DSP (CenterPoint relationship is a Cantus asset); an independent interconnection engineer (or Splight, pending TSP/ERCOT acceptance); a QSE (PCLR/WLPUN); a Texas notary (Form W/X); firm gas supplier + midstream; TCEQ air-permitting engineer; civil/geotech/water engineers; project finance/capital (the $50k/MW security + CIAC); tax/incentives advisor (ITC + FEOC); and the binding offtaker. Cantus holds the orchestration seat over all of them.

## Caveats

- Partner facts marked "per public reporting" are **unverified** web sources as of the dates shown; confirm in diligence before relying.
- Greenflash facts are from a **confidential** intro deck (internal use only).
- All rule figures (Batch Zero deadlines, PCLR/WLPUN mechanics) remain **DRAFT** pending regulatory approval.

## Sources

- Greenflash Infrastructure intro deck, December 2025 (confidential; uploaded).
- Splight — Interconnection Intelligence: [splight.com/grid-interconnection-navigation](https://www.splight.com/grid-interconnection-navigation)
- Thunderhead / TCDC 250 MW deal: [Rigzone](https://www.rigzone.com/news/texas_critical_data_centers_and_thunderhead_ink_preliminary_power_deal-03-sep-2025-181677-article/), [Hart Energy](https://www.hartenergy.com/exclusives/tcdc-thunderhead-ink-power-agreement-permian-data-center-213998/), [BusinessWire](https://www.businesswire.com/news/home/20250902177723/en/New-Era-Energy-Digitals-TCDC-and-Thunderhead-Energy-Solutions-Sign-Strategic-Power-Agreement-for-250-MW-AI-Data-Center-Campus-in-Texas)
- Thunderhead / Harbert funding + 1.5 GW: [PRNewswire](https://www.prnewswire.com/news-releases/thunderhead-energy-solutions-secures-funding-partnership-from-harbert-management-corporation-302446488.html), [DCD](https://www.datacenterdynamics.com/en/news/thunderhead-and-hmc-to-deliver-up-to-15gw-of-offgrid-natural-gas-power-for-us-data-centers/)
- Turbine-X / Baker Hughes NovaLT: [Turbomachinery Magazine](https://www.turbomachinerymag.com/view/turbine-x-energy-contracts-baker-hughes-to-power-data-centers-with-novalt-turbines), [Baker Hughes](https://investors.bakerhughes.com/news-releases/news-release-details/baker-hughes-secures-order-provide-reliable-and-efficient-power)
- Turbine-X / Eos storage JDA: [DCD](https://www.datacenterdynamics.com/en/news/eos-energy-partners-with-turbine-x-to-develop-and-deploy-power-infrastructure-for-the-us-ai-data-center-market/)

---

*Draft registry. Pairs with the Batch Zero playbook and the Cantus execution operating model. Aligns to [[Strategy/Cantus-Infrastructure]] (Cantus Prime) and the back-end-PPA economics. Author of record: Dom Espinosa. 2026-06-05.*
