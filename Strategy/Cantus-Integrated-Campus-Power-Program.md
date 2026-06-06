---
type: strategy
status: draft
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-06-05
updated: 2026-06-06
strategy_area: energy
related_framework: ["[[Strategy/Cantus-Power-Sector-Thesis]]", "[[Strategy/Cantus-Business-Plan]]", "[[Strategy/Cantus-Development]]", "[[Strategy/Cantus-Infrastructure]]", "[[Strategy/Cantus-Markets]]"]
related_pages: ["[[Strategy/Batch-Zero-Power-Strategy-Playbook]]", "[[Partners/Execution-Partners-Registry]]", "[[Strategy/Cantus-Execution-Operating-Model]]", "[[Strategy/Cantus-NPI-Boundary]]"]
working_files:
  - "~/Documents/Cantus/Cantus/Execution-Model/Cantus-Execution-Operating-Model-v0.1.xlsx"
  - "~/Documents/Cantus/Cantus/Deliverables/Cantus-Integrated-Campus-Power-Program-2026-06-05.docx"
applies_to_phase: building
tags: [strategy, integrated-campus, power-program, wlpun, pclr, ccgt, bridge-to-grid, private-use-network, revenue-stack]
---

# The Cantus Integrated Campus Power Program

*One platform, both phases, one PPA — adapted to Cantus. Takes the integrated power-and-real-estate campus model and resolves it against Cantus's actual posture, then weaves in Greenflash (battery / PCLR / power quality) and Splight (interconnection intelligence). NPI remains the arm's-length advisory sister (see [[Strategy/Cantus-NPI-Boundary]]).*

> Draft strategy — not legal or engineering advice. All ERCOT rule figures are DRAFT pending regulatory approval (PGRR145 / PUCT §25.194 / NOGRR282). Named firms are illustrative, not endorsements. Author of record: Dom Espinosa.

---

## 1. What we keep from the model

The core of the model is right and worth adopting wholesale: **sign one long-tenor PPA with the anchor and orchestrate every layer beneath it, so the customer sees a single counterparty across both phases.** Three layers under one contract:

1. **Bridge / speed-to-power (yr 1–5) — WLPUN.** Co-located, non-exporting simple-cycle turbines cover the gap between the load and whatever firm grid import exists. The campus elects WLPUN; the turbines are the nameplate. Fast, financed as a power service, redeployable.
2. **Battery layer — PCLR + power quality.** Co-located BESS smooths AI training loads (20–100% swings in 1–10s; resonant oscillations rotating generation can't absorb), provides UPS and ride-through, and enables a PCLR election on the grid-import slice. Because the battery is required for power quality anyway, the PCLR economics come at near-zero incremental cost.
3. **Permanent power (yr 5+) — CCGT.** A combined-cycle plant built over ~4–5 years, timed to the end of the bridge. The anchor's PPA carries an **optional 5-year off-ramp** that is a *right to re-point, not to terminate*: freed capacity flows to the grid (the CCGT interconnects as a grid asset) and to other campus users.

And the campus is a **Private Use Network** — anchor plus suppliers/manufacturers behind one point of interconnection, sharing generation, BESS, microgrid, EMS, and interconnection, with WLPUN as the Batch Zero flavor. This is precisely the Cantus **Intelligent Campus**, expressed as a power structure.

The reason this compounds is the model's best insight: **speed-to-power de-risks and multiplies the real estate.** A powered shell that can actually energize on schedule is worth far more than raw powered land — so the power program and the real estate make each other more valuable. That is the Cantus integration thesis, stated in cash flows.

## 2. The one decision the model forces: do we own the CCGT fleet, or orchestrate it?

The model's "why we are the right owner" argument rests on being a **CCGT fleet owner with a trading desk** — the balance sheet to finance across phases and the book to monetize the CCGT's second life after the off-ramp. **Cantus is not that today.** Cantus is a developer-principal and integrator (see [[Strategy/Cantus-Execution-Operating-Model]]): it owns land, buildings, and the orchestration, and it keeps a back-end participation in the power contract — it does not own a merchant generation fleet or run a trading desk. So the model can't be adopted unchanged; the fleet-ownership layer has to be resolved. Three options:

| Option | Who owns the CCGT fleet + trading | Cantus role | Capital | Fit |
|---|---|---|---|---|
| **A — Orchestrate (recommended now)** | A fleet-owner partner (NRG / Constellation-type) or funded IPP | Cantus owns land + buildings + orchestration, signs the anchor PPA, keeps real-estate economics + a power back-end | Light–medium | Building / Activation |
| **B — Cantus-sponsored JV / platform** | A purpose-built SPV: Cantus (land, buildings, origination, CII/DealOS) + fleet/capital partner (CCGT, trading, balance sheet) | Cantus is the integrator-sponsor (GP-like); partner is the power-capital principal | Medium | Activation → Compounding |
| **C — Own the fleet (become the full platform)** | Cantus | Cantus captures the entire power margin + trading upside | Heavy; needs balance sheet + trading desk | Compounding / Studio only |

**Recommendation: run Option A now, structure toward Option B, hold Option C as a Studio-phase election.** This matches Cantus Infrastructure's stated posture — integrator/structurer now, "selective direct operator in Compounding+" — and the open question on that page about when Cantus becomes a direct Power Asset operator. The trigger to internalize fleet ownership (Option C) is the same one the framework already names: when integrated microgrid/fleet control becomes inseparable from the campus operating envelope *and* Cantus has the persistent capital to carry it.

Crucially, **the "one PPA, one counterparty" promise survives all three options.** Cantus (or the Cantus-sponsored SPV) signs the anchor PPA and subcontracts the fleet beneath it. The anchor still sees one platform; Cantus still controls origination, site, buildings, and the integration. What changes across A→B→C is only *how much of the power margin Cantus keeps vs. shares* — see §5.

## 3. The three-layer power program, the Cantus way

Mapped onto the partners we've already lined up ([[Partners/Execution-Partners-Registry]]):

- **Bridge / WLPUN (yr 1–5).** Simple-cycle for speed. **Thunderhead** (Harbert-funded BTM IPP, recip+turbine hybrid, bridge-or-permanent) funds, owns, and operates the bridge plant; **Turbine-X** supplies the turbines (Baker Hughes NovaLT, quick-start, multi-fuel). Cantus orchestrates and holds the back-end. The bridge is financed as a power service, off the anchor's balance sheet.
- **Battery / PCLR + power quality.** **Greenflash** delivers the co-located BESS + EMS + power quality (BESS-UPS at MV, ride-through, 90%+ ripple reduction). Engage **Build-Transfer-Operate, not BOOM**, so ownership and energy-management economics stay with Cantus. Because the battery is required for power quality regardless of posture, the PCLR election rides on top at near-zero incremental cost — exactly the model's point.
- **Permanent / CCGT (yr 5+).** **Turbine-X** combined-cycle is the equipment leg; the **fleet-owner partner** (Option A/B) absorbs the CCGT's second life and trading after the off-ramp. Cantus structures the re-point of freed capacity to the grid and to campus users.

### Splight is the lever that improves every layer

Splight isn't just the load-study vendor for the July 10 deadline — it changes the sizing of the whole program. Its claim to unlock **2–3x usable transmission capacity** means it can **raise the firm grid-import number**. Every incremental firm MW Splight unlocks is a MW the bridge turbines *don't* have to cover — directly shrinking the bridge capex, the gas requirement, and the air-permit burden. So Splight does four things here:

1. Runs the next-gen electrical/load studies and the WLPUN generator-FIS support toward July 10.
2. **Maximizes firm grid import → minimizes the bridge generation Cantus has to finance** (the single biggest cost lever in the whole program).
3. Accelerates the CCGT-to-grid interconnection at the off-ramp (its generation-interconnection use case).
4. Screens the CII Parcel Registry portfolio-wide for *true* available capacity, upgrading site selection upstream.

Net: **Splight shrinks the bridge; Greenflash makes the load behave; Thunderhead/Turbine-X carry the shortfall; the fleet partner takes the permanent leg; Cantus owns the campus and the PPA.**

## 4. The campus as a Private Use Network

The anchor-plus-suppliers campus behind a single point of interconnection is more capital-efficient (shared CIAC, security, O&M) and more bankable (staggered ramps, varied credit) than any single tenant — and it gives the off-ramp capacity a *home* as the anchor migrates to grid. This is the Cantus Intelligent Campus, and it is what makes the conditioned off-ramp financeable: the long anchor PPA underwrites the CCGT debt; the optional off-ramp gives the anchor flexibility; the grid + campus-user re-point is the platform's hedge. Cantus Development assembles and owns the land and shells; Cantus Prime runs the power program; Cantus Markets carries the PPA, capital, and back-end.

## 5. Cantus's stacked revenue model

Cantus captures value at every layer it owns. The real-estate and land economics accrue to Cantus in *all three* ownership options; only the power-margin line changes:

| Revenue layer | Source | Option A (orchestrate) | Option C (own fleet) |
|---|---|---|---|
| **Power margin** | Bridge PPA + permanent CCGT PPA + merchant/grid after off-ramp + PCLR/ancillary value from BESS | Back-end PPA participation (~$1–2.5/MWh illustrative) + integration/structuring fees | Full power margin + trading upside |
| **Powered-shell leases** | Buildings delivered power-ready, leased to anchor + campus users (~$80–120/kW-month illustrative) | Cantus | Cantus |
| **Land lift** | Raw → entitled/powered → developed campus (~$2.5–10K/acre → ~$800K/acre, TX ref) | Cantus | Cantus |
| **Integration premium** | Speed-to-power multiplying the real estate (a schedulable powered shell ≫ raw powered land) | Cantus | Cantus |

*(Figures illustrative / from `_parameters.md`; validate per deal.)*

The strategic read: **the real-estate stack — powered-shell leases, land lift, and the integration premium — is Cantus's to keep regardless of the fleet decision.** That is the capital-light, durable core. The fleet-ownership decision is really a decision about whether to *add* the full power margin and trading upside (Option C) on top — at the cost of carrying merchant generation and a trading book. Recommendation stands: take the real-estate + back-end stack now (Option A), and only reach for the full power margin once persistent capital and an operating rationale justify it.

## 6. Counterparties Cantus orchestrates

From the registry, plus the gaps this model adds:

- **Battery / microgrid + EMS:** Greenflash (Build-Transfer-Operate). ✓ lined up
- **Bridge IPP + turbines:** Thunderhead (funded operator) + Turbine-X (NovaLT turbines; CCGT leg). ✓ lined up
- **Interconnection studies + capacity unlock:** Splight. ✓ lined up
- **CCGT fleet owner / trading partner:** NRG / Constellation-type — **gap to fill (the Option A/B partner).**
- **Fast-turbine bridge alternative:** ProEnergy / GE Vernova TM2500-type mobile units — optional second bridge source.
- **Firm gas supply + midstream; gas+substation EPC; ERCOT counsel; interconnecting TSP/DSP (CenterPoint relationship is a Cantus asset); QSE; notary; air-permitting engineer; project finance; anchor offtaker (hyperscaler-grade credit); real-estate development/leasing/land teams** — **standard open seats** per the playbook.
- **Origination / advisory:** NPI, arm's-length (the boundary holds).

## 7. Structuring the off-ramp (the financeable detail)

The off-ramp must be an **option conditioned on replacement offtake**, not a termination right — a right to *re-point*. The long anchor PPA underwrites the CCGT debt; the conditioned option gives the anchor flexibility; the re-point to grid + campus users is the platform's hedge and where the Private Use Network earns its keep. Whoever owns the fleet (Cantus in C; the partner in A/B) absorbs the transition into the fleet and trading book — it is their core business, not the anchor's risk. Cantus's job in A/B is to *structure* that re-point and keep a participation in it.

## 8. Workplan to July 10, 2026

Per the [[Strategy/Batch-Zero-Power-Strategy-Playbook]], with the layers parallelized. Binding regulatory gates:

- **WLPUN:** notarized **Form X** + generator **FIS complete by July 10** (Splight + interconnection engineer own this — the hardest gate).
- **PCLR:** notarized **Form W — Part A by July 10, Part B by March 1, 2027** (Greenflash + QSE).
- **Air permit:** simple-cycle as primary power for 5 years needs a **non-emergency air permit** (long lead — start now).
- **Turbine slots + firm gas:** long-lead, parallel workstreams — reserve ahead of the ~30-day designation rush (Turbine-X / Thunderhead + gas/midstream).
- **Splight** runs studies to maximize firm import *before* the bridge is sized, so the generation block is as small as possible.
- **Fleet-owner partner** (Option A/B) engaged in parallel so the permanent-CCGT and off-ramp terms are in the anchor PPA from signing.

## Caveats

- Rules are DRAFT (PGRR145 / PUCT §25.194 / NOGRR282) and may change; verify against current filings before binding use.
- All economics are illustrative and must be validated per deal.
- Partner facts are per the registry (some unverified web sources); named firms are illustrative, not endorsements.
- NPI remains arm's-length advisory; no NPI internal material is used here.

---

*Draft strategy. Pairs with the Batch Zero playbook, the partners registry, the seat memo, and the Cantus–NPI boundary. Aligns to the v2 four-vertical architecture and the Power Producer → Production Company → Studio arc. Author of record: Dom Espinosa. 2026-06-05.*
