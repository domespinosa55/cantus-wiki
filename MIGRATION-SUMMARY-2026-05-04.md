---
type: reference
status: active
audience: internal
owner: "Dom Espinosa"
created: 2026-05-04
updated: 2026-05-04
tags: [migration, phase-4, summary, vault-meta]
---

# Phase 4 Migration Summary — 2026-05-04

*One-page record of the migration from the prior unified `~/Documents/obsidian/` vault into Cantus-wiki, Newmark-wiki, and the renamed Personal vault. Author of record: Dom Espinosa.*

For the canonical version of this summary (with mirror NPI tables) see also `~/Documents/Newmark-wiki/MIGRATION-SUMMARY-2026-05-04.md`.

---

## Cantus-wiki (this vault)

| Section | Pages | Notes |
|---|---|---|
| Strategy | 10 | Foundational framework (Cantus-Framework Parts 1 & 2, Layers, Primary-Inputs 1-3, Market-Sizing, Bridge-to-Grid-Thesis, Advanced-Industrial-Spec) plus the new ERCOT-Positioning-Thesis fork |
| Products | 1 | CII-Iteration-Document |
| DealOS | 12 | Reclassified as `dealos_spec`, `audience: internal`. Folder structure preserved (Architecture/, Founding-Team/, GTM/, Product/) |
| GTM | 4 | Executive-Summary, Investor-Deck-Outline, Team-and-Org, Go-To-Market-Plan. Cerebras-Outreach-Draft excluded — moved to Newmark-wiki/Marketing per Dom |
| Vision | 3 | Tier-1-Architecture (active workshop — do not edit Layer 1 references until workshop resolves), Parking-Lot, _README |
| Workshop | 2 | Hopkins-Performance-Tuning (verbatim from prior vault), Unified-AI-Native-Knowledge-Platform (with CII architectural-lessons note) |
| Reference | 2 | Hopkins-Persona (Cantus tone register), Crusoe-Structural-Reference (internal-only) |
| Deliverables | 8 docx | Polished mirrors of strategy/product memos |

---

## Tone Audit

- **No "Cantus Forge"** in body content of migrated Strategy/Products/GTM. The active Tier-1-Architecture workshop legitimately discusses the Forge → Prime retirement and is preserved verbatim.
- **No "Caesar," "Rubicon," or single-charismatic-founder framing** detected.
- **No business-speak superlatives** ("best-in-class," "world-class," "transformative") detected.
- **Crusoe references** present only in `Reference/Crusoe-Structural-Reference.md` with explicit "internal use only — not for external Cantus articulation" banner.
- **No comparable-driven identity claims** detected.
- **NPI internal language** (Section 14 scoring, "Ready to show," v2 assessment) is NOT present in any Cantus-wiki page. Bridge-to-Grid was forked carefully with the "For Cantus" subsection retained here and removed in the Newmark version.

---

## Forks Across Vaults

| Topic | Cantus version (here) | Newmark version |
|---|---|---|
| Hopkins-Persona | `Reference/Hopkins-Persona.md` — Cantus tone register | `Newmark-wiki/Reference/Hopkins-Persona.md` — NPI tone register |
| Hopkins-Performance-Tuning | `Workshop/Active/` (verbatim) | `Newmark-wiki/Workshop/Active/` (verbatim) |
| Unified-AI-Native-Knowledge-Platform | `Workshop/Active/` (with CII architectural-lessons note) | `Newmark-wiki/Workshop/Active/` (verbatim) |
| Crusoe | `Reference/Crusoe-Structural-Reference.md` (internal only) | `Newmark-wiki/Companies/Crusoe.md` (counterparty) |
| ERCOT regulatory framework | `Strategy/ERCOT-Positioning-Thesis.md` (firm positioning) | `Newmark-wiki/Regulatory/ERCOT-Large-Load-Framework.md` (NPI client primer) |
| Bridge-to-Grid | `Strategy/Bridge-to-Grid-Thesis.md` (full thesis) | `Newmark-wiki/Intelligence/Bridge-to-Grid-Conversation-Playbook.md` ("For Cantus" subsection removed) |

---

## Decisions Locked (from the stop-and-ask round)

1. Palangana (deal name) reconciled to match working folder.
2. Source preservation: copy-then-archive — source pages in `~/Documents/LifeOS/Cantus/`, `~/Documents/LifeOS/DealOS/`, `~/Documents/LifeOS/Hopkins/Hopkins-Persona.md`, etc. all carry `status: archived`.
3. Personal vault renamed `~/Documents/obsidian/` → `~/Documents/LifeOS/` (note: collision with the `LifeOS/` subfolder produces a `LifeOS/LifeOS/` nested path; flatten on Dom's call).
4. Cerebras-Outreach-Draft → Newmark-wiki/Marketing (NPI tenant-rep treatment, not Cantus direct pitch).
5. Hopkins persona: scoped rewrite per vault.
6. Crusoe-Structural-Reference at `Reference/` (chosen over `Workshop/Resolved/`).
7. DealOS audience: `internal` default for all 12 pages.

---

## Still Open

- **Tier-1 Architecture workshop** — `Vision/Active/Tier-1-Architecture.md` is the live workshop on Cantus Edge / Compute / Prime tier placement. Layer-1 references in `Cantus-Framework-Layers-2-3-4.md` were preserved verbatim per the brief; that workshop's resolution will update them.
- **Capital, Partners, Intelligence sections** are empty — populate as the firm advances.
- **DealOS placeholder wikilinks** (`[[Architecture-Financial-Analyst-Layer]]`, `[[Clawdbot-Platform-Strategy]]`, `[[Mesh-Router]]`, `[[Supabase-Integration]]`) point to pages that lived in the prior vault's `Hopkins/Garage/` area but did not migrate. Decide whether to backfill or strip.
- **Cross-vault wikilinks** were converted to plain-text "see Newmark-wiki/X" references. If Dom wants tighter cross-referencing, build a small reference-bridge convention.
- **Phase 4 docx mirrors:** the 8 docx files in `Deliverables/` are the polished versions of the markdown strategy/product memos. As Strategy pages evolve, the docx mirrors drift; regeneration cadence is Dom's call.

---

## Files

- This vault's index: [[index]]
- This vault's log: [[log]]
- NPI mirror summary: see `~/Documents/Newmark-wiki/MIGRATION-SUMMARY-2026-05-04.md`
- Personal vault: `~/Documents/LifeOS/`
