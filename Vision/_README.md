---
type: vision-readme
status: active
context: cantus
created: 2026-05-03
---

# Cantus Vision

*Workshop space for company-vision topics. Use this folder when a question is foundational to what Cantus is or what Cantus becomes — architectural seams in the framework, naming decisions, capability questions, customer-positioning evolutions, capital architecture trade-offs. Things that deserve more thought than a chat exchange but aren't yet ready to update the Framework documents or the cowork-context.*

*Per the Cantus tone: brilliant, polite, has a soul. Acknowledge difficulty. Composure under acknowledged uncertainty is more credible than confidence projected over hidden weakness. The Vision folder is where uncertainty gets thought through.*

---

## When to Open a Vision Doc

- A change to one of the Framework documents that warrants more deliberation than a quick edit
- A naming question that ripples across multiple deliverables
- A capability or operating-model question where the answer shapes capital architecture
- A customer-stack or tenant-positioning evolution
- An architectural seam between *what Cantus is* and *what Cantus is becoming*
- A capital-partner narrative question that requires defensible articulation
- Anything that, if rushed, would produce a credibility problem

---

## When to Use the Parking Lot Instead

`Cantus/Vision/Parking-Lot.md` — for vision-relevant ideas you want to capture but aren't ready to develop. One bullet or short paragraph each. Promote out when the idea earns its own page.

---

## Two Modes

### Active/

Folder of pages being actively workshopped. One page per topic.

When a topic resolves:
1. **Document the decision** inside the page itself — preserve the reasoning trail
2. **Update the canonical home** — Framework, Layer docs, cowork-context, parameters, terminology table — wherever the resolution belongs
3. **Either move the resolved doc to `Resolved/`** (if reasoning is worth keeping accessible) **or delete** (if the canonical update fully captures the conclusion)

### Parking-Lot.md

Single file. Stub ideas. Low overhead to add.

---

## Frontmatter Schema

```yaml
---
type: vision
status: active | parked | resolved | abandoned
context: cantus
topic: ""                              # short title
priority: high | medium | low | someday
opened: YYYY-MM-DD
last_touched: YYYY-MM-DD
resolution_target: YYYY-MM-DD | none
related_pages: []                      # wikilinks to Framework / Layer / Strategy docs
tags: [vision, cantus]
---
```

---

## Conventions

- Hopkins drafts; Dom signs
- Cantus voice and tone bans apply (no Caesar, no comparable-driven identity, no borrowed legitimacy, no "our mission," no Forge)
- Acknowledge open questions explicitly — don't paper over uncertainty
- Cite specific Framework/Layer pages this would change so the downstream impact is legible
- Distinguish what Dom has *decided* from what is being *proposed* or *explored*

---

## Current Active Topics

| Topic | Priority | Opened | Status |
|---|---|---|---|
| [[Vision/Active/Tier-1-Architecture]] | high | 2026-05-03 | active |

---

*Last updated: 2026-05-03. Author of record: Dom Espinosa.*
