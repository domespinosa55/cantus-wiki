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
# Domain Expertise: CRE Financial Analysis

> The complete domain knowledge required to build the Financial Analyst Layer of DealOS.

**Author:** Domain Expert Agent  
**Created:** 2026-01-26  
**Status:** 📋 Ready for Morning Review  
**Related:** [[DealOS-Founding-Vision]]

---

## Table of Contents

1. [How CRE Deals Actually Work](#1-how-cre-deals-actually-work)
2. [Due Diligence Process](#2-due-diligence-process)
3. [Financial Modeling Requirements](#3-financial-modeling-requirements)
4. [Investment Memo Structure](#4-investment-memo-structure)
5. [Comp Analysis Methodology](#5-comp-analysis-methodology)
6. [Appraisal Requirements](#6-appraisal-requirements)
7. [Domain Terminology Glossary](#7-domain-terminology-glossary)
8. [Expert Tips for AI Implementation](#8-expert-tips-for-ai-implementation)

---

## 1. How CRE Deals Actually Work

### The End-to-End Deal Lifecycle

```
┌────────────────────────────────────────────────────────────────────────────┐
│                         CRE TRANSACTION LIFECYCLE                          │
├────────────────────────────────────────────────────────────────────────────┤
│                                                                            │
│  ORIGINATION        UNDERWRITING       EXECUTION         CLOSING          │
│  (2-4 weeks)        (2-6 weeks)        (4-12 weeks)      (2-4 weeks)      │
│                                                                            │
│  ┌──────────┐      ┌──────────┐       ┌──────────┐      ┌──────────┐     │
│  │ Sourcing │ ──▶  │ Initial  │ ──▶   │   DD &   │ ──▶  │ Contract │     │
│  │ & Screen │      │ Analysis │       │ Negotiation     │ & Close  │     │
│  └──────────┘      └──────────┘       └──────────┘      └──────────┘     │
│       │                 │                  │                  │           │
│       ▼                 ▼                  ▼                  ▼           │
│  • Deal sourcing   • Financial model  • Full DD         • PSA execution  │
│  • Initial screen  • Preliminary BOV  • Title/survey    • Escrow         │
│  • NDA/CA signing  • IC screening     • Legal review    • Lender close   │
│  • OM review       • LOI submission   • Lender process  • Fund transfer  │
│  • Site visit      • Term negotiation • IC approval     • Title transfer │
│                                       • PSA negotiation                   │
│                                                                            │
└────────────────────────────────────────────────────────────────────────────┘
```

### Deal Origination Channels

| Channel | Volume | Quality | Competition |
|---------|--------|---------|-------------|
| **Broker relationships** | High | Varies | High |
| **Direct owner outreach** | Low | High | Low |
| **Off-market networks** | Medium | High | Medium |
| **Auction platforms** | Medium | Varies | Very High |
| **Distressed/special situations** | Low | Opportunistic | Medium |
| **1031 exchange buyers** | Medium | Motivated | High |

### Key Stakeholders in Every Deal

```
                    ┌─────────────────┐
                    │     SELLER      │
                    │  (Principal)    │
                    └────────┬────────┘
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
     ┌────────────┐  ┌────────────┐  ┌────────────┐
     │  Listing   │  │   Seller   │  │    Tax     │
     │   Broker   │  │  Attorney  │  │  Advisor   │
     └────────────┘  └────────────┘  └────────────┘
                             │
                    ┌────────┴────────┐
                    │   THE DEAL      │
                    └────────┬────────┘
                             │
     ┌──────────────┬────────┼────────┬──────────────┐
     ▼              ▼        ▼        ▼              ▼
┌─────────┐  ┌──────────┐ ┌──────┐ ┌──────────┐ ┌─────────┐
│ Buyer   │  │  Buyer   │ │Lender│ │  Title   │ │Appraiser│
│ Broker  │  │ Attorney │ │      │ │ Company  │ │         │
└─────────┘  └──────────┘ └──────┘ └──────────┘ └─────────┘
                    │
              ┌─────┴─────┐
              ▼           ▼
       ┌──────────┐ ┌──────────┐
       │  Equity  │ │   LP     │
       │ Partner  │ │Investors │
       └──────────┘ └──────────┘
```

### Timeline Reality Check

| Phase | Optimistic | Realistic | Complex Deal |
|-------|------------|-----------|--------------|
| **Sourcing to LOI** | 1 week | 2-3 weeks | 4-6 weeks |
| **LOI to PSA** | 1 week | 2-4 weeks | 4-8 weeks |
| **Due Diligence** | 30 days | 45-60 days | 90+ days |
| **Lender Process** | 45 days | 60-90 days | 90-120 days |
| **Closing** | 1 week | 2-3 weeks | 4+ weeks |
| **TOTAL** | 10-12 weeks | 16-24 weeks | 30-52 weeks |

---

## 2. Due Diligence Process

### 2.1 Standard Checklist Categories

#### A. Financial Due Diligence
```
□ RENT ROLL ANALYSIS
  □ Current rent roll (with lease abstracts)
  □ Historical rent rolls (24-36 months)
  □ Lease expiration schedule
  □ Tenant credit analysis
  □ Rent collection history
  □ Accounts receivable aging
  □ Security deposit verification

□ OPERATING STATEMENTS
  □ T-12 (trailing 12 months) actuals
  □ T-3 year historical financials
  □ Current year budget vs. actual
  □ CAM reconciliations (3 years)
  □ Utility bills (12-24 months)
  □ Property tax bills (3 years)
  □ Insurance policies and claims history

□ INCOME VERIFICATION
  □ Tenant payment history
  □ Percentage rent calculations
  □ Parking income verification
  □ Other income substantiation
  □ Tenant sales reports (retail)
```

#### B. Legal Due Diligence
```
□ TITLE & SURVEY
  □ Preliminary title report
  □ Title exceptions review
  □ ALTA survey (current)
  □ Easement documentation
  □ CC&Rs and restrictions
  □ HOA documents (if applicable)

□ LEASE REVIEW
  □ All tenant leases (executed copies)
  □ Lease amendments and modifications
  □ Guaranty agreements
  □ SNDAs (Subordination, Non-Disturbance, Attornment)
  □ Estoppel certificates
  □ Commission agreements
  □ Tenant correspondence file

□ CONTRACTS & AGREEMENTS
  □ Service contracts inventory
  □ Management agreement
  □ Vendor contracts
  □ Equipment leases
  □ Ground lease (if applicable)
  □ Operating agreements
```

#### C. Physical Due Diligence
```
□ BUILDING CONDITION
  □ Property Condition Assessment (PCA)
  □ Environmental Site Assessment (Phase I)
  □ Phase II (if Phase I triggers)
  □ Seismic risk assessment (applicable markets)
  □ ADA compliance review
  □ Fire/life safety inspection

□ ENGINEERING & SYSTEMS
  □ HVAC age and condition
  □ Roof inspection/warranty
  □ Elevator inspection certificates
  □ Electrical capacity analysis
  □ Plumbing assessment
  □ Parking structure condition (if applicable)

□ CAPITAL NEEDS
  □ Deferred maintenance inventory
  □ CapEx history (5 years)
  □ Planned capital improvements
  □ Tenant improvement obligations
  □ Reserve analysis
```

#### D. Market Due Diligence
```
□ MARKET ANALYSIS
  □ Submarket overview
  □ Competitive set analysis
  □ Rent comparable study
  □ Sales comparable study
  □ Supply pipeline analysis
  □ Absorption trends
  □ Economic drivers assessment

□ TENANT ANALYSIS
  □ Tenant financial statements
  □ Business viability assessment
  □ Industry outlook
  □ Location dependency analysis
  □ Expansion/contraction likelihood
```

### 2.2 Document Types & Their Importance

| Document | Criticality | Common Issues | AI Extraction Value |
|----------|-------------|---------------|---------------------|
| **Rent Roll** | 🔴 Critical | Stale data, missing fields | HIGH - structured data |
| **T-12 P&L** | 🔴 Critical | Non-recurring items buried | HIGH - pattern recognition |
| **Leases** | 🔴 Critical | Missing amendments, abstract errors | VERY HIGH - NLP extraction |
| **Title Report** | 🔴 Critical | Unresolved exceptions | MEDIUM - legal complexity |
| **Phase I ESA** | 🔴 Critical | RECs not addressed | MEDIUM - technical language |
| **PCA Report** | 🟡 Important | Optimistic reserve estimates | HIGH - structured findings |
| **Survey** | 🟡 Important | Encroachments missed | LOW - visual/spatial |
| **Tax Returns** | 🟡 Important | Not always provided | HIGH - consistency check |
| **Service Contracts** | 🟢 Standard | Auto-renewal traps | HIGH - term extraction |

### 2.3 Red Flags to Detect

#### 🚩 Financial Red Flags
```
INCOME RED FLAGS:
├── Rent roll ≠ lease terms (discrepancy > 2%)
├── Large tenant pays below-market rent
├── Concentration risk (single tenant > 25% of income)
├── "Other income" > 10% of total revenue
├── Straight-line rent significantly above cash rent
├── Percentage rent assumptions unrealistic
├── Parking income inflated vs. actual counts
└── Recent large rent concessions not disclosed

EXPENSE RED FLAGS:
├── Management fee below market (< 3% = self-managed)
├── Property taxes based on old assessment
├── Insurance appears understated
├── No reserve contributions
├── R&M suspiciously low (deferred maintenance)
├── Utilities allocated differently than leases specify
├── Missing expense categories
└── Large "miscellaneous" or "other" line items

OCCUPANCY RED FLAGS:
├── Physical occupancy ≠ economic occupancy
├── Tenants on month-to-month > 15% of NRA
├── Lease expirations concentrated in single year
├── Recent move-outs not reflected
├── "Signed leases" counted but not commenced
└── Free rent periods extending past close
```

#### 🚩 Legal Red Flags
```
LEASE RED FLAGS:
├── Termination rights (kickouts, co-tenancy)
├── Exclusive use clauses limiting tenant mix
├── ROFO/ROFR on adjacent spaces
├── Purchase options at favorable prices
├── Expansion options consuming vacant space
├── CAM caps limiting recovery
├── Assignment rights (sublease without consent)
└── Above-market TI/LC obligations remaining

TITLE RED FLAGS:
├── Unresolved mechanic's liens
├── Easements through parking or building
├── Deed restrictions limiting use
├── Outstanding litigation
├── Tax liens or assessments
├── Survey encroachments
└── Missing HOA or REA consents
```

#### 🚩 Physical Red Flags
```
BUILDING RED FLAGS:
├── Deferred maintenance > $5/SF
├── Roof age > 15 years without recent inspection
├── HVAC end-of-life (> 20 years)
├── ADA non-compliance issues
├── Fire code violations
├── Structural concerns noted
├── Asbestos or lead paint presence
└── Environmental contamination history

SITE RED FLAGS:
├── Flood zone designation
├── Wetlands encroachment
├── Parking ratio below code
├── Access limitations
├── Adjacent property risks
└── Zoning non-conformity
```

#### 🚩 Market Red Flags
```
MARKET RED FLAGS:
├── Supply pipeline > 10% of inventory
├── Negative absorption trend (3+ quarters)
├── Submarket vacancy > market average
├── Declining employment in key sectors
├── Rent growth assumptions exceed historical
├── Cap rate assumptions below market
├── Major tenant relocations announced
└── Competitive new development announced
```

### 2.4 DD Workflow for AI Agent

```
INPUT: Raw DD documents (PDFs, spreadsheets, images)

STAGE 1: DOCUMENT CLASSIFICATION
├── Identify document type
├── Extract key metadata (date, parties, property)
├── OCR if needed (older scanned docs)
└── Route to appropriate extraction pipeline

STAGE 2: DATA EXTRACTION
├── Structured extraction (rent rolls, financials)
├── Clause extraction (leases, contracts)
├── Finding extraction (PCA, ESA)
└── Cross-reference existing property data

STAGE 3: VALIDATION
├── Internal consistency checks
├── Cross-document reconciliation
├── Market reasonableness tests
├── Historical comparison
└── Flag anomalies for human review

STAGE 4: RED FLAG SCORING
├── Assign severity (Critical / Major / Minor / Note)
├── Quantify financial impact where possible
├── Link to source document/page
└── Generate remediation recommendations

STAGE 5: REPORT GENERATION
├── Executive summary of findings
├── Detailed checklist with status
├── Red flag report with evidence
├── Outstanding items tracker
└── Recommended next steps

OUTPUT: Structured DD report with confidence scores
```

---

## 3. Financial Modeling Requirements

### 3.1 Standard Proforma Structure

#### Multi-Year Cash Flow Model

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                     PROPERTY: [NAME] - [ADDRESS]                             │
│                     10-YEAR DISCOUNTED CASH FLOW ANALYSIS                    │
├──────────────────────────────────────────────────────────────────────────────┤
│                        Year 1    Year 2    Year 3   ...   Year 10  Total    │
├──────────────────────────────────────────────────────────────────────────────┤
│ REVENUE                                                                      │
│ ──────────────────────────────────────────────────────────────────────────── │
│ Base Rent Revenue                                                            │
│   └── By tenant (contract rent)                                              │
│ Absorption/Turnover Revenue                                                  │
│ Expense Reimbursements                                                       │
│   ├── CAM Recovery                                                           │
│   ├── Tax Recovery                                                           │
│   └── Insurance Recovery                                                     │
│ Percentage Rent                                                              │
│ Parking Income                                                               │
│ Other Income                                                                 │
│ ──────────────────────────────────────────────────────────────────────────── │
│ GROSS POTENTIAL REVENUE (GPR)                                                │
│                                                                              │
│ Less: Vacancy & Credit Loss                                                  │
│   ├── Physical Vacancy                                                       │
│   ├── Free Rent (Concessions)                                                │
│   └── Bad Debt / Collection Loss                                             │
│ ──────────────────────────────────────────────────────────────────────────── │
│ EFFECTIVE GROSS INCOME (EGI)                                                 │
├──────────────────────────────────────────────────────────────────────────────┤
│ OPERATING EXPENSES                                                           │
│ ──────────────────────────────────────────────────────────────────────────── │
│ RECOVERABLE EXPENSES                                                         │
│   ├── CAM / Common Area Maintenance                                          │
│   │     ├── Management Fee                                                   │
│   │     ├── Utilities                                                        │
│   │     ├── Repairs & Maintenance                                            │
│   │     ├── Janitorial                                                       │
│   │     ├── Landscaping                                                      │
│   │     ├── Security                                                         │
│   │     └── General & Administrative                                         │
│   ├── Real Estate Taxes                                                      │
│   └── Insurance                                                              │
│                                                                              │
│ NON-RECOVERABLE EXPENSES                                                     │
│   ├── Management Fee (owner portion)                                         │
│   ├── Legal & Professional                                                   │
│   └── Marketing / Leasing                                                    │
│ ──────────────────────────────────────────────────────────────────────────── │
│ TOTAL OPERATING EXPENSES                                                     │
├──────────────────────────────────────────────────────────────────────────────┤
│ NET OPERATING INCOME (NOI)                                                   │
├──────────────────────────────────────────────────────────────────────────────┤
│ CAPITAL EXPENDITURES                                                         │
│ ──────────────────────────────────────────────────────────────────────────── │
│   ├── Tenant Improvements (TI)                                               │
│   ├── Leasing Commissions (LC)                                               │
│   ├── Capital Reserves                                                       │
│   └── Major Capital Projects                                                 │
│ ──────────────────────────────────────────────────────────────────────────── │
│ CASH FLOW BEFORE DEBT SERVICE (CFBDS)                                        │
├──────────────────────────────────────────────────────────────────────────────┤
│ DEBT SERVICE                                                                 │
│ ──────────────────────────────────────────────────────────────────────────── │
│   ├── Interest                                                               │
│   └── Principal Amortization                                                 │
│ ──────────────────────────────────────────────────────────────────────────── │
│ CASH FLOW AFTER DEBT SERVICE (CFADS)                                         │
├──────────────────────────────────────────────────────────────────────────────┤
│ REVERSION (Sale in Year N)                                                   │
│ ──────────────────────────────────────────────────────────────────────────── │
│   Sale Price (Year N+1 NOI / Exit Cap Rate)                                  │
│   Less: Selling Costs                                                        │
│   Less: Loan Payoff                                                          │
│ ──────────────────────────────────────────────────────────────────────────── │
│ NET SALE PROCEEDS                                                            │
└──────────────────────────────────────────────────────────────────────────────┘
```

### 3.2 Key Metrics & Calculations

#### Return Metrics

| Metric | Formula | Typical Target | Use Case |
|--------|---------|----------------|----------|
| **IRR (Levered)** | Discount rate where NPV = 0 (equity flows) | 15-25% | Primary return metric |
| **IRR (Unlevered)** | Discount rate where NPV = 0 (property flows) | 8-12% | Property-level return |
| **Equity Multiple** | Total distributions / Total equity invested | 1.8-2.5x | Absolute return measure |
| **Cash-on-Cash** | Annual CFADS / Equity invested | 6-10% | Current yield focus |
| **NPV** | PV(cash flows) - Initial investment | > $0 | Absolute value creation |

#### Valuation Metrics

| Metric | Formula | Typical Range | Notes |
|--------|---------|---------------|-------|
| **Cap Rate (Going-In)** | Year 1 NOI / Purchase Price | 4-8% | Market/risk indicator |
| **Cap Rate (Exit)** | Terminal NOI / Sale Price | Usually +25-50bps vs going-in | Conservatism assumption |
| **Price/SF** | Purchase Price / Net Rentable Area | Market-dependent | Quick comparability |
| **Price/Unit** | Purchase Price / # Units (MF) | Market-dependent | Multifamily metric |
| **GRM** | Purchase Price / Gross Annual Rent | 8-15x | Quick screen |

#### Operating Metrics

| Metric | Formula | Healthy Range | Red Flag |
|--------|---------|---------------|----------|
| **Occupancy (Physical)** | Occupied SF / Total SF | > 90% | < 80% |
| **Occupancy (Economic)** | Actual rent collected / Potential rent | > 88% | < 75% |
| **Operating Expense Ratio** | OpEx / EGI | 30-50% | > 55% |
| **NOI Margin** | NOI / EGI | 50-70% | < 45% |
| **CapEx Ratio** | CapEx / NOI | 10-20% | > 30% |
| **WALT** | Weighted Avg Lease Term (by income) | > 4 years | < 2 years |
| **Break-even Occupancy** | (OpEx + Debt Service) / GPR | < 80% | > 90% |

#### Debt Metrics

| Metric | Formula | Lender Requirement | Stress Test |
|--------|---------|-------------------|-------------|
| **LTV** | Loan Amount / Property Value | < 65-75% | > 80% |
| **DSCR** | NOI / Annual Debt Service | > 1.25x | < 1.10x |
| **Debt Yield** | NOI / Loan Amount | > 8-10% | < 7% |

### 3.3 Scenario Analysis Patterns

#### Standard Scenarios to Model

```
BASE CASE (50% probability weight)
├── Market rent growth: 2.5-3.0% annually
├── Expense growth: 2.5-3.0% annually  
├── Occupancy: Stabilized at 93-95%
├── Exit cap rate: +25bps vs going-in
└── Hold period: 5-7 years

UPSIDE CASE (25% probability weight)
├── Market rent growth: 4.0-5.0% annually
├── Expense growth: 2.0% annually (operating efficiencies)
├── Occupancy: 96-97%
├── Exit cap rate: flat to going-in
├── Accelerated lease-up
└── Value-add execution succeeds

DOWNSIDE CASE (25% probability weight)
├── Market rent growth: 0-1.0% annually
├── Expense growth: 3.5-4.0% annually
├── Occupancy: 85-88%
├── Exit cap rate: +75bps vs going-in
├── Major tenant loss
└── Extended hold period
```

#### Sensitivity Tables

**Two-Variable Sensitivity (IRR)**
```
                    Exit Cap Rate
                4.50%   4.75%   5.00%   5.25%   5.50%
          2.0%  22.1%   20.8%   19.6%   18.4%   17.3%
  Rent    2.5%  23.5%   22.1%   20.8%   19.6%   18.5%
  Growth  3.0%  24.9%   23.4%   22.0%   20.8%   19.6%
          3.5%  26.3%   24.7%   23.3%   21.9%   20.7%
          4.0%  27.7%   26.1%   24.5%   23.1%   21.8%
```

**Key Sensitivity Combinations:**
1. Exit Cap Rate vs. Rent Growth (most common)
2. Going-In Cap Rate vs. Exit Cap Rate
3. Occupancy vs. Rental Rate
4. LTV vs. Interest Rate
5. Hold Period vs. Exit Cap Rate

### 3.4 How Argus Works (And What to Replicate)

#### Argus Enterprise Core Modules

```
┌─────────────────────────────────────────────────────────────────┐
│                    ARGUS ENTERPRISE ARCHITECTURE                │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────────────────┐     ┌──────────────────────┐         │
│  │   LEASE ABSTRACTION  │     │    MARKET INPUTS     │         │
│  │   ─────────────────  │     │   ────────────────   │         │
│  │   • Tenant info      │     │   • Market rents     │         │
│  │   • Term dates       │     │   • Growth rates     │         │
│  │   • Base rent steps  │     │   • Vacancy factors  │         │
│  │   • Recoveries       │     │   • TI/LC costs      │         │
│  │   • Options          │     │   • Absorption       │         │
│  │   • Free rent        │     │   • Renewal prob     │         │
│  └──────────┬───────────┘     └──────────┬───────────┘         │
│             │                            │                      │
│             └───────────┬────────────────┘                      │
│                         ▼                                       │
│           ┌─────────────────────────┐                          │
│           │     CASH FLOW ENGINE    │                          │
│           │    ─────────────────    │                          │
│           │    • Month-by-month     │                          │
│           │    • Lease rollovers    │                          │
│           │    • Speculative leases │                          │
│           │    • Expense modeling   │                          │
│           │    • Capital events     │                          │
│           └───────────┬─────────────┘                          │
│                       ▼                                         │
│  ┌─────────────────────────────────────────────────────────┐   │
│  │                 VALUATION & ANALYSIS                     │   │
│  │  ───────────────────────────────────────────────────────│   │
│  │  • DCF Valuation          • Sensitivity analysis        │   │
│  │  • Direct cap valuation   • Scenario comparison         │   │
│  │  • Waterfall returns      • Partnership modeling        │   │
│  │  • Debt analysis          • Portfolio aggregation       │   │
│  └─────────────────────────────────────────────────────────┘   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

#### What Makes Argus Powerful (Features to Replicate)

1. **Lease-Level Granularity**
   - Every tenant modeled individually
   - Step rents, CPI adjustments, percentage rent
   - Option exercise probability modeling
   - Recovery clause complexity (base year, NNN, modified gross)

2. **Speculative Lease Assumptions**
   - Market rent absorption for vacant space
   - Renewal probability vs. new lease
   - Downtime between leases
   - TI/LC cost differentiation

3. **Recovery Calculation Engine**
   - Gross-up calculations
   - Base year stops
   - CAM caps and administrative fees
   - Tax reassessment modeling

4. **Reporting Suite**
   - Standard institutional reports
   - Customizable templates
   - Audit trail
   - Compare scenarios side-by-side

#### DealOS Advantage vs. Argus

| Argus Limitation | DealOS Opportunity |
|------------------|-------------------|
| Manual data entry | AI lease extraction |
| Static market assumptions | Real-time market data integration |
| Complex UI, steep learning curve | Natural language interface |
| $15-20K per seat annually | Included in platform |
| No collaboration | Real-time multi-user |
| Siloed from deal flow | Integrated with sourcing & DD |
| Reports only | Actionable insights & recommendations |

---

## 4. Investment Memo Structure

### 4.1 Standard IC Memo Sections

```
INVESTMENT MEMORANDUM
═══════════════════════════════════════════════════════════════

1. EXECUTIVE SUMMARY (1-2 pages)
   ├── Investment thesis (3-5 sentences)
   ├── Key metrics table
   ├── Risk/return profile
   └── Recommendation

2. PROPERTY OVERVIEW (2-3 pages)
   ├── Property description
   │     ├── Address & location
   │     ├── Building specifications
   │     ├── Site characteristics
   │     └── Photos/aerials
   ├── Tenancy summary
   │     ├── Rent roll summary
   │     ├── Major tenant profiles
   │     └── Lease expiration schedule
   └── Historical performance
         ├── Occupancy trend
         ├── Rent growth history
         └── NOI history

3. MARKET ANALYSIS (3-4 pages)
   ├── Metro overview
   │     ├── Economic drivers
   │     ├── Employment trends
   │     └── Population/demographics
   ├── Submarket analysis
   │     ├── Supply/demand dynamics
   │     ├── Competitive set
   │     └── Rent/vacancy trends
   ├── Comparable analysis
   │     ├── Sales comps
   │     └── Rent comps
   └── Market outlook

4. FINANCIAL ANALYSIS (4-6 pages)
   ├── Sources & uses
   ├── Operating assumptions
   │     ├── Revenue assumptions
   │     ├── Expense assumptions
   │     └── Capital assumptions
   ├── 10-year cash flow summary
   ├── Sensitivity analysis
   ├── Debt assumptions & terms
   └── Returns summary
         ├── Unlevered IRR/NPV
         ├── Levered IRR/NPV
         └── Cash-on-cash by year

5. BUSINESS PLAN (2-3 pages)
   ├── Value creation strategy
   ├── Operational improvements
   ├── Capital investment plan
   ├── Leasing strategy
   └── Exit strategy

6. RISK FACTORS (1-2 pages)
   ├── Market risks
   ├── Property-specific risks
   ├── Tenant risks
   ├── Execution risks
   └── Mitigants for each

7. RECOMMENDATION (1 page)
   ├── Go/No-Go recommendation
   ├── Key conditions
   ├── Bid guidance
   └── Next steps

APPENDICES
   ├── A: Detailed cash flow model
   ├── B: Rent roll
   ├── C: Lease abstracts
   ├── D: Market data
   ├── E: Photos
   └── F: Maps

═══════════════════════════════════════════════════════════════
```

### 4.2 What Investment Committees Want to See

#### The 5-Minute IC Test
```
IC members will form 80% of their opinion in the first 5 minutes.
They need to immediately understand:

1. WHAT are we buying? (30 seconds)
   └── Asset type, size, location, quality

2. WHY this asset? (60 seconds)
   └── Investment thesis in 3 bullet points

3. HOW do we make money? (60 seconds)
   └── Value creation strategy, clear and specific

4. WHAT are the risks? (90 seconds)
   └── Top 3 risks and how they're mitigated

5. WHAT are the returns? (60 seconds)
   └── IRR, multiple, cash yield - with conviction
```

#### IC Pet Peeves to Avoid

| Don't Do This | Do This Instead |
|---------------|-----------------|
| Bury the thesis | Lead with the "so what" |
| Show only upside | Present balanced view with mitigants |
| Use boilerplate market sections | Provide property-specific market insight |
| Model unrealistic rent growth | Anchor to comps and historicals |
| Ignore basis risk | Show price/SF vs. replacement cost |
| Present single scenario | Show base/up/down with probabilities |
| Use stale comps | Recent transactions, adjusted |
| Hand-wave execution risk | Detail the operational plan |

#### Key Metrics Every IC Wants Front and Center

```
┌────────────────────────────────────────────────────────────┐
│                 INVESTMENT SUMMARY                          │
├────────────────────────────────────────────────────────────┤
│                                                             │
│  Purchase Price:        $XX,XXX,XXX    Cap Rate:   X.XX%   │
│  Price/SF:              $XXX           Year 1 NOI: $X,XXX  │
│                                                             │
│  Equity Required:       $XX,XXX,XXX    LTV:        XX%     │
│  Loan Amount:           $XX,XXX,XXX    DSCR:       X.XXx   │
│                                                             │
├────────────────────────────────────────────────────────────┤
│                 RETURN METRICS (5-Year Hold)               │
├────────────────────────────────────────────────────────────┤
│                   Base Case    Upside    Downside          │
│  Levered IRR:       XX.X%      XX.X%      XX.X%           │
│  Equity Multiple:   X.XXx      X.XXx      X.XXx           │
│  Avg Cash Yield:    X.X%       X.X%       X.X%            │
│                                                             │
└────────────────────────────────────────────────────────────┘
```

---

## 5. Comp Analysis Methodology

### 5.1 Sales Comp Analysis

#### Finding Relevant Comps

**Criteria Hierarchy (in order of importance):**
1. **Property type** - Must match (office to office, retail to retail)
2. **Location** - Same submarket > same metro > similar metros
3. **Timing** - Within 12 months ideal, 24 months max
4. **Size** - Within 50% of subject (+/- in SF)
5. **Quality** - Same class (A, B, C) or adjacent
6. **Transaction type** - Arm's length sales only

**Data Sources for Comps:**
```
PRIMARY SOURCES (Verified, Detailed)
├── CoStar (industry standard, expensive)
├── Real Capital Analytics (institutional focus)
├── CBRE/JLL/Cushman research
└── County recorder (deeds, transfer taxes)

SECONDARY SOURCES (Requires Verification)
├── LoopNet (often asking prices, not closed)
├── Reonomy (property data aggregator)
├── News/press releases
└── Broker contacts

VERIFICATION METHODS
├── Cross-reference multiple sources
├── Calculate implied cap rate (sanity check)
├── Confirm arm's length nature
└── Adjust for portfolio premiums/discounts
```

#### Comp Adjustment Framework

```
SUBJECT PROPERTY: Downtown Office, 150,000 SF, Class A, 2015 Vintage

COMP 1: 123 Main Street
─────────────────────────────────────────────────────────────
Sale Price:         $52,500,000
Price/SF:           $350/SF
Cap Rate:           5.25%
Sale Date:          6 months ago
Size:               150,000 SF
Class:              A
Vintage:            2010

ADJUSTMENTS:
├── Location:       Same submarket          →  +0%
├── Size:           Same                    →  +0%
├── Quality:        Class A (same)          →  +0%
├── Age/Condition:  5 years older           →  -3%
├── Occupancy:      95% vs. subject 92%     →  -2%
├── Market Time:    6 mo. market movement   →  +2%
└── Other:          Corner lot premium      →  +1%
                                            ────────
                    NET ADJUSTMENT:         →  -2%

ADJUSTED PRICE/SF: $350 × (1 - 2%) = $343/SF
─────────────────────────────────────────────────────────────
```

#### Standard Adjustments by Factor

| Factor | Typical Range | How to Quantify |
|--------|---------------|-----------------|
| **Location** | ±10-30% | Submarket rent differential |
| **Size** | ±5-15% | Larger = slight discount |
| **Age/Condition** | ±5-20% | CapEx requirements |
| **Quality/Class** | ±10-25% | Rent premium differential |
| **Occupancy** | ±5-15% | Lease-up risk |
| **Lease Terms** | ±5-15% | WALT, tenant credit |
| **Time (market movement)** | ±2-5%/year | Index or cap rate trend |
| **Transaction Type** | ±5-10% | Portfolio discount, REO |

### 5.2 Rent Comp Analysis

#### Rent Comp Data Points to Capture

```
FOR EACH RENT COMP:
├── Property name & address
├── Tenant name (if disclosed)
├── Transaction date
├── Space size (SF)
├── Lease term (years)
├── Base rent ($/SF NNN or gross)
├── Rent structure (flat, steps, CPI)
├── Expense structure (NNN, MG, FSG)
├── Free rent (months)
├── TI allowance ($/SF)
├── Effective rent calculation
├── Renewal vs. new
└── Landlord/broker source
```

#### Effective Rent Calculation

```
EFFECTIVE RENT FORMULA:

                    (Total Base Rent) - (Free Rent Value) - (TI Cost) - (LC Cost)
Effective Rent =    ───────────────────────────────────────────────────────────────
                                        Lease Term in Months

EXAMPLE:
─────────────────────────────────────────────────────────────
Base Rent:          $30.00/SF NNN
Lease Term:         5 years (60 months)
Free Rent:          3 months
TI Allowance:       $50/SF
Leasing Commission: 6% of total rent

Space Size:         10,000 SF

CALCULATION:
Total Base Rent:    $30 × 10,000 SF × 5 years = $1,500,000
Free Rent Value:    $30 × 10,000 SF × 3 mo / 12 = $75,000
TI Cost:            $50 × 10,000 SF = $500,000
LC Cost:            6% × $1,500,000 = $90,000

Effective Rent:     ($1,500,000 - $75,000 - $500,000 - $90,000) / 60 months
                    = $835,000 / 60
                    = $13,917/month
                    = $16.70/SF/year effective (vs. $30 face)
─────────────────────────────────────────────────────────────
```

### 5.3 Data Sources Comparison

| Source | Cost | Coverage | Quality | Best For |
|--------|------|----------|---------|----------|
| **CoStar** | $$$$ | Excellent | High | Full analysis |
| **Real Capital Analytics** | $$$ | Institutional | Very High | Sales comps |
| **CompStak** | $$$ | Urban markets | High | Rent comps |
| **Yardi Matrix** | $$$ | Multifamily | High | MF rents |
| **REIS (Moody's)** | $$$ | Good | High | Market forecasts |
| **Reonomy** | $$ | Good | Medium | Property data |
| **LoopNet** | Free-$$ | Good | Low-Med | Listings/leads |
| **County Records** | Free | Complete | Raw | Verification |

---

## 6. Appraisal Requirements

### 6.1 Three Approaches to Value

#### Income Approach (Most Important for Investment Property)

```
INCOME APPROACH METHODS:

1. DIRECT CAPITALIZATION
   ────────────────────────────────────────────
   Value = Net Operating Income / Cap Rate
   
   When to Use:
   • Stabilized properties
   • Sufficient market cap rate data
   • Single-year analysis adequate
   
   Example:
   NOI = $1,000,000
   Cap Rate = 5.5%
   Value = $1,000,000 / 0.055 = $18,181,818

2. DISCOUNTED CASH FLOW (DCF)
   ────────────────────────────────────────────
   Value = Σ (Cash Flow_t / (1 + r)^t) + (Reversion / (1 + r)^n)
   
   When to Use:
   • Lease-up properties
   • Properties with complex lease structures
   • Value-add situations
   • Institutional requirements
   
   Key Inputs:
   • Holding period (typically 10 years)
   • Discount rate (typically 6-10%)
   • Terminal cap rate
   • Growth assumptions
```

#### Sales Comparison Approach

```
SALES COMPARISON PROCESS:

1. IDENTIFY COMPARABLE SALES
   ├── Similar property type
   ├── Similar size and quality
   ├── Recent transactions (< 24 months)
   └── Arm's length transactions

2. ANALYZE EACH COMPARABLE
   ├── Confirm sale details
   ├── Calculate price metrics
   └── Identify differences from subject

3. ADJUST COMPARABLES
   ├── Property rights conveyed
   ├── Financing terms
   ├── Conditions of sale
   ├── Market conditions (time)
   ├── Location
   ├── Physical characteristics
   └── Economic characteristics

4. RECONCILE TO VALUE INDICATION
   ├── Weight by comparability
   └── Narrow to supportable range
```

#### Cost Approach

```
COST APPROACH FORMULA:

Value = Land Value + Replacement Cost New - Depreciation

COMPONENTS:

1. LAND VALUE
   ├── Sales comparison (land sales)
   ├── Extraction from improved sales
   └── Allocation (% of improved value)

2. REPLACEMENT COST NEW (RCN)
   ├── Direct costs (construction)
   ├── Indirect costs (soft costs)
   └── Entrepreneurial profit (10-20%)

3. DEPRECIATION
   ├── Physical deterioration
   │     ├── Curable (deferred maintenance)
   │     └── Incurable (age-related)
   ├── Functional obsolescence
   │     ├── Curable (upgradeable)
   │     └── Incurable (layout, design)
   └── External obsolescence
         └── Always incurable (location, market)

WHEN COST APPROACH IS RELEVANT:
• New construction (minimal depreciation)
• Special-purpose properties
• Insurance purposes
• Limited income/sales data
```

### 6.2 USPAP Compliance Considerations

#### Uniform Standards of Professional Appraisal Practice

```
USPAP REQUIREMENTS FOR REAL PROPERTY (Standards 1 & 2):

STANDARD 1: Real Property Appraisal Development
─────────────────────────────────────────────────
• Identify the problem to be solved
• Determine scope of work
• Collect and verify data
• Analyze relevant data
• Apply appropriate approaches
• Reconcile to final value opinion

STANDARD 2: Real Property Appraisal Reporting
─────────────────────────────────────────────────
• Clearly communicate analysis
• Contain sufficient information
• Not be misleading
• Contain signed certification
• Include required disclosures

REPORT TYPES:
• Appraisal Report (detailed)
• Restricted Appraisal Report (limited distribution)
```

#### Key USPAP Concepts for AI Implementation

| Concept | Requirement | AI Implication |
|---------|-------------|----------------|
| **Independence** | Unbiased opinion | Cannot be influenced by desired outcome |
| **Competency** | Know the property type/market | Need specialized training data |
| **Scope of Work** | Appropriate for intended use | Must disclose limitations |
| **Certification** | Licensed appraiser signs | AI assists, human certifies |
| **Workfile** | Support for all conclusions | Full audit trail required |
| **Hypothetical Conditions** | Must be disclosed | Clear labeling in outputs |
| **Extraordinary Assumptions** | Must be disclosed | Explicit assumption tracking |

#### Regulatory Context

```
FIRREA REQUIREMENTS (for federally-related transactions):
─────────────────────────────────────────────────────────
• Transactions > $500,000 require full appraisal
• Must be performed by state-licensed/certified appraiser
• Must conform to USPAP
• Review appraisals for compliance

AVM GUIDANCE (OCC, FDIC, Federal Reserve):
─────────────────────────────────────────────────────────
• AVMs can support below-threshold transactions
• Must have model validation program
• Require human oversight and review
• Disclosure requirements for consumers

DEALOS POSITIONING:
─────────────────────────────────────────────────────────
Position as "appraisal support tool" not "appraisal replacement"
• Accelerates data gathering
• Validates comparable selection
• Performs calculations consistently
• Generates draft narratives
• Licensed appraiser reviews and signs
```

---

## 7. Domain Terminology Glossary

### Core Financial Terms

| Term | Definition | Formula/Example |
|------|------------|-----------------|
| **NOI** | Net Operating Income - revenue minus operating expenses before debt/capex | EGI - OpEx |
| **Cap Rate** | Capitalization Rate - yield measure for real estate | NOI / Value |
| **IRR** | Internal Rate of Return - discount rate where NPV = 0 | Solve for r where Σ CF/(1+r)^t = 0 |
| **NPV** | Net Present Value - present value of future cash flows minus investment | Σ CF/(1+r)^t - Initial Investment |
| **Cash-on-Cash** | Annual cash return on equity invested | Annual CFADS / Equity |
| **Equity Multiple** | Total return multiple on equity | Total Distributions / Equity |
| **DSCR** | Debt Service Coverage Ratio | NOI / Annual Debt Service |
| **LTV** | Loan-to-Value Ratio | Loan Amount / Property Value |
| **Debt Yield** | Lender return metric | NOI / Loan Amount |

### Lease & Occupancy Terms

| Term | Definition |
|------|------------|
| **NNN** | Triple Net - tenant pays taxes, insurance, CAM |
| **FSG** | Full Service Gross - landlord pays all expenses |
| **MG** | Modified Gross - shared expense responsibility |
| **CAM** | Common Area Maintenance expenses |
| **TI** | Tenant Improvements - buildout allowance |
| **LC** | Leasing Commissions |
| **Free Rent** | Rent abatement period |
| **WALT** | Weighted Average Lease Term |
| **NRA** | Net Rentable Area |
| **GLA** | Gross Leasable Area |
| **Load Factor** | Common area added to usable SF |
| **Base Year Stop** | Expense structure freezing base year expenses |
| **CPI Adjustment** | Rent increase tied to inflation index |
| **Percentage Rent** | Rent based on tenant sales (retail) |
| **Breakpoint** | Sales threshold for percentage rent |
| **Co-Tenancy** | Lease clause tied to other tenants |
| **Kickout** | Termination right based on performance |
| **ROFO/ROFR** | Right of First Offer/Refusal |
| **SNDA** | Subordination, Non-Disturbance, Attornment |
| **Estoppel** | Certificate confirming lease terms |

### Property & Market Terms

| Term | Definition |
|------|------------|
| **Basis** | Total invested capital in property |
| **Replacement Cost** | Cost to build new equivalent |
| **FAR** | Floor Area Ratio (density measure) |
| **Entitlements** | Approved development rights |
| **Phase I/II** | Environmental site assessments |
| **PCA** | Property Condition Assessment |
| **ALTA Survey** | Comprehensive property survey |
| **Title Exception** | Items excluded from title insurance |
| **Easement** | Right to use another's land |
| **Encumbrance** | Claim or restriction on property |
| **Going-In/Exit Cap** | Cap rates at acquisition/sale |
| **Stabilized** | Property at market occupancy |
| **Value-Add** | Strategy to increase value through improvements |
| **Core** | Stable, low-risk properties |
| **Core Plus** | Core with modest value-add |
| **Opportunistic** | High-risk, high-return strategies |

### Transaction Terms

| Term | Definition |
|------|------------|
| **LOI** | Letter of Intent |
| **PSA** | Purchase and Sale Agreement |
| **CA/NDA** | Confidentiality Agreement |
| **OM** | Offering Memorandum |
| **BOV** | Broker Opinion of Value |
| **DD** | Due Diligence |
| **Hard Money** | Non-refundable earnest money |
| **Day One Hard** | Earnest money hard at signing |
| **Inspection Period** | DD period with refund rights |
| **Closing Conditions** | Requirements to close |
| **Representations & Warranties** | Seller assurances |
| **Survival** | Period R&W remain enforceable post-close |

### Investment Structure Terms

| Term | Definition |
|------|------------|
| **GP/LP** | General Partner / Limited Partner |
| **Promote** | GP incentive above pro-rata share |
| **Waterfall** | Distribution priority structure |
| **Preferred Return** | Minimum return to LPs before promote |
| **Catch-Up** | GP share after pref before split |
| **Clawback** | Return of promote if returns fall short |
| **Capital Call** | Request for committed capital |
| **Co-Invest** | Side investment alongside fund |
| **Fund Level** | Returns across entire fund |
| **Asset Level** | Returns on individual property |

---

## 8. Expert Tips for AI Implementation

### 8.1 Data Extraction Priorities

```
HIGH VALUE AI EXTRACTION TARGETS:
─────────────────────────────────────────────────────────────
1. RENT ROLLS (Critical, Structured)
   ├── Tenant name normalization
   ├── Suite/unit mapping
   ├── Rent amount extraction
   ├── Lease dates (start, end, options)
   └── Expense responsibility classification
   
   WHY: Forms foundation of all analysis, currently manual entry

2. LEASE ABSTRACTS (Critical, Complex)
   ├── Base rent and escalations
   ├── Recovery provisions
   ├── Options (renewal, termination, expansion)
   ├── Co-tenancy and exclusives
   └── Assignment/subletting rights
   
   WHY: Errors here cascade through model; currently expensive legal review

3. OPERATING STATEMENTS (Critical, Semi-Structured)
   ├── Line item classification
   ├── Non-recurring identification
   ├── Normalization to standard chart of accounts
   └── YoY comparison flagging
   
   WHY: Garbage in/garbage out for underwriting

4. PROPERTY CONDITION REPORTS (Important, Structured)
   ├── Immediate repairs needed
   ├── CapEx reserve recommendations
   ├── System ages and conditions
   └── Code compliance issues
   
   WHY: Directly impacts CapEx assumptions and risk
```

### 8.2 Model Architecture Recommendations

```
RECOMMENDED APPROACH: Specialized Agents, Orchestrated

┌─────────────────────────────────────────────────────────────┐
│                    ORCHESTRATOR AGENT                        │
│                    (Deal Context Manager)                    │
│                                                              │
│   Maintains deal state, routes tasks, synthesizes output     │
└─────────────────────────────────────────────────────────────┘
            │           │           │           │
            ▼           ▼           ▼           ▼
      ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐
      │   DD    │ │ Modeling│ │ Research│ │  Memo   │
      │ Agent   │ │  Agent  │ │  Agent  │ │  Agent  │
      └─────────┘ └─────────┘ └─────────┘ └─────────┘
            │           │           │           │
            ▼           ▼           ▼           ▼
      ┌─────────────────────────────────────────────────┐
      │              SHARED DEAL DATA LAYER             │
      │   (Property, Leases, Financials, Market Data)   │
      └─────────────────────────────────────────────────┘

WHY THIS ARCHITECTURE:
• Specialized agents = better at specific tasks
• Shared data layer = consistency across outputs
• Orchestrator = maintains deal narrative
• Allows parallel processing
• Easier to improve individual components
```

### 8.3 Common Pitfalls to Avoid

| Pitfall | Problem | Solution |
|---------|---------|----------|
| **Over-trusting OCR** | Old docs have errors | Implement confidence scores, human verification triggers |
| **Generic market data** | Every deal looks the same | Property-specific comps, submarket granularity |
| **Black box valuations** | IC won't trust it | Show work, link to sources, explain reasoning |
| **Optimistic defaults** | Makes every deal look good | Conservative defaults, require override justification |
| **Ignoring seasonality** | Retail/hospitality mismodeled | Property-type specific patterns |
| **Static assumptions** | Miss lease-level detail | Model at tenant level, roll up |
| **Missing edge cases** | Blows up on complex leases | Extensive lease clause taxonomy |

### 8.4 Critical Success Factors

```
TO BEAT ARGUS, WE MUST:
─────────────────────────────────────────────────────────────
1. MATCH THEIR ACCURACY
   • Institutional-grade calculations
   • Audit trail for every number
   • Reconciliation to source docs
   
2. 10X THEIR SPEED
   • Minutes not hours for model setup
   • Automatic lease abstraction
   • Pre-populated market assumptions

3. REDUCE THEIR COMPLEXITY
   • Natural language interface
   • Sensible defaults
   • Explain calculations in plain English

4. EXCEED THEIR INTEGRATION
   • Connected to deal pipeline
   • Real-time market data
   • Output directly to IC memo

5. DEMOCRATIZE ACCESS
   • Not $15K/seat
   • No 3-day training requirement
   • Usable by analyst or principal
```

### 8.5 Quality Assurance Framework

```
AUTOMATED CHECKS TO IMPLEMENT:
─────────────────────────────────────────────────────────────
MATHEMATICAL CHECKS
├── NOI = EGI - OpEx (verify identity)
├── DSCR, LTV, Debt Yield consistency
├── IRR/NPV calculation verification
├── Cap rate implied from price/NOI
└── Year-over-year growth rate reasonableness

LOGICAL CHECKS
├── Lease end dates > lease start dates
├── Occupancy ≤ 100%
├── Expenses grow over time (inflation)
├── Rent roll SF = building SF
└── Recovery income ≤ recoverable expenses

MARKET CHECKS
├── Cap rate within market range (±100bps)
├── Rent/SF within submarket range (±20%)
├── Expense ratio within property type norm
├── Growth assumptions ≤ historical max
└── Exit cap rate ≥ going-in cap rate

RED FLAG ALERTS
├── Single tenant > 40% of income
├── Lease concentration in single year
├── Below-market major tenant rents
├── Unusual expense line items
└── Recent occupancy drop
```

### 8.6 Output Formats by Audience

```
FOR INVESTMENT COMMITTEE:
├── Executive summary (1 page)
├── Key metrics dashboard
├── Scenario comparison table
├── Risk matrix
└── Recommendation with conviction level

FOR DEAL TEAM:
├── Full cash flow model (Excel export)
├── Assumption documentation
├── Sensitivity tables
├── DD checklist status
└── Open items tracker

FOR LENDERS:
├── Argus-format output (XML export)
├── Rent roll with lease abstracts
├── Historical operating statements
├── Third-party report summaries
└── Sponsor track record

FOR LIMITED PARTNERS:
├── Investment summary
├── Return projections with scenarios
├── Comparable investments
├── Risk factors and mitigants
└── Manager terms summary
```

---

## Summary: What We're Building

```
THE FINANCIAL ANALYST LAYER = 5 Specialized AI Agents

1. DUE DILIGENCE AGENT
   Input:  Raw documents (PDFs, spreadsheets)
   Output: Structured DD findings, red flags, checklist
   
2. FINANCIAL MODELING AGENT
   Input:  Rent roll, assumptions, market data
   Output: Institutional-grade proforma, scenarios
   
3. INVESTMENT MEMO AGENT
   Input:  Deal data, analysis, research
   Output: IC-ready investment memorandum
   
4. RESEARCH & COMP AGENT
   Input:  Property details, market parameters
   Output: Sales comps, rent comps, market analysis
   
5. APPRAISAL AGENT
   Input:  Property data, comps, financials
   Output: Draft valuation with three approaches

COMBINED VALUE PROPOSITION:
─────────────────────────────────────────────────────────────
"What used to take a deal team 2 weeks now takes 2 hours."

From receiving an OM to producing an IC memo:
• Manual process: 40-80 hours
• DealOS process: 2-4 hours

That's 10-20x productivity improvement.
That's how we win.
```

---

## Next Steps for Engineering

1. **Start with rent roll extraction** - highest value, structured problem
2. **Build cash flow engine** - match Argus calculations exactly
3. **Create lease taxonomy** - handle edge cases in clause extraction
4. **Integrate market data** - need comp source strategy
5. **Design output templates** - institutional format standards

---

*Document prepared for morning review. Questions → Slack.*
