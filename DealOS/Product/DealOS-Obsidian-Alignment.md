---
type: dealos_spec
status: active
audience: internal
owner: "Dom Espinosa"
created: 2026-05-02
updated: 2026-05-04
spec_class: frontend
build_status: spec
linked_cii_data_asset: ""
linked_cii_loop: ""
related_pages: []
tags: [dealos, dealos-spec]
---
# DealOS ↔ Obsidian Alignment

*Data Model Synchronization for CRE Workflows*

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                         POCKET (Ears)                            │
│     Voice capture → Transcripts → Entity extraction             │
└────────────────────────────┬────────────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│                      OBSIDIAN (Brain/Hands)                      │
│                                                                  │
│  /Companies     /Contacts     /Deals     /Properties            │
│  /Touchpoints   /Tasks        /Intelligence                     │
│                                                                  │
│  - Markdown files with YAML frontmatter                         │
│  - Backlinks for relationships                                  │
│  - Dataview queries for dynamic views                           │
└────────────────────────────┬────────────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────────────┐
│                  DEALOS / Mission Control (UI)                   │
│                                                                  │
│  PostgreSQL Database (source of truth for structured data)      │
│  - Companies, Contacts, Deals, Properties, Tasks                │
│  - Agent Suggestions (AI-generated, human-reviewed)             │
│  - Touchpoints, Intelligence, Audit Logs                        │
│                                                                  │
│  Features:                                                       │
│  - Deal Pipeline visualization                                  │
│  - Contact relationship mapping                                 │
│  - Task management                                              │
│  - Agent suggestion review                                      │
└─────────────────────────────────────────────────────────────────┘
```

---

## Entity Mapping

| DealOS Entity | Obsidian Folder | Template | Sync Direction |
|---------------|-----------------|----------|----------------|
| Company | `/Companies` | Company Template | Bidirectional |
| Contact | `/Contacts` | Contact Template | Bidirectional |
| Transaction | `/Deals` | Deal Template | Bidirectional |
| Property | `/Properties` | Property Template | Bidirectional |
| Touchpoint | `/Touchpoints` | Touchpoint Template | Obsidian → DealOS |
| Task | `/Tasks` | Task Template | Bidirectional |
| IntelligenceRecord | `/Intelligence` | Intelligence Template | Obsidian → DealOS |

---

## Folder Structure (Aligned)

```
obsidian/
├── Companies/           # LPs, Developers, Operators, Brokers
├── Contacts/            # People with full CRE profiles
├── Deals/
│   ├── Active/          # Current pipeline
│   ├── Pipeline/        # Pre-marketing, qualification
│   ├── Closed/          # Won deals
│   └── Dead/            # Lost deals
├── Properties/          # Physical assets
├── Touchpoints/         # Calls, meetings, emails, tours
├── Tasks/
│   ├── Todo/
│   ├── InProgress/
│   └── Done/
├── Intelligence/        # Market intel, competitor info
├── Conversations/       # Pocket transcripts
├── Meetings/           # Calendar-linked meeting notes
├── Daily Notes/        # Daily journals
├── Templates/          # Entity templates
└── LifeOS/             # Meta/planning docs
```

---

## CRE-Specific Fields

### Company Types
- **LP** - Limited Partner (investor)
- **Developer** - Builds/develops properties
- **Operator** - Manages/operates properties
- **Broker** - Transaction intermediary
- **Utility** - Power provider
- **Hyperscaler** - Cloud/tech (AWS, Google, Meta)
- **Manufacturer** - Equipment/hardware
- **Consultant** - Advisory services
- **Vendor** - Service providers
- **Legal** - Law firms

### Deal Stages (Pipeline)
1. **ORIGINATION** - Initial lead/opportunity
2. **QUALIFICATION** - Vetting the opportunity
3. **PRE_MARKETING** - Preparing materials
4. **MARKETING** - Active marketing
5. **UNDER_LOI** - Letter of Intent signed
6. **DUE_DILIGENCE** - DD period
7. **UNDER_CONTRACT** - PSA signed
8. **CLOSED** - Deal completed
9. **DEAD** - Deal fell through

### Property Types
- **DATA_CENTER** - DC/colocation
- **INDUSTRIAL** - Warehouse/distribution
- **LAND** - Raw land/development sites
- **OFFICE** - Office buildings
- **RETAIL** - Shopping/retail
- **MULTIFAMILY** - Apartments
- **MIXED_USE** - Combined uses

### Data Center Specific
- **Power (MW)** - Megawatt capacity
- **PUE** - Power Usage Effectiveness
- **Redundancy** - N, N+1, 2N, 2N+1
- **Fiber providers** - Connectivity

---

## Workflow Integration

### 1. Voice Capture (Pocket → Obsidian)
```
[Record meeting on Pocket]
        ↓
[Transcript saved to Conversations/]
        ↓
[Brain Sync Agent extracts entities]
        ↓
[Creates/updates: Contacts, Companies, Deals, Tasks]
        ↓
[Agent Suggestions appear in DealOS for review]
```

### 2. Deal Pipeline (DealOS ↔ Obsidian)
```
[Deal created in DealOS]
        ↓
[Synced to Obsidian: Deals/Active/Deal Name.md]
        ↓
[Notes added in Obsidian]
        ↓
[Synced back to DealOS]
```

### 3. Intelligence Capture (Field → Obsidian → DealOS)
```
[Learn market intel at conference]
        ↓
[Quick note in Obsidian: Intelligence/]
        ↓
[Agent extracts structured data]
        ↓
[Creates IntelligenceRecord in DealOS]
```

---

## Next Steps

1. [ ] Set up bidirectional sync (Obsidian ↔ DealOS)
2. [ ] Configure Brain Sync Agent for all entity types
3. [ ] Create Dataview dashboards in Obsidian
4. [ ] Test full workflow: Pocket → Obsidian → DealOS

---

*Aligned: January 25, 2026*
