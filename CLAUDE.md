# CLAUDE.md — Cantus Wiki

*Agent entry point. Read this first.*

## Where you are

You are in `~/Documents/Cantus-wiki/` — the **Wiki** surface of The Cantus Company. This is the agent-maintained markdown knowledge base. The companion native-format surface is `~/Documents/Cantus/`.

## Architecture (Karpathy LLM Wiki pattern)

This vault is built on the **LLM Wiki pattern** described by Andrej Karpathy in April 2026: instead of running RAG over raw documents on every query, an agent pre-compiles knowledge into structured, interlinked markdown pages. Knowledge compounds. Answers persist.

The canonical three layers, as instantiated here:

| Layer | Location | Role |
|---|---|---|
| **`raw/`** | `Cantus-wiki/raw/` (inbox + persistent assets) | Immutable source material — articles, transcripts, PDFs, conversation captures |
| **wiki pages** | All non-`raw/` folders in `Cantus-wiki/` | LLM-generated, schema-conformant, interlinked markdown |
| **`CLAUDE.md`** | This file (entry point) → `_README.md` (full schema) | Agent operating instructions |

Cantus extends the canonical pattern with a **fourth surface** at `~/Documents/Cantus/` for native-format deliverables (docx, pptx, xlsx). Wiki pages reference those files via the `working_files:` frontmatter field.

References on the pattern: Karpathy's [original gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f), [VentureBeat coverage](https://venturebeat.com/data/karpathy-shares-llm-knowledge-base-architecture-that-bypasses-rag-with-an).

## Required reading order

1. **This file** (orientation — you are here)
2. **`_README.md`** — full operating manual: framework, schemas, agent behavior, hard rules, tone, naming, terminology. The longest file. Read it completely before taking action.
3. **`_cowork-context.md`** — Cantus-specific operating context for cowork sessions
4. **`_parameters.md`** — single source of truth for numbers, names, dates, thresholds. Read before producing anything that cites a figure.
5. **`index.md`** — wiki content catalog. Read before creating any new page (avoid duplicates).
6. **`log.md`** — append-only operation log. Skim recent entries for context on what just happened.
7. **`ONBOARDING.md`** — new-contributor walkthrough (also useful as a fresh-session refresher)

If `_README.md`, `_cowork-context.md`, or `_parameters.md` contradict this file, **they win**. CLAUDE.md is a pointer; the operating manual is the source of truth.

## The four agent workflows

From `_README.md` § Agent Behavior — internalize these:

- **INGEST** — process raw material into wiki pages, update `index.md`, append to `log.md`
- **QUERY** — answer questions by reading `index.md` first, drilling in, citing via wikilinks
- **LINT** — periodic health check: orphans, stale pages, parameter drift, broken wikilinks
- **DIGEST** — periodic founder digest: changes, partner pipeline, parameter deltas, open workshops

## Hard rules (top-of-mind)

1. **Author of record is always Dom Espinosa.** Hopkins (the agent) drafts; Dom signs.
2. **Never use "Cantus Forge."** Retired. Cantus Prime replaces it.
3. **Always read `_parameters.md`** before producing material with numbers, names, or dates.
4. **Use Cantus terminology** — Intelligent Campus, Time-to-Operational, Margin lift, Friction tax, Mispriced critical infrastructure, and the v2 four-vertical architecture (Cantus Development / Infrastructure / Technology / Markets) with two Foundations (Labor/Community + CII/DealOS). Never use the v1 four-arm structure (Cantus Land / Infrastructure / Industries / Commodities — deprecated). Full terminology list in `_README.md`.
5. **Firewall with Newmark / NPI is hard.** No NPI client material in this vault. NPI internal scoring/assessment language stays out of Cantus deliverables.
6. **Don't write `.docx` deliverables without first asking** unless format has been specified.
7. **Don't fabricate.** Mark `Unknown` and ask.
8. **Don't break framework coherence.** Downstream documents must align with the v2 Power Sector Framework, the [[Strategy/Cantus-Power-Sector-Thesis]], and `_parameters.md`.

The full hard-rules list is in `_README.md` — these are the ones you'll hit most often.

## Power Sector Framework v2 (canonical as of 2026-05-24)

- **10 sub-industries**: Power Assets, Power Equipment, Power Services, Power Land, Power Facilities, Power Machines, Power Industries, Power Commodities, Power Markets (broad allocation), Power Technology. See `Strategy/Power-Sector/`.
- **4 Cantus operating verticals**: Development (Land + Facilities), Infrastructure (Assets + Equipment + Services), Technology (Machines + Power Technology), Markets (Industries + Commodities + Markets-broad).
- **2 Foundations cross-cutting**: Labor/Community, CII/DealOS.
- **Identity arc**: Power Producer → Power Production Company → Power Studio.
- **Foundational thesis**: [[Strategy/Cantus-Power-Sector-Thesis]]. Supersedes Bridge-to-Grid as primary articulation; Bridge-to-Grid remains as a supporting demand-side thesis.

## The companion working-files surface

`~/Documents/Cantus/` holds native-format deliverables (decks, models, polished docx, term sheets, source assets). When a wiki page produces a working-file deliverable, record it on the page:

```yaml
working_files:
  - "~/Documents/Cantus/Deliverables/Bridge-to-Grid-Thesis.docx"
```

When working in that folder, read its `CLAUDE.md` and `README.md` for surface-specific rules.

---

*Pattern: Karpathy LLM Wiki (April 2026). Operating manual: `_README.md`. Source of truth on numbers: `_parameters.md`. Author of record: Dom Espinosa. Last updated: 2026-05-04.*
