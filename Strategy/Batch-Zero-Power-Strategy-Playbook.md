---
type: playbook
status: draft
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-06-05
updated: 2026-06-06
strategy_area: energy
related_framework: ["[[Strategy/Cantus-Infrastructure]]", "[[Strategy/Cantus-Power-Sector-Thesis]]", "[[Strategy/Bridge-to-Grid-Thesis]]", "[[Strategy/ERCOT-Positioning-Thesis]]"]
related_pages: ["[[Strategy/Cantus-Execution-Operating-Model]]"]
working_files:
  - "~/Documents/Cantus/Cantus/Execution-Model/Cantus-Execution-Operating-Model-v0.1.xlsx"
applies_to_phase: building
tags: [playbook, batch-zero, ercot, pgrr145, sb6, interconnection, power-strategy, btm, wlpun, pclr]
---

# Cantus Batch Zero Power Strategy Playbook

*A reusable Cantus advisory engagement for executing a large-load (≥75 MW) power strategy under ERCOT's Batch Zero interconnection process (PGRR145 / SB6 / PUCT 16 TAC §25.194). This is the productized form of the Cantus Prime power-strategy seat. It pairs with the execution model in `Cantus-Execution-Operating-Model-v0.1.xlsx` and the seat analysis in [[Strategy/Cantus-Execution-Operating-Model]].*

> **All rule figures below are DRAFT and pending regulatory approval. This is advisory — not legal or engineering advice.** Author of record: Dom Espinosa.

---

## 1. What this engagement is

This is the engagement Cantus runs when a large-load developer, offtaker, or site owner has to place a project into ERCOT's one-shot Batch Zero study and get it right. It maps to **Phase 2 — Power strategy & interconnection** of the Cantus execution model, and it is the wedge that opens the rest of the integrated production: site, equipment procurement, EaaS/IPP selection, and a back-end participation in the resulting PPA.

Cantus does not become the IPP, the EPC, or the EaaS operator. Cantus is the **development quarterback** — it sets the posture, runs the team, brokers the equipment slots, brings in the best operator, and structures the commercial so that a slice of the power contract accrues to Cantus over its life. (See §6.)

**Use it when:** a project is ≥75 MW, sits in ERCOT, and is not already through validated studies with an executed interconnection agreement — i.e., almost every new large load. **The output** is a recommended posture with rationale, a named execution team with gaps flagged, and a dated workplan to the July 10, 2026 eligibility deadline.

## 2. The clock

The decision is made in this round. There is no retroactive entry or election.

| Date (DRAFT) | Gate |
|---|---|
| **July 10, 2026** | Hard eligibility deadline. Required study components, intermediate/interconnection agreements, and (for WLPUN) the generator Full Interconnection Study must be complete. |
| **July 24, 2026** | TSP/DSP attestation. |
| **August 7, 2026** | Classifications issued (Base Load vs Studied Load). |
| **~30 days out (per TSP intel)** | A wave of ERCOT designations is expected to pull combustion turbines / reciprocating engines off the market — equipment availability tightens sharply right as demand for it spikes. |
| **Batch One (per TSP intel)** | The window may not open until ~Q3 2027, with answers not landing until mid-to-late 2028 — i.e., missing Batch Zero is not a short wait. |

As of this draft (2026-06-05), the eligibility deadline is roughly **five weeks out.** That compression is the single most important planning fact: it forces parallel workstreams and it makes WLPUN reachable this round only for projects whose generator FIS is already in flight (see §3, §7).

## 3. The two decisions

### Decision 1 — Classification: Base Load vs Studied Load

```
Are validated ERCOT studies complete AND an interconnection agreement
executable, with construction able to energize before 2028?
        │
        ├── YES ──►  BASE LOAD.  Take it. Full requested MW guaranteed,
        │            requested energization date kept, no allocation risk.
        │            The flexibility elections below are then OPTIONAL.
        │
        └── NO  ──►  STUDIED LOAD.  Low bar to enter (one approved study
                     component + intermediate agreement), but energization
                     resets to 2028+, and ERCOT sets your annual served
                     capacity — which can be cut, worst case to zero, in a
                     constrained year until transmission is built (2028–mid-2030s).
                     ► Go to Decision 2.
```

**Rule of thumb: if you can reach Base Load, take it.** Base is mostly reachable only by already-studied / advanced projects. For everything else, the project is Studied, and the *posture election becomes the entire decision.*

### Decision 2 — Posture (only if Studied): Firm vs PCLR vs WLPUN

| Posture | What it is | Min allocation | Cutback exposure | Form / gate | Fits |
|---|---|---|---|---|---|
| **Studied Firm** | Take ERCOT's allocation as-is | ERCOT-set | **Most exposed** | Standard | Sites confident in regional firm capacity; no flex |
| **PCLR** (Provisional Controllable Load Resource) | Commit a firm Low Power Consumption and curtail to it on constrained hours (controllable demand) | **0 — escapes cutbacks** | Avoided via curtailment | Notarized **Form W** + QSE | Loads that can shift/pause or ride through on **storage** |
| **WLPUN** (Withdrawal-Limited Private Use Network) | Co-locate non-exporting generation; ERCOT caps grid **import** and your generation covers the rest | **0 — escapes cutbacks** | Avoided via self-generation | Notarized **Form X** + generator **FIS complete by July 10** | Sites with **firm fuel + dispatchable generation** |

Both PCLR and WLPUN drive minimum allocation to zero and thereby **escape the cutback** that makes Studied Firm risky. The choice between them is a choice between **carrying the shortfall with demand flexibility (PCLR)** or **carrying it with your own generation (WLPUN)**.

## 4. The one number that drives everything

If the project is Studied, the whole strategy reduces to **one number: how much firm grid capacity ERCOT will actually allocate, and when.** Everything else is sizing off that.

> **Shortfall = Load − Firm grid allocation.** That shortfall has to be carried by controllable demand (PCLR) or your own generation (WLPUN).

At scale this is **not** occasional backup. A **1 GW load with ~500 MW firm allocation needs ~550–600 MW of continuous-duty generation** that runs most hours in the early years and tapers only as transmission arrives (2028–mid-2030s). Two consequences follow immediately:

- **Permitting class tracks run-hours.** Continuous duty needs a longer-lead air permit (TCEQ), *not* an emergency-standby permit. Size the permit to the real run-hour profile or the plant is not legal to run as the strategy requires.
- **Fuel must be as firm as the power.** Firm gas supply *and* firm transport (midstream/pipeline) have to be contracted to the same reliability as the load. "We have gas nearby" is not firm fuel.

This is why the Batch Zero decision is inseparable from equipment procurement and fuel: the posture election *implies* a generation or storage build, and that build has lead-time and permitting consequences that start now.

## 5. Posture selection guide

| If the site profile is… | Recommended posture | Why |
|---|---|---|
| Already studied + IA executable, energize <2028 | **Base Load** | Guaranteed MW, no allocation risk; elections optional |
| Strong regional firm capacity, no operational flex, schedule-tolerant | **Studied Firm** | Simplest; accept allocation risk only where the region supports it |
| Load can shift/pause, or storage can ride through constrained hours | **PCLR** | Min allocation 0, lighter capex than full generation, fits flexible manufacturing / storage-backed loads |
| Firm fuel + dispatchable generation available; load needs continuous power | **WLPUN** | Min allocation 0; self-generation carries the shortfall — but only viable this round if the generator FIS is already underway |
| Need power fast, grid years away, want eventual grid asset | **WLPUN as bridge** (see below) | Speed-to-power now, transitions to grid asset later |

### The bridge structure (the high-value pattern)

The pattern that recurs in live deals: a **20-year PPA with a ~5-year off-ramp**, generation built **simple-cycle for speed-to-power**, transitioning over 4–5 years to **combined-cycle (CCGT) pointed back at the grid as a system resource.** This gives the offtaker speed and a price guarantee while the IPP builds the permanent asset that ultimately serves downstream load. Watch the economics: **simple-cycle alone does not pencil as a baseload grid asset** (utilization too low) — the transition to CCGT, or partnering with a group that already owns CCGT fleets, is what makes the back end real. This is where a balance-sheet utility/IPP (vs. a packager bolting a turbine into a box) is the right partner for the grid-asset leg.

## 6. The Cantus seat and where the economics are

Cantus holds the **orchestrator / power-strategy seat** and brokers procurement — it does **not** operate the asset. The monetization is a **back-end participation in the PPA**, defended by control of the scarce inputs.

- **What Cantus does:** sets posture (this playbook), runs the integrated team, brokers and *holds* equipment slots, selects and integrates the best EaaS/IPP, structures the PPA.
- **How Cantus earns:** a back-end participation that rides the PPA for its term — cleanest as a per-MWh override; alternatively a carried promote in the project SPV, or a structuring + ongoing energy-management fee.
- **Why it's durable (the lock):** Cantus controls the two inputs the operator can't self-source under this deadline — **equipment slots** (the long-lead iron — turbines, reciprocating engines, transformers, switchgear, BESS) and **site / interconnection position.** Make Cantus a *party to the PPA* (contract the power, sleeve it to the tenant, subcontract delivery to the EaaS/IPP) so the participation is a contract right, not goodwill.
- **Scale:** illustratively, a 500 MW campus at ~85% load factor is ~3.7M MWh/yr; a $1–2.5/MWh participation is ~$4–9M/yr, recurring, against an IG-credit counterparty, over a 15–20 year PPA. (Illustrative; validate per deal.)

This is the lighter-capital posture (close to "orchestrator") but with annuity economics — see [[Strategy/Cantus-Execution-Operating-Model]] for how it sits across the three seat postures.

## 7. The execution team

One firm may cover several roles. **Bold = the Cantus-held seat or where Cantus drives selection.** Flag gaps explicitly per engagement.

**Regulatory & interconnection**
- ERCOT regulatory / energy counsel fluent in PGRR145, SB6, §25.194.
- The interconnecting **TSP/DSP** — the gatekeeper; studies are TSP-led (CenterPoint, Oncor, AEP Texas per geography). *CenterPoint relationship is a Cantus asset.*
- Power-systems / interconnection engineer — runs and coordinates the ERCOT studies (steady-state, stability, short-circuit), dynamic load modeling, and the generator FIS for WLPUN.
- Qualified Scheduling Entity (QSE) — resource registration, telemetry, dispatch (required for PCLR; for WLPUN control).
- Texas notary — Form W/X and §9.2.1.2 attestations.

**Generation (WLPUN path)**
- **Generation developer / IPP** with dispatchable units — *Cantus selects and lines up the trusted IPPs* (e.g., the Thunderhead-type fast-deploy packagers for speed-to-power; NRG / Constellation-type balance-sheet utilities for the CCGT-to-grid leg). Match the partner to the leg.
- Prime-mover OEM — reciprocating engines or aeroderivative/gas turbines (Caterpillar, Wärtsilä, Cummins, GE Vernova, Mitsubishi Power, Solar Turbines per `_parameters`). Long lead times — slot-hold now.
- EPC contractor — plant, substation, interconnection facilities. (Install + site setup is the majority of cost — installed all-in observed ~$2.5–2.6M/MW excl. pipeline; illustrative.)
- Firm fuel — gas supplier + midstream/pipeline for firm supply *and* transport.
- Air-permitting / environmental engineer (TCEQ) — **sized to the run-hour profile** (continuous-duty, not emergency-standby).

**Demand flexibility (PCLR path)**
- Battery storage developer/integrator + storage OEM (Tesla, Fluence, Powin per `_parameters`).
- Controllable-load / demand-response controls provider — software that dispatches between Low and Max Power Consumption.
- Telemetry / SCADA integrator.

**Site & development**
- Land owner / **powered-land developer** (site control: lease/deed/PSA/option) — *Cantus Development seat where Cantus is principal.*
- Real estate / site advisory (land, transmission adjacency, water).
- Civil, geotechnical, water/wastewater engineers; survey & title.
- Land-use / zoning counsel for discretionary approvals.

**Capital & commercial**
- Project finance / capital markets — fund generation/storage and post the **$50,000/MW security + CIAC** (cash, BBB-/Baa3 guaranty, or A- bank LC).
- Tax / incentives advisor — federal program capital, storage ITC, manufacturing credits.
- End user / offtaker — the binding demand commitment.
- **Energy procurement / power-marketing advisor — PPA structuring** (*Cantus, where it captures the back-end participation*).

**Orchestration**
- **Development quarterback / owner's engineer — coordinating power, site, tenant, and capital as ONE engagement** (*the Cantus seat*), plus corporate/transaction counsel for the interconnection agreement, leases, and development agreements.

## 8. Workplan to July 10, 2026

Working back from the deadline (~5 weeks). Parallel, not sequential. Owners are role-tagged; one party may hold several.

| When | Milestone | Owner |
|---|---|---|
| **Week 1 (now)** | Lock the "one number": pull TSP read on firm allocation + queue position; classification triage (Base-eligible or Studied?). Engage ERCOT counsel + interconnection engineer. Confirm site control status. | Quarterback (Cantus) · TSP · Counsel |
| **Week 1** | **WLPUN gate check:** is a generator FIS already in flight? If not, WLPUN is likely off the table this round → default to PCLR or Studied Firm. | Engineer · QSE |
| **Week 1–2** | Posture decision (Firm / PCLR / WLPUN) with sizing of the shortfall and the generation/storage block it implies. | Quarterback (Cantus) · Engineer |
| **Week 2** | Equipment: secure OEM slot reservations / IPP LOI *now* — ahead of the ~30-day designation rush. PCLR: engage storage + controls/QSE. | Cantus (procurement) · IPP/OEM |
| **Week 2–3** | Studies: secure the one approved study component (Studied bar) or push validated studies to executable IA (Base bar). TSP coordination. | Engineer · TSP |
| **Week 3–4** | Forms: draft Form W (PCLR) or Form X (WLPUN); §9.2.1.2 attestations; notary. Air permit application started, sized to run-hours (WLPUN). | Counsel · Notary · Env engineer |
| **Week 3–4** | Capital: arrange $50,000/MW security + CIAC instrument (cash / guaranty / LC). Firm fuel LOIs (WLPUN). | Project finance · Fuel supplier |
| **By July 10** | **Eligibility submission complete** — study component + intermediate/interconnection agreement (+ generator FIS for WLPUN). | Quarterback (Cantus) |
| **July 24** | TSP/DSP attestation filed. | TSP/DSP |
| **August 7** | Classification received; confirm posture holds; begin build mobilization. | Quarterback (Cantus) |

**Binding gate:** the WLPUN generator-FIS-by-July-10 requirement is the hardest constraint. If the FIS is not already underway, treat WLPUN as unavailable this round and choose between PCLR and Studied Firm.

## 9. Worked example — Singleton / Gibbons Creek

*Applies the framework to the Singleton opportunity carried in `_parameters` (Singleton 345kV, ~500 MW interconnection at Singleton substation; repositioned toward large-load / hyperscale use). Facts below are partly drawn from internal pipeline notes and partly open — confirm before relying.*

**What we know / believe:**
- Interconnection at the **Singleton 345 kV substation**; CenterPoint territory.
- CenterPoint guidance: serving additional load off the 290s corridor depends on **new generation to the north** — i.e., the grid will not carry the full load near-term without co-located/new generation.
- A large (~3 GW) downstream load corridor exists in the **Gibbons Creek** area; the retired Gibbons Creek site is a brownfield with potential transferable interconnection value — a candidate for the generation-to-the-north that ultimately becomes a grid asset.

**Read against the framework:**
- **Classification:** new large load, studies not validated/IA-executed → **Studied Load.** Base is not reachable here this round.
- **Posture:** because CenterPoint has effectively said firm grid capacity is constrained until generation/transmission catches up, the firm allocation (the "one number") is low near-term → carry the shortfall with **self-generation → WLPUN**, *if* a generator FIS can be in place by July 10. If the FIS is not already underway, fall back to **PCLR** (storage-backed ride-through) for this round and pursue the generation build for a later transition.
- **Structure:** this is the textbook **bridge** case (§5): simple-cycle for speed-to-power under a 20-year PPA with a ~5-year off-ramp, transitioning to **CCGT pointed back at CenterPoint as a grid asset** — exactly the generation-to-the-north CenterPoint needs to unlock the downstream corridor. Pair a fast-deploy IPP for the bridge with a balance-sheet utility/IPP (NRG / Constellation-type) for the CCGT-to-grid leg; simple-cycle alone won't pencil as baseload.
- **Cantus seat / economics:** Cantus quarterbacks the strategy, holds the equipment slots and the Singleton site/interconnection position, brings the IPP(s), and takes a back-end PPA participation — durable because Cantus controls the slot + site that the generation-to-the-north depends on, and because the generation it enables serves *downstream* Cantus pipeline load.

**Facts still needed to finalize (the ROLE site-facts block):**
- Exact requested MW and target energization date.
- Current ERCOT study status and whether any component is approved.
- Site control instrument and status (lease/deed/PSA/option).
- Gas access — firm supply + transport availability to Singleton.
- Whether a generator FIS is already in progress (the WLPUN gate).
- Sponsor credit / who posts the $50k/MW security + CIAC.
- Storage option sizing if PCLR is the fallback.

## 10. Economics quick-reference (illustrative / DRAFT)

For framing only — every figure is deal-specific and must be validated.

| Item | Illustrative value | Note |
|---|---|---|
| BTM / IPP PPA, all-in delivered (incl. gas pass-through) | ~$100/MWh (10¢/kWh) for a 15–20 yr PPA | Reservation portion ~$50–60/MWh; equipment off the offtaker's balance sheet |
| Grid power fully landed (Corpus/AEP reference) | ~$45–55/MWh (run $50); some quote $35 by ignoring T&D — not valid | Manufacturing teams' line-in-the-sand ~$65/MWh |
| ERCOT interconnect feeder security | $50,000/MW | Plus CIAC |
| Installed generation, out-the-door (excl. pipeline) | ~$2.5–2.6M/MW | Install + site setup > equipment cost |
| Delay penalty (lost revenue for late power) | $4M/MW/yr (illustrative midpoint; data-center cases cited $8–12M/MW/yr) | Use case–specific; this is what neutralizes the BTM premium |

The strategic point the numbers make: once you price in the **delay penalty**, the BTM premium over Studied-grid largely neutralizes — and on a constrained Studied site, **speed-to-power behind-the-meter can come out ahead.** As BTM adoption rises, expect equipment to leave the market faster and lead times to extend — so the procurement-slot position is itself a source of advantage.

---

## Caveats

- All rule figures (deadlines, thresholds, forms, allocation mechanics) are **DRAFT and pending regulatory approval** (PGRR145 / SB6 / PUCT 16 TAC §25.194). Confirm current rule text before relying.
- This is **advisory, not legal or engineering advice.** Counsel and licensed engineers own the regulatory filings and the studies.
- Economic figures are **illustrative** and must be validated per deal.

---

*Draft playbook. Pairs with the Cantus execution operating model. Aligns to the v2 four-vertical architecture, [[Strategy/Cantus-Infrastructure]] (Cantus Prime), and the Power Producer → Production Company → Studio arc. Author of record: Dom Espinosa. 2026-06-05.*
