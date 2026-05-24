# Wiki Log

*Append-only chronological record of all operations on this vault. Format defined in `_README.md`.*

*Parse recent entries: `grep "^## \[" log.md | tail -5`*

---

## [2026-05-24] add | Cantus Business Plan — v2 canonical operating plan

**Source:** Dom direction to do the business plan rewrite as the next open item. The wiki did not previously contain a single canonical Cantus Business Plan; v1 business-plan-equivalent content was spread across GTM pages (Executive-Summary, Go-To-Market-Plan, Investor-Deck-Outline, Team-and-Org). The v2 business plan integrates the Power Sector Thesis, four vertical pages, two Foundation pages, and `_parameters.md` into a single operating-plan document.

**Action:**
- **Created** `Strategy/Cantus-Business-Plan.md` — ~5,500 words across 14 sections covering: Executive Summary; Strategic Position (anchored to [[Strategy/Cantus-Power-Sector-Thesis]]); The Cantus Operating Architecture (four verticals + two Foundations); Customer Strategy (six demand vectors with prioritization across Compute / Supply Chain Manufacturing / Advanced Manufacturing / Defense / Biomanufacturing / Energy Transition; Two Customer Stacks as Tier-1 simplification); Geographic Strategy (ERCOT primary, expansion sequence to PJM / MISO / Western / Southeast); Revenue Model (by vertical and consolidated into Year 6 FCF Build); Capital Architecture (balance sheet → Fund I → multi-fund family → Power Studio); Phasing in Detail (Building / Activation / Compounding / Mature with vertical-specific activity breakdowns); Year 1–2 Operating Roadmap (specific milestones across all four verticals plus both Foundations plus cross-vertical); Organizational Structure (Year 6 modeled headcount allocation; compensation; reporting structure; talent acquisition); Risk Factors and Mitigation (capital risk, pipeline execution risk, tenant risk, workforce risk, regulatory/political risk, competitive risk); Competitive Position (five-way differentiation matrix); KPIs and Reporting (firm-level, vertical-specific, Foundation-specific, cadence); The Stakes (closing).
- **Updated** `index.md` — added Cantus Business Plan to the Foundational + supporting theses section as canonical operating plan.

**Cross-links added:** The Business Plan cross-references all four operating vertical pages, both Foundation pages, the foundational thesis, [[Strategy/Cantus-Customer-Category]], [[Strategy/Power-Sector/Power-Industries]], and the relevant Primary Inputs pages. Heavy reliance on `_parameters.md` for all numerical claims (advisory fees, Year 6 FCF Build, Fund I target, Year 10/15 targets, mixed-tenant campus economics, capital partner categories, pipeline projects).

**Audience:** capital_partner. The Business Plan is designed as the document Cantus would share with a Fund I anchor LP, a strategic capital partner, or a major capital-partner candidate in lieu of an investor deck for first deep-dive conversations. The Investor Deck Outline (a separate GTM page still on v1 framing) would be the slide-format derivative; the Business Plan is the narrative-document long form.

**Notes:**
- The Business Plan is structurally an *operationalization* of the foundational thesis. The thesis articulates the strategic claim about the Power sector emerging and Cantus's position as integrator; the Business Plan translates that claim into specific phases, verticals, revenue streams, capital plans, milestones, risks, and KPIs.
- Year 1–2 milestones across the four verticals and two Foundations are specific and traceable to the active pipeline and the parameters file: Cantus Development to close Land control on 2–3 sites with executed interconnection; Cantus Infrastructure to institutionalize equipment slot reservations across the [[_parameters]] OEM cohort; Cantus Technology to establish NVIDIA corporate-level relationship (flagged as priority gap); Cantus Markets to reach $2M+ ARR by Month 12 and scope Fund I anchor commitment.
- Open items flagged inside the Business Plan that flow to subsequent revision:
  - Fund I vehicle structure (open-end vs. closed-end; specific carry hurdle; co-investment policy)
  - Strategic corporate LP architecture (Microsoft, Meta, Oracle as candidates)
  - NVIDIA strategic relationship as priority gap in [[_parameters]] Strategic OEM Relationships
  - Cantus Compute scope (campus-internal vs. external customer base)
  - Cantus Robotics priority and timeline
  - PWA-compliance technology and tracking — CII vs. Foundation ownership
  - Two Customer Stacks vs. six-demand-vector framing reconciliation
- The GTM-folder pages (Executive-Summary, Go-To-Market-Plan, Investor-Deck-Outline, Team-and-Org) still reflect v1 framing and would benefit from v2 updates as a next item. The Business Plan supersedes them as canonical narrative; the GTM pages are now derivatives that need to be brought in line.
- No `_parameters.md` updates in this batch; the Business Plan cites the existing parameters extensively but does not introduce new ones.
- No NPI material crossed. Cantus Forge not referenced. Hopkins not signed; author of record Dom Espinosa throughout. The Business Plan uses production-company metaphor (Hollywood-derived) per the foundational thesis; no Caesar-archetype language; no comparable-driven identity claims.

**Author:** Dom Espinosa

## [2026-05-24] add | v2 architecture build-out — 4 vertical pages, 2 Foundation pages, parameters update, v1 archival

**Source:** Dom direction to continue through open v2 build-out items. Scope: create the four Cantus operating vertical pages (Development, Infrastructure, Technology, Markets), create the two Foundation pages (Labor/Community, CII/DealOS), update `_parameters.md` for v2-specific parameters, archive v1 framework pages (Cantus-Framework, Cantus-Framework-Layers-2-3-4, Layers), and reconcile Cantus-Customer-Category with the v2 six-vector framing.

**Action:**
- **Created** four Cantus operating vertical pages, each ~1,500–2,500 words covering: what the vertical is, sub-industries owned, operating model, deliverables, sub-vertical activities, counterparty universe, capital architecture, phasing (Building / Activation / Compounding / Mature), key operating metrics, what the vertical is not, open questions:
  - `Strategy/Cantus-Development.md` — Power Land + Power Facilities (direct principal). Creates the sites.
  - `Strategy/Cantus-Infrastructure.md` — Power Assets + Power Equipment + Power Services. Cantus Prime as firm-level orchestration label. Powers the sites.
  - `Strategy/Cantus-Technology.md` — Power Machines + Power Technology. Orchestrator + selective operator. Cantus Compute as named selective-operator business; Cantus Robotics modeled; Cantus Edge inside this vertical. Makes the sites productive.
  - `Strategy/Cantus-Markets.md` — Power Industries + Power Commodities + Power Markets-broad. Includes capital architecture (Fund I → multi-fund family → Power Studio). Monetizes and finances the output.
- **Created** `Strategy/Foundations/` folder with two Foundation pages explicitly framed as cross-cutting all four verticals:
  - `Strategy/Foundations/Labor-Community-Foundation.md` — workforce development, R1 university partnerships, area-education programs, IBEW JATCs, community engagement. Framing page; substantive content remains in [[Strategy/Primary-Inputs-03-Labor-Community]].
  - `Strategy/Foundations/CII-DealOS-Foundation.md` — Cantus Integrated Intelligence (23 data assets across 5 families, 4 prediction-and-resolution loops, 23 surfaces across 6 user categories) plus DealOS deal-level operating system. Framing page; substantive content remains in [[Products/CII-Iteration-Document]] and [[DealOS/README]].
- **Updated** `_parameters.md`:
  - Added "Primary Cantus vertical" attribution column to Year 6 FCF Build, mapping the five revenue streams to v2 verticals.
  - Added Year 6 Headcount by Vertical table (modeled allocation of 80–150 total to each vertical, Foundations, and exec/shared services).
  - Added v2 Architecture Parameters section: Four Verticals table, Two Foundations table, Cantus Compute economics (capital intensity, pilot deployment sizing, capital structure, customer-base scope open question), Identity Arc (Power Producer → Power Production Company → Power Studio with phase mapping).
  - Updated Change Log with two new rows documenting the v2 additions.
- **Archived** three v1 framework pages with redirect notes pointing to v2 canonical articulation:
  - `Strategy/Cantus-Framework.md` — status: archived; redirect to Cantus-Power-Sector-Thesis + four vertical pages + two Foundation pages. v1 content preserved.
  - `Strategy/Cantus-Framework-Layers-2-3-4.md` — same pattern; explicit mapping of v1 Layer 1/2/3/4 concepts to v2 vertical equivalents in the redirect note.
  - `Strategy/Layers.md` — archived with short redirect note.
- **Updated** `Strategy/Cantus-Customer-Category.md` — added v2 framework reconciliation section at the top of the page with explicit mapping table from six demand vectors (v2 canonical) to Two Customer Stacks (Tier-1 simplification). Frontmatter updated; status remains active because the substantive content of the customer category articulation remains accurate; v2 mapping is added as amendment.
- **Updated** `index.md` — Strategy section restructured into four subsections: Foundational + supporting theses; Operating verticals (v2); Foundations (v2); Strategy memos and primary inputs; Archived (v1, superseded by v2). The v2 architecture is now navigationally legible from the index.

**Cross-links added:** All four operating vertical pages cross-reference each other and the relevant sub-industry pages. Foundation pages cross-reference all four operating verticals plus the related substantive pages. Cantus-Customer-Category now points to Cantus-Power-Sector-Thesis and Power-Industries as primary v2 references. Archived v1 pages each carry `superseded_by` frontmatter pointing to the v2 canonical articulation.

**Audience:** capital_partner (operating vertical pages designed to be shareable with capital partners; Foundation pages internal-leaning but capital-partner-readable).

**Notes:**
- The v2 architecture is now fully documented across the wiki: foundational thesis (Cantus-Power-Sector-Thesis), 10 sub-industry pages (Strategy/Power-Sector/), 4 operating vertical pages, 2 Foundation pages, parameters update, and updated operating manual (_README.md, both CLAUDE.md files updated in prior batch).
- Cantus Compute is now articulated as the named selective-operator business inside Cantus Technology vertical. The major open question for the business plan rewrite is whether Cantus Compute serves campus-internal tenants only or also external customers (CoreWeave-with-integration-advantage pattern).
- The NVIDIA strategic relationship is flagged as a priority gap in [[_parameters]] Strategic OEM Relationships — Cantus Technology's most important Machine OEM is not yet captured at the corporate-relationship level.
- Strategic-corporate LP architecture (Microsoft, Meta, Oracle wanting LP exposure to platforms they buy from) is flagged across multiple pages as an item to specify in the business plan rewrite.
- Bridge-to-Grid Thesis is preserved as a supporting strategic thesis (demand-side execution argument for ERCOT specifically); ERCOT-Positioning Thesis similarly framed as supporting market-structure thesis.
- Open items remaining for the v2 build-out: business plan rewrite (Years 1–2 operating plan; specific milestones; org structure); GTM Executive Summary and Investor Deck Outline updates to reflect v2 architecture; Team-and-Org page update to reflect new vertical structure; capital-partner-facing docx exports of the new Cantus Power Sector Thesis and (selectively) vertical pages.
- No NPI material crossed. Cantus Forge not referenced. Hopkins not signed; author of record Dom Espinosa throughout.

**Author:** Dom Espinosa

## [2026-05-24] revision | Operating manual updated to v2; foundational thesis introduced

**Source:** Dom direction to update wiki operating manual (_README.md, both CLAUDE.md files) to reflect the v2 four-vertical Cantus architecture and to write the foundational Cantus Power Sector Thesis that supersedes Bridge-to-Grid as the firm's primary articulation.

**Action:**
- **Updated** `Cantus-wiki/_README.md` — substantial rewrite of the What Cantus Is, Four-Vertical Architecture (replaces v1 Four-Layer Framework), Two Foundations (now Labor/Community + CII/DealOS, replacing Labor/Community + Technology Integration), Cantus Compute / Cantus Robotics / Cantus Prime / Cantus Edge sections, Phasing, terminology hot-list, and Getting Started sections. Operating Triangle retained as analytical lens within the new framing; v1 Operating Split (Cantus Operations Tiers 1-2 / Cantus Infrastructure Tiers 3-4) deprecated and replaced with the four-vertical (Development / Infrastructure / Technology / Markets) structure.
- **Updated** `Cantus-wiki/CLAUDE.md` — Hard rules section updated to reference v2 four-vertical architecture; new "Power Sector Framework v2 (canonical as of 2026-05-24)" section added with the 10 sub-industries, 4 verticals, 2 Foundations, identity arc, and foundational-thesis pointer.
- **Updated** `Cantus/Cantus/CLAUDE.md` — Hard rules updated to v2 architecture; foundational thesis pointer added.
- **Created** `Cantus-wiki/Strategy/Cantus-Power-Sector-Thesis.md` — new foundational thesis (~3,500 words). Sections: The Sentence; Power as the Organizing Sector; The Ten Sub-Industries; The Frontier Company Is Becoming Selectively Asset-Heavy; Cantus's Position in the Framework (four-vertical architecture and identity arc); What Cantus Does Differently (vs. infra funds, vs. vertically integrated supply-side, vs. MPC developers, vs. BTS DC developers, vs. hyperscaler self-orchestration); Why Now (load growth reversal, interconnection collapse, industrial policy supercycle, capital concentration, workforce constraints, co-location standardization); The Integrated Production (Hollywood production-company metaphor); Phasing and Strategic Horizon; The Stakes.
- **Updated** `Cantus-wiki/Strategy/Bridge-to-Grid-Thesis.md` — reframed from `thesis_class: foundational` to `thesis_class: strategic` with explicit status note at the top stating that Bridge-to-Grid is now a supporting strategic thesis (the demand-side execution argument for ERCOT specifically) sitting beneath the Cantus Power Sector Thesis as the new foundational. Bridge-to-Grid content preserved unchanged; status framing updated.
- **Updated** `Cantus-wiki/index.md` — Strategy section reordered with Cantus Power Sector Thesis at the top as foundational (current); Bridge-to-Grid and ERCOT-Positioning re-labeled as strategic/supporting; v1 Cantus-Framework, Cantus-Framework-Layers-2-3-4, Layers, and Cantus-Customer-Category marked as pending v2 rewrite or v2 reconciliation.

**Cross-links added:** The Cantus Power Sector Thesis cross-references all ten v2 sub-industry pages plus CII Iteration Document. Bridge-to-Grid frontmatter now references the new foundational thesis. CLAUDE.md files point to the new foundational thesis as the canonical reference.

**Audience:** internal (operating manual) + capital_partner (foundational thesis).

**Notes:**
- The four-vertical architecture and two-Foundation structure is now locked into the operating manual; the v1 four-layer / two-Foundation structure (Operating Triangle, Platform Operations, Capital Architecture, Strategic Position with Labor/Community + Technology Integration Foundations) is retained inside the v1 framework pages but flagged as pending v2 rewrite.
- The Cantus Power Sector Thesis is structured around the seven-part Dom articulation of the Power Sector Thesis with the Cantus-specific positioning added: foundational claim about Power as the organizing sector; the ten sub-industries; the frontier-company asset-heavy observation; Cantus's four-vertical architecture; differentiation from each competitive class; structural why-now conditions; the integrated production deliverable; phasing.
- Bridge-to-Grid is preserved and remains active; the reframing is from foundational to supporting (demand-side execution argument inside ERCOT specifically). The thesis content remains unchanged.
- Open follow-ups remain: four Cantus operating vertical pages (Cantus Development, Cantus Infrastructure, Cantus Technology, Cantus Markets); two Foundation pages (Labor/Community Foundation, CII/DealOS Foundation); _parameters.md updates for v2 architecture (Cantus Compute economics, multi-vertical FCF allocation); v2 rewrite of Cantus-Framework and Cantus-Framework-Layers-2-3-4; reconciliation of Cantus-Customer-Category Two-Stacks framing with v2 six-vector framing.
- No NPI material crossed. No identity-claim language used. Cantus Forge not referenced. Hopkins not signed; author of record Dom Espinosa throughout. The foundational thesis avoided "the BlackRock of X" / "the Berkshire of Y" framings explicitly.

**Author:** Dom Espinosa

## [2026-05-24] revision | Power Sector Framework v2 — pivot to four-vertical Cantus + new sub-industry taxonomy

**Source:** Dom session laying out the Power Sector Thesis as v2 of the sector framework and the four-vertical Cantus operating architecture (Development / Infrastructure / Technology / Markets). The v2 pivot displaces the v1 sub-industry-mirrored arm structure (Land / Infrastructure / Industries / Commodities) with a value-creation-stage structure modeled on industrial production company architecture ("Development creates the sites. Infrastructure powers them. Technology makes them productive. Markets monetizes and finances the output."). The v2 sub-industry taxonomy adds Power Facilities and Power Machines, narrows Power Industries to operator-only, and consolidates Power Capital + Power Markets + Power Retail into Power Markets-broad as the allocation layer.

**Three implementation decisions (locked):**
- **Cantus Technology = orchestrator + selective operator.** Cantus Technology operates Power Machines + Power Technology sub-industries; orchestrates for all Cantus campuses; selectively operates Cantus Compute (hosted GPU) and possibly Cantus Robotics in time. Major strategic expansion vs. v1 framework's "Cantus does not operate compute" posture.
- **CII and DealOS = Foundation cross-cutting all four verticals.** Not inside Cantus Technology; parallels Labor/Community as a Foundation flowing across Development, Infrastructure, Technology, Markets.
- **Rewrite 10 sub-industry pages in place.** Existing pages updated to v2 framework; Power Capital and Power Retail archived (status: archived) with redirect notes to Power Markets-broad; Power Facilities and Power Machines created as new sub-industry pages; Power Industries and Power Markets substantially rewritten.

**Action:**
- **Created** `Strategy/Power-Sector/Power-Facilities.md` — new sub-industry covering AI campuses, data centers, fabs, gigafactories, defense plants, biopharma plants, critical minerals processing. Cantus Development as direct principal alongside Power Land.
- **Created** `Strategy/Power-Sector/Power-Machines.md` — new sub-industry covering productive machinery inside Power Facilities: GPUs, semi tools (ASML), industrial and humanoid robotics, battery manufacturing equipment, bioreactors, electrolyzers, automation, additive manufacturing. Cantus Technology orchestrates + selectively operates (Cantus Compute, possibly Cantus Robotics).
- **Rewrote** `Strategy/Power-Sector/Power-Industries.md` — narrowed to operator-only definition (Microsoft, TSMC, Tesla, Anduril, Lilly as marquee names). Facility content moved to Power Facilities; Machine content moved to Power Machines. Cantus Markets vertical owns the relationship now.
- **Rewrote** `Strategy/Power-Sector/Power-Markets.md` — broad allocation layer absorbing the prior Power Capital and Power Retail content. Four sub-segments: Capital allocation, Wholesale electricity allocation, Retail and customer allocation, Commercial contracting. Cantus Markets vertical.
- **Archived** `Strategy/Power-Sector/Power-Capital.md` and `Strategy/Power-Sector/Power-Retail.md` — frontmatter status: archived; redirect notes added to top of page pointing to Power Markets-broad. v1 content preserved beneath for historical traceability.
- **Updated** `Strategy/Power-Sector/Power-Assets.md` — added "backs up, or conditions" to definition; updated Cantus posture to v2 Cantus Infrastructure vertical framing; removed resolved Supply-vs-Infrastructure naming open question.
- **Updated** `Strategy/Power-Sector/Power-Equipment.md` — clarified boundary against new Power Machines sub-industry; updated Cantus posture to v2 Cantus Infrastructure vertical.
- **Updated** `Strategy/Power-Sector/Power-Services.md` — updated Cantus posture to v2 Cantus Infrastructure vertical; clarified Labor/Community Foundation framing.
- **Updated** `Strategy/Power-Sector/Power-Land.md` — updated Cantus posture from "Cantus Land arm" to Cantus Development vertical (covering Land + Facilities); replaced "Cantus Land" references with "Cantus Development" throughout.
- **Updated** `Strategy/Power-Sector/Power-Commodities.md` — added "robot labor capacity" to definition (v2 addition); updated Cantus posture from "Cantus Commodities arm" to Cantus Markets vertical; replaced "Cantus Commodities" references with "Cantus Markets" throughout.
- **Updated** `Strategy/Power-Sector/Power-Technology.md` — significant rewrite of Cantus relationship section: Cantus Technology vertical operates as orchestrator + selective operator across Power Machines and Power Technology; CII and DealOS moved to Foundation framing cross-cutting all four verticals (not inside Cantus Technology vertical); Cantus Compute articulated as selective-operator business inside the vertical.
- **Updated** `index.md` — new Power Sector Framework v2 section with the 10 sub-industries mapped to the four Cantus verticals; archived pages listed separately.

**Cross-links added:** Each sub-industry page now cross-references the new Power Facilities and Power Machines pages where boundaries intersect (Power Equipment vs. Power Machines, Power Industries vs. Power Facilities vs. Power Machines). The Power Markets-broad page lists Power Capital and Power Retail as superseded under `supersedes:` frontmatter.

**Audience:** internal (framework development; thesis and business plan rewrite to follow).

**Notes:**
- The v2 framework matches Dom's articulation in the May 24 session ("Power is the emerging financial sector / the organizing sector of the next industrial era / the feedstock that gets converted into compute, intelligence, batteries, chips, refined minerals, defense capacity, robotics, biologics, and other scarce industrial outputs.").
- The four-vertical Cantus structure ("Development creates the sites. Infrastructure powers them. Technology makes them productive. Markets monetizes and finances the output.") replaces the v1 four-arm sub-industry mirror (Land / Infrastructure / Industries / Commodities). The new structure aligns with the Power Producer → Power Production Company → Power Studio identity arc.
- Cantus Compute is now explicitly inside Cantus Technology as a selective-operator business; this is a meaningful strategic expansion vs. the v1 framework, which had Cantus explicitly not operating compute. The Crusoe / CoreWeave competitive class is now a comparison and a competitive frame rather than a "structural reference only" position.
- CII and DealOS as Foundations parallels Labor/Community Foundation; both flow across all four verticals.
- Open questions surfaced in each sub-industry page for thesis-and-business-plan rewrite include: Cantus Compute scope (campus-internal vs. external customers); Cantus Robotics priority; NVIDIA strategic relationship; captive silicon treatment for hyperscale tenants; Crusoe-style vertically integrated competitor class; six-vector-to-Two-Customer-Stacks reconciliation; hyperscaler self-orchestration treatment; Power Studio target form (Brookfield / Stonepeak / EQT / sui generis); private-microgrid jurisdictional treatment; CII surface externalization criteria.
- No `_parameters.md` updates in this batch; v2 framework structure is fully captured in sub-industry pages and index. Parameter changes will follow the thesis rewrite.
- No NPI material crossed. No identity-claim language used. Cantus Forge not referenced. Hopkins not signed; author of record Dom Espinosa throughout.

**Author:** Dom Espinosa

## [2026-05-24] add | Power Sector Framework — 10 sub-industry pages drafted (v1, superseded same day)

**Source:** Dom session articulating the Power sector framework (sector + 10 sub-industries) as the architecture to anchor the upcoming thesis and business plan rewrite, displacing prior "Powered Industrial" / "Industrial Power" framings. Session input included the four operating arms (Cantus Land, Cantus Infrastructure, Cantus Industries, Cantus Commodities), the integrator posture (Power Producer → Power Production Company → Power Studio), and the explicit ten sub-industries: Power Assets, Power Equipment, Power Services, Power Land, Power Industries, Power Commodities, Power Capital, Power Markets, Power Retail, Power Technology.

**Action:**
- **Created** `Strategy/Power-Sector/` folder as the canonical home for the sector taxonomy.
- **Created** ten sub-industry pages, each built out along eight dimensions (definition, deliverables, major players US-focused, capital structures and economics, counterparty universe, regulatory environment, Cantus's relationship by phase, and trends over the next 5–10 years), with a ninth "open questions" section in each page surfacing items for the framework rewrite:
  - `Strategy/Power-Sector/Power-Assets.md`
  - `Strategy/Power-Sector/Power-Equipment.md`
  - `Strategy/Power-Sector/Power-Services.md`
  - `Strategy/Power-Sector/Power-Land.md` (the sub-industry where Cantus Land operates as direct principal)
  - `Strategy/Power-Sector/Power-Industries.md` (six demand vectors framing the Cantus Customer Category at sub-industry resolution)
  - `Strategy/Power-Sector/Power-Commodities.md`
  - `Strategy/Power-Sector/Power-Capital.md` (most multi-layered Cantus relationship — recipient, curator, future GP, Power Studio)
  - `Strategy/Power-Sector/Power-Markets.md`
  - `Strategy/Power-Sector/Power-Retail.md` (lightest Cantus engagement)
  - `Strategy/Power-Sector/Power-Technology.md` (CII and DealOS as internal-facing Power Technology, not generalist vendor)
- **Updated** `index.md` with a new "Power Sector Framework" section listing all ten pages with their sub-industry index and Cantus posture by arm.
- All pages carry `status: drafting` per Dom's direction; review in parallel as drafted.

**Cross-links added:** Each sub-industry page links back to relevant existing strategy pages (`Strategy/Cantus-Framework`, `Strategy/Bridge-to-Grid-Thesis`, `Strategy/Cantus-Customer-Category`, `Strategy/ERCOT-Positioning-Thesis`, `Strategy/Primary-Inputs-01-Land-Aggregation`, `Strategy/Primary-Inputs-03-Labor-Community`, `Products/CII-Iteration-Document`, `DealOS/README`) and to adjacent sub-industry pages within the framework. `_parameters` referenced throughout for tenant tolerance bands, mixed-tenant campus economics, OEM relationships, partner cohort, capital partner categories, and Year 6 FCF build.

**Audience:** internal (framework development; not capital-partner-facing in current form).

**Notes:**
- The framework rewrites the prior "Powered Industrial" articulation as "Power sector with 10 sub-industries" and aligns Cantus's four operating arms cleanly against the sub-industry taxonomy: Cantus Land = direct principal in Power Land; Cantus Infrastructure = integrator across Power Assets + Power Equipment + Power Services; Cantus Industries = advisor / orchestrator within Power Industries; Cantus Commodities = advisor / structurer within Power Commodities.
- Open questions to resolve in the thesis / business plan rewrite (carried at the bottom of each page, with the most consequential collected here):
  - Cantus Supply vs. Cantus Infrastructure naming for the arm spanning Assets / Equipment / Services. Pages currently use "Cantus Infrastructure" but flag the open question.
  - Mapping from six demand vectors to Two Customer Stacks (existing [[Strategy/Cantus-Customer-Category]] framing) — is the Two-Stacks framing a Tier-1 simplification of the six vectors, or does it get superseded?
  - Treatment of the Crusoe-style vertically integrated competitor class.
  - At what threshold does Cantus become a direct Power Asset operator? (Compounding phase, but criteria need explicit articulation.)
  - Power Studio target form for Year 10+ — Brookfield-style multi-asset infra, Stonepeak-style focused infrastructure, EQT-style sector-specialized, or sui generis.
  - Permian-specific Cantus Land strategy given multi-use overlap of surface, mineral, water, power.
  - Water rights as a separate Power-sector function or nested inside Power Land.
  - Boundary between captive vs. market output in Power Industries → Power Commodities classification.
  - CII surface externalization criteria and DealOS internal-only vs. market-product question.
- No `_parameters.md` updates in this batch; the sub-industry pages cite parameters but do not introduce new ones. Parameter updates will follow the thesis rewrite.
- No NPI material crossed. No identity-claim language used (no "the BlackRock of X" framing). Cantus Forge not referenced; Cantus Prime referenced where relevant. Hopkins not signed; author of record Dom Espinosa throughout.

**Author:** Dom Espinosa

## [2026-05-05] revision | Cantus Primer v3 — Integrated Intelligence voice

**Source:** Dom-authored writing style prompt ("Integrated Intelligence" — partner voice, terseness, anti-AI-marker discipline, opinionated stance, in-motion opening, no speaker introduction). Applied to the v2 primer to produce v3.

**Action:**
- **Rewrote** `~/Documents/Cantus/Deliverables/Cantus-Primer-Infrastructure-Operators-2026-05-05.docx` (overwrites v2). Same six-section structure (backdrop → silo diagnosis → pull quote → what Cantus does → pipeline → where this ends), restated in first-person partner voice with the Vision-Memo register from Rule 6.
- **Added** in-motion opening paragraph before the first heading: *"For several years I've been working at the intersection of AI infrastructure, advanced manufacturing reshoring, and the energy that powers both. What I keep seeing is one problem expressed in different vocabularies, and a structural gap nobody is built to fill. This is what Cantus is for."* No speaker introduction; the voice arrives by way of the work.
- **Folded** the speaker into the body where it earns its place: *"Cantus is the integrated developer for power-heavy industrial demand — the firm I'm building to fill the gap above."* One first-person grounding in the architecture paragraph; the rest stays third-person institutional.
- **Tightened** the silo diagnosis closing into three short fragment sentences ("The bottleneck for this cycle is execution capacity. Not real estate. Not capital.") for sentence-rhythm variation per Rule 3.
- **Promoted** The Sentence to a standalone centered paragraph at the close, replacing the v2 author footer. The Sentence is the punch line; it earns the visual emphasis. Author of record carried in docx properties + the subtitle line "The Cantus Company  |  May 2026  |  Confidential" rather than a redundant footer.
- **Compressed** "What Cantus does" two paragraphs back into one (saved a paragraph break for page-fit) and trimmed the closing paragraph to fit one US Letter page.
- **Updated** wiki markdown mirror to match.

**Cross-links added:** None new — same as v2.

**Audience:** partner (co-development / venture context).

**Notes:**
- AI marker check passed: no *vibrant, tapestry, unleash, delve, comprehensive, leverage, robust, seamless, navigate, transformative, world-class, best-in-class*. No connective ticks (*Furthermore, Moreover, Indeed*, sentence-initial *Importantly*). No throat-clearing openers.
- Em-dash count moderate — used for emphasis and parenthetical, not as the load-bearing rhythm device. Sentence-rhythm variation achieved via fragment punctuation in the silo diagnosis closing rather than dash overuse.
- Opinionated stance preserved without overclaiming. The strongest position is in the silo diagnosis ("The integrated capability barely exists today") and the pull quote ("nobody is reliably providing it"). The closing avoids the Vision-Memo's "Nobody occupies the position we are building" framing per the prior tone audit.
- All `_parameters.md` numbers preserved unchanged.
- Same docx filename — v2 is overwritten. Iteration trail preserved in this log entry sequence.

**Author:** Dom Espinosa

## [2026-05-05] revision | Cantus Primer v2 — backdrop + silo diagnosis added

**Source:** Dom feedback on v1 primer after reviewing the March 2026 Vision & Opportunity Memo (`raw/agentic/Cantus_Vision_and_Opportunity_Memo.docx`) — wanted the operator primer to incorporate the memo's strengths around (a) market backdrop and (b) "how Cantus helps" via the silo diagnosis.

**Action:**
- **Restructured** `~/Documents/Cantus/Deliverables/Cantus-Primer-Infrastructure-Operators-2026-05-05.docx` (overwrites v1, same filename per single-source-of-truth convention). New structure: The Backdrop → Why Nobody Else Fits → Time-to-Operational pull quote → What Cantus Does → Pipeline → Where This Ends.
- **Added** "The Backdrop" section: three forces compressed (40x power density step-up; semiconductor and battery reshoring under CHIPS/IRA; ~18B sq ft of mostly 40+ year old industrial base). Numbers sourced from the Vision Memo; tone calibrated to operator audience (no superlatives, no "largest buildout since postwar").
- **Added** "Why Nobody Else Fits" section: silo diagnosis adapted from the Vision Memo. Real estate / energy / tech-and-capital / engineering — each sees one face. Closes on the bottleneck claim.
- **Removed** the separate Customer Category section (was 110 words). The Customer Category framing is now folded into the closing paragraph as the answer to "what does Cantus serve" rather than as a standalone framework dump.
- **Removed** the separate "Operating problem" section. The operating problem is now established by the combination of Backdrop + Silo Diagnosis.
- **Renamed** closing section "Why integrated, and where it ends" → "Where this ends." The "why integrated" argument is now carried by the silo diagnosis upstream; the closing focuses on customer category, strategic endpoint, financial horizon, and The Sentence.
- **Updated** wiki markdown mirror at `Cantus-wiki/Deliverables/Cantus-Primer-Infrastructure-Operators-2026-05-05.md` to match.

**Cross-links added:** Markdown mirror now references the Vision & Opportunity Memo as a structural source in its preamble.

**Audience:** partner (co-development / venture context).

**Notes:**
- Tone audit on the new content: no "largest buildout since postwar," no "Nobody occupies the position we are building" — the two specific moments in the Vision Memo that edged toward overstatement were not imported. Substantive directness preserved.
- Single page constraint maintained (US Letter, 0.5" top/bottom margins, 0.7" left/right, 11pt Calibri body, navy `#1F2A44` headings).
- All `_parameters.md` numbers preserved unchanged from v1.
- Same docx filename — v1 is overwritten. If audit trail matters, the v1 content is preserved in the prior log entry's narrative + the v1 markdown mirror was overwritten in this revision (both v1 and v2 content can be reconstructed from log entries).

**Author:** Dom Espinosa

## [2026-05-05] deliverable | Cantus Primer for Infrastructure Operators

**Source:** Custom one-page primer requested by Dom for 2026-05-06 dinner with two current/former Tesla infrastructure operators discussing potential venture partnership.
**Action:**
- **Created** docx deliverable at `~/Documents/Cantus/Deliverables/Cantus-Primer-Infrastructure-Operators-2026-05-05.docx`. Single US Letter page. Cantus standard formatting (Calibri 11pt body, navy `#1F2A44` headings, one centered pull quote on Time-to-Operational). Six sections: What Cantus is / Customer Category / Operating Problem / What Cantus Delivers / Pipeline / Why Integrated and Where It Ends. Closes with The Sentence.
- **Created** markdown mirror at `Cantus-wiki/Deliverables/Cantus-Primer-Infrastructure-Operators-2026-05-05.md` (type: gtm, gtm_area: positioning, target_audience: co_dev_partner). `working_files:` frontmatter cites the docx.
- Calibration choices: led with operating-firm framing (developer, not advisory), used Brockman-style input-transformation framing without naming Brockman, surfaced specific pipeline numbers from `_parameters.md`, emphasized vertical-capability logic in the closing ("the same logic the most demanding operators apply inside their own walls"), avoided capital architecture and fund mechanics entirely (per the Tesla-operator audience read).

**Cross-links added:** New deliverable page → [[Strategy/Cantus-Framework]], [[Strategy/Cantus-Customer-Category]], [[Strategy/Bridge-to-Grid-Thesis]], [[_parameters]].

**Audience:** partner (co-development / venture context).

**Notes:**
- Tone audit: no "Cantus Forge," "Caesar," "best-in-class," "world-class," "transformative," exclamation points, or comparable-driven identity claims. The phrase "the most demanding operators" is generic — does not name Tesla.
- Numbers cited: Year 6 FCF $100M, Year 10 $300–500M, Year 15 $750M–$1B; campus model 300+150+50 = 500 MW with $90/MWh AI blended and $55/MWh manufacturing; near-term sites 50–180 MW (2027 energization); large sites 500 MW – 1 GW (Q4 2028 / Q1 2029); 200–300 MW manufacturing tenant discussions; 50 mi Houston CBD radius; Bridge-to-Grid 12–18 months vs interconnection 36–48 months. All sourced from `_parameters.md` and the Cantus Framework Part 1.
- Format compression: required margin reduction to 0.5"/0.7" and a single combined closing paragraph (Why Integrated + The Sentence) to fit one page while preserving all substantive content. Standard Cantus 11pt body retained.
- Pull quote: "Time-to-Operational is the deliverable that matters, and nobody is reliably providing it." — chosen as the single load-bearing claim the audience should leave with.

**Author:** Dom Espinosa

## [2026-05-05] ingest | Cantus Framework Amendment — Customer Category 1

**Source:** `raw/agentic/cantus_framework_amendment_customer_category_1.docx` (Dom-authored amendment to the Cantus Framework, dropped 2026-05-05)
**Action:**
- **Created** [[Strategy/Cantus-Customer-Category]] (type: framework, framework_layer: 1, audience: capital_partner) — full canonical wiki articulation of the unified Customer Category. Cites the source docx via `working_files:`. Five defining characteristics (industrial scale, globally competitive output, input-transformation business model, energy/infrastructure intensity, strategic significance to American industrial capacity). Five sub-categories with tier prioritization (Hyperscale AI + Adv mfg → Tier 1; Energy transition + Sovereign-aligned → Tier 2; Adjacent industrial → Tier 3). Closing "Open Questions to Resolve" section flags Criterion 5 calibration, Foundation Two rewrite scope, energy transition tenant economics, and customer education sequencing.
- **Updated** [[Strategy/Cantus-Framework]] — added "The Two Stacks Are Dominant Expressions of a Unified Customer Category" section after the Two Factory Stacks table. Rewrote Foundation Two to position Technology Integration as native to the entire Customer Category, alongside Energy Execution rather than below it. Frontmatter `related_pages` populated; `updated` bumped to 2026-05-05.
- **Updated** `_README.md` terminology table — added "Cantus Customer Category" as umbrella strategic articulation, recontextualized "Two Customer Stacks" as dominant current expression of the Category, added "Input-transformation arbitrage" as the structural shape, augmented Two Foundations row to note Technology Integration is category-native.
- **Updated** `_parameters.md` Tenant Power Price Tolerance Spectrum — added Energy Transition sub-category section with 7 indicative ranges (green hydrogen, DAC, post-combustion CCUS, e-fuels/SAF, utility-scale BESS, utility-scale solar developer ops, advanced nuclear developer). All marked as estimates pending Dom-side validation. Change Log updated.
- **Updated** `index.md` Strategy table — added new page row.

**Cross-links added:**
- [[Strategy/Cantus-Customer-Category]] ↔ [[Strategy/Cantus-Framework]] (bidirectional, both directions of related_pages and inline section anchors)
- [[Strategy/Cantus-Customer-Category]] → [[Strategy/Cantus-Framework-Layers-2-3-4]], [[Strategy/Bridge-to-Grid-Thesis]], [[Strategy/Primary-Inputs-02-Energy-Execution]], [[Strategy/Market-Sizing]], [[Products/CII-Iteration-Document]], [[_parameters]]
- `_parameters.md` Energy Transition section → [[Strategy/Cantus-Customer-Category]]

**Audience:** capital_partner (new page) + internal (terminology, parameters)

**Notes:**
- Source docx preserved at `raw/agentic/cantus_framework_amendment_customer_category_1.docx` as persistent asset (cited by the new wiki page via `working_files:`). The `agentic/` subfolder is a new convention introduced by Dom; left in place rather than relocating into existing raw/ subfolders.
- The amendment does not retire the two-vertical articulation — it situates AI Factory and Manufacturing Factory as the dominant current expression of the broader Cantus Customer Category. Both terms now coexist in the terminology table with the umbrella above the operational subset.
- Foundation Two rewrite is light-touch in this ingest. The amendment's "Open Questions to Resolve" section flags whether a fuller Foundation Two memo is warranted; deferred to Dom.
- Criterion 5 ("strategic significance to American industrial capacity") preserved as written in the source. Calibration concern surfaced in the new page's Open Questions section: capital partner categories include sovereign wealth across allied jurisdictions (Saudi PIF, Singapore GIC, Norwegian NBIM per `_parameters.md`); decision pending on whether the American frame is load-bearing or one expression of broader strategic-significance language flexed by audience.
- Energy Transition tenant economics were missing from `_parameters.md` prior to this ingest. Indicative ranges added but explicitly marked as estimates pending validation — do not cite in capital partner material until validated.
- Tier movement language ("operational, not architectural; earned through capability build") captured in the new page as a planning principle.
- No NPI material crossed the firewall in this ingest. Energy transition customer base discussion is conceptual / category-level; no specific NPI counterparties referenced.

**Author:** Dom Espinosa

## [2026-05-04] init | Cantus-wiki vault initialized

**Action:** Created vault skeleton at `~/Documents/Cantus-wiki/`. Folder tree, `_README.md`, `_cowork-context.md` (promoted from prior unified vault `obsidian/Cantus/`), `_parameters.md` (promoted), `index.md` (empty structure), this log, `ONBOARDING.md`.
**Cross-links added:** none yet — content migration is Phase 4.
**Audience:** internal
**Notes:** Vault is the agent-maintained markdown surface for The Cantus Company. Working files surface lives at `~/Documents/Cantus/`. Wiki references working files via `working_files:` frontmatter. Phase 4 migration will populate Strategy, Products, GTM, Vision, etc. from the prior unified `obsidian/` vault. DealOS migrates here from `obsidian/DealOS/` per Dom's classification — DealOS is a Cantus play. Until migration completes, this vault is empty of Cantus content. The prior `obsidian/` vault remains intact; nothing has been deleted.
**Author:** Dom Espinosa

## [2026-05-04] migration | Phase 4 content migration from prior unified vault

**Source:** `~/Documents/obsidian/` (prior unified Cantus + NPI + Personal vault)
**Action:** Created and populated the following from the prior unified vault:
- `Strategy/` — 9 foundational strategy pages migrated with new schema (`Cantus-Framework`, `Cantus-Framework-Layers-2-3-4`, `Layers`, `Primary-Inputs-01-Land-Aggregation`, `Primary-Inputs-02-Energy-Execution`, `Primary-Inputs-03-Labor-Community`, `Market-Sizing`, `Bridge-to-Grid-Thesis`, `Advanced-Industrial-Spec`). Type assignments: framework, thesis, or strategy per `_README.md` schemas. Audience: capital_partner for the foundational thesis pages, internal for in-progress sketches. Layer-2-3-4 doc was copied verbatim per the brief's note that the Tier-1 architecture workshop is still active — Layer 1 references in the doc are not edited until that workshop resolves.
- `Products/` — `CII-Iteration-Document` migrated as `type: product`, `audience: internal`.
- `GTM/` — `Executive-Summary`, `Investor-Deck-Outline`, `Team-and-Org`, `Go-To-Market-Plan` migrated as `type: gtm`. (`Cerebras-Outreach-Draft` migrated to Newmark-wiki/Marketing per Dom's classification — treated as NPI tenant-rep work, not a Cantus direct pitch.)
- `DealOS/` — 12 pages from `obsidian/DealOS/` reclassified from generic to `type: dealos_spec`, `audience: internal` per Dom's call. Folder structure preserved (`Architecture/`, `Founding-Team/`, `Founding-Vision.md`, `GTM/`, `Product/`, `README.md`).
- `Vision/` — `Tier-1-Architecture` (active workshop), `Parking-Lot`, `_README.md` migrated.
- `Workshop/Active/` — `Hopkins-Performance-Tuning` (verbatim from prior vault) and `Unified-AI-Native-Knowledge-Platform` (with an explicit Cantus-side note that the CII data-asset / loops / surfaces decomposition is the closest precedent if the firm ever builds against this market gap).
- `Reference/` — `Hopkins-Persona` scoped to Cantus tone register (separate from the NPI version in Newmark-wiki). `Crusoe-Structural-Reference` created with `audience: internal` and an explicit "internal structural comparable; not for external Cantus articulation" banner per the Cantus voice ban on Crusoe references in external material.
- `Strategy/ERCOT-Positioning-Thesis.md` — created fresh as the Cantus-side fork of the ERCOT regulatory framework. Reframes the regulatory facts as a firm positioning thesis: "Texas's large-load interconnection regime selects for the integrated developer." Audience: capital_partner.
- `Deliverables/` — 8 polished docx exports copied from `obsidian/Cantus/Deliverables/`.

**Cross-links added:** Strategy ↔ Strategy and Strategy ↔ Reference where applicable. Wikilinks vault-wide rewritten via sed pass (`Cantus/Strategy/X` → `Strategy/X`, `Hopkins/Hopkins-Persona` → `Reference/Hopkins-Persona`, `Intelligence/Cantus/ERCOT-Large-Load-Interconnection-Framework` → `Strategy/ERCOT-Positioning-Thesis`). Cross-vault wikilinks (to Newmark-wiki content) converted to plain-text "see Newmark-wiki/..." references per the firewall.

**Audience:** Mixed — see per-page `audience:` field.
**Notes:**
- Source pages in `~/Documents/obsidian/Cantus/` and `~/Documents/obsidian/DealOS/` were marked `status: archived` per Dom's preservation choice (copy-then-archive).
- Tone audit: no "Cantus Forge," "Caesar," "Rubicon," or "best-in-class" superlative occurrences in body content of the migrated Strategy/Products/GTM pages. The active Tier-1-Architecture workshop doc legitimately discusses the Forge → Prime retirement and is preserved verbatim.
- Tags cleanup pass on Companies in Newmark-wiki stripped the `cantus` tag (per firewall); Cantus-wiki pages keep their existing tags.
- Index.md fully rebuilt with per-section tables enumerating migrated pages.

**Author:** Dom Espinosa
