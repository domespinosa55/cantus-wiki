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
# Financial Analyst Layer: Technical Architecture

> **Author:** Technical Architect Agent  
> **Date:** 2026-01-26  
> **Status:** DRAFT — Ready for morning review  
> **Version:** 1.0

---

## Executive Summary

The Financial Analyst Layer is the **agentic intelligence core** of DealOS — a system of 5 specialized AI agents that automate the analytical work currently done by expensive human analysts and legacy software. This document provides implementation-ready architecture for building this layer on top of Clawdbot core.

**Key Design Principles:**
- **Composable agents** — Each agent is standalone but orchestrated for complex workflows
- **Clawdbot-native** — Built on existing runtime, not a parallel system
- **Local-first inference** — Minimize cloud costs, maximize speed for routine tasks
- **Domain-specific tooling** — CRE-optimized, not generic AI
- **Human-in-the-loop** — Automation with oversight, not replacement

---

## 1. System Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────────────────────────┐
│                              DEALOS CLIENT LAYER                                     │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐                 │
│  │   Web App   │  │ Mobile App  │  │   Slack/    │  │   Email     │                 │
│  │  (Next.js)  │  │   (React    │  │  Discord    │  │  Triggers   │                 │
│  │             │  │   Native)   │  │             │  │             │                 │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘                 │
│         │                │                │                │                        │
│         └────────────────┴────────────────┴────────────────┘                        │
│                                    │                                                 │
│                                    ▼                                                 │
├─────────────────────────────────────────────────────────────────────────────────────┤
│                              API GATEWAY                                             │
│                         (REST + WebSocket)                                           │
│                                                                                      │
│    ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌────────────┐                   │
│    │   Auth     │  │  Rate      │  │  Request   │  │   Audit    │                   │
│    │   Layer    │  │  Limiter   │  │  Router    │  │   Logger   │                   │
│    └────────────┘  └────────────┘  └────────────┘  └────────────┘                   │
│                                    │                                                 │
├────────────────────────────────────┼────────────────────────────────────────────────┤
│                                    ▼                                                 │
│    ╔═══════════════════════════════════════════════════════════════════════════╗    │
│    ║                    AGENT ORCHESTRATOR                                      ║    │
│    ║                    (Clawdbot Session Manager)                              ║    │
│    ║                                                                            ║    │
│    ║    ┌─────────────────────────────────────────────────────────────────┐    ║    │
│    ║    │                   WORKFLOW ENGINE                                │    ║    │
│    ║    │    • DAG execution    • State machine    • Retry/resume         │    ║    │
│    ║    │    • Parallel dispatch • Dependency resolution                   │    ║    │
│    ║    └─────────────────────────────────────────────────────────────────┘    ║    │
│    ║                              │                                             ║    │
│    ║              ┌───────────────┼───────────────┐                            ║    │
│    ║              ▼               ▼               ▼                            ║    │
│    ║    ┌─────────────┐  ┌─────────────┐  ┌─────────────┐                     ║    │
│    ║    │   Task      │  │   Agent     │  │   Result    │                     ║    │
│    ║    │   Queue     │  │   Registry  │  │   Cache     │                     ║    │
│    ║    │ (BullMQ)    │  │             │  │  (Redis)    │                     ║    │
│    ║    └─────────────┘  └─────────────┘  └─────────────┘                     ║    │
│    ╚═══════════════════════════════════════════════════════════════════════════╝    │
│                                    │                                                 │
├────────────────────────────────────┼────────────────────────────────────────────────┤
│                                    ▼                                                 │
│    ╔═════════════════════════════════════════════════════════════════════════════╗  │
│    ║                         AGENT POOL                                           ║  │
│    ║                                                                              ║  │
│    ║  ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐                ║  │
│    ║  │ DUE DILIGENCE   │ │ FINANCIAL       │ │ INVESTMENT      │                ║  │
│    ║  │ AGENT           │ │ MODELING AGENT  │ │ MEMO AGENT      │                ║  │
│    ║  │                 │ │                 │ │                 │                ║  │
│    ║  │ • Doc parsing   │ │ • Proforma gen  │ │ • Summary gen   │                ║  │
│    ║  │ • Risk flagging │ │ • IRR/NPV calc  │ │ • Risk analysis │                ║  │
│    ║  │ • Checklist mgmt│ │ • Scenarios     │ │ • Rec synthesis │                ║  │
│    ║  │ • Entity extract│ │ • Sensitivity   │ │ • Template fill │                ║  │
│    ║  └────────┬────────┘ └────────┬────────┘ └────────┬────────┘                ║  │
│    ║           │                   │                   │                          ║  │
│    ║  ┌────────┴──────────────┐ ┌──┴──────────────────┐                          ║  │
│    ║  │ RESEARCH & COMP       │ │ APPRAISAL           │                          ║  │
│    ║  │ AGENT                 │ │ AGENT               │                          ║  │
│    ║  │                       │ │                     │                          ║  │
│    ║  │ • Market data fetch   │ │ • AVM engine        │                          ║  │
│    ║  │ • Comp identification │ │ • Income approach   │                          ║  │
│    ║  │ • Rent studies        │ │ • Sales comparison  │                          ║  │
│    ║  │ • Submarket analysis  │ │ • Cost approach     │                          ║  │
│    ║  │ • Trend detection     │ │ • USPAP compliance  │                          ║  │
│    ║  └───────────────────────┘ └─────────────────────┘                          ║  │
│    ╚═════════════════════════════════════════════════════════════════════════════╝  │
│                                    │                                                 │
├────────────────────────────────────┼────────────────────────────────────────────────┤
│                                    ▼                                                 │
│    ╔═════════════════════════════════════════════════════════════════════════════╗  │
│    ║                         SHARED SERVICES                                      ║  │
│    ║                                                                              ║  │
│    ║  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐         ║  │
│    ║  │ Document    │  │ Calculation │  │ Template    │  │ Data        │         ║  │
│    ║  │ Processor   │  │ Engine      │  │ Renderer    │  │ Enrichment  │         ║  │
│    ║  │             │  │             │  │             │  │             │         ║  │
│    ║  │ • PDF parse │  │ • DCF/IRR   │  │ • Markdown  │  │ • Geocoding │         ║  │
│    ║  │ • OCR       │  │ • NPV       │  │ • Excel gen │  │ • Demo data │         ║  │
│    ║  │ • Table ext │  │ • Amort     │  │ • PDF gen   │  │ • Census    │         ║  │
│    ║  │ • Schema    │  │ • Cap rate  │  │ • DOCX gen  │  │ • Economics │         ║  │
│    ║  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘         ║  │
│    ╚═════════════════════════════════════════════════════════════════════════════╝  │
│                                    │                                                 │
├────────────────────────────────────┼────────────────────────────────────────────────┤
│                                    ▼                                                 │
│    ╔═════════════════════════════════════════════════════════════════════════════╗  │
│    ║                         LLM ROUTING LAYER                                    ║  │
│    ║                         (Clawdbot LLM Router)                                ║  │
│    ║                                                                              ║  │
│    ║    ┌─────────────────────────────────────────────────────────────────┐      ║  │
│    ║    │                    MODEL SELECTOR                                │      ║  │
│    ║    │    Task → Complexity → Cost → Model                              │      ║  │
│    ║    └─────────────────────────────────────────────────────────────────┘      ║  │
│    ║                              │                                               ║  │
│    ║          ┌───────────────────┼───────────────────┐                          ║  │
│    ║          ▼                   ▼                   ▼                          ║  │
│    ║    ┌───────────┐      ┌───────────┐      ┌───────────┐                     ║  │
│    ║    │  LOCAL    │      │  CLOUD    │      │  CLOUD    │                     ║  │
│    ║    │  (Ollama) │      │ (Anthropic│      │ (OpenAI)  │                     ║  │
│    ║    │           │      │  Claude)  │      │           │                     ║  │
│    ║    │ • Llama3  │      │ • Claude  │      │ • GPT-5.2 │                     ║  │
│    ║    │ • Mistral │      │   Opus    │      │   Pro     │                     ║  │
│    ║    │ • Qwen    │      │ • Sonnet  │      │ • Codex   │                     ║  │
│    ║    └───────────┘      └───────────┘      └───────────┘                     ║  │
│    ╚═════════════════════════════════════════════════════════════════════════════╝  │
│                                                                                      │
├──────────────────────────────────────────────────────────────────────────────────────┤
│                              DATA LAYER                                              │
│                                                                                      │
│    ┌───────────────┐  ┌───────────────┐  ┌───────────────┐  ┌───────────────┐      │
│    │   Supabase    │  │    Redis      │  │  S3/R2       │  │  Vector DB    │      │
│    │   (Postgres)  │  │   (Cache +    │  │  (Documents) │  │  (Embeddings) │      │
│    │               │  │    Queue)     │  │              │  │               │      │
│    │ • Deals       │  │ • Sessions    │  │ • PDFs       │  │ • Document    │      │
│    │ • Properties  │  │ • Results     │  │ • Reports    │  │   chunks      │      │
│    │ • Analyses    │  │ • Locks       │  │ • Images     │  │ • Property    │      │
│    │ • Comps       │  │ • Pub/Sub     │  │ • Templates  │  │   vectors     │      │
│    └───────────────┘  └───────────────┘  └───────────────┘  └───────────────┘      │
│                                                                                      │
├──────────────────────────────────────────────────────────────────────────────────────┤
│                              EXTERNAL DATA SOURCES                                   │
│                                                                                      │
│    ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐ ┌───────────┐          │
│    │  County   │ │  Census   │ │  FRED     │ │  Google   │ │  News     │          │
│    │  Records  │ │  Bureau   │ │  Economic │ │  Maps     │ │  APIs     │          │
│    └───────────┘ └───────────┘ └───────────┘ └───────────┘ └───────────┘          │
│                                                                                      │
└──────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Agent Orchestration Design

### 2.1 Agent Communication Model

Agents communicate through a **shared context** model with explicit message passing:

```
┌──────────────────────────────────────────────────────────────────────────┐
│                         DEAL ANALYSIS CONTEXT                             │
│                                                                           │
│    deal_id: "deal_abc123"                                                 │
│    property: { address, type, sf, units, ... }                           │
│    documents: [ { id, type, parsed_at, content }, ... ]                  │
│    analyses: {                                                            │
│        due_diligence: { status, findings, risks, ... },                  │
│        financial_model: { status, proforma, scenarios, ... },            │
│        comps: { status, sales_comps, rent_comps, ... },                  │
│        valuation: { status, avm_value, approaches, ... },                │
│        memo: { status, draft, sections, ... }                            │
│    }                                                                      │
│    workflow_state: "analysis_in_progress"                                │
│    messages: [ { from, to, type, payload, timestamp }, ... ]             │
│                                                                           │
└──────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Workflow Patterns

**Pattern A: Full Deal Analysis (Sequential with Parallel Branches)**

```
                                START
                                  │
                                  ▼
                    ┌─────────────────────────────┐
                    │    DOCUMENT INGESTION       │
                    │    (Upload + Parse)         │
                    └─────────────┬───────────────┘
                                  │
                                  ▼
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
    ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
    │ DUE DILIGENCE   │ │ RESEARCH &      │ │ FINANCIAL       │
    │ AGENT           │ │ COMP AGENT      │ │ MODELING AGENT  │
    │ (doc review)    │ │ (market data)   │ │ (base proforma) │
    └────────┬────────┘ └────────┬────────┘ └────────┬────────┘
             │                   │                   │
             │                   ▼                   │
             │         ┌─────────────────┐          │
             │         │ APPRAISAL       │          │
             │         │ AGENT           │◄─────────┘
             │         │ (needs comps +   │
             │         │  financials)     │
             │         └────────┬────────┘
             │                  │
             └────────┬─────────┘
                      │
                      ▼
            ┌─────────────────┐
            │ INVESTMENT      │
            │ MEMO AGENT      │
            │ (synthesizes    │
            │  all inputs)    │
            └────────┬────────┘
                     │
                     ▼
                 COMPLETE
```

**Pattern B: Quick Valuation (Minimal Path)**

```
START → Research Agent → Appraisal Agent → COMPLETE
        (comps only)     (AVM only)        (~2 min)
```

**Pattern C: Diligence Focus**

```
START → Doc Ingestion → Due Diligence Agent → Investment Memo Agent → COMPLETE
                        (deep review)         (DD summary only)
```

### 2.3 Agent State Machine

Each agent follows a consistent lifecycle:

```
                         ┌─────────┐
                         │ PENDING │ (task queued)
                         └────┬────┘
                              │ assign
                              ▼
                         ┌─────────┐
               ┌────────►│ RUNNING │◄────────┐
               │         └────┬────┘         │
               │              │              │
          wait_for       complete       needs_input
               │              │              │
               ▼              ▼              ▼
         ┌─────────┐   ┌─────────┐   ┌─────────┐
         │ WAITING │   │ SUCCESS │   │ BLOCKED │
         │ (deps)  │   └─────────┘   │ (human) │
         └────┬────┘                 └────┬────┘
              │                           │
              └───────────────────────────┘
                           │
                      retry/resume
```

### 2.4 Inter-Agent Messaging Protocol

```typescript
interface AgentMessage {
  id: string;
  from: AgentType;
  to: AgentType | 'orchestrator' | 'human';
  type: 'request' | 'response' | 'event' | 'escalation';
  payload: {
    action?: string;
    data?: any;
    question?: string;
    priority?: 'low' | 'normal' | 'high' | 'critical';
  };
  correlationId?: string;  // links request/response
  timestamp: number;
}

// Example: Research Agent → Appraisal Agent
{
  "id": "msg_001",
  "from": "research_agent",
  "to": "appraisal_agent",
  "type": "event",
  "payload": {
    "action": "comps_ready",
    "data": {
      "sales_comps": [...],
      "rent_comps": [...],
      "confidence": 0.85
    }
  },
  "correlationId": "deal_abc123",
  "timestamp": 1737877200000
}
```

### 2.5 Orchestrator Logic

```typescript
class DealAnalysisOrchestrator {
  
  async runFullAnalysis(dealId: string, options: AnalysisOptions) {
    const context = await this.initializeContext(dealId);
    
    // Phase 1: Document ingestion (always first)
    await this.ingestDocuments(context);
    
    // Phase 2: Parallel independent analyses
    const parallelTasks = await Promise.all([
      this.dispatch('due_diligence_agent', 'analyze_documents', context),
      this.dispatch('research_agent', 'gather_comps', context),
      this.dispatch('financial_modeling_agent', 'build_base_proforma', context),
    ]);
    
    // Phase 3: Appraisal (needs comps + financials)
    await this.waitForDependencies(['research_agent', 'financial_modeling_agent']);
    await this.dispatch('appraisal_agent', 'generate_valuation', context);
    
    // Phase 4: Synthesis
    await this.waitForAll();
    await this.dispatch('investment_memo_agent', 'synthesize_memo', context);
    
    return context.getResults();
  }
  
  private async dispatch(agent: AgentType, task: string, context: DealContext) {
    const job = await this.queue.add({
      agent,
      task,
      contextId: context.id,
      priority: this.calculatePriority(task),
    });
    
    return job;
  }
}
```

---

## 3. Data Flow

### 3.1 Input Sources

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              INPUTS                                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  DOCUMENTS (User Upload)         PROPERTY DATA (System)                 │
│  ────────────────────────        ─────────────────────                  │
│  • Offering memorandum           • Address / APN                        │
│  • Rent rolls                    • Property type                        │
│  • T12/T3 financials            • Building SF                          │
│  • Lease abstracts               • Unit count                           │
│  • Purchase agreements           • Year built                           │
│  • Environmental reports         • Lot size                             │
│  • Title reports                 • Zoning                               │
│  • Appraisals                                                           │
│  • Survey / site plans                                                   │
│                                                                          │
│  MARKET DATA (Fetched)           USER INPUT (Optional)                  │
│  ────────────────────            ────────────────────                   │
│  • Comparable sales              • Purchase price                       │
│  • Comparable rents              • Target returns                       │
│  • Economic indicators           • Hold period                          │
│  • Demographics                  • Financing terms                      │
│  • Employment data               • Custom assumptions                   │
│  • Permit activity                                                       │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

### 3.2 Processing Pipeline

```
┌─────────────────────────────────────────────────────────────────────────┐
│                           PROCESSING                                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  STAGE 1: INGESTION                                                     │
│  ───────────────────                                                    │
│  Documents → PDF Parser → OCR → Table Extraction → Schema Mapping       │
│                    ↓                                                     │
│            Text Chunks → Embeddings → Vector Store                      │
│                                                                          │
│  STAGE 2: EXTRACTION                                                    │
│  ────────────────────                                                   │
│  • Entity extraction (tenants, terms, amounts)                          │
│  • Financial parsing (rent rolls → structured data)                     │
│  • Date/term extraction (lease expirations)                             │
│  • Risk phrase detection ("environmental", "litigation")                │
│                                                                          │
│  STAGE 3: ANALYSIS                                                      │
│  ────────────────────                                                   │
│  • Per-agent analysis (see Agent Pool)                                  │
│  • Cross-reference validation                                           │
│  • Confidence scoring                                                    │
│  • Anomaly detection                                                     │
│                                                                          │
│  STAGE 4: SYNTHESIS                                                     │
│  ────────────────────                                                   │
│  • Result aggregation                                                    │
│  • Narrative generation                                                  │
│  • Report formatting                                                     │
│  • Human review flagging                                                 │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

### 3.3 Output Products

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              OUTPUTS                                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  STRUCTURED DATA                 DOCUMENTS                              │
│  ───────────────                 ─────────                              │
│  • deal_analysis (JSON)          • Investment memo (PDF/DOCX)           │
│  • financial_model (JSON)        • Proforma (Excel)                     │
│  • risk_assessment (JSON)        • Valuation report (PDF)               │
│  • valuation_result (JSON)       • Comp analysis (PDF)                  │
│  • comp_set (JSON)               • DD checklist (PDF)                   │
│                                                                          │
│  METRICS                         NOTIFICATIONS                          │
│  ───────                         ─────────────                          │
│  • Confidence scores             • Analysis complete                    │
│  • Risk ratings                  • Human review needed                  │
│  • Valuation range               • Risk flags triggered                 │
│  • IRR/equity multiple           • Anomalies detected                   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Integration Points with DealOS/Clawdbot

### 4.1 Clawdbot Core Integration

```typescript
// Financial Analyst Layer registers as a Clawdbot skill
// Located at: /root/clawd/skills/financial-analyst/

export const financialAnalystSkill: ClawdbotSkill = {
  name: 'financial-analyst',
  version: '1.0.0',
  
  // Tools exposed to main agent
  tools: [
    {
      name: 'analyze_deal',
      description: 'Run full financial analysis on a deal',
      parameters: {
        deal_id: { type: 'string', required: true },
        analysis_type: { 
          type: 'enum', 
          values: ['full', 'quick_val', 'dd_only', 'memo_only'],
          default: 'full'
        },
      },
      handler: async (params, context) => {
        const orchestrator = new DealAnalysisOrchestrator();
        return orchestrator.runAnalysis(params.deal_id, params.analysis_type);
      }
    },
    {
      name: 'get_comps',
      description: 'Find comparable properties for a subject',
      parameters: {
        property: { type: 'object', required: true },
        comp_type: { type: 'enum', values: ['sales', 'rent', 'both'] },
        radius_miles: { type: 'number', default: 3 },
      },
      handler: async (params, context) => {
        const researchAgent = new ResearchAgent();
        return researchAgent.findComps(params);
      }
    },
    {
      name: 'generate_proforma',
      description: 'Generate financial proforma for a property',
      parameters: { /* ... */ },
      handler: async (params, context) => { /* ... */ }
    },
    {
      name: 'value_property',
      description: 'Generate automated valuation',
      parameters: { /* ... */ },
      handler: async (params, context) => { /* ... */ }
    },
  ],
  
  // Sub-agents spawnable by orchestrator
  agents: [
    'due-diligence',
    'financial-modeling', 
    'investment-memo',
    'research-comp',
    'appraisal',
  ],
};
```

### 4.2 DealOS Database Integration

```sql
-- Extend existing DealOS schema (assumed structure)

-- Link analysis to deals
ALTER TABLE deals ADD COLUMN analysis_id UUID REFERENCES deal_analyses(id);
ALTER TABLE deals ADD COLUMN analysis_status VARCHAR(50);

-- Analysis results accessible from deal view
CREATE VIEW deal_with_analysis AS
SELECT 
  d.*,
  da.status as analysis_status,
  da.valuation_low,
  da.valuation_mid,
  da.valuation_high,
  da.risk_score,
  da.irr_leveraged,
  da.equity_multiple,
  da.memo_url
FROM deals d
LEFT JOIN deal_analyses da ON d.analysis_id = da.id;
```

### 4.3 Event Integration

```typescript
// DealOS events trigger analysis workflows

// When new deal created
eventBus.on('deal.created', async (deal) => {
  if (deal.auto_analyze) {
    await financialAnalyst.analyze_deal({
      deal_id: deal.id,
      analysis_type: 'quick_val'  // Start with quick assessment
    });
  }
});

// When documents uploaded
eventBus.on('deal.documents.uploaded', async (event) => {
  await financialAnalyst.process_documents({
    deal_id: event.deal_id,
    document_ids: event.document_ids
  });
});

// When analysis completes
eventBus.on('analysis.completed', async (analysis) => {
  // Update deal record
  await supabase.from('deals')
    .update({ 
      analysis_status: 'complete',
      analysis_summary: analysis.summary 
    })
    .eq('id', analysis.deal_id);
    
  // Notify user
  await notify(analysis.user_id, {
    type: 'analysis_complete',
    deal_id: analysis.deal_id,
    summary: analysis.summary
  });
});
```

### 4.4 API Mount Points

```
DealOS API                     Financial Analyst API
───────────                    ─────────────────────
/api/deals/:id        ────►    /api/deals/:id/analysis
/api/deals/:id/docs   ────►    /api/deals/:id/analysis/documents
/api/properties/:id   ────►    /api/properties/:id/valuation
                               /api/properties/:id/comps
```

---

## 5. LLM Strategy

### 5.1 Model Selection Matrix

| Task | Complexity | Latency Req | Model | Location | Cost |
|------|------------|-------------|-------|----------|------|
| Document classification | Low | Low | Llama 3.2 8B | Local | ~$0 |
| Entity extraction | Medium | Medium | Llama 3.2 70B | Local | ~$0 |
| Table parsing | Medium | Medium | Qwen 2.5 72B | Local | ~$0 |
| Risk phrase detection | Low | Low | Llama 3.2 8B | Local | ~$0 |
| Financial narrative | High | Medium | Claude Sonnet | Cloud | ~$0.003/1K |
| Proforma generation | High | Low | Claude Sonnet | Cloud | ~$0.003/1K |
| Memo writing | Very High | Low | Claude Opus | Cloud | ~$0.015/1K |
| Complex reasoning | Very High | Low | GPT-5.2 Pro | Cloud | ~$0.010/1K |
| Valuation synthesis | High | Medium | Claude Sonnet | Cloud | ~$0.003/1K |
| Quick Q&A | Medium | High | Llama 3.2 8B | Local | ~$0 |

### 5.2 Routing Logic

```typescript
class LLMRouter {
  
  selectModel(task: TaskType, context: TaskContext): ModelConfig {
    
    // Priority 1: User preference override
    if (context.user?.preferredModel) {
      return this.getModel(context.user.preferredModel);
    }
    
    // Priority 2: Task-specific routing
    const taskRouting: Record<TaskType, ModelConfig> = {
      // Local inference (free, fast)
      'document_classify': { model: 'llama3.2:8b', location: 'local' },
      'entity_extract': { model: 'llama3.2:70b', location: 'local' },
      'table_parse': { model: 'qwen2.5:72b', location: 'local' },
      'risk_detect': { model: 'llama3.2:8b', location: 'local' },
      'quick_qa': { model: 'llama3.2:8b', location: 'local' },
      
      // Cloud inference (quality, expensive)
      'financial_narrative': { model: 'claude-sonnet-4', location: 'cloud' },
      'proforma_generate': { model: 'claude-sonnet-4', location: 'cloud' },
      'memo_write': { model: 'claude-opus-4', location: 'cloud' },
      'valuation_synthesize': { model: 'claude-sonnet-4', location: 'cloud' },
      
      // Escalation (hardest problems)
      'complex_reasoning': { model: 'gpt-5.2-pro', location: 'cloud' },
    };
    
    return taskRouting[task] || { model: 'claude-sonnet-4', location: 'cloud' };
  }
  
  async invoke(task: TaskType, prompt: string, context: TaskContext) {
    const config = this.selectModel(task, context);
    
    if (config.location === 'local') {
      return this.invokeOllama(config.model, prompt);
    } else {
      return this.invokeCloud(config.model, prompt);
    }
  }
}
```

### 5.3 Local Inference Setup (harlan-desktop)

```yaml
# Ollama models to pre-pull on harlan-desktop (RTX 4070 Super, 12GB VRAM)

models:
  primary:
    - llama3.2:8b      # Fast, general purpose (fits in VRAM)
    - qwen2.5:7b       # Good at tables/structured (fits in VRAM)
    
  offload_to_ram:
    - llama3.2:70b     # Heavy lifting, 4-bit quantized (~40GB RAM needed)
    - qwen2.5:72b      # Tables/code, 4-bit quantized (~40GB RAM needed)
    
# Note: 70B+ models will use GPU+CPU offloading
# Expect ~5-10 tok/sec for 70B vs ~50 tok/sec for 8B
```

### 5.4 Cost Management

```typescript
// Monthly budget allocation
const LLM_BUDGET = {
  monthly_cap: 500,  // $500/month
  per_analysis_cap: 2.00,  // Max $2 per deal analysis
  
  alerts: {
    warning: 0.75,  // Alert at 75% of budget
    critical: 0.90, // Pause non-essential at 90%
  }
};

// Track usage
class CostTracker {
  async trackUsage(model: string, tokens: number, cost: number) {
    await supabase.from('llm_usage').insert({
      model,
      tokens_in: tokens.input,
      tokens_out: tokens.output,
      cost,
      timestamp: new Date(),
    });
  }
  
  async getMonthlySpend(): Promise<number> {
    const { data } = await supabase
      .from('llm_usage')
      .select('cost')
      .gte('timestamp', startOfMonth());
    return data.reduce((sum, r) => sum + r.cost, 0);
  }
}
```

---

## 6. Database Schema Additions

```sql
-- ============================================
-- FINANCIAL ANALYST LAYER SCHEMA
-- ============================================

-- Core analysis record
CREATE TABLE deal_analyses (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    deal_id UUID NOT NULL REFERENCES deals(id) ON DELETE CASCADE,
    user_id UUID NOT NULL REFERENCES users(id),
    
    -- Status tracking
    status VARCHAR(50) NOT NULL DEFAULT 'pending',
    workflow_type VARCHAR(50) NOT NULL DEFAULT 'full',
    started_at TIMESTAMPTZ,
    completed_at TIMESTAMPTZ,
    
    -- Summary results (denormalized for fast access)
    valuation_low NUMERIC(15,2),
    valuation_mid NUMERIC(15,2),
    valuation_high NUMERIC(15,2),
    risk_score INTEGER CHECK (risk_score BETWEEN 0 AND 100),
    confidence_score DECIMAL(3,2),
    
    -- Financial metrics
    irr_unlevered DECIMAL(5,2),
    irr_levered DECIMAL(5,2),
    equity_multiple DECIMAL(4,2),
    cash_on_cash_y1 DECIMAL(5,2),
    
    -- Output references
    memo_document_id UUID REFERENCES documents(id),
    proforma_document_id UUID REFERENCES documents(id),
    
    -- Metadata
    created_at TIMESTAMPTZ DEFAULT NOW(),
    updated_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_deal_analyses_deal ON deal_analyses(deal_id);
CREATE INDEX idx_deal_analyses_status ON deal_analyses(status);

-- Per-agent task tracking
CREATE TABLE analysis_tasks (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    
    agent_type VARCHAR(50) NOT NULL,
    task_name VARCHAR(100) NOT NULL,
    status VARCHAR(50) NOT NULL DEFAULT 'pending',
    
    -- Execution details
    started_at TIMESTAMPTZ,
    completed_at TIMESTAMPTZ,
    duration_ms INTEGER,
    retry_count INTEGER DEFAULT 0,
    
    -- Results (JSONB for flexibility)
    input_params JSONB,
    output_result JSONB,
    error_message TEXT,
    
    -- Cost tracking
    llm_tokens_used INTEGER,
    llm_cost_cents INTEGER,
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_analysis_tasks_analysis ON analysis_tasks(analysis_id);
CREATE INDEX idx_analysis_tasks_agent ON analysis_tasks(agent_type);

-- Due diligence findings
CREATE TABLE dd_findings (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    
    category VARCHAR(100) NOT NULL, -- 'environmental', 'title', 'lease', 'financial'
    severity VARCHAR(20) NOT NULL,  -- 'info', 'warning', 'critical'
    
    title VARCHAR(500) NOT NULL,
    description TEXT,
    source_document_id UUID REFERENCES documents(id),
    source_page INTEGER,
    source_excerpt TEXT,
    
    -- AI confidence
    confidence DECIMAL(3,2),
    requires_human_review BOOLEAN DEFAULT FALSE,
    
    -- Human review
    reviewed_by UUID REFERENCES users(id),
    reviewed_at TIMESTAMPTZ,
    review_notes TEXT,
    is_valid BOOLEAN,  -- NULL = not reviewed, TRUE = confirmed, FALSE = false positive
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_dd_findings_analysis ON dd_findings(analysis_id);
CREATE INDEX idx_dd_findings_severity ON dd_findings(severity);

-- Comparable properties
CREATE TABLE comp_properties (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    
    -- Location
    address VARCHAR(500) NOT NULL,
    city VARCHAR(100),
    state VARCHAR(50),
    zip VARCHAR(20),
    latitude DECIMAL(10,8),
    longitude DECIMAL(11,8),
    
    -- Property characteristics
    property_type VARCHAR(50),
    subtype VARCHAR(50),
    year_built INTEGER,
    gross_sf INTEGER,
    rentable_sf INTEGER,
    units INTEGER,
    stories INTEGER,
    lot_size_sf INTEGER,
    
    -- Transaction data (for sales comps)
    sale_date DATE,
    sale_price NUMERIC(15,2),
    price_per_sf NUMERIC(10,2),
    cap_rate DECIMAL(5,2),
    
    -- Rental data (for rent comps)
    asking_rent_psf NUMERIC(8,2),
    effective_rent_psf NUMERIC(8,2),
    occupancy DECIMAL(5,2),
    
    -- Source tracking
    data_source VARCHAR(100), -- 'county', 'costar', 'manual', 'scraped'
    source_url TEXT,
    last_updated TIMESTAMPTZ,
    
    -- Quality
    data_quality_score INTEGER CHECK (data_quality_score BETWEEN 0 AND 100),
    
    created_at TIMESTAMPTZ DEFAULT NOW(),
    updated_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_comp_properties_location ON comp_properties USING GIST (
    ll_to_earth(latitude, longitude)
);
CREATE INDEX idx_comp_properties_type ON comp_properties(property_type);
CREATE INDEX idx_comp_properties_sale_date ON comp_properties(sale_date);

-- Link comps to analyses
CREATE TABLE analysis_comps (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    comp_id UUID NOT NULL REFERENCES comp_properties(id),
    
    comp_type VARCHAR(20) NOT NULL, -- 'sale', 'rent'
    relevance_score DECIMAL(3,2),
    distance_miles DECIMAL(5,2),
    
    -- Adjustments applied
    adjustments JSONB, -- { "age": -0.05, "size": 0.02, "location": 0.03 }
    adjusted_value NUMERIC(15,2),
    
    -- Selection reasoning
    selection_reason TEXT,
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_analysis_comps_analysis ON analysis_comps(analysis_id);

-- Financial models / proformas
CREATE TABLE financial_models (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    
    model_type VARCHAR(50) NOT NULL, -- 'acquisition', 'development', 'refinance'
    scenario_name VARCHAR(100) DEFAULT 'base',
    
    -- Key assumptions (stored for reproducibility)
    assumptions JSONB NOT NULL,
    /*
    {
      "purchase_price": 10000000,
      "closing_costs_pct": 0.02,
      "hold_period_years": 5,
      "exit_cap_rate": 0.065,
      "rent_growth_annual": 0.03,
      "expense_growth_annual": 0.025,
      "vacancy_rate": 0.05,
      "ltv": 0.65,
      "interest_rate": 0.065,
      "loan_term_years": 10,
      "amortization_years": 30
    }
    */
    
    -- Summary metrics
    metrics JSONB NOT NULL,
    /*
    {
      "irr_unlevered": 0.082,
      "irr_levered": 0.142,
      "equity_multiple": 1.85,
      "cash_on_cash_y1": 0.065,
      "noi_y1": 650000,
      "debt_service_coverage": 1.45
    }
    */
    
    -- Detailed cash flows (year-by-year)
    cash_flows JSONB NOT NULL,
    /*
    {
      "years": [
        { "year": 1, "revenue": 800000, "expenses": 150000, "noi": 650000, ... },
        ...
      ]
    }
    */
    
    -- Generated Excel file
    excel_document_id UUID REFERENCES documents(id),
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_financial_models_analysis ON financial_models(analysis_id);

-- Valuation records
CREATE TABLE valuations (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    
    -- Three approaches to value
    income_approach_value NUMERIC(15,2),
    income_approach_details JSONB,
    
    sales_comparison_value NUMERIC(15,2),
    sales_comparison_details JSONB,
    
    cost_approach_value NUMERIC(15,2),
    cost_approach_details JSONB,
    
    -- Reconciled value
    reconciled_value_low NUMERIC(15,2),
    reconciled_value_mid NUMERIC(15,2),
    reconciled_value_high NUMERIC(15,2),
    
    reconciliation_narrative TEXT,
    
    -- Confidence & quality
    confidence_score DECIMAL(3,2),
    data_quality_score INTEGER,
    
    -- USPAP compliance tracking
    uspap_compliant BOOLEAN DEFAULT FALSE,
    assumptions_and_limitations TEXT,
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_valuations_analysis ON valuations(analysis_id);

-- Investment memos
CREATE TABLE investment_memos (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    analysis_id UUID NOT NULL REFERENCES deal_analyses(id) ON DELETE CASCADE,
    
    -- Memo structure
    executive_summary TEXT,
    investment_thesis TEXT,
    property_description TEXT,
    market_analysis TEXT,
    financial_analysis TEXT,
    risk_factors TEXT,
    recommendation TEXT,
    
    -- Recommendation
    recommendation_type VARCHAR(20), -- 'strong_buy', 'buy', 'hold', 'pass'
    recommendation_confidence DECIMAL(3,2),
    
    -- Generated documents
    pdf_document_id UUID REFERENCES documents(id),
    docx_document_id UUID REFERENCES documents(id),
    
    -- Version tracking
    version INTEGER DEFAULT 1,
    is_draft BOOLEAN DEFAULT TRUE,
    
    created_at TIMESTAMPTZ DEFAULT NOW(),
    updated_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_investment_memos_analysis ON investment_memos(analysis_id);

-- LLM usage tracking
CREATE TABLE llm_usage (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    
    -- Context
    analysis_id UUID REFERENCES deal_analyses(id),
    task_id UUID REFERENCES analysis_tasks(id),
    user_id UUID REFERENCES users(id),
    
    -- Usage details
    model VARCHAR(100) NOT NULL,
    provider VARCHAR(50) NOT NULL, -- 'anthropic', 'openai', 'local'
    
    tokens_input INTEGER NOT NULL,
    tokens_output INTEGER NOT NULL,
    cost_cents INTEGER NOT NULL,
    
    latency_ms INTEGER,
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_llm_usage_created ON llm_usage(created_at);
CREATE INDEX idx_llm_usage_user ON llm_usage(user_id);

-- Document chunks for RAG
CREATE TABLE document_chunks (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    document_id UUID NOT NULL REFERENCES documents(id) ON DELETE CASCADE,
    
    chunk_index INTEGER NOT NULL,
    content TEXT NOT NULL,
    
    -- Metadata
    page_number INTEGER,
    section_title VARCHAR(500),
    chunk_type VARCHAR(50), -- 'text', 'table', 'header'
    
    -- Vector embedding (pgvector)
    embedding vector(1536),
    
    created_at TIMESTAMPTZ DEFAULT NOW()
);

CREATE INDEX idx_document_chunks_document ON document_chunks(document_id);
CREATE INDEX idx_document_chunks_embedding ON document_chunks 
    USING ivfflat (embedding vector_cosine_ops) WITH (lists = 100);

-- ============================================
-- VIEWS
-- ============================================

CREATE VIEW analysis_summary AS
SELECT 
    da.id,
    da.deal_id,
    d.name as deal_name,
    da.status,
    da.workflow_type,
    da.valuation_mid,
    da.risk_score,
    da.irr_levered,
    da.equity_multiple,
    da.confidence_score,
    da.created_at,
    da.completed_at,
    EXTRACT(EPOCH FROM (da.completed_at - da.started_at)) as duration_seconds,
    COUNT(at.id) as task_count,
    SUM(at.llm_cost_cents) as total_llm_cost_cents
FROM deal_analyses da
JOIN deals d ON da.deal_id = d.id
LEFT JOIN analysis_tasks at ON da.id = at.analysis_id
GROUP BY da.id, d.name;
```

---

## 7. API Design

### 7.1 REST Endpoints

```yaml
# Financial Analyst Layer API
# Base path: /api/v1/analyst

# ============================================
# ANALYSIS ENDPOINTS
# ============================================

POST /api/v1/analyst/analyses
  description: Start a new deal analysis
  body:
    deal_id: string (required)
    workflow_type: 'full' | 'quick_val' | 'dd_only' | 'memo_only'
    options:
      target_irr: number
      hold_period: number
      financing_assumptions: object
  response:
    201:
      analysis_id: string
      status: 'pending'
      estimated_duration_minutes: number

GET /api/v1/analyst/analyses/:id
  description: Get analysis status and results
  response:
    200:
      id: string
      status: 'pending' | 'running' | 'completed' | 'failed'
      progress: number (0-100)
      results: AnalysisResults | null
      tasks: TaskStatus[]

GET /api/v1/analyst/analyses/:id/tasks
  description: Get detailed task breakdown
  response:
    200:
      tasks:
        - id: string
          agent: string
          status: string
          started_at: timestamp
          completed_at: timestamp
          result_summary: string

POST /api/v1/analyst/analyses/:id/retry
  description: Retry failed analysis
  body:
    task_ids: string[] (optional, retry specific tasks)

DELETE /api/v1/analyst/analyses/:id
  description: Cancel running analysis

# ============================================
# VALUATION ENDPOINTS  
# ============================================

POST /api/v1/analyst/valuations/quick
  description: Quick AVM for a property (no full analysis)
  body:
    property:
      address: string
      type: string
      sf: number
      units: number
      noi: number (optional)
  response:
    200:
      value_low: number
      value_mid: number
      value_high: number
      confidence: number
      methodology: string
      comps_used: number

GET /api/v1/analyst/valuations/:analysis_id
  description: Get detailed valuation from analysis
  response:
    200:
      income_approach: ValueApproach
      sales_comparison: ValueApproach
      cost_approach: ValueApproach
      reconciled: ReconciledValue

# ============================================
# COMP ENDPOINTS
# ============================================

POST /api/v1/analyst/comps/search
  description: Search for comparable properties
  body:
    subject:
      address: string
      lat: number
      lng: number
      type: string
      sf: number
    comp_type: 'sale' | 'rent' | 'both'
    radius_miles: number
    date_range_months: number
    limit: number
  response:
    200:
      comps:
        - id: string
          address: string
          distance_miles: number
          relevance_score: number
          sale_price: number
          price_psf: number
          cap_rate: number
          sale_date: date

GET /api/v1/analyst/comps/:id
  description: Get comp property details

POST /api/v1/analyst/comps/adjust
  description: Apply adjustments to comp set
  body:
    subject_property: object
    comp_ids: string[]
    adjustment_factors: object
  response:
    200:
      adjusted_comps:
        - comp_id: string
          raw_value: number
          adjustments: object
          adjusted_value: number

# ============================================
# FINANCIAL MODEL ENDPOINTS
# ============================================

POST /api/v1/analyst/models/generate
  description: Generate proforma model
  body:
    deal_id: string
    model_type: 'acquisition' | 'development' | 'refinance'
    assumptions: FinancialAssumptions
  response:
    200:
      model_id: string
      metrics: FinancialMetrics
      cash_flows: CashFlow[]

GET /api/v1/analyst/models/:id
  description: Get model details

POST /api/v1/analyst/models/:id/scenarios
  description: Run scenario analysis
  body:
    scenarios:
      - name: string
        assumption_overrides: object
  response:
    200:
      scenarios:
        - name: string
          metrics: FinancialMetrics

GET /api/v1/analyst/models/:id/excel
  description: Download model as Excel
  response:
    200: binary (application/vnd.openxmlformats-officedocument.spreadsheetml.sheet)

# ============================================
# DOCUMENT PROCESSING ENDPOINTS
# ============================================

POST /api/v1/analyst/documents/process
  description: Process uploaded documents
  body:
    deal_id: string
    document_ids: string[]
  response:
    202:
      job_id: string
      status: 'processing'

GET /api/v1/analyst/documents/:id/extracted
  description: Get extracted data from document
  response:
    200:
      document_type: string
      extracted_entities: Entity[]
      tables: Table[]
      risk_flags: RiskFlag[]

POST /api/v1/analyst/documents/query
  description: RAG query against deal documents
  body:
    deal_id: string
    query: string
    document_ids: string[] (optional)
  response:
    200:
      answer: string
      sources:
        - document_id: string
          page: number
          excerpt: string
          relevance: number

# ============================================
# DUE DILIGENCE ENDPOINTS
# ============================================

GET /api/v1/analyst/dd/:analysis_id/findings
  description: Get due diligence findings
  query:
    category: string (optional)
    severity: 'info' | 'warning' | 'critical' (optional)
  response:
    200:
      findings:
        - id: string
          category: string
          severity: string
          title: string
          description: string
          source_document: string
          confidence: number
          requires_review: boolean

POST /api/v1/analyst/dd/findings/:id/review
  description: Submit human review of finding
  body:
    is_valid: boolean
    notes: string

GET /api/v1/analyst/dd/:analysis_id/checklist
  description: Get DD checklist status
  response:
    200:
      categories:
        - name: string
          items:
            - item: string
              status: 'pending' | 'complete' | 'na'
              notes: string

# ============================================
# MEMO ENDPOINTS
# ============================================

GET /api/v1/analyst/memos/:analysis_id
  description: Get investment memo
  response:
    200:
      id: string
      sections: MemoSections
      recommendation: string
      is_draft: boolean
      version: number

POST /api/v1/analyst/memos/:analysis_id/regenerate
  description: Regenerate memo with updated inputs
  body:
    sections: string[] (optional, specific sections to regenerate)
    guidance: string (optional, user guidance)

GET /api/v1/analyst/memos/:analysis_id/pdf
  description: Download memo as PDF
  response:
    200: binary (application/pdf)

GET /api/v1/analyst/memos/:analysis_id/docx
  description: Download memo as Word document
  response:
    200: binary (application/vnd.openxmlformats-officedocument.wordprocessingml.document)
```

### 7.2 WebSocket Events

```typescript
// Real-time analysis progress updates

// Client subscribes
ws.send({
  type: 'subscribe',
  channel: 'analysis:deal_abc123'
});

// Server events
interface AnalysisEvent {
  type: 'analysis.progress' | 'analysis.task_complete' | 'analysis.complete' | 'analysis.error';
  analysisId: string;
  payload: {
    progress?: number;
    currentTask?: string;
    completedTask?: { agent: string; duration: number; summary: string };
    results?: AnalysisResults;
    error?: { code: string; message: string };
  };
  timestamp: number;
}

// Example event stream:
// { type: 'analysis.progress', payload: { progress: 10, currentTask: 'Parsing documents...' } }
// { type: 'analysis.task_complete', payload: { completedTask: { agent: 'due_diligence', ... } } }
// { type: 'analysis.progress', payload: { progress: 45, currentTask: 'Finding comps...' } }
// { type: 'analysis.complete', payload: { results: { ... } } }
```

---

## 8. Technology Recommendations

### 8.1 Core Stack

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Runtime** | Node.js 22 + TypeScript | Matches Clawdbot core, strong async |
| **API Framework** | Hono / Express | Lightweight, fast, familiar |
| **Task Queue** | BullMQ (Redis) | Battle-tested, good DX, visibility |
| **Database** | PostgreSQL (Supabase) | Already in stack, pgvector support |
| **Cache** | Redis | Queue backend, caching, pub/sub |
| **Object Storage** | Cloudflare R2 | S3-compatible, no egress fees |
| **Vector DB** | pgvector | Keep in Postgres, good enough for scale |

### 8.2 Document Processing

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **PDF Parsing** | pdf-parse + pdfplumber (Python) | Best extraction quality |
| **OCR** | Tesseract 5 / DocTR | Open source, GPU-accelerated |
| **Table Extraction** | Camelot / Tabula | Specialized for tables |
| **Embeddings** | text-embedding-3-small | Good quality/cost tradeoff |

### 8.3 Financial Calculations

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Core Calc Engine** | TypeScript (custom) | Full control, auditable |
| **IRR/NPV** | financial-fns library | Proven formulas |
| **Excel Generation** | ExcelJS | Feature-complete, maintained |
| **PDF Generation** | Puppeteer + HTML templates | Flexible, high quality |

### 8.4 LLM Infrastructure

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Local Inference** | Ollama | Simple, works on harlan-desktop |
| **Cloud Routing** | LiteLLM | Unified interface, fallbacks |
| **Prompt Management** | Custom + version control | Audit trail, iteration |
| **Structured Output** | Instructor + Zod | Type-safe LLM responses |

### 8.5 Monitoring & Observability

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Logging** | Pino + Axiom | Structured, hosted |
| **Metrics** | Prometheus + Grafana | Industry standard |
| **Tracing** | OpenTelemetry | Distributed traces |
| **Error Tracking** | Sentry | Already in stack |

---

## 9. Build vs Buy Decisions

### 9.1 BUILD (Core IP)

| Component | Why Build |
|-----------|-----------|
| **Agent Orchestrator** | Core differentiator, needs tight Clawdbot integration |
| **Financial Modeling Engine** | Domain-specific, must control formulas |
| **Investment Memo Generator** | Unique output format, voice/style matters |
| **Due Diligence Analyzer** | CRE-specific risk detection |
| **Comp Selection Logic** | Domain expertise embedded in algorithms |

### 9.2 BUY / USE EXISTING

| Component | Solution | Why Buy |
|-----------|----------|---------|
| **PDF Parsing** | pdf-parse + pdfplumber | Commodity, works well |
| **OCR** | Tesseract / cloud OCR | Hard to beat quality |
| **Task Queue** | BullMQ | Solved problem |
| **Vector DB** | pgvector | Good enough, in-stack |
| **Excel Gen** | ExcelJS | No competitive advantage |
| **LLM APIs** | Anthropic/OpenAI | Obviously |

### 9.3 EVALUATE LATER

| Component | Options | Decision Criteria |
|-----------|---------|-------------------|
| **Comp Data** | Build scraper vs. data provider | Data quality, cost, legal |
| **Geocoding** | Google Maps vs. open source | Volume, accuracy needs |
| **Market Data** | FRED + Census vs. paid feeds | Depth requirements |

### 9.4 Cost Estimates

| Category | Monthly Cost | Notes |
|----------|--------------|-------|
| LLM APIs | $300-500 | Depends on volume |
| Infrastructure | $100-200 | VPS, Supabase, R2 |
| Third-party Data | $0 (phase 1) | Public sources only initially |
| **Total** | **$400-700** | Scales with usage |

---

## 10. Technical Risks and Mitigations

### 10.1 Risk Matrix

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| **LLM hallucinations in financials** | High | Critical | Calculation engine separate from LLM, validation layer |
| **Document parsing failures** | Medium | High | Fallback to OCR, human review queue |
| **Comp data quality** | High | High | Multiple sources, confidence scoring, manual override |
| **Appraisal liability** | Medium | Critical | Clear disclaimers, USPAP compliance notes |
| **Cost overruns (LLM)** | Medium | Medium | Local inference default, budget caps |
| **Latency (user experience)** | Medium | Medium | Async processing, progress updates |
| **Integration complexity** | Medium | Medium | Clean interfaces, feature flags |

### 10.2 Detailed Mitigations

#### LLM Hallucination Prevention

```typescript
// NEVER let LLM calculate financials directly
// LLM describes intent → deterministic engine calculates

// BAD: "What's the IRR?" → LLM answers "12.5%"
// GOOD: LLM extracts assumptions → CalculationEngine.computeIRR(assumptions) → 12.47%

class FinancialModelingAgent {
  async generateProforma(context: DealContext) {
    // Step 1: LLM extracts/validates assumptions
    const assumptions = await this.llm.extractAssumptions(context.documents);
    
    // Step 2: Validate assumptions are reasonable
    this.validateAssumptions(assumptions);
    
    // Step 3: Deterministic calculation
    const proforma = CalculationEngine.buildProforma(assumptions);
    
    // Step 4: LLM generates narrative ABOUT the numbers
    const narrative = await this.llm.generateNarrative(proforma);
    
    return { proforma, narrative };
  }
}
```

#### Document Processing Fallbacks

```typescript
class DocumentProcessor {
  async process(document: Document) {
    try {
      // Primary: Native PDF parsing
      return await this.parsePDF(document);
    } catch (e) {
      // Fallback 1: OCR
      try {
        return await this.ocrDocument(document);
      } catch (e) {
        // Fallback 2: Manual review queue
        await this.queueForManualReview(document, {
          reason: 'parsing_failed',
          attempts: 2
        });
        throw new ProcessingFailedError('Document queued for manual review');
      }
    }
  }
}
```

#### Appraisal Liability Protection

```typescript
const VALUATION_DISCLAIMER = `
IMPORTANT DISCLAIMER

This Automated Valuation Model (AVM) output is provided for informational 
purposes only and does not constitute an appraisal or opinion of value 
as defined by the Uniform Standards of Professional Appraisal Practice (USPAP).

This analysis:
- Is NOT a substitute for a professional appraisal
- Should NOT be relied upon for lending, investment, or legal decisions
- May contain errors or be based on incomplete information
- Reflects market conditions as of the analysis date only

For formal valuations, please engage a licensed MAI appraiser.
`;

// Always include disclaimer
class AppraisalAgent {
  async generateValuation(context: DealContext) {
    const valuation = await this.computeValuation(context);
    
    return {
      ...valuation,
      disclaimer: VALUATION_DISCLAIMER,
      is_appraisal: false,
      requires_professional_review: true,
    };
  }
}
```

#### Cost Control

```typescript
class CostGuard {
  private monthlyBudget = 500; // dollars
  private perAnalysisBudget = 2; // dollars
  
  async checkBudget(analysisId: string): Promise<boolean> {
    const monthlySpend = await this.getMonthlySpend();
    const analysisSpend = await this.getAnalysisSpend(analysisId);
    
    if (monthlySpend > this.monthlyBudget * 0.9) {
      // Switch to local models only
      this.setLocalOnlyMode(true);
      this.alertAdmin('Monthly budget 90% exhausted');
    }
    
    if (analysisSpend > this.perAnalysisBudget) {
      throw new BudgetExceededError('Analysis budget exceeded');
    }
    
    return true;
  }
}
```

---

## 11. Implementation Roadmap

### Phase 1: Foundation (2 weeks)

```
Week 1:
├── [ ] Set up project structure in /root/clawd/skills/financial-analyst
├── [ ] Implement basic orchestrator (single-threaded, serial execution)
├── [ ] Build calculation engine (IRR, NPV, cap rate, cash flows)
├── [ ] Create document processor (PDF → text → chunks)
├── [ ] Integrate with Supabase (core schema)

Week 2:
├── [ ] Financial Modeling Agent v1 (basic proforma)
├── [ ] Excel generation
├── [ ] Basic API endpoints (start analysis, get status)
├── [ ] LLM routing layer (local/cloud selection)
├── [ ] End-to-end test with sample deal
```

### Phase 2: Core Agents (3 weeks)

```
Week 3:
├── [ ] Research Agent (comp search, manual data for now)
├── [ ] Comp database + similarity matching
├── [ ] Sales comp adjustments

Week 4:
├── [ ] Due Diligence Agent (document analysis, risk flagging)
├── [ ] Entity extraction pipeline
├── [ ] DD checklist templates

Week 5:
├── [ ] Appraisal Agent (income approach, sales comparison)
├── [ ] Investment Memo Agent v1
├── [ ] PDF/DOCX generation
```

### Phase 3: Polish & Integration (2 weeks)

```
Week 6:
├── [ ] Parallel execution in orchestrator
├── [ ] Progress WebSocket updates
├── [ ] DealOS UI integration
├── [ ] Error handling & retries

Week 7:
├── [ ] Local inference optimization (harlan-desktop)
├── [ ] Cost tracking dashboard
├── [ ] Performance optimization
├── [ ] Documentation & testing
```

---

## 12. Open Questions for Founder

1. **Comp Data Strategy**: Public records only for MVP, or should we budget for a data provider? CoStar API is expensive ($$$), but ATTOM/CoreLogic are options.

2. **Appraisal Positioning**: How prominently do we market the appraisal feature? Regulatory sensitivity around "automated appraisals" — need to position carefully.

3. **Local Inference Priority**: How much should we invest in optimizing local inference vs. just using cloud APIs? The RTX 4070 can run 8B models fast, but 70B is slow.

4. **Excel vs. Web**: Do users actually need downloadable Excel files, or can we build interactive web-based proformas? Excel is expected in CRE, but it's a lot of work.

5. **Human-in-the-Loop Workflow**: How much friction is acceptable? Require review of DD findings? Approve memo before sending? Need to balance automation with trust.

6. **Multi-tenancy**: Is this single-user (founder's deals) initially, or multi-tenant from day 1? Affects auth, data isolation, pricing.

---

## Appendix A: Sample Agent Prompts

### Financial Modeling Agent - Proforma Generation

```markdown
You are a commercial real estate financial analyst generating an acquisition proforma.

## INPUTS PROVIDED
- Property: {{property}}
- Rent Roll: {{rent_roll}}
- T12 Operating Statement: {{t12}}
- Market Assumptions: {{market_data}}
- Financing Terms: {{financing}}

## YOUR TASK
Extract and validate the following assumptions from the inputs:
1. In-place rent (per unit type or PSF)
2. Market rent (for vacancy/turnover)
3. Operating expenses (by category)
4. Capital reserves
5. Vacancy/collection loss rate

Respond with JSON:
```json
{
  "assumptions_extracted": {
    "rental_income": { ... },
    "other_income": { ... },
    "expenses": { ... },
    "capital_reserves": ...,
    "vacancy_rate": ...
  },
  "data_quality_notes": ["...", "..."],
  "missing_data": ["...", "..."],
  "confidence": 0.85
}
```

DO NOT calculate IRR, NPV, or returns. Only extract assumptions.
The calculation engine will compute metrics from your extracted data.
```

### Due Diligence Agent - Risk Detection

```markdown
You are a commercial real estate due diligence analyst reviewing documents for risk factors.

## DOCUMENT
{{document_content}}

## YOUR TASK
Identify potential risks, red flags, or items requiring further investigation.

Categories to check:
- Environmental (contamination, hazmat, flood zone)
- Title (liens, encumbrances, easements, boundary disputes)
- Lease (below-market terms, termination rights, tenant creditworthiness)
- Financial (declining NOI, deferred maintenance, unusual expenses)
- Legal (litigation, code violations, zoning non-conformance)
- Physical (structural issues, deferred capex, obsolescence)

For each finding, provide:
```json
{
  "findings": [
    {
      "category": "environmental",
      "severity": "critical|warning|info",
      "title": "Phase I identifies REC",
      "description": "Document indicates a Recognized Environmental Condition...",
      "source_excerpt": "\"The Phase I ESA identified a REC related to...\"",
      "page_reference": 12,
      "recommended_action": "Obtain Phase II ESA before proceeding",
      "confidence": 0.92
    }
  ]
}
```

Be thorough but avoid false positives. If uncertain, use "info" severity.
```

---

## Appendix B: Calculation Engine Formulas

```typescript
// Core financial calculations (deterministic, auditable)

export class CalculationEngine {
  
  static calculateIRR(cashFlows: number[], guess = 0.1): number {
    // Newton-Raphson method for IRR
    const maxIterations = 100;
    const tolerance = 0.0001;
    
    let rate = guess;
    for (let i = 0; i < maxIterations; i++) {
      const npv = this.calculateNPV(cashFlows, rate);
      const npvDerivative = this.calculateNPVDerivative(cashFlows, rate);
      
      const newRate = rate - npv / npvDerivative;
      if (Math.abs(newRate - rate) < tolerance) {
        return newRate;
      }
      rate = newRate;
    }
    
    throw new Error('IRR did not converge');
  }
  
  static calculateNPV(cashFlows: number[], discountRate: number): number {
    return cashFlows.reduce((npv, cf, t) => {
      return npv + cf / Math.pow(1 + discountRate, t);
    }, 0);
  }
  
  static calculateCapRate(noi: number, value: number): number {
    return noi / value;
  }
  
  static calculateDSCR(noi: number, debtService: number): number {
    return noi / debtService;
  }
  
  static calculateLoanPayment(
    principal: number,
    annualRate: number,
    amortYears: number
  ): number {
    const monthlyRate = annualRate / 12;
    const numPayments = amortYears * 12;
    
    return principal * 
      (monthlyRate * Math.pow(1 + monthlyRate, numPayments)) / 
      (Math.pow(1 + monthlyRate, numPayments) - 1);
  }
  
  static buildProforma(assumptions: ProformaAssumptions): Proforma {
    const years: CashFlow[] = [];
    
    for (let year = 1; year <= assumptions.holdPeriod; year++) {
      const revenue = this.projectRevenue(assumptions, year);
      const expenses = this.projectExpenses(assumptions, year);
      const noi = revenue - expenses;
      const debtService = this.calculateAnnualDebtService(assumptions);
      const cashFlow = noi - debtService;
      
      years.push({
        year,
        revenue,
        expenses,
        noi,
        debtService,
        cashFlow,
      });
    }
    
    // Exit
    const exitNOI = years[years.length - 1].noi * (1 + assumptions.rentGrowth);
    const exitValue = exitNOI / assumptions.exitCapRate;
    const loanBalance = this.calculateLoanBalance(assumptions);
    const exitEquity = exitValue - loanBalance - assumptions.dispositionCosts;
    
    // Build cash flow array for IRR
    const equityInvested = assumptions.purchasePrice * (1 - assumptions.ltv) + 
                          assumptions.closingCosts;
    const cashFlowsForIRR = [-equityInvested, ...years.map(y => y.cashFlow)];
    cashFlowsForIRR[cashFlowsForIRR.length - 1] += exitEquity;
    
    return {
      years,
      metrics: {
        irrUnlevered: this.calculateUnleveredIRR(assumptions, years, exitValue),
        irrLevered: this.calculateIRR(cashFlowsForIRR),
        equityMultiple: (years.reduce((sum, y) => sum + y.cashFlow, 0) + exitEquity) / equityInvested,
        cashOnCashY1: years[0].cashFlow / equityInvested,
        avgDSCR: years.reduce((sum, y) => sum + y.noi / y.debtService, 0) / years.length,
      },
      exitAnalysis: {
        exitNOI,
        exitValue,
        loanBalance,
        exitEquity,
      },
    };
  }
}
```

---

*Document prepared for morning review. Ready for feedback and iteration.*

**Next Steps:**
1. Founder review and questions
2. Refine based on feedback
3. Begin Phase 1 implementation
