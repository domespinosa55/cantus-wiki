---
type: strategy
status: active
audience: capital_partner
owner: "Dom Espinosa"
created: 2026-05-24
updated: 2026-05-24
strategy_area: gtm
tags: [prospecting, operating-system, automation, cii, dealos, notion, autonomous-agents]
related_framework: ["[[Strategy/Prospecting/Cantus-Prospecting-Framework]]", "[[Strategy/Prospecting/Cantus-Prospecting-Playbook]]", "[[Strategy/Cantus-Markets]]", "[[Strategy/Foundations/CII-DealOS-Foundation]]"]
applies_to_phase: building
---

# The Cantus Prospecting System

*The operating system that runs the [[Strategy/Prospecting/Cantus-Prospecting-Framework]] autonomously. Combines scheduled agents, a Notion-backed prospect tracker, and a Cowork dashboard into a continuously-updating institutional capability. Sits inside the CII / DealOS Foundation as the prospecting-specific instantiation of the firm's integration intelligence.*

*Companion to the [[Strategy/Prospecting/Cantus-Prospecting-Framework]] (what to score) and [[Strategy/Prospecting/Cantus-Prospecting-Playbook]] (where signals come from). This document is the system that turns the Framework + Playbook into a running operation.*

---

## I. Purpose

The Framework defines the scoring discipline. The Playbook defines the sourcing. The System is what runs the discipline against the sourcing on a continuous schedule, without requiring the founder to manually re-score every quarter.

The objectives:

1. **Autonomous signal ingestion.** New signals enter the prospect tracker as they arrive — not when an analyst gets to them.
2. **Continuous scoring.** Tier rankings update as signals change, not on a manual cycle.
3. **Compounding institutional memory.** Every prospect scored, every engagement closed, every calibration writes back into the CII / DealOS Foundation.
4. **Founder-friendly review.** Reports are pushed to where Dom already works (Slack for fast signals, Notion for the active roster, the wiki for institutional memory).
5. **Reproducibility.** Any analyst (or capital partner reviewing the discipline) sees the same scoring logic operating against the same sources.

The system is built on tools that already exist in the Cowork environment — Notion, Slack, scheduled Claude agents, Cowork artifacts, Box, WebSearch, web_fetch. No bespoke software development.

## II. The Five-Layer Architecture

| Layer | Function | Implementation |
|---|---|---|
| **Signal Ingestion** | Watches sources for new signals (filings, awards, transcripts, trade press) and pulls them as they arrive | Scheduled Claude agents using WebSearch / web_fetch / Box / connector tools |
| **Prospect Database** | Structured store of firms, signals, scores, tiering, engagement history, source provenance | Notion database (the Cantus Prospect Tracker) |
| **Agent Layer** | Reads new signals, extracts structured observations against the Framework rubric, scores them, surfaces changes | Claude agents invoked by scheduled tasks |
| **Scoring Engine** | Applies the four-dimension rubric per vector, the two multipliers, and produces the composite + tier | Agent prompt + Notion formula properties for deterministic composite calculation |
| **Report Layer** | Generates digests, calibration memos, capital-partner reports, the live dashboard | Slack messages, Notion pages, Cowork artifacts, wiki-committed memos |

Each layer maps cleanly to the existing v2 architecture:

| System layer | Maps to v2 component |
|---|---|
| Signal Ingestion | CII data assets — Regulatory, Operational, Tenant, Capital families |
| Prospect Database | CII Tenant family (canonical prospect records) |
| Agent Layer | DealOS agent layer (LLM-augmented agents in the DealOS spec) |
| Scoring Engine | CII Tenant match loop |
| Report Layer | CII product surfaces (capital-partner-visible, internal, founder-DM) |

## III. The Autonomous Operating Loop

The loop runs on four cadences, each with its own purpose, agent prompt, and review point.

### Daily (00:00 CT cron, automated)

**Agent prompt:** Scan federal-program databases (DOE LPO, CHIPS, DPA, IBAS, BARDA, IRA transferability marketplaces), SEC EDGAR for new 10-Q / 8-K / S-1 filings from tracked prospects, ERCOT GINR and large-load registration updates, NVIDIA news, and the top-tier trade press (Data Center Dynamics, Mission Critical, The Information, BNEF top stories). Extract new signals. Match each new signal to a tracked prospect (or create a new prospect record if the signal surfaces an untracked firm scoring ≥3.0 on initial assessment). Write to Notion with source URL and timestamp. Flag any signal that would shift a tracked prospect's tier by ≥0.5.

**Output:** Notion database updates. Slack-channel digest only if a tier-shift flag triggers (otherwise silent — no notification fatigue).

### Weekly (Monday 07:00 CT, automated)

**Agent prompt:** Compile the past 7 days of signal activity. Group by prospect, by vector, by tier. Identify the top five most-significant signal movements (e.g., new federal awards, material capacity announcements, new hyperscaler-supplier disclosures). Format as a structured digest. Highlight any prospects that moved between tiers. Highlight any signal that warrants a deep-dive scoring memo.

**Output:** Slack message to the Cantus prospecting channel (or founder DM). Mirror page in Notion. Notification volume: one message per week.

### Monthly (1st of the month 07:00 CT, automated)

**Agent prompt:** Run full re-score of Tier A and Tier B roster. For each firm: re-pull the most-recent signals across all dimensions, re-apply the four-dimension rubric per vector, re-apply the two multipliers, recompute the composite, update the tier. Note tier changes since prior month. Generate a one-page cross-vertical operating summary covering Tier distribution shifts, new Tier A entries, fallen Tier A exits, and aggregate Power Pull movement by vector.

**Output:** Notion page "Monthly Operating Review {YYYY-MM}" + Slack summary. Founder review expected within 5 business days.

### Quarterly (last business day of the quarter, semi-automated)

**Agent prompt:** Draft the Prospecting Calibration Memo for the quarter. Sections: (1) Engagements closed this quarter; (2) Calibration anchors updated; (3) Score deltas across the Tier A and B roster; (4) Multi-vector multiplier curve fit against observed outcomes; (5) Vertical-integration trajectory signals updated; (6) Open questions from the Framework §XII with status. Reference all underlying data in Notion. Save draft as `Strategy/Prospecting/Quarterly-Calibration-{YYYY-Q}.md` in the wiki.

**Output:** Wiki-committed memo (draft). Founder reviews, edits, signs. Final version commits to GitHub as the institutional record for the quarter.

### Ad-hoc (on-demand)

**Agent prompt:** Run full diligence protocol from [[Strategy/Prospecting/Cantus-Prospecting-Playbook]] §VI.B against a specified prospect. Produce a 2–4 page Tier A scoring memo with sourcing notes, multi-vector breakdown, vertical-integration assessment, geographic fit specifics, and a recommended Cantus engagement framing.

**Output:** Notion deep-dive page + saved memo in Cantus-wiki. Founder review before any outreach action.

## IV. The Notion Database Schema

The Cantus Prospect Tracker is one Notion database with multiple views. Schema:

### Properties

| Property | Type | Description |
|---|---|---|
| **Firm Name** | Title | Canonical name |
| **Ticker** | Text | Public ticker if applicable |
| **Public / Private** | Select | Public, Private, Subsidiary, Sovereign |
| **Primary Vector** | Select | Compute / Supply Chain Mfg / Advanced Mfg / Defense IB / Biomanufacturing & Critical Materials / Energy Transition Mfg |
| **Secondary Vectors** | Multi-select | Other vectors the firm operates under |
| **Power Pull score** | Number | 0–5, primary vector |
| **Timing score** | Number | 0–5 |
| **Counterparty Strength score** | Number | 0–5 |
| **Geographic & Site Fit score** | Number | 0–5 |
| **Base Composite** | Formula | (Power Pull × 0.40) + (Timing × 0.25) + (Counterparty × 0.20) + (Site Fit × 0.15) |
| **Multi-Vector Count** | Number | Number of vectors scoring ≥3.0 |
| **Multi-Vector Multiplier** | Formula | 1.00 / 1.10 / 1.20 / 1.30 based on Multi-Vector Count |
| **Vertical-Integration Trajectory** | Select | None / Stated / Active 2-3 / Aggressive 4+ |
| **Vertical-Integration Multiplier** | Formula | 1.00 / 1.05 / 1.15 / 1.25 |
| **Composite Score** | Formula | Base Composite × Multi-Vector Multiplier × Vertical-Integration Multiplier |
| **Tier** | Formula | A / B / C / D based on Composite |
| **Estimated MW** | Number | Per the Framework MW translation heuristic |
| **MW estimate notes** | Text | Why this MW range |
| **Active Pipeline Site Match** | Multi-select | Mathis McDonald / GoodPeak / Joule / Palangana / Wilmer / T1 / Singleton / Future site |
| **Engagement Status** | Select | Not contacted / Initial outreach / NDA executed / Site visit / Term sheet / Definitive / Closed |
| **Last Signal Date** | Date | Most recent material signal observed |
| **Last Scored Date** | Date | Last full re-scoring |
| **Source URLs** | URL multi-property | Links to filings, transcripts, press, federal databases supporting the score |
| **Constraint Flags** | Multi-select | Water-intensive / Workforce-constrained / Permitting-long / Cleared-personnel-required / Other |
| **Vertical-Integration Signals** | Text | Brief notes on observed integration moves |
| **Founder Notes** | Text | Internal notes |
| **Relationship Path** | Text | Existing Cantus / Newmark / founder-network paths to the firm |

### Views

| View | Filter | Sort |
|---|---|---|
| **Tier A Active Roster** | Tier = A | Composite descending |
| **Tier B Cultivate** | Tier = B | Composite descending |
| **By Vector** | grouped by Primary Vector | Composite descending within vector |
| **By Pipeline Site** | grouped by Active Pipeline Site Match | Composite descending |
| **Recent Signal Movement** | Last Signal Date within 30 days | Last Signal Date descending |
| **Multi-Vector Anchors** | Multi-Vector Count ≥ 3 | Composite descending |
| **Engagement Active** | Engagement Status ≠ Not contacted | Last activity descending |
| **Newly Added** | Created date within 30 days | Created date descending |

### Companion databases

**Signals database** (related to Prospect Tracker):
- Properties: Signal | Date Observed | Signal Type (federal-award, filing-disclosure, trade-press, ISO-registration, etc.) | Source URL | Affected Prospect (relation) | Score Impact (text) | Vector Affected (multi-select)

**Engagements database** (related to Prospect Tracker):
- Properties: Engagement | Prospect (relation) | Stage | Date Initiated | Last Activity | Next Action | Owner | Notes

**Calibration database** (related to Prospect Tracker):
- Properties: Quarter | Prospect (relation) | Prior Composite | New Composite | Tier Change | Driver Signals | Notes

## V. Scheduled Task Specifications

Four standing scheduled tasks plus on-demand triggers.

### Task 1: Daily Signal Scan

- **Cadence:** Every day at 00:00 CT
- **Duration target:** ~10–20 minutes per run
- **Agent prompt:** Scan the standing source list (federal databases per Playbook §V.B, EDGAR for tracked tickers per Playbook §II.A, ERCOT GINR per Playbook §II.E, NVIDIA news + GTC/CES/Computex feeds per Playbook §V.A, top-tier trade press per Playbook §II.D). For each new signal, identify the affected prospect (or create a new prospect record). Write the signal to the Signals database with source URL. Update affected prospect's Power Pull score if the signal materially changes the score. Flag tier shifts ≥0.5 for Slack notification.
- **Output:** Updated Notion records. Slack notification only on tier-shift flags.

### Task 2: Weekly Signal Digest

- **Cadence:** Every Monday at 07:00 CT
- **Duration target:** ~20–40 minutes per run
- **Agent prompt:** Pull all signals from the Signals database from the prior 7 days. Group by prospect, vector, tier. Compute aggregate movement statistics. Identify the top five most-significant movements. Note any prospects that crossed tier bands. Format as a structured digest with sections: "This Week's Tier Movements," "Top 5 Signals," "New Prospects Added," "Engagement Status Changes." Post to Slack channel + create a Notion page mirror.
- **Output:** Slack message + Notion page.

### Task 3: Monthly Full Re-Score

- **Cadence:** 1st of every month at 07:00 CT
- **Duration target:** ~2–3 hours per run (or split across multiple shorter runs)
- **Agent prompt:** For each prospect in Tier A and Tier B, re-pull the most-recent signals across all dimensions. Re-apply the four-dimension rubric per primary vector. Re-apply the two multipliers. Recompute the composite. Update the Tier. Note tier changes in the Calibration database with driver signals. Generate a one-page Monthly Operating Review covering Tier distribution shifts, new Tier A entries, fallen Tier A exits, and aggregate Power Pull movement by vector. Save to Notion as "Monthly Operating Review {YYYY-MM}" and post a Slack summary.
- **Output:** Notion page + Slack summary. Founder review expected within 5 business days.

### Task 4: Quarterly Calibration Memo

- **Cadence:** Last business day of the quarter at 12:00 CT
- **Duration target:** ~3–5 hours per run
- **Agent prompt:** Draft the Prospecting Calibration Memo for the quarter. Sections per §III above. Cite all underlying data references (Notion record IDs, source URLs, prior calibrations). Save as `Strategy/Prospecting/Quarterly-Calibration-{YYYY-Q}.md` in the Cantus-wiki working copy. Notify founder via Slack.
- **Output:** Draft wiki page committed to local working tree (not auto-pushed to GitHub). Founder reviews, edits, commits, pushes.

### Ad-hoc Task: Deep Dive

- **Trigger:** Founder request via Slack or Notion comment
- **Duration target:** ~1–2 hours per run
- **Agent prompt:** Run the full diligence protocol from Playbook §VI.B against the specified prospect. Produce a structured 2–4 page Tier A scoring memo with sourcing notes, multi-vector breakdown, vertical-integration assessment, geographic fit specifics, and a recommended Cantus engagement framing.
- **Output:** Notion deep-dive page + saved memo in Cantus-wiki under `Strategy/Prospecting/Deep-Dives/{firm-name}-{YYYY-MM}.md`.

## VI. The Live Prospect Dashboard

A Cowork artifact that pulls fresh data from Notion on each open and provides the founder's primary review surface. Persists across sessions; re-fetches on each open.

### Dashboard sections

1. **Tier distribution.** Stacked bar of count and total estimated MW by tier (A / B / C / D).
2. **Tier A roster.** Sortable table — firm, primary vector, composite, MW estimate, pipeline-site match, engagement status, last signal date.
3. **Recent signal activity.** Timeline of signals from the past 7 / 30 days.
4. **By vector.** Six-panel breakdown of Tier distribution and MW by demand vector.
5. **Pipeline-site matching.** For each active Cantus site, the list of Tier A / B prospects matched to it.
6. **Multi-vector anchors.** Highlight box of firms with Multi-Vector Count ≥ 3.
7. **Calibration anchors.** Tesla and Celestica scoring detail with last-update timestamp.
8. **Quick actions.** Triggers for deep-dive requests, manual re-score, source-link verification.

The dashboard does not duplicate Notion; it presents the data in a founder-review-optimized form.

## VII. Slack Delivery Configuration

Posts go to a designated Cantus prospecting channel (channel name TBD; recommend `#cantus-prospecting` or founder DM during the Building phase).

Cadence and content:

| Cadence | Content | Tone |
|---|---|---|
| **Tier-shift event** | Single message: "[Firm] tier shift {old → new}. Driver signals: [list]. View in Notion: [link]." | Notification, not summary |
| **Weekly digest** | Structured digest (Monday 07:00 CT). Sections: tier movements, top 5 signals, new prospects, engagement changes | Founder-readable, prose with bullet lists |
| **Monthly summary** | Short summary (1st of month) with link to the Notion Operating Review | Executive summary tone |
| **Quarterly calibration** | Notification with link to wiki draft | Notification, founder reviews |
| **Deep-dive completion** | Notification when an ad-hoc deep dive is ready | Notification with summary |

## VIII. Human-in-the-Loop Checkpoints

The system is autonomous on signal ingestion and scoring; founder review applies at four points:

1. **Tier-shift threshold (any prospect's tier shifts ≥0.5)** — immediate Slack notification; founder reviews the driving signals and confirms or adjusts.
2. **Monthly Operating Review** — founder reviews aggregate movement, signs off on the month.
3. **Quarterly Calibration Memo** — founder reviews draft, edits, signs, commits to wiki / pushes to GitHub.
4. **Engagement-stage advancement** — moving a prospect from Tier A to Engagement Status = "Initial outreach" or beyond is a founder-only action. The system surfaces candidates; the founder commits.

For Tier C / D scoring or signal ingestion at the Tier A / B layer that doesn't shift tiers, the system runs without checkpoint.

## IX. Calibration and Maintenance

### Quarterly calibration

The Quarterly Calibration Memo is the primary maintenance mechanism. Reviews:

- Engagement-anchor updates (Tesla, Celestica, future engagements)
- Multi-vector multiplier curve fit
- Vertical-integration trajectory signal accuracy
- MW heuristic accuracy (especially the NVIDIA power-density trajectory)
- Source quality and completeness (which sources surfaced signals; which sources missed signals)
- Open questions from the Framework §XII status

### Annual framework refresh

Once per year, a more substantial calibration cycle:

- Full re-read of the Framework against observed performance
- Adjustment of dimension weights if calibration data warrants
- Addition or removal of demand vectors if the sector evolves
- Update of the source hierarchy in the Playbook
- Schema review for the Notion tracker

### Signal source drift

Sources change. Trade publications consolidate, federal databases reorganize, ISOs change reporting formats. The system needs a quarterly source-health check: for each source in the Playbook, has it been accessed in the last quarter? Has the format changed? Are signals coming through with expected volume?

## X. Build Sequence

The system gets built in five phases:

| Phase | Components | Status |
|---|---|---|
| **Phase 1** | This document — operating-system architecture | **In progress (this commit)** |
| **Phase 2** | Notion database + companion databases | Next |
| **Phase 3** | Seed Tier A ERCOT-focused prospects in Notion | Next |
| **Phase 4** | Scheduled tasks for daily / weekly / monthly / quarterly | Next |
| **Phase 5** | Live Prospect Dashboard artifact | Next |
| **Phase 6** | First calibration run + ongoing operation | Ongoing |

## XI. What This System Replaces

The system replaces what would otherwise be analyst-intensive manual scoring of the prospect base every quarter. The v0.1 Box Tenant Targeting framework's "next step" was an Excel scoring workbook; the v2.0 System is the institutional equivalent — Notion replaces Excel, scheduled Claude agents replace analyst hours, the dashboard replaces founder pulling reports.

What it does NOT replace:
- Founder relationship work (the Tier A outreach itself)
- Capital partner cultivation (still founder-led)
- Strategic judgment (the system supports judgment; doesn't make decisions)
- Deal closing (DealOS handles deal execution; the System handles pre-engagement)

## XII. Cross-References

| Page | Relationship |
|---|---|
| [[Strategy/Prospecting/Cantus-Prospecting-Framework]] | The scoring discipline the system operates |
| [[Strategy/Prospecting/Cantus-Prospecting-Playbook]] | The sourcing manual the system follows |
| [[Strategy/Foundations/CII-DealOS-Foundation]] | The Foundation this system instantiates |
| [[Products/CII-Iteration-Document]] | CII data assets and loops |
| [[DealOS/README]] | DealOS agent layer this system uses |
| [[Strategy/Cantus-Markets]] | Operating vertical that owns the system |
| [[Strategy/Cantus-Business-Plan]] | Year 1–2 operating roadmap that includes this build |

## XIII. Open Items for Ongoing Operation

- **Slack channel choice.** `#cantus-prospecting` vs. founder DM. To finalize before scheduling Task 2 (Weekly Digest).
- **Tier-shift threshold tuning.** Currently 0.5. May need adjustment after first calibration cycle.
- **Notion workspace governance.** Who has read/write access. Capital-partner view permissions later (read-only specific views).
- **GitHub commit automation.** Whether quarterly calibration memos auto-push to GitHub or remain founder-reviewed-then-pushed. Currently the latter.
- **Source-credential management.** Some federal databases and trade publications require login. The system relies on what's freely web-accessible plus the connector-tool access already established (Box, Notion, Slack).
- **NVIDIA roadmap signal automation.** Currently dependent on quarterly NVIDIA earnings + GTC/CES/Computex events. Could automate via dedicated quarterly cadence task.

---

*The Cantus Prospecting System v2.0 — autonomous prospecting infrastructure operating inside the Cantus Markets vertical. Anchored to the [[Strategy/Prospecting/Cantus-Prospecting-Framework]] and powered by the CII / DealOS Foundation. Author of record: Dom Espinosa.*
