# The Cantus Company — Wiki Operating Manual

*Source of truth for any LLM agent working in this repository. Read it completely before taking any action. When in doubt, re-read the relevant section.*

*Operating mode: agent-as-chief-of-staff. The agent drafts; **Dom Espinosa** signs as author of record on every output. The agent maintains the wiki; humans contribute knowledge and make decisions. The agent never appears as a byline.*

*Authoritative companions: read `_cowork-context.md` and `_parameters.md` at repo root before any task. Read `index.md` to find what exists before creating anything new.*

---

## What This Repository Is

A founder-led wiki for **The Cantus Company (Cantus Coordination LLC)** — Dallas-based powered infrastructure advisory, intelligence, and investment firm targeting AI infrastructure and advanced manufacturing markets.

This vault is built on the Karpathy LLM Wiki pattern. Knowledge accumulates in structured markdown pages with rich frontmatter and explicit cross-references. Agents handle structure, cross-references, and bookkeeping. Dom contributes the strategic articulation, decisions, and direction.

This is **not** a practice within a larger organization. Cantus is its own firm. Operating discipline reflects that — lighter governance than enterprise wikis, tighter strategic coherence than multi-stakeholder repos.

This is **not** the Newmark Powered Industries vault. NPI is Dom's current role at Newmark; Cantus is the firm being built independently. Different repos, different audiences, different conventions. See "Firewall with Newmark / NPI" below.

---

## The Sentence

> *Cantus is building integrated intelligence.*

Memorize. Use as the anchor. Every strategic document pulls toward this sentence.

---

## What Cantus Is

The integrator across the emerging Power sector — the firm that assembles Land, builds Facilities, powers them with integrated Infrastructure, makes them productive through Machines and software, and commercializes the platform through capital, customer, contract, and commodity allocation. Cantus operates across the 10 Power sub-industries through a four-vertical operating architecture, anchored by two cross-cutting Foundations. The strategic claim is that the Power sector is forming as the organizing sector of the next industrial era, and that no single-tier operator can replicate the integrated platform Cantus is constructing.

The firm's identity arc:

- **Power Producer** — current. Senior Cantus staff function as Power Producers (the orchestrator role analogous to film producers — integrators of multi-sub-industry productions).
- **Power Production Company** — current firm form. A company that aggregates Power Producers, infrastructure, and integration intelligence into delivered productions.
- **Power Studio** — strategic horizon (Years 8+). Platform-level firm with persistent capital, multi-fund family, controlled operating positions. The reference cohort: Brookfield Infrastructure, BlackRock-GIP, Stonepeak, EQT Infrastructure, and major sovereign wealth platforms — but constructed from the demand-side outward rather than the supply-side outward.

### The Four-Vertical Architecture (v2, 2026-05-24)

Cantus operates through four value-creation-stage verticals rather than ten sub-industry mirrors. Each vertical maps to a stage in the firm's integrated production sequence:

| Vertical | Power sub-industries owned | Role in the sequence |
|---|---|---|
| **Cantus Development** | Power Land + Power Facilities | Creates the sites |
| **Cantus Infrastructure** | Power Assets + Power Equipment + Power Services | Powers them |
| **Cantus Technology** | Power Machines + Power Technology | Makes them productive |
| **Cantus Markets** | Power Industries + Power Commodities + Power Markets (broad allocation) | Monetizes and finances the output |

Cantus Development and Cantus Markets are the direct-principal verticals. Cantus Infrastructure is integrator + counterparty + structurer. Cantus Technology is orchestrator + selective operator (Cantus Compute is the named selective-operator business; Cantus Robotics is the modeled future addition).

### Two Foundations

Beneath the four verticals, two Foundations cross-cut every vertical and compound across the firm:

- **Labor / Community** — workforce development, R1 university partnerships, area-education program coordination, community engagement. The most labor-intensive consumer is Cantus Infrastructure; the function flows across all four verticals.
- **CII / DealOS** — Cantus Integrated Intelligence (23 data assets across 5 families, 4 prediction-and-resolution loops, 23 product surfaces) plus the deal-level operating system. The Foundation is internal-first with selective external surface exposure to capital partners, tenants, and co-development partners.

Technology Integration, which was a Foundation in v1, is now operationally executed inside the **Cantus Technology** vertical (no longer a separate Foundation — the v2 framework promotes the operating layer into a vertical and reserves Foundation status for capabilities that don't fit one vertical).

### Cantus Compute, Cantus Robotics, Cantus Prime, Cantus Edge

Long-horizon Cantus business identifiers sitting inside the four-vertical architecture:

- **Cantus Compute** — hosted GPU and AI compute operating business. Lives inside Cantus Technology as a selective-operator Power Machines + Power Technology business. The Crusoe / CoreWeave structural reference and competitive frame; Cantus Compute is differentiated by the integrated Land + Facility + Infrastructure stack.
- **Cantus Robotics (modeled)** — robotics-as-a-service for industrial tenants, especially Advanced Manufacturing and Defense Industrial Base. Compounding phase or later.
- **Cantus Prime** — customer-agnostic infrastructure prime contractor archetype. Lives inside Cantus Infrastructure as the firm-level orchestration label.
- **Cantus Edge** — on-prem AI for tenants. Lives inside Cantus Technology, not as a standalone Tier-1 business.

**Cantus Forge is retired.** Cantus Prime replaces it. Never use "Forge."

### Phasing

| Phase | Years | What |
|---|---|---|
| Building | 1–2 | Capability building, advisory, first co-development; balance-sheet operation; capital-partner curation; CII data-asset construction |
| Activation | 3–4 | First Cantus-led Intelligent Campuses; Fund I ($250M–$500M); principal positions in Development; Cantus Compute pilot in Cantus Technology |
| Compounding | 5–7 | Multi-campus operating; second funds; selective Cantus Technology operating businesses scaling; multi-vertical mature operations |
| Mature platform | 8+ | Institutionalized Power Studio with full integrated platform across the four verticals |

---

## Goals

1. **Founder coherence.** Cantus's strategic articulation stays internally consistent across documents. The framework, parameters, and capital story align.
2. **Compounding institutional knowledge.** Every conversation, partner discussion, and capital-partner meeting feeds the wiki. Future-Dom and future hires inherit the full context.
3. **Agent-extended thinking.** The agent runs intelligence loops, drafts strategic articulations, and surfaces cross-document tensions Dom should resolve.
4. **Clean defensibility.** Every claim in capital-partner-facing material traces back to a parameter, a thesis page, or a referenced source. The vault is the chain of custody.
5. **Portable.** Plain markdown, plain Git. No vendor lock-in. The firm's intellectual property is owned by the firm, not by the tooling.

---

## Surfaces and Paths

| Surface | Purpose | Path |
|---|---|---|
| **Wiki (this vault)** | Agent-maintained markdown pages, frameworks, parameters, intelligence | `~/Documents/Cantus-wiki/` |
| **Working files** | Native-format firm-building materials (capital partner decks, partner term sheets, financial models) | `~/Documents/Cantus/` |

Wiki pages reference working files via the `working_files:` frontmatter field. The agent reads both surfaces.

---

## Contributors

Currently solo (Dom). Designed to scale gracefully:

- **Dom Espinosa** — Founder, sole contributor today
- Selective contributors over time: advisors with specific expertise, future hires (per the Team-and-Org GTM doc), capital partners running diligence (read-only access to specific subsets)

Governance is intentionally lighter than the NPI vault until headcount justifies more structure. See "Git Workflow" below.

---

## Firewall with Newmark / NPI

Dom's day role is Senior Managing Director at Newmark Powered Industries. NPI work has its own vault at `~/Documents/Newmark-wiki/`. Hard rules:

1. **No NPI client material in this vault.** Active NPI deal files, client OMs, broker compensation, NPI v2 assessment internals — none of it crosses.
2. **Cantus terminology is Cantus-only.** "Intelligent Campus," "Cantus Prime," "Operating Triangle," "Two Customer Stacks," "Cantus Integrated Intelligence" are foundational here. They do not appear in NPI deliverables.
3. **NPI internal language is NPI-only.** Section 14 scoring, NPI v2 assessment, "Ready to show now / with caveats / not yet" verdicts are NPI-internal. Cantus capital-partner and tenant material reads as independent firm articulation.
4. **Some pages are intentionally forked across both vaults** with different framing — Bridge-to-Grid Thesis (NPI conversation playbook / Cantus foundational thesis), ERCOT regulatory framework (NPI client primer / Cantus positioning thesis), Crusoe (NPI counterparty page / Cantus internal structural reference).
5. **The synthesizer behind both is Dom.** That's deliberate. NPI and Cantus are different voices for different audiences. The strategic intent comes from one person.

If you find content that seems to belong in the other vault, do not move it. Flag it for Dom.

---

## Folder Structure

```
Cantus-wiki/
├── _README.md                  # This file
├── _cowork-context.md          # Cantus-specific operating context
├── _parameters.md              # Single source of truth for numbers, names, dates
├── index.md                    # Wiki content catalog
├── log.md                      # Append-only operation log
├── ONBOARDING.md               # New contributor walkthrough
├── raw/                        # Source material — two-mode (inbox + persistent assets)
│   ├── inbox/
│   ├── articles/
│   ├── papers/
│   ├── transcripts/
│   ├── data/
│   └── assets/
├── Strategy/                   # Framework Parts 1-2, Primary Inputs, Bridge-to-Grid, Market Sizing, Advanced Industrial Spec
├── Products/                   # CII (Cantus Integrated Intelligence) — data assets, loops, surfaces
├── DealOS/                     # DealOS product specs, architecture, GTM
├── GTM/                        # Go-to-market, team, exec summary, investor deck, outreach drafts
├── Capital/                    # Capital architecture, fund structure, principal positions, Year 6 FCF model
├── Partners/                   # Co-development partners (Hillwood, Crow, Howard Hughes, Majestic), capital partners, OEM strategic relationships
├── Intelligence/               # Market intel, regulatory positioning, competitive analysis (Cantus-relevant)
├── Vision/                     # Active company-vision workshop docs
├── Workshop/                   # Cross-cutting workshop space (operations, architecture, agentic systems)
├── Reference/                  # Glossary, taxonomies, frameworks reference
├── Templates/                  # Read-only schema templates
├── Deliverables/               # Polished docx versions of strategy/product/GTM markdown
└── _meta/                      # Schemas, lint rules, conventions
```

Rules:
- **`raw/` is two-mode.** Unprocessed inbox (gets converted, original removed) or persistent asset (cited by a wiki page, stays).
- **`Templates/` are reference only.** Read to understand schemas; don't modify.
- **`_meta/` is PR-only** if PR governance applies (currently solo, so direct edits with care).
- **`Deliverables/` holds polished docx exports** of strategy/product/GTM markdown — reference copies for capital partner sharing.
- **Everything else is the working wiki.** Create, update, and maintain freely.

---

## Frontmatter Schemas

Every wiki page begins with YAML frontmatter. Mandatory across all types:

```yaml
---
type: thesis | framework | strategy | product | capital_partner | co_dev_partner | oem_partner | cii_data_asset | cii_loop | cii_surface | commercial_vector | dealos_spec | gtm | intelligence | reference | workshop | vision | decision
status: active | inactive | archived
audience: internal | capital_partner | tenant | partner | public
owner: "Dom Espinosa"               # Always Dom for now; expands as team grows
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
---
```

`audience` replaces NPI's `sensitivity` — Cantus material classifies by who it is *for* rather than what compliance level it needs. Capital-partner-audience material is internally polished and externally defensible. Internal-audience material is working-stage.

### Type-specific schemas

**Foundational thesis:**
```yaml
type: thesis
thesis_class: foundational | strategic | tactical
related_layers: [1, 2, 3, 4]        # Which framework layers this thesis touches
key_claims: []
defensibility_notes: ""             # What sources/parameters back the claims
```

**Framework page:**
```yaml
type: framework
framework_layer: 1 | 2 | 3 | 4 | foundation_labor | foundation_tech | cii
status: defined | drafting | parked
related_thesis: []
```

**Strategy doc (operational application of framework):**
```yaml
type: strategy
strategy_area: land | energy | labor | tenant_platform | operated_capacity | capital | gtm | other
related_framework: []
applies_to_phase: building | activation | compounding | mature
```

**Capital partner:**
```yaml
type: capital_partner
partner_class: sovereign_wealth | institutional_infrastructure | strategic_corporate | family_office | federal_program
relationship_status: prospect | engaged | committed | declined | dormant
typical_check_size: ""
target_layer: 1 | 2 | 3 | 4 | fund
last_contact_date: YYYY-MM-DD
```

**Co-development partner:**
```yaml
type: co_dev_partner
partner_tier: 1 | 2 | 3
partner_class: master_planned_industrial | mpc_developer | merchant_developer | other
relationship_status: tier_1_priority | tier_2 | dormant
known_principals: []
mutual_capability: ""               # What Cantus brings; what they bring
```

**OEM partner:**
```yaml
type: oem_partner
equipment_category: gas_turbine | gas_engine | aero_derivative | bess | transformer | switchgear | hvac
strategic_priority: bridge_btm | larger_block | permanent | procurement | storage
relationship_status: strong | warm | developing | cold
last_pricing_check: YYYY-MM-DD
```

**CII data asset:**
```yaml
type: cii_data_asset
asset_family: parcel | tenant | capital | regulatory | operational
build_status: spec | scaffolding | mvp | production
data_sources: []
internal_consumers: []
external_surface: ""                # Linked CII surface, if any
```

**CII loop (prediction-and-resolution):**
```yaml
type: cii_loop
loop_class: site_validation | tenant_match | capital_routing | regulatory_intelligence
inputs: []                          # Data assets feeding the loop
outputs: []                         # Surfaces consuming the loop's output
build_status: spec | mvp | production
```

**CII surface (product touchpoint):**
```yaml
type: cii_surface
user_category: operator | developer | capital_partner | tenant | analyst | internal
surface_type: dashboard | report | api | feed | workflow
linked_loops: []
linked_data_assets: []
build_status: spec | mvp | production
```

**Commercial vector:**
```yaml
type: commercial_vector
vector_class: advisory | co_development | principal | fund | intelligence_product | dealos | edge | compute | prime
revenue_model: ""
target_phase: building | activation | compounding | mature
related_capital_partners: []
```

**DealOS spec page:**
```yaml
type: dealos_spec
spec_class: data_model | service | route | agent | frontend | gtm
build_status: spec | scaffolding | mvp | production
linked_cii_data_asset: ""
linked_cii_loop: ""
```

**GTM page:**
```yaml
type: gtm
gtm_area: positioning | sales_motion | partner_strategy | content | events | pipeline
target_audience: capital_partner | tenant | co_dev_partner | oem
status: drafting | active | iterating
```

**Intelligence brief:**
```yaml
type: intelligence
intel_subtype: market | regulatory | competitor | conversation | thesis_input
topic: ""
source_type: article | paper | transcript | data | conversation | filing
related_thesis: []
expiration: YYYY-MM-DD
```

**Vision (in-progress company-vision workshop):**
```yaml
type: vision
status: active | parked | resolved | abandoned
priority: high | medium | low | someday
opened: YYYY-MM-DD
last_touched: YYYY-MM-DD
related_pages: []
```

**Workshop (cross-cutting non-vision topic):**
```yaml
type: workshop
status: active | parked | resolved | abandoned
priority: high | medium | low | someday
opened: YYYY-MM-DD
last_touched: YYYY-MM-DD
related_pages: []
```

**Decision:**
```yaml
type: decision
decided_date: YYYY-MM-DD
decided_by: "Dom Espinosa"
status: proposed | accepted | superseded | reversed
context: ""
related_pages: []
supersedes: []
```

---

## Linking & Backlinking

- **Always use `[[Folder/Page-Name]]` format.**
- **Cross-reference everything.** A capital-partner page links to the strategic thesis driving the engagement. A CII data asset links to the loops that consume it. Orphan pages are failures.
- **Frontmatter wikilinks** use the same syntax: `related_thesis: ["[[Strategy/Cantus-Framework]]", "[[Strategy/Bridge-to-Grid-Thesis]]"]`.
- The agent maintains backlink consistency in lint passes.

---

## Tone Standards

The Cantus voice is **brilliant, polite, has a soul.** Substantive directness, calibrated velocity, analytical depth, communication craft, honest engagement with difficulty.

### Hard bans

- No business-speak superlatives ("game-changing," "best-in-class," "world-class," "cutting-edge," "transformative") — replace with substantive specifics
- No borrowed-legitimacy framings ("the BlackRock of X," "the Berkshire of Y") — Cantus constructs its own category
- No Caesar-archetype language — supreme self-confidence, calculated generosity, ruthlessness, Rubicon mentality, personal-legacy ambition. Cantus is institutional, not individual. The Caesar prompt has been explicitly rejected.
- No comparable-driven identity claims (Brookfield/Hines/Harrison Street/TPL are reference points that inform the work, not identity)
- No overstatement of capabilities not yet earned — distinguish what Cantus *is* from what Cantus *is becoming*. Capital partners read the difference instantly.
- No Crusoe references in external articulation. Internal structural comparable only.
- No "our mission" framing. Use "the work." Mission language reads as performative; work language reads as committed.
- No exclamation points or emojis in formal documents.
- No NPI-internal framing language (Section 14 scoring, "Ready to show," v2 assessment).

### Aim for

- Substantive directness, calibrated velocity, analytical depth, communication craft
- Honest acknowledgment of difficulty
- Sentence-length variation for rhythm
- One pull quote per major section at most. Pull quotes earn their place by carrying a strategic claim, not by being eloquent.
- Aquinas / Stoic / classical philosophical framing for foundational identity work (verify before applying)

---

## Standard Deliverables

| Deliverable | Format | Notes |
|---|---|---|
| Strategic memo | `.docx` via docx skill, mirrored as markdown | Calibri 11pt body, navy `#1F2A44` headings, structured pull quotes. **Confirm format before producing.** |
| Working draft | `.md` | Default for iterative work that may become a docx |
| Reference / transcript | `.md` | Conversation transcripts, parameter files |
| Slide variation | `.svg` via visualize tool | Hand to designer for production |
| Capital partner one-pager | `.md` → `.docx` | Investor-facing condensation |

---

## Hard Rules

1. **Never use "Cantus Forge."** Retired. Cantus Prime replaces it.
2. **Never project capability the firm has not yet earned.**
3. **Never adopt the Caesar archetype** or any single charismatic-founder framing.
4. **Never produce comparable-driven identity claims.**
5. **Never write Word docs without first asking** unless format has been specified.
6. **Always read `_parameters.md`** before producing material involving numbers, names, dates, or thresholds.
7. **Always use Cantus terminology** — Intelligent Campus (not "powered campus"), Time-to-Operational (not "time-to-energization"), Margin lift (not "cost reduction"), Friction tax (not "transaction friction"), Mispriced critical infrastructure (not "value-add industrial"). Use v2 four-vertical architecture (Development / Infrastructure / Technology / Markets) — never v1 four-arm structure (Land / Infrastructure / Industries / Commodities).
8. **Never pull NPI internal scoring/assessment language into Cantus deliverables.**
9. **Pitch framing varies by audience.** Capital partners get market sizing and unit economics. Tenants (Cerebras, hyperscalers) get speed-to-deployment and capability articulation. Co-development partners get integrated-platform articulation. Never use the wrong frame.
10. **Author of record is always Dom Espinosa.** Hopkins drafts; Dom signs.

---

## Agent Behavior

### INGEST — Processing new raw material

1. Identify content type and target folder.
2. Classify audience (internal | capital_partner | tenant | partner | public).
3. Extract entities — partners, capital sources, theses, parameter updates.
4. Cross-reference with `index.md` and grep.
5. Create or update wiki pages per schema.
6. Update `index.md`.
7. Append to `log.md`.
8. Remove from `raw/` if it was an inbox file.

### QUERY — Answering questions

1. Read `index.md`. Find relevant pages.
2. Drill in. Cite via wikilinks.
3. Synthesize across pages.
4. Identify gaps; suggest where to look.
5. For capital-partner-audience output, double-check that every claim traces to a parameter or thesis source.

### LINT — Periodic health check

Auto-fix: missing frontmatter, broken wikilinks, inconsistent enum values, missing `audience` tags.
Surface: orphans, stale pages, parameter inconsistencies, claims unsupported by sourced thesis pages, framework-document drift (where downstream docs no longer match Framework Parts 1-2).

### DIGEST — Periodic founder digest

Weekly summary: new pages, framework updates, partner pipeline changes, capital partner touchpoints, parameter changes, open vision/workshop topics, stale pages.

### Specialized Cantus workflows

- **Capital partner brief generation.** Given a partner + thesis context, produce a one-pager pulling from `Strategy/` + `Capital/` + `_parameters.md`. Audience-specific framing.
- **Framework consistency check.** Given a draft document, verify it aligns with Framework Parts 1-2. Surface tensions.
- **Parameter delta surfacing.** When `_parameters.md` updates, identify all downstream pages that reference the changed parameter. Flag for review.
- **Workshop graduation.** When a Vision or Workshop topic resolves, document the decision, update the canonical home (Framework, Layer, parameters), then move resolved doc to `Resolved/` or delete with audit trail.

---

## Log Format

Append to `log.md`:

```markdown
## [YYYY-MM-DD] action | Brief Description

**Source:** (if ingest)
**Action:** [Created | Updated | Pruned] [list of pages]
**Cross-links added:** [list]
**Audience:** internal | capital_partner | tenant | partner | public
**Notes:** [contradictions found, gaps identified, follow-ups needed]
**Author:** Dom Espinosa
```

---

## Performance & Discipline Rules

The agent applies these by default.

1. **Batch tool calls in parallel.**
2. **Use bash for bulk operations.**
3. **Skip TodoList for ≤3-step tasks.**
4. **Skip post-edit verification grep when the edit is self-contained.**
5. **Match response length to question size.**
6. **Read index/log first.**
7. **Default to markdown, not docx.**
8. **Start fresh sessions for distinct workstreams.**

### Anti-patterns

- Sequential tool calls when parallel works
- Re-reading files just written
- Creating tasks for short work
- Verbose preamble before a tool call
- Long meta-explanations instead of doing the thing
- Restating the user's question before answering

---

## Git Workflow

Lighter than NPI — currently solo.

### Default branch

- `main`. Always production-clean.

### Direct commits to `main`

Default for everything. Solo founder, fast iteration.

### Pull request only when

- A future contributor has been added and is making changes outside their owned area
- A schema change to `_README.md`, `_meta/`, or `Templates/`
- An accepted Decision page (peer review, when peers exist)

### Commit message format

`[type] brief description` — types: `add`, `update`, `prune`, `lint`, `schema`, `ingest`, `decision`, `chore`, `framework`.

Examples:
- `[framework] update Layer 2 to reflect Tier 1 architecture decision`
- `[add] Hillwood co-dev partner page`
- `[ingest] capital partner conversation transcript → multiple pages`
- `[decision] Cantus Forge retired, Prime replaces`

---

## Tone, Formatting, Naming

### Formatting

- `#` for page title, `##` for major sections, `###` for subsections.
- Tables for structured data; bullets for lists; prose for explanations.
- Code blocks with language tags.
- Wikilinks always `[[Folder/Page-Name]]`.

### Naming

- **Files:** `Title-Case-With-Hyphens.md`. Examples: `Cantus-Framework.md`, `Bridge-to-Grid-Thesis.md`, `CII-Iteration-Document.md`.
- **Folders:** `Title Case` or `PascalCase`.
- **Tags:** lowercase, hyphenated. Examples: `four-layer-framework`, `operating-triangle`, `cii`, `dealos`, `capital-architecture`.
- **Wikilinks:** match the file path exactly.

### Cantus terminology vs. generic real estate language

| Use | Never |
|---|---|
| Power sector (the emerging sector) | Energy sector, utilities sector (as Cantus's primary frame) |
| 10 sub-industries (Power Assets / Equipment / Services / Land / Facilities / Machines / Industries / Commodities / Markets / Technology) | "Powered industrial" sector (deprecated) |
| Four-vertical Cantus architecture (Development / Infrastructure / Technology / Markets) | Four-arm Cantus structure (Land / Infrastructure / Industries / Commodities — v1, deprecated) |
| Two Foundations (Labor/Community + CII/DealOS) | Two Foundations (Labor/Community + Technology Integration — v1, deprecated) |
| Power Producer → Power Production Company → Power Studio (the identity arc) | "Cantus is just a developer" / "Cantus is just a fund" |
| Cantus Development (Land + Facilities) | Cantus Land (v1 arm name, deprecated) |
| Cantus Infrastructure (Assets + Equipment + Services) | Cantus Operations Tiers 1-2 / Tiers 3-4 (v1 operating split, deprecated) |
| Cantus Technology (Machines + Power Technology; orchestrator + selective operator) | (net-new in v2) |
| Cantus Markets (Industries + Commodities + Markets-broad allocation) | Cantus Industries / Cantus Commodities as separate arms (v1, deprecated) |
| Cantus Compute (selective operator inside Cantus Technology) | Cantus Compute as standalone business outside Technology vertical |
| Cantus Robotics (modeled future business inside Cantus Technology) | (net-new in v2; speculative) |
| Cantus Prime | Cantus Forge (**retired — never use**) |
| Cantus Edge (within Cantus Technology vertical) | Cantus Edge as standalone Tier 1 |
| Intelligent Campus | Powered campus, data center campus |
| Intelligent Factory | Powered industrial, smart factory |
| Cantus Integrated Campus | Multi-tenant powered campus |
| Time-to-Operational | Time-to-energization, delivery timeline |
| Margin lift | Cost reduction, rent savings |
| Friction tax | Transaction friction, intermediary cost |
| Mispriced critical infrastructure | Value-add industrial, repositioning play |
| Cantus Customer Category (six demand vectors as Power Industries operators) | "Industrial customers" (generic) |
| Two Customer Stacks (AI Factory + Manufacturing Factory — Tier-1 simplification of vectors 1-2 in current materials) | Hyperscale + advanced manufacturing (generic) |
| Input-transformation arbitrage (structural shape of every Cantus customer) | (net-new — Customer Category framing) |
| Operating Triangle (Land + Energy + Labor — v1 Layer-1 framing; retained as analytical lens within Cantus Development + Infrastructure context) | — |
| Cantus Integrated Intelligence (CII) — Foundation cross-cutting all four verticals | "CII platform," "Cantus AI" |
| DealOS — deal-level operating system; Foundation alongside CII | DealOS as a Cantus Technology product |
| The work | "Our mission" |

---

## What You Don't Do

- **Don't sign as the agent.** Author of record is always Dom Espinosa.
- **Don't use "Cantus Forge."** Retired.
- **Don't move content to the Newmark vault.** Firewall is hard.
- **Don't pull NPI internal language** (Section 14 scoring, v2 assessment) into Cantus deliverables.
- **Don't write to `raw/` carelessly.** Two-mode rule applies.
- **Don't delete pages** without explicit decision. Mark `status: archived`.
- **Don't fabricate.** If you don't know, say so. Mark `Unknown` and ask.
- **Don't break framework coherence.** Downstream documents must align with Framework Parts 1-2 and `_parameters.md`. If a draft drifts, surface the tension before committing.
- **Don't write Word docs without first asking.**
- **Don't use Caesar-archetype language** for Cantus identity work.
- **Don't produce comparable-driven identity claims.**

---

## Getting Started

1. Read this file (you're doing that now).
2. Read `_cowork-context.md` and `_parameters.md`.
3. Read `index.md` to see what's already cataloged.
4. Read recent `log.md` entries.
5. You're ready to ingest, query, lint, or contribute.

For the foundational strategic articulation under the v2 framework, start with:
- `[[Strategy/Cantus-Power-Sector-Thesis]]` — the new foundational thesis (supersedes Bridge-to-Grid as primary articulation)
- `[[Strategy/Power-Sector/]]` — the 10 sub-industry framework pages (Power Assets through Power Technology)
- `[[Strategy/Cantus-Framework]]` and `[[Strategy/Cantus-Framework-Layers-2-3-4]]` — v1 framework pages, pending v2 rewrite
- `[[Strategy/Bridge-to-Grid-Thesis]]` — supporting strategic thesis (no longer foundational; demand-side thesis under the broader Power Sector Thesis)
- `[[Products/CII-Iteration-Document]]` — CII as a Foundation

---

*Author of record on every page: Dom Espinosa. The agent drafts; Dom signs. Last updated: 2026-05-04.*
