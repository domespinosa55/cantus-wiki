# The Cantus Company Wiki — Contributor Onboarding

*Get from zero to productive in <30 minutes. Currently solo (Dom). This doc evolves as the team grows.*

---

## Prerequisites

- Mac or Windows laptop
- Git installed
- GitHub account with access to the team repo (when applicable)
- Anthropic Claude access
- 30 minutes

---

## Step 1 — Anthropic access

If you're a future contributor: Dom invites you to the Anthropic workspace. Accept via email; log in at `https://console.anthropic.com`.

---

## Step 2 — Cowork

Install the Claude desktop app from `https://claude.ai/download`. Switch to Cowork mode.

---

## Step 3 — Clone the repo

```bash
cd ~/Documents
git clone [REPO_URL] Cantus-wiki
cd Cantus-wiki
```

Verify:
```bash
ls -la
```

---

## Step 4 — Grant Cowork access

Cowork → folder icon → select `~/Documents/Cantus-wiki`. Cowork loads `_README.md` automatically.

Confirm: *"What repo are you in? Read the _README.md and confirm The Sentence."*

The agent should respond with: *"Cantus is building integrated intelligence."*

---

## Step 5 — Optional: Obsidian

Open `~/Documents/Cantus-wiki` as a vault in Obsidian if you want backlinks and graph view.

---

## Step 6 — Read the operating manual

Skim `_README.md`:

- "What This Repository Is" and "The Sentence"
- "What Cantus Is" — Four-Layer Framework, Two Foundations, CII, phasing
- "Firewall with Newmark / NPI"
- "Frontmatter Schemas"
- "Tone Standards" and the bans list
- "Hard Rules"

Don't memorize. Re-read as needed.

---

## Step 7 — First task

> *"Read `index.md` and recent `log.md`. One-paragraph status of where the firm articulation stands. Don't make edits."*

---

## Step 8 — First contribution

If you're contributing strategic thinking: drop the source material into `raw/inbox/` and ask the agent to ingest it into the appropriate Strategy/, Capital/, Partners/, or Intelligence/ folder.

If you're contributing a partner profile: use the `co_dev_partner` or `capital_partner` schema, populate from existing relationships, link to relevant strategy pages.

If you're contributing to CII or DealOS: read `Products/CII-Iteration-Document.md` first, then add `cii_data_asset`, `cii_loop`, or `cii_surface` pages following the schema.

---

## Best Practices

- Source material into `raw/` before drafting from scratch.
- Cantus voice: brilliant, polite, has a soul. No business-speak superlatives. No comparable-driven identity claims. No Caesar.
- Cross-reference everything.
- Default to markdown; ask before generating docx.
- Start fresh Cowork sessions when switching contexts.
- Verify against `_parameters.md` before publishing any number, date, or counterparty fact.

---

## Common Pitfalls

| Pitfall | Fix |
|---|---|
| Used "Cantus Forge" | Replace with Cantus Prime. |
| Used Caesar / borrowed-legitimacy framing | Strip. Cantus constructs its own category. |
| Pulled NPI Section 14 scoring into Cantus material | Strip. NPI internal only. |
| Page lacks `audience:` tag | Add. Default to `internal`. |
| Wikilinks broken | "Fix any wikilinks using bare names instead of folder paths." |
| Cowork session slow | Start fresh session. |

---

## Where to Ask for Help

DM Dom. Solo founder; he's the maintainer.

---

*Maintainer: Dom Espinosa. Last updated: 2026-05-04.*
