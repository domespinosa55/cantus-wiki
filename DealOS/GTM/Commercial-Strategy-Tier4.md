---
type: dealos_spec
status: active
audience: internal
owner: "Dom Espinosa"
created: 2026-05-02
updated: 2026-05-04
spec_class: gtm
build_status: spec
linked_cii_data_asset: ""
linked_cii_loop: ""
related_pages: []
tags: [dealos, dealos-spec]
---
# Commercial Strategy: Tier 4 Platform

> Enterprise AI for commercial real estate — Open infrastructure, proprietary intelligence, advisory moat.

**Status:** 🗓️ Strategic planning

---

## The Three-Layer Business Model

```
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 1: INFRASTRUCTURE                       │
│                      (Open Source)                               │
│                                                                  │
│    Mesh Router │ Data Pipeline │ Integration Framework           │
│                                                                  │
│    "You can run this yourself. Here's how."                     │
│    Builds trust. Reduces lock-in fear. Community contribution.  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 2: MANAGED SERVICE                      │
│                      (SaaS Pricing)                              │
│                                                                  │
│    "We'll run it for you. Better, faster, cheaper."             │
│                                                                  │
│    • LLM brokerage (bulk deals, routing, failover)              │
│    • Managed infrastructure (no DevOps needed)                   │
│    • Security + compliance (SOC2, enterprise-grade)             │
│    • Support + SLAs                                              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 3: INTELLIGENCE                         │
│                      (Proprietary Moat)                          │
│                                                                  │
│    "Insights only we can provide."                              │
│                                                                  │
│    • CRE-tuned models (trained on platform data)                │
│    • Benchmarking ("You vs. Market")                            │
│    • Predictive analytics (market timing, valuation)            │
│    • Advisory services (data-driven recommendations)            │
│                                                                  │
│    This is the lock-in. Can't get this anywhere else.           │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Layer 1: Open Source Strategy

### What to Open Source

| Component | Why Open It |
|-----------|-------------|
| Mesh Router | Builds trust, reduces "vendor lock-in" fear |
| Data pipeline framework | Shows transparency in how data is handled |
| Integration SDK | Makes it easy to adopt, community contributes |
| Anonymization tools | Proves privacy commitment |

### What to Keep Proprietary

| Component | Why Keep It |
|-----------|-------------|
| Trained CRE models | The actual value |
| Aggregated platform data | The moat |
| Benchmarking algorithms | The insight engine |
| Advisory playbooks | The expertise |

### The Psychology

```
Enterprise Buyer Thinking:
"I'm nervous about AI vendor lock-in..."

Your Response:
"The infrastructure is open source. You can fork it tomorrow.
 You're paying for the intelligence layer — the models trained
 on data you can't get anywhere else."

Result:
✓ Control fear → neutralized
✓ Value prop → clear
✓ Switching cost → real but fair (it's the data, not the tooling)
```

---

## Layer 2: AI Brokerage Model

### The Problem You Solve

Enterprises face AI chaos:
- OpenAI vs Anthropic vs Google vs Mistral vs...
- Pricing changes constantly
- Each has different strengths
- Security/compliance requirements
- No one wants to manage 5 vendor relationships

### The Solution: AI Brokerage

```
┌─────────────────────────────────────────────────────────────────┐
│                      DEALOS AI LAYER                             │
│                                                                  │
│  Enterprise Customer                                             │
│         │                                                        │
│         │  Single API, single contract, single invoice           │
│         ▼                                                        │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │              DealOS Intelligent Router                   │    │
│  │                                                          │    │
│  │  • Routes to optimal model for each request              │    │
│  │  • Handles failover automatically                        │    │
│  │  • Enforces security/compliance policies                 │    │
│  │  • Applies enterprise-specific fine-tuning               │    │
│  │  • Tracks usage, provides analytics                      │    │
│  │                                                          │    │
│  └─────────────────────────────────────────────────────────┘    │
│         │           │           │           │                    │
│         ▼           ▼           ▼           ▼                    │
│     Anthropic    OpenAI     Google      Local/Private           │
│                                                                  │
│  Bulk pricing │ Negotiated rates │ Volume discounts              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### How You Make Money on Brokerage

1. **Spread** — Negotiate bulk rates, charge retail (keep margin)
2. **Efficiency** — Smart routing saves tokens, you pocket the savings
3. **Management fee** — Flat % for handling the complexity
4. **Upsell** — Start with routing, expand to intelligence layer

### What Enterprises Get

| Pain Point | Your Solution |
|------------|---------------|
| "Which model should we use?" | Automatic routing |
| "How do we negotiate with OpenAI?" | You already did |
| "What about compliance?" | SOC2, audit trails, data residency |
| "What if Anthropic goes down?" | Automatic failover |
| "How do we control costs?" | Usage analytics + optimization |

---

## Layer 3: Intelligence Advisory

### The Ultimate Flywheel

```
Customer uses DealOS
        │
        ▼
Their data joins the platform
(anonymized, aggregated)
        │
        ▼
Platform intelligence improves
        │
        ▼
You can now tell them:
        │
        ├── "Your deals take 23% longer to close than market avg"
        ├── "Your cap rate assumptions are 50bps conservative"
        ├── "Similar deals in this market closed 15% higher"
        ├── "We predict this submarket will outperform by Q3"
        │
        ▼
They can't leave (where else would they get this?)
        │
        ▼
More customers want this insight
        │
        └──────────► More data ──────────┘
```

### Advisory Services (Premium Tier)

| Service | What It Is | Why It's Defensible |
|---------|-----------|---------------------|
| Deal Benchmarking | "How does this deal compare?" | Only you have the comp data |
| Market Timing | "When should we buy/sell?" | Predictive models on real flows |
| Valuation Audit | "Is this priced right?" | Cross-platform pattern matching |
| Portfolio Optimization | "What's underperforming?" | Aggregated performance data |
| Acquisition Targeting | "What should we buy next?" | Platform-wide opportunity detection |

### The Conversation

```
You: "Based on 2,847 comparable deals on our platform,
     your average hold period is 18 months longer than
     optimal. Here's what top performers do differently..."

Enterprise: "How do you know this?"

You: "We see every deal. Anonymized, but we see the patterns.
     No one else can tell you this."

Enterprise: *opens wallet*
```

---

## Pricing Strategy

### Tiered Model

| Tier | What's Included | Price Signal |
|------|-----------------|--------------|
| **Starter** | Basic platform access, shared models | $X/seat/month |
| **Professional** | + AI routing, usage analytics | $2X/seat/month |
| **Enterprise** | + Custom fine-tuning, dedicated support | $4X/seat/month |
| **Intelligence** | + Benchmarking, advisory, predictions | Custom (high $$$) |

### Usage Components

| Component | Model |
|-----------|-------|
| Platform access | Per-seat subscription |
| AI queries | Usage-based (per 1K queries) with volume discounts |
| Model training | One-time + maintenance fee for custom fine-tunes |
| Advisory | Retainer or per-engagement |

### Enterprise Levers

- **Commit to volume** → Better AI rates (you pass through some savings)
- **Contribute data** → Discount (their data makes platform smarter)
- **Multi-year** → Price lock + priority features
- **Advisory bundle** → Highest margin, strongest lock-in

---

## Go-to-Market Sequence

### Phase 1: Land with Infrastructure

```
"We'll help you integrate AI into your CRE workflow.
 Open source foundation. You're in control."

- Low friction entry
- Prove value with routing + cost savings
- Build relationship
```

### Phase 2: Expand with Managed Service

```
"Let us handle the complexity.
 Focus on deals, not DevOps."

- Convert DIY to managed
- Add fine-tuning on their data
- Upsell support + SLAs
```

### Phase 3: Lock-in with Intelligence

```
"Here's what the market is doing.
 Here's where you compare.
 Here's what you should do next."

- Advisory engagement
- Benchmarking subscription
- They can't leave — data is unique
```

---

## Competitive Positioning

### vs. Generic AI Platforms (AWS Bedrock, Azure OpenAI)

```
Them: "Here's access to models. Figure it out."
You:  "Here's CRE-tuned AI that knows your domain,
       routes intelligently, and tells you how you
       compare to the market."
```

### vs. CRE Incumbents (CoStar, Yardi)

```
Them: "Here's data about properties."
You:  "Here's intelligence about deals, patterns,
       and predictions. Plus AI that actually works."
```

### vs. In-House AI Teams

```
Them: "We'll build our own."
You:  "With what training data? We have the entire
       platform's deal flow. You have yours."
```

---

## Risk Mitigation

| Risk | Mitigation |
|------|------------|
| "What if enterprises want to leave?" | Open source infra = they can fork. But they lose the intelligence layer. Fair trade. |
| "What if they're scared of data sharing?" | Transparent anonymization. Open source the pipeline. SOC2 cert. |
| "What if LLM prices drop?" | Routing layer still valuable. Intelligence layer is the real moat. |
| "What if competitors copy?" | They can copy the tooling (it's open). They can't copy the data. |

---

## The Insane Flywheel (Full Picture)

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│   Open Source Infrastructure                                     │
│          │                                                       │
│          ▼                                                       │
│   Low friction adoption ───────────────────────┐                │
│          │                                      │                │
│          ▼                                      │                │
│   Enterprises onboard                           │                │
│          │                                      │                │
│          ▼                                      │                │
│   Their data joins platform ◄───────────────────┘                │
│          │                                                       │
│          ▼                                                       │
│   Better models + benchmarks                                     │
│          │                                                       │
│          ▼                                                       │
│   Intelligence tier unlocks                                      │
│          │                                                       │
│          ▼                                                       │
│   Advisory becomes indispensable                                 │
│          │                                                       │
│          ▼                                                       │
│   Highest margins + strongest lock-in                           │
│          │                                                       │
│          ▼                                                       │
│   More enterprises want this ──────────────────┐                │
│          │                                      │                │
│          └──────────────────────────────────────┘                │
│                                                                  │
│   Competitors can copy the tools.                               │
│   They can't copy the data.                                     │
│   They can't copy the network.                                  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Action Items

- [ ] Identify which mesh router components to open source first
- [ ] Design data contribution incentive model
- [ ] Price modeling: brokerage margins at various volumes
- [ ] Legal review: data usage rights in enterprise ToS
- [ ] SOC2 certification roadmap
- [ ] Advisory service packaging + pricing
- [ ] Competitive teardown: what are CoStar/Yardi offering in AI?

---

## Dependencies

- [[Data-Flywheel-Strategy]] — The data architecture
- [[Supabase-Integration]] — The data layer
- [[Mesh-Router]] — The routing layer (open source candidate)
- DealOS product roadmap

---

*Open the door with infrastructure. Close the deal with intelligence. Lock it in with data.*
