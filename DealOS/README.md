---
type: dealos_spec
status: active
audience: internal
owner: "Dom Espinosa"
created: 2026-05-02
updated: 2026-05-04
spec_class: data_model
build_status: spec
linked_cii_data_asset: ""
linked_cii_loop: ""
related_pages: []
tags: [dealos, dealos-spec]
---
# DealOS

> The operating system for commercial real estate. From discovery to close.

---

## Structure

```
DealOS/
├── Founding-Vision.md      # North star vision document
├── Founding-Team/          # Agent team analysis & planning
│   └── README.md
├── Product/                # Product specs & roadmaps
│   ├── Product-Vision.md
│   ├── Product-Spec-Financial-Analyst-Layer.md
│   └── DealOS-Obsidian-Alignment.md
├── Architecture/           # Technical design & systems
│   ├── Architecture-Financial-Analyst-Layer.md
│   └── Data-Flywheel-Strategy.md
├── Research/               # Market research & domain expertise
│   ├── Market-Research-Competitive-Analysis.md
│   └── Domain-CRE-Financial-Analysis.md
└── GTM/                    # Go-to-market strategy
    ├── GTM-Strategy.md
    └── Commercial-Strategy-Tier4.md
```

---

## Key Documents

| Document | Purpose |
|----------|---------|
| [[Founding-Vision]] | The full stack vision: what we're building |
| [[Product-Spec-Financial-Analyst-Layer]] | Financial Analyst agents spec |
| [[Architecture-Financial-Analyst-Layer]] | Technical architecture |
| [[Market-Research-Competitive-Analysis]] | Competitive landscape |
| [[GTM-Strategy]] | Distribution & growth strategy |

---

## Database

- **Supabase Project:** satpzfwidcndbibxbnrv
- **Schema:** See `/root/clawd/dealos-schema.sql`
- **Source:** Migrated from Prisma (mission-control repo)

---

## Related

- **Code:** `/root/mission-control/` (legacy Next.js app)
- **Hopkins:** My agent persona for DealOS coordination
- **Clawdbot:** Open source foundation

---

*Building the future of CRE, one deal at a time.*
