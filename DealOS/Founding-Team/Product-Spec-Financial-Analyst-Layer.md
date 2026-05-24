---
type: dealos_spec
status: active
audience: internal
owner: "Dom Espinosa"
created: 2026-05-02
updated: 2026-05-04
spec_class: agent
build_status: spec
linked_cii_data_asset: ""
linked_cii_loop: ""
related_pages: []
tags: [dealos, dealos-spec]
---
# Product Spec: Financial Analyst Layer

> **Status:** DRAFT — Ready for Founder Review  
> **Created:** 2026-01-26  
> **Author:** Product Lead (Subagent)  
> **Review Date:** Morning sync

---

## Executive Summary

The Financial Analyst Layer is DealOS's AI-native intelligence engine. It's a suite of five specialized agents that automate the analytical grunt work currently done by junior analysts at investment shops, brokerage firms, and appraisal companies.

**Value proposition:** Do in 10 minutes what takes a team 10 hours.

**Primary disruption targets:**
- Argus Enterprise (complex, expensive financial modeling)
- CoStar (overpriced, stale market data)
- Traditional appraisal industry ($5-50K per report, weeks of turnaround)
- Manual Excel-based due diligence

---

## 1. User Personas

### 1.1 Private Equity Associate — "Jordan"

**Demographics:**
- 26-32 years old
- 2-5 years CRE experience
- Works at PE fund or family office
- Evaluates 50-100 deals/month, closes 2-5/year

**Pain Points:**
- Drowning in deal flow, can't analyze fast enough
- Spends 60% of time on Excel modeling
- Manually combing through data rooms
- Has to create IC memos at 2am before committee meetings
- Pays $15K+/year for Argus licenses they barely use

**Success Metric:** More deals reviewed → better deals closed → better carry

**Quote:** *"If I could get a first-pass model and memo done in an hour instead of a weekend, I'd look at 3x more deals."*

---

### 1.2 Investment Sales Broker — "Marcus"

**Demographics:**
- 30-45 years old
- Runs a team at CBRE, JLL, Cushman, or boutique shop
- Handles 10-30 listings/year
- Needs to advise clients on pricing and market positioning

**Pain Points:**
- Clients expect instant market analysis
- Comp research is tedious and time-consuming
- Marketing materials require custom financial projections
- Needs credible valuations for pricing recommendations
- CoStar subscription is $25K+/year and data is stale

**Success Metric:** Faster time to market → higher close rate → bigger commissions

**Quote:** *"My clients want a broker opinion of value before listing. Currently takes me 2 days. Should take 2 hours."*

---

### 1.3 Lender/Debt Fund Analyst — "Priya"

**Demographics:**
- 24-30 years old
- Works at CMBS shop, debt fund, or bank CRE group
- Reviews 20-50 loan applications/month
- Has strict compliance and documentation requirements

**Pain Points:**
- Due diligence checklists are manual and error-prone
- Needs to verify borrower financials against property performance
- Creates credit memos for every deal
- Red flags get missed under time pressure
- Appraisal review is a bottleneck

**Success Metric:** Faster underwriting → more loans closed → better portfolio performance

**Quote:** *"I need to know in 15 minutes if a deal is worth spending a week on."*

---

### 1.4 Developer/Owner-Operator — "David"

**Demographics:**
- 35-55 years old
- Owns/operates 5-50 properties
- Evaluates acquisition opportunities opportunistically
- Handles own analysis or has small team

**Pain Points:**
- Doesn't have dedicated acquisition team
- Needs to move fast on opportunities
- Can't afford big software licenses
- Relies on broker-provided analysis (biased)
- Wants independent validation of deals

**Success Metric:** Confident decision-making without huge overhead

**Quote:** *"I see a deal Friday night, I need to know by Monday if it's real."*

---

### 1.5 Appraisal Firm Principal — "Sandra"

**Demographics:**
- 45-60 years old
- Runs appraisal shop with 5-20 appraisers
- Serves banks, investors, litigation clients
- Operates on thin margins with high labor costs

**Pain Points:**
- Each appraisal takes 20-40 hours of analyst time
- USPAP compliance is meticulous and error-prone
- Comp selection is subjective and time-consuming
- Struggling to hire qualified appraisers
- Lender clients want faster turnaround

**Success Metric:** 2x throughput with same headcount

**Quote:** *"If AI could do the first 80% of an appraisal, my MAI appraisers could do 3x the volume."*

---

## 2. User Journeys by Agent

### 2.1 Due Diligence Agent

**Purpose:** Automated document review, risk identification, and checklist management

#### User Journey: Jordan reviews a new acquisition opportunity

```
┌─────────────────────────────────────────────────────────────────┐
│ TRIGGER: Seller shares data room link                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. CONNECT DATA ROOM                                           │
│     • Jordan pastes Dropbox/Google Drive/VDR link              │
│     • Agent authenticates, indexes all documents               │
│     • Document inventory generated (50-500 files)              │
│                                                                 │
│  2. AUTOMATED DOCUMENT CLASSIFICATION                           │
│     • Agent categorizes: Leases, Financials, Title, Survey,    │
│       Environmental, Legal, Permits, Tax, Insurance            │
│     • Missing document checklist auto-generated                │
│     • "You're missing: Phase I, rent roll > 6 months old"      │
│                                                                 │
│  3. DOCUMENT EXTRACTION                                         │
│     • Lease abstracts created automatically                    │
│     • Rent roll reconciled against leases                      │
│     • Financial statements parsed, trended                     │
│     • Key dates surfaced (lease expirations, options)          │
│                                                                 │
│  4. RED FLAG DETECTION                                          │
│     • "Lease with ABC Corp has unusual termination clause"     │
│     • "Property taxes increased 47% YoY — verify"              │
│     • "Environmental report references prior contamination"    │
│     • Risk items ranked by severity                            │
│                                                                 │
│  5. DD REPORT GENERATION                                        │
│     • Executive summary of findings                            │
│     • Detailed item-by-item review                             │
│     • Open items list for follow-up                            │
│     • Export to PDF/Word for IC package                        │
│                                                                 │
│  OUTCOME: 4 hours of work done in 30 minutes                   │
└─────────────────────────────────────────────────────────────────┘
```

#### Core Features (Prioritized)

| Priority | Feature | Complexity | Impact |
|----------|---------|------------|--------|
| P0 | Document upload/ingestion | Medium | Critical |
| P0 | Lease abstracting | High | Critical |
| P0 | Red flag detection | Medium | High |
| P1 | Rent roll reconciliation | High | High |
| P1 | Missing document checklist | Low | Medium |
| P2 | Multi-property portfolios | High | Medium |
| P2 | VDR direct integration | Medium | Medium |

---

### 2.2 Financial Modeling Agent

**Purpose:** Automated proforma generation, scenario analysis, IRR/NPV calculations

#### User Journey: Jordan builds a model for IC presentation

```
┌─────────────────────────────────────────────────────────────────┐
│ TRIGGER: Jordan has extracted rent roll + financials from DD   │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. DATA INGESTION                                              │
│     • Agent pulls from DD Agent or manual upload               │
│     • Rent roll parsed: tenants, terms, rent, options          │
│     • T-12 financials extracted: NOI, expenses, capex          │
│     • Market assumptions suggested (from Research Agent)        │
│                                                                 │
│  2. ASSUMPTION CONFIGURATION                                    │
│     • Jordan reviews/adjusts:                                  │
│       - Acquisition price / basis                              │
│       - Financing terms (LTV, rate, IO period)                 │
│       - Market rent growth assumptions                         │
│       - Expense growth assumptions                             │
│       - Exit cap rate / hold period                            │
│     • Defaults populated from market data                      │
│                                                                 │
│  3. MODEL GENERATION                                            │
│     • 10-year monthly/annual cash flow projection              │
│     • Lease-by-lease rollover modeling                         │
│     • Debt service schedule                                    │
│     • Capital reserves and TI/LC budgeting                     │
│     • Waterfall modeling (LP/GP splits)                        │
│                                                                 │
│  4. SCENARIO ANALYSIS                                           │
│     • Base / Bull / Bear cases auto-generated                  │
│     • Sensitivity tables: Price vs. Exit Cap                   │
│     • "What if tenant X vacates?" scenarios                    │
│     • Break-even analysis                                      │
│                                                                 │
│  5. OUTPUT                                                      │
│     • Interactive dashboard with key metrics                   │
│     • Export to Excel (formatted, formula-linked)              │
│     • Export charts/tables for presentations                   │
│     • API endpoint for downstream agents                       │
│                                                                 │
│  OUTCOME: Full Argus-quality model in 20 minutes vs. 2 days    │
└─────────────────────────────────────────────────────────────────┘
```

#### Core Features (Prioritized)

| Priority | Feature | Complexity | Impact |
|----------|---------|------------|--------|
| P0 | Basic proforma (revenue, expense, NOI) | Medium | Critical |
| P0 | Debt modeling (interest, amort) | Medium | Critical |
| P0 | IRR/NPV/Equity Multiple calc | Low | Critical |
| P0 | Excel export (clean, auditable) | Medium | High |
| P1 | Lease-by-lease modeling | High | High |
| P1 | Sensitivity tables | Medium | High |
| P1 | Scenario comparison | Medium | Medium |
| P2 | Waterfall modeling | High | Medium |
| P2 | Monte Carlo simulation | High | Low |

---

### 2.3 Investment Memo Agent

**Purpose:** Auto-generate IC memos, executive summaries, and recommendation synthesis

#### User Journey: Jordan prepares IC package before committee meeting

```
┌─────────────────────────────────────────────────────────────────┐
│ TRIGGER: Financial model complete, DD findings ready           │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. CONTEXT GATHERING                                           │
│     • Agent pulls from DD Agent findings                       │
│     • Agent pulls from Financial Modeling Agent outputs        │
│     • Agent pulls from Research Agent market data              │
│     • Jordan provides investment thesis (optional)             │
│                                                                 │
│  2. MEMO STRUCTURE SELECTION                                    │
│     • Jordan selects firm template or uses default             │
│     • Sections: Exec Summary, Property, Market, Financials,    │
│       Risk Factors, Recommendation                             │
│     • Configurable: length, detail level, tone                 │
│                                                                 │
│  3. AUTOMATED DRAFTING                                          │
│     • Executive summary (1-page deal overview)                 │
│     • Property description (sourced from docs + web)           │
│     • Market analysis (Research Agent data)                    │
│     • Financial summary (key metrics, charts)                  │
│     • Risk factors (from DD red flags)                         │
│     • Recommendation with supporting rationale                 │
│                                                                 │
│  4. HUMAN REVIEW & REFINEMENT                                   │
│     • Jordan edits inline (tracked changes)                    │
│     • AI assistant for rewrites, clarifications                │
│     • Add/remove sections as needed                            │
│     • Attach supporting exhibits                               │
│                                                                 │
│  5. OUTPUT                                                      │
│     • Formatted PDF/Word for IC distribution                   │
│     • Presentation slides (key points)                         │
│     • One-pager summary for quick review                       │
│     • Version history maintained                               │
│                                                                 │
│  OUTCOME: IC-ready memo in 1 hour vs. overnight                │
└─────────────────────────────────────────────────────────────────┘
```

#### Core Features (Prioritized)

| Priority | Feature | Complexity | Impact |
|----------|---------|------------|--------|
| P0 | Exec summary generation | Medium | Critical |
| P0 | Financial summary section | Medium | Critical |
| P0 | Risk factors from DD | Low | High |
| P0 | PDF export | Low | High |
| P1 | Custom template support | Medium | Medium |
| P1 | Market analysis section | Medium | Medium |
| P1 | Inline editing/refinement | Medium | Medium |
| P2 | Presentation slide generation | High | Low |
| P2 | Comparison across deals | High | Medium |

---

### 2.4 Research & Comp Agent

**Purpose:** Market research automation, comparable sales/rent analysis, submarket intelligence

#### User Journey: Marcus needs BOV for new listing pitch

```
┌─────────────────────────────────────────────────────────────────┐
│ TRIGGER: Marcus meeting potential seller next week             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. PROPERTY IDENTIFICATION                                     │
│     • Marcus enters: address, property type, SF, unit count    │
│     • Agent enriches from public records, assessor data        │
│     • Property characteristics confirmed                       │
│                                                                 │
│  2. COMPARABLE SALES SEARCH                                     │
│     • Agent searches: last 24 months, 5-mile radius            │
│     • Filters by: property type, size, quality, vintage        │
│     • Sources: public records, deal databases, news            │
│     • 5-15 potential comps identified                          │
│                                                                 │
│  3. COMP ANALYSIS                                               │
│     • Price/SF, cap rate, $/unit calculated                    │
│     • Adjustments suggested (location, condition, size)        │
│     • Comp quality scored (how similar?)                       │
│     • Marcus selects final comp set                            │
│                                                                 │
│  4. MARKET CONTEXT                                              │
│     • Submarket overview (supply, demand, absorption)          │
│     • Rent trends and vacancy data                             │
│     • Recent news/developments affecting market                │
│     • Forecast: rent growth, cap rate trajectory               │
│                                                                 │
│  5. RENT COMP ANALYSIS (for income properties)                  │
│     • Current market rents by unit type/SF                     │
│     • Concession trends                                        │
│     • Lease-up velocity benchmarks                             │
│     • Rent vs. owned comparison                                │
│                                                                 │
│  6. OUTPUT                                                      │
│     • Broker Opinion of Value with range                       │
│     • Comp summary table                                       │
│     • Market overview document                                 │
│     • Data exportable for OM preparation                       │
│                                                                 │
│  OUTCOME: Replace $25K CoStar subscription, better output      │
└─────────────────────────────────────────────────────────────────┘
```

#### Core Features (Prioritized)

| Priority | Feature | Complexity | Impact |
|----------|---------|------------|--------|
| P0 | Property lookup/enrichment | Medium | Critical |
| P0 | Comp search (sales) | High | Critical |
| P0 | Basic comp analysis | Medium | High |
| P1 | Rent comp search | High | High |
| P1 | Submarket analytics | High | High |
| P1 | BOV generation | Medium | Medium |
| P2 | News/development tracking | Medium | Low |
| P2 | Forecast modeling | High | Medium |

**Data Strategy Note:** MVP can use public records + user-contributed data. Long-term moat requires proprietary data ingestion pipelines.

---

### 2.5 Appraisal Agent

**Purpose:** Automated valuation models, USPAP-compliant reports, income/sales/cost approaches

#### User Journey: Sandra's firm needs appraisal for bank client

```
┌─────────────────────────────────────────────────────────────────┐
│ TRIGGER: Bank orders appraisal for refinance                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  1. ENGAGEMENT SETUP                                            │
│     • Sandra creates engagement: client, property, purpose     │
│     • Scope of work defined (full vs. restricted)              │
│     • USPAP requirements flagged based on use                  │
│     • Appraiser assignment (MAI oversight)                     │
│                                                                 │
│  2. DATA COLLECTION                                             │
│     • Agent pulls from Research Agent (comps, market)          │
│     • Property data ingested (rent roll, financials)           │
│     • Public records enrichment                                │
│     • Inspection photos/notes uploaded                         │
│                                                                 │
│  3. INCOME APPROACH                                             │
│     • NOI reconstruction from financials                       │
│     • Market rent analysis (vs. contract rent)                 │
│     • Cap rate selection with rationale                        │
│     • Direct cap and DCF valuations                            │
│                                                                 │
│  4. SALES COMPARISON APPROACH                                   │
│     • Comp selection with adjustment grid                      │
│     • Automated adjustments (size, age, location, quality)     │
│     • Appraiser reviews/overrides adjustments                  │
│     • Indicated value reconciliation                           │
│                                                                 │
│  5. COST APPROACH (if applicable)                               │
│     • Replacement cost estimation                              │
│     • Depreciation calculation                                 │
│     • Land value extraction                                    │
│                                                                 │
│  6. RECONCILIATION & REPORT                                     │
│     • Weight approaches based on property type                 │
│     • Final value opinion with range                           │
│     • USPAP-compliant narrative generated                      │
│     • Certifications, limiting conditions, assumptions         │
│     • MAI appraiser reviews, signs off                         │
│                                                                 │
│  7. OUTPUT                                                      │
│     • Full narrative appraisal report (PDF)                    │
│     • Summary report option                                    │
│     • XML/data export for lender systems                       │
│     • Work file documentation maintained                       │
│                                                                 │
│  OUTCOME: 30-hour appraisal becomes 8 hours                    │
└─────────────────────────────────────────────────────────────────┘
```

#### Core Features (Prioritized)

| Priority | Feature | Complexity | Impact |
|----------|---------|------------|--------|
| P0 | Income approach (direct cap) | Medium | Critical |
| P0 | Sales comparison approach | High | Critical |
| P0 | Basic report generation | High | Critical |
| P1 | DCF analysis | High | High |
| P1 | Adjustment grid automation | High | High |
| P1 | USPAP compliance checks | Medium | High |
| P2 | Cost approach | Medium | Low |
| P2 | Full narrative generation | High | Medium |
| P2 | XML/MISMO export | Medium | Low |

---

## 3. Feature Prioritization Matrix

### Build Order Rationale

**Phase 1: Core Engine** — Financial Modeling Agent first. Why?
- Clearest disruption target (Argus)
- Most immediate pain point (everyone models deals)
- Foundation for other agents (Memo, Appraisal need models)
- Fastest path to demonstrable value

**Phase 2: Intelligence Layer** — Research & Comp Agent
- Enables market context for modeling
- CoStar disruption story is compelling for sales
- Data collection starts building the moat
- Required for Appraisal Agent accuracy

**Phase 3: Automation** — Due Diligence Agent
- Highest labor savings
- Document processing is AI's strength
- Natural upsell from modeling
- Feeds Investment Memo Agent

**Phase 4: Output** — Investment Memo Agent
- Synthesizes other agents' work
- Lower complexity (narrative generation)
- Clear ROI for busy professionals
- Differentiator vs. pure tools

**Phase 5: Professional Services** — Appraisal Agent
- Highest complexity (regulatory compliance)
- Requires mature Research Agent
- Longer sales cycle (firm relationships)
- Premium pricing tier

---

### Priority Matrix

| Agent | MVP Complexity | Revenue Potential | Strategic Value | Build Order |
|-------|----------------|-------------------|-----------------|-------------|
| Financial Modeling | Medium | High | High | **1st** |
| Research & Comp | High | High | Very High (moat) | **2nd** |
| Due Diligence | Medium | Medium | Medium | **3rd** |
| Investment Memo | Low | Medium | Medium | **4th** |
| Appraisal | Very High | Very High | High | **5th** |

---

## 4. MVP Scope: 2-Week Sprint

### Sprint Goal
**Ship Financial Modeling Agent v0.1 that generates a basic proforma from uploaded rent roll and T-12.**

### Scope Definition

#### IN SCOPE (Must Have)
1. **Rent roll ingestion**
   - Accept Excel/CSV upload
   - Parse: tenant, unit, SF, rent, lease dates
   - Display parsed data for verification

2. **T-12 ingestion**
   - Accept Excel/CSV upload
   - Parse: revenue line items, expense categories
   - Trailing 12-month NOI calculation

3. **Assumption configuration**
   - Purchase price input
   - Exit cap rate input
   - Hold period (years)
   - Rent growth assumption (% annual)
   - Expense growth assumption (% annual)

4. **Proforma generation**
   - Annual cash flow projection (hold period)
   - NOI projection with growth
   - Unlevered IRR calculation
   - Simple exit value (NOI / exit cap)

5. **Basic output**
   - On-screen summary with key metrics
   - Excel export (single worksheet, clean format)

#### OUT OF SCOPE (v0.2+)
- Debt modeling
- Lease-by-lease modeling
- Sensitivity analysis
- Scenario comparison
- Waterfall structures
- PDF reports

### Technical Requirements

| Component | Requirement |
|-----------|-------------|
| File parsing | Support XLS, XLSX, CSV |
| Data validation | Flag parsing errors, require confirmation |
| Calculation engine | Pure functions, auditable |
| Export | Excel with formulas (not just values) |
| State management | Persist deal data between sessions |
| API design | RESTful, ready for agent orchestration |

### Sprint Breakdown

**Week 1: Data Layer**
- Day 1-2: File upload infrastructure
- Day 3-4: Rent roll parser (handle common formats)
- Day 5: T-12 parser

**Week 2: Model Layer**
- Day 1-2: Proforma calculation engine
- Day 3: Assumption UI
- Day 4: Excel export
- Day 5: Testing, polish, documentation

### Definition of Done
- [ ] User can upload rent roll → see parsed tenants
- [ ] User can upload T-12 → see calculated NOI
- [ ] User can input 5 key assumptions
- [ ] System generates 10-year proforma
- [ ] User can download Excel file
- [ ] IRR and key metrics displayed
- [ ] Works with 3 real deal datasets

---

## 5. Success Metrics

### MVP Success Criteria (Week 2)

| Metric | Target | Measurement |
|--------|--------|-------------|
| Functional proforma | ✅ Works | Manual testing with real data |
| Parse accuracy | >90% | Fields correctly extracted |
| Calculation accuracy | 100% | Verified against Excel models |
| Export quality | Usable | User can modify Excel output |
| Time to first output | <10 min | From upload to download |

### Phase 1 Success Criteria (Month 1)

| Metric | Target | Measurement |
|--------|--------|-------------|
| Proformas generated | 50 | Usage tracking |
| Unique users | 10 | User accounts |
| NPS score | >40 | User survey |
| Time savings | >50% | User interviews |
| Error reports | <5 critical | Bug tracking |

### Phase 2 Success Criteria (Quarter 1)

| Metric | Target | Measurement |
|--------|--------|-------------|
| Active weekly users | 100 | Analytics |
| Paid conversions | 25 | Billing |
| Revenue | $10K MRR | Stripe |
| Agent coverage | 3 of 5 agents live | Roadmap |
| Data points collected | 10K properties | Database |

### North Star Metric
**Deals analyzed per user per month** — measures core value delivery

### Lagging Indicators
- Revenue / MRR
- User retention (monthly)
- Deals closed using DealOS analysis

### Leading Indicators  
- Proformas generated
- Document pages processed
- Time from upload to insight
- Feature adoption rate

---

## 6. Open Questions for Founder

### Strategic Questions

1. **Pricing model:** Seat-based like Argus, or usage-based (per proforma/per report)? Usage-based aligns with value delivery but complicates forecasting.

2. **Vertical focus:** All CRE, or start with specific asset class (multifamily, office, industrial)? Multifamily has most standardized data, easiest to model.

3. **Self-serve vs. sales-led:** Target individual analysts directly, or sell to firms? Individual is faster to start, firm deals are bigger but longer.

4. **Open source positioning:** How much of Financial Analyst Layer is open (Clawdbot style) vs. proprietary? Open drives adoption, closed protects moat.

5. **Integration priority:** Build standalone first, or prioritize integration with existing workflows (Excel plugins, VDR integrations)?

### Product Questions

6. **Template library:** How much do we standardize (opinionated defaults) vs. let users configure everything? More opinions = faster to value, less flexibility.

7. **Data room integrations:** Which VDRs matter most? (Intralinks, Venue, Firmex, Google Drive, Dropbox) — this affects DD Agent architecture.

8. **Appraisal compliance:** Do we aim for full USPAP-compliant reports, or position as "pre-appraisal analysis tool"? Full compliance is much harder but bigger market.

9. **Multi-property:** When do we need portfolio-level analysis? Some users will want to model 10 properties at once.

10. **Mobile:** Is mobile access important for roadshow/travel? Could deprioritize if not.

### Technical Questions

11. **Model persistence:** Should users be able to "version" models and compare? Adds complexity but valuable for iterative analysis.

12. **Collaboration:** Multi-user editing on same deal? Needed for teams but adds significant complexity.

13. **Offline:** Do users need offline access? (Excel export partially solves this)

### Go-to-Market Questions

14. **Launch strategy:** Start with founder's network (warm, limited), or broader beta? Warm deals provide feedback, broad provides scale.

15. **Competitive positioning:** Attack Argus directly ("Argus killer"), or position as complement ("works alongside your existing tools")?

---

## Appendix A: Competitive Landscape

| Competitor | Strength | Weakness | Our Angle |
|------------|----------|----------|-----------|
| **Argus Enterprise** | Industry standard, powerful | Expensive ($10K+/seat), steep learning curve | 10x faster, AI-native, modern UX |
| **CoStar** | Comprehensive data | Expensive ($25K+/year), stale data | Fresh data, AI analysis layer |
| **Reonomy** | Good UI, property data | Limited financial tools | Full analysis suite |
| **CREXi** | Deal marketplace | Weak analytics | Analysis + marketplace |
| **Excel** | Flexible, familiar | Manual, error-prone | AI-generated, auditable |

---

## Appendix B: Technical Architecture Notes

```
┌─────────────────────────────────────────────────────────────────┐
│                     DealOS Financial Analyst Layer              │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌─────────────────┐  ┌─────────────────┐  ┌────────────────┐  │
│  │  Document       │  │  Calculation    │  │  Report        │  │
│  │  Processing     │  │  Engine         │  │  Generation    │  │
│  │  Service        │  │                 │  │  Service       │  │
│  └────────┬────────┘  └────────┬────────┘  └───────┬────────┘  │
│           │                    │                    │           │
│           └────────────────────┼────────────────────┘           │
│                                │                                │
│                    ┌───────────┴───────────┐                   │
│                    │   Orchestration Layer │                   │
│                    │   (Agent Coordinator) │                   │
│                    └───────────┬───────────┘                   │
│                                │                                │
│                    ┌───────────┴───────────┐                   │
│                    │     Data Layer        │                   │
│                    │  (Deals, Properties,  │                   │
│                    │   Comps, Market Data) │                   │
│                    └───────────────────────┘                   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

**Key Architectural Decisions (TBD):**
- Calculation engine: Custom vs. existing library?
- Document processing: Custom vs. off-shelf (Unstructured, etc.)?
- Excel generation: SheetJS vs. ExcelJS vs. server-side?
- Agent orchestration: How do agents communicate?

---

## Document History

| Date | Version | Author | Changes |
|------|---------|--------|---------|
| 2026-01-26 | 0.1 | Product Lead | Initial draft |

---

*This spec is a living document. Update as we learn.*
