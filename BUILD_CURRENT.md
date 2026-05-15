# EWP Practice Impact — Current Build Document

**Live URL:** https://ewp-practice-impact-production.up.railway.app/
**Repository:** https://github.com/beckySB/ewp-practice-impact
**Deployment:** Railway (auto-deploy from `main` branch)
**Access Gate:** Code `1857` (sessionStorage-persisted)
**Generated:** May 15, 2026

---

## Strategic Frame (Governs All Copy)

This document is a field perspective delivered to Northwestern Mutual home office. It is not a commercial proposal, a product pitch, or a personal practice showcase. It exists to surface a strategic problem and demonstrate that a working process-backed methodology for sophisticated business owner planning has been built and tested inside the firm.

### The one-sentence positioning

> A structured operating model for sophisticated business owner planning, built and tested inside NM, designed to be replicable, and aligned to the firm's compliance and product architecture.

### The dominant phrase: process-backed methodology

The deck uses **process-backed methodology** as its dominant descriptor. The compound phrase carries both halves of the institutional argument:

- **Process-backed** signals proven, executable, repeatable, validated through actual use
- **Methodology** retains the framework-level signal of analytical depth and intellectual seriousness

After the compound phrase has been established in a section's opening, subsequent references can shorten to *the process* or *the methodology* alone.

### NM AI Strategy Alignment

On May 12, 2026, Northwestern Mutual published its AI strategy through Field Focus and the *Ops & Tech* article. The firm's stated posture: buy, build, integrate (model-agnostic), prioritize AI that scales safely across the field. The deck carries NM's vocabulary — model-agnostic, integration-first, compose across workflows, scale safely — without directly quoting the framework.

**Meeting-only intelligence (not in the deck):**
- Hybrid buy-vs-build answer: methodology becomes NM IP, platform integrates as model-agnostic tool the firm can shape or internalize
- $150M Future Ventures commitment opens structural options (licensing, partnership, venture investment)
- Optional opener: *"I saw the Field Focus episode and the buy-vs-build piece this week. A lot of what I want to share today actually fits inside that frame."*

### What must not appear in deployed copy

- Software/AI/platform described as built outside the firm
- Pricing, licensing, proposal language
- Direct quotation of NM's four priorities or buy-vs-build framework
- Reference to $150M Future Ventures
- Personal first names, anecdotes, "what I do with clients" framing
- PiroScope vocabulary (customer concentration, operational maturity, churn cohorts, unit economics)

### IP Boundary Discipline

Continuum and PiroScope are independent products. Non-overlapping audiences, non-overlapping problem domains. They do not integrate, are not on a shared roadmap, and should never be cross-referenced.

---

## Architecture

| Layer | Technology |
|-------|-----------|
| Type | Static single-page HTML (all CSS + JS embedded in `index.html`) |
| Hosting | Railway via `npx serve . -l $PORT -s` |
| Build | Nixpacks (Railway default) |
| Fonts | Google Fonts: Playfair Display (headings), Nunito (body) |
| Images | `images/hero-bg.png` (golden waves), `images/closing-bg.png` (navy marble) |
| Responsive | CSS media queries at 1024px and 640px |
| Access Control | Client-side gate (code `1857`), sessionStorage persistence |

### File Structure

```
ewp-practice-impact/
├── index.html              # Single-file site (1558 lines)
├── BUILD_CURRENT.md        # This build document
├── package.json            # serve ^14.0.0
├── railway.json            # Railway deploy config
├── .gitignore              # node_modules/, .DS_Store
└── images/
    ├── hero-bg.png
    └── closing-bg.png
```

---

## Design System

### Colors (CSS Custom Properties)

| Token | Hex | Usage |
|-------|-----|-------|
| `--navy` | `#1B2E4A` | Primary dark backgrounds, headings |
| `--navy-light` | `#243B5A` | Access gate input background |
| `--gold` | `#C9A962` | Accent, labels, borders, ornaments, stat numbers |
| `--cream` | `#FAF8F5` | Light section backgrounds |
| `--cream-light` | `#FAF6F0` | Card backgrounds |
| `--cream-warm` | `#F5EFE3` | Four Questions background |
| `--white` | `#FFFFFF` | Alternate section backgrounds |
| `--light-teal` | `#E8F4F6` | Spine callout backgrounds, flip card backs |
| `--teal` | `#2A7F8C` | Spine callout accents, eyebrow text |
| `--teal-deep` | `#1F5E6A` | Spine subhead, thesis text |
| `--text-dark` | `#1B2E4A` | Headings, dark body text |
| `--text-body` | `#6B6560` | Body text |
| `--text-body-alt` | `#5A5550` | Darker body text |
| `--text-muted` | `#8A8580` | Muted labels |
| `--text-light` | `#C8C0B8` | Light text on dark |
| `--text-cream` | `#E0DCD6` | Cream text on dark |
| `--border` | `#E8E2D8` | Card/divider borders |

Gold also has alpha variants: `--gold-20` (20%), `--gold-40`, `--gold-50`, `--gold-60`, `--gold-80`.

### Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| Hero headline | Playfair Display italic | 400 | 72px |
| Section headings | Playfair Display | 700 | 44px |
| Spine heading | Playfair Display | — | 56px |
| Spine subhead | Playfair Display italic | — | 30px |
| Pillars thesis | Playfair Display | 600 | 32px |
| Quote text | Playfair Display italic | — | 36px |
| Flip card titles (front) | Playfair Display | — | 28px |
| Flip card titles (back) | Playfair Display italic | — | 22px |
| Stat numbers | Playfair Display | 700 | 68px |
| Body text | Nunito | 400-600 | 14-22px |
| Section labels | Nunito | 600 | 16px, 3px spacing |
| Eyebrows | Nunito | 700 | 11-13px, 2-3px spacing |

---

## Deployed Sections (Current State)

### Section 1: Access Gate

Full-screen fixed overlay on navy background. Gold "ETERNAL WEALTH PARTNERS" eyebrow, "Access Code" heading, 4-digit numeric input. Code `1857` auto-submits on 4th digit, fades overlay over 300ms. Wrong code shows "Invalid code" for 2 seconds. Persisted in `sessionStorage` as key `ewp-access`.

### Section 2: Hero

**Background:** Full viewport height. `hero-bg.png` with multi-stop gradient: `#1B2E4AE0` (0%) through `#FAF8F5` (100%).

**Current deployed content:**
- Gold-bordered badge: *"Eternal Wealth Partners · A Field Perspective for Northwestern Mutual Home Office"*
- Headline: *"Where the Business Owner Plan Lives"*
- Subhead: *"Twenty years in the field. A process-backed methodology for the most under-served, most lucrative segment we serve."*
- Three stat blocks: **$124T** Wealth in Transfer Through 2048 | **12M** Boomer-Owned Businesses Exiting | **37%** Of Advisors Retiring This Decade
- Gold ornament: — ✦ —

**Note:** Hero tagline ("The pages that follow are the answer.") was removed. CSS class `.hero-tagline` remains in stylesheet but no element uses it.

### Section 3: Four Questions

**Background:** Cream-warm with top border.

**Current deployed content:**
- Gold label: *"The Four Questions This Document Answers"*
- Four question rows, each with decorative gold `?` and numbered label:
  - **Q01:** "Where does the firm's existing investment in sophisticated planning talent, credentials, and home office services compound, and where does it leak?"
  - **Q02:** "In a decade where 37% of advisors transition and the business owner segment becomes the largest planning event of a generation, what infrastructure does the field force need to hold both at once?"
  - **Q03:** "When the firm's most complex planning work is happening in spreadsheets and external tools, who owns the data, the workflow, and the firm's intellectual property in the segment?"
  - **Q04:** "What does the operating layer for Northwestern Mutual's business owner planning look like?"
- Closing: *"The pages that follow answer each one in turn."*

### Section 4: Market in Transition

**Background:** Cream.

**Current deployed content:**
- Label: *"The Market in Transition · Answering Questions 01 and 04"*
- Heading: *"The supply curve and the demand curve are crossing."* (italic)
- Lead: Three demographic forces converging. Each alone would be the largest planning event of a generation.
- **Three stat cards** (gold top border, cream-light background):
  - **$124T** — WEALTH IN TRANSFER: Through 2048. 81% from Baby Boomers. Half from households representing 2% of the population.
  - **12M** — BUSINESSES CHANGING HANDS: ~$10T in business assets in motion. McKinsey projects $5T come to market. Of ~510,000 small/medium US businesses that exited in 2022, 92% exited via closure, not sale (McKinsey Institute for Economic Mobility, 2026). "Transferability is the difference between a transition and a payout."
  - **37%** — ADVISORS TRANSITIONING: $10.4T in client assets. 26% unsure of succession plan (Cerulli).
- Closing: *"The convergence creates the opportunity. The fragmentation of the work prevents the field from capturing it."*

### Section 5: Market Reality

**Background:** White.

**Current deployed content:**
- Label: *"What is happening in the field right now"*
- Heading: *"The build is happening with or without us."*
- **Four body paragraphs:**
  1. Names the 1,498 CFP base (largest in the IBD channel). Advisors doing sophisticated work in spreadsheets, Word docs, outside tools. "The talent and the credential are there. The operating layer is not."
  2. NM has acknowledged the gap — white-labeled valuation platform for one pillar, evaluating next-gen tooling. "The next four years are the window." Closes with model-agnostic, integration-first, compose-across-workflows language.
  3. Three dimensions of data sovereignty risk: regulatory responsibility, commercial asset, strategic moat. "The longer the operating layer stays outside the firm, the more of those three the firm gives up."
  4. Competitive context: larger independent RIAs, major family office platforms, PE-backed wealth aggregators building from the segment outward. NM has deeper credentials but not the field-side operating layer.

- **Three cards** (gold top border, centered gold — ✦ — ornament, navy bold title, italic body):
  - **The piece that exists.** "The firm has built and licensed infrastructure for parts of the financial mechanics of business owner planning. Each piece addresses a slice of the work. None of them run together, and none of them define the larger discipline they sit inside."
  - **The work that runs without a home.** "Values work. Cash flow modeling. Risk and investment audit. Tax strategy. Exit planning. Legacy work. The dimensions that make up a business owner's plan happen in the field today, in spreadsheets, in third-party tools, in the advisor's experience. No firm-owned architecture."
  - **The environment that does not exist.** "A business owner plan is the integration of those dimensions, not the sum of them. There is no single environment where the firm runs them together for a client. The pieces that exist do not connect. The plan lives in fragments."

- **Closing paragraph:** "The methodology and Contnuum are designed to complete what the white-label has started. One workspace. Seven pillars... The strategic question this raises is not whether the workspace gets built. It is who builds it, and whether the operating layer that results is built deliberately for the firm Northwestern Mutual has spent decades becoming."
- **Pull quote:** *"The market is moving. The question is what version of this story Northwestern Mutual writes."* (centered, gold ornaments above and below)

### Section 6: Quote

**Background:** Navy.

- Opening quotation mark decorative element
- *"The supply of advisors who can serve sophisticated business owner planning is shrinking at exactly the moment demand is reaching record highs."*
- Closing quotation mark
- Attribution: *"A field perspective on a structural problem."*

### Section 7: The Spine

**Background:** Cream.

**Current deployed content:**
- Label: *"The Spine of This Document"*
- Heading: *"The Seven Pillars are the process-backed methodology."*
- Subhead: *"Contnuum is the operating system that lets a firm built for advanced planning actually deliver it at scale."*
- **Paragraph 1:** Names NM's existing investment — CFP base, Sophisticated Planning Strategies team, Estate and Business Planning Specialists, Schools at home office. "The firm has built itself to be a sophisticated planning firm."
- **Paragraph 2:** "The Seven Pillars are the process-backed methodology that delivers sophisticated business owner planning. Contnuum is the operating system that runs the process across the field force, designed model-agnostic and integration-ready to sit inside the firm's existing AI architecture."
- **Callout 1 — "What the system does":** Three items: deepens client relationship, drives plan implementation (NM-approved language, handoffs to Concierge Planning / Private Client Services / Fee-Based Planning), makes team's job easier (notes flow, visualizations populate, senior advisor stops being bottleneck).
- **Callout 2 — "Built for the firm's compliance posture":** SOC2, FINRA/SEC audit-ready, single-tenant data sovereignty, explainable and model-agnostic AI, complete audit trail. "Mature enough to scale safely and responsibly across the field."
- **Callout 3 — "Why one workspace matters":** Heading: *"One process. One workspace. The math reconciles across pillars."* Formula integrity argument. PX integration so personal plan and business plan reconcile. "The plan holds up. The numbers hold up across pillars." Makes the plan defensible to client, CPA, attorney, and the firm.

### Section 8: Seven Pillars with Flip Cards

**Background:** White.

- Label: *"The Process-Backed Methodology · Answering All Four Questions"*
- Heading: *"Seven Pillars, Seven Flip Panels."*
- Axis: BUSINESS ← YOU → FAMILY (centered, teal, uppercase)
- Thesis: *"The Seven Pillars are the process-backed methodology. Contnuum is the workflow that lets a great wealth advisor deliver them."*
- Framing: The process and Contnuum remove the demand for advisors to operate as CPAs, attorneys, analysts. "Each card flips to show what changes for the advisor and the team when the workflow runs."

**Flip Card System:** CSS 3D transforms (perspective 1400px, rotateY 180deg, backface-visibility hidden). Toggle via `onclick`. Front: cream-light with navy left border. Back: light-teal with gold left border.

| Pillar | Title | Front Content | Back Pattern |
|--------|-------|---------------|-------------|
| 01 | Values & Vision | EWP Discovery Sequence, vision statements, Growth/Liquidity/Control ranking | Gap: structured discovery needed → Contnuum runs guided path → "The advisor stays a wealth advisor. The conversation that anchors every later pillar actually happens." |
| 02 | Cash Flow & Balance Sheet Alignment | Eternal Wealth Snapshot, Guardrails, multi-year profitability trend, 4-week vacation test | Gap: cash flow as living model → Recommendations integrated as inputs → "The plan gets the sustainability it should have had." |
| 03 | Risk & Investment Audit | Personal/business protection inventory, Buy-Sell review, key person, executive carve-out | Gap: reading legal docs, modeling exposure → Contnuum reads agreement, calculates funding gap → "The case gets the depth it should have had." |
| 04 | Lifetime Tax-Efficient Strategy | Multi-decade tax strategy, RSU/ISO/NSO/ESOP/83B/AMT, entity structures | Gap: tracking tax events from memory → Contnuum tracks events, surfaces implications → "The plan gets the multi-year tax efficiency it should have had." |
| 05 | Business Valuation | Enterprise value, five value drivers, Exit Gap, Value Acceleration Roadmap | Gap: estimating vs quantifying → Contnuum runs valuation, Transferability Score, Exit Gap → "The case gets the analytical rigor it should have had." |
| 06 | Exit & Transition Planning | Exit Readiness Assessment, Strategy Options, Multi-Year Roadmap, Post-Exit Income Plan. 76% post-exit regret (EPI 2023). | Gap: exits not run as planned campaigns → Contnuum builds roadmap backward from exit date → "The exit gets the runway it should have had." |
| 07 | Legacy & Estate Planning | Wills, Trusts, Asset Ownership, Generation Skipping, Liquidity at Death, Charitable/Gifting | Gap: advisors are not estate attorneys → Contnuum generates estate diagram, models gifting, routes to Concierge Planning → "The legacy gets the coherence it should have had." |

Every back card ends: *"The advisor stays a wealth advisor. The [domain] gets the [quality] it should have had."*

### Section 9: Revenue and Retention

**Background:** Cream.

- Label: *"Answering Question 01 · Why this compounds"*
- Heading: *"Why business owner relationships compound where personal planning relationships do not."*
- Lead: "The work that compounds for clients also compounds for the firm."
- **Comparison table** (6 rows):

| Dimension | Personal Planning | Business Owner |
|-----------|------------------|----------------|
| First-year insurance premium | $2K-$5K | $30K-$150K+ |
| Insurance sale events over 20 years | 1-2 | 4-7 |
| Pre-event AUM accumulation | $500K-$2M | $1M-$10M+ |
| The liquidity event | None (gradual drawdown) | $5M-$50M+ deposited |
| Post-event AUM | Decumulating | Compounding into next generation |
| Multi-generational continuation | Sometimes | Almost always |

- Subhead: *"Retention runs in both directions."* — structural stickiness for both client and advisor.
- Pull quote: *"Multiplied across the field force, the segment economics are an order of magnitude larger than any single practice."*

### Section 10: Five Components

**Background:** Cream.

- Label: *"Fully Operationalized · Answering All Four Questions"*
- Heading: *"Five components, one operating model."*
- Lead: "A process-backed methodology this rich, deployed across a field this large, requires more than a training program. It requires an integrated operating model."

**Five component cards** (gold top border):

| # | Title | Current Deployed Description |
|---|-------|------------------------------|
| 01 | The Process-Backed Methodology | Seven Pillars, validated and stress-tested across cases. Documented, repeatable, the same shape for every client. The framework that allows one advisor to hold the whole picture together across two decades of relationship. |
| 02 | The Client Journey | Discovery, valuation, multi-year roadmap, quarterly review, exit readiness, post-exit planning. Same for every client. Teachable, repeatable, reliable across a field force. |
| 03 | The Planning Experience | Eternal Wealth Plan, Eternal Wealth Snapshot, Eternal Wealth Guardrails, Transferability Score, Exit Gap Calculation. Every artifact ties to a pillar. Every pillar ties to a question. |
| 04 | The Platform Substrate · Contnuum | SOC2, FINRA/SEC audit-ready, single-tenant data sovereignty, explainable AI. Built model-agnostic and integration-first — designed to integrate with PX, AILA, LinknetGPT, NMGPT, and NM Connect through API, and to compose with whatever AI models and third-party tools the firm chooses across advisor workflows, not to replace any of them. |
| 05 | The Client-Facing Extension | In the spirit of NM Connect, for business owner clients. Owner sees plan, valuation, roadmap, progress in one place. Advisor sees what client sees plus analytical depth. |

- Closing quote: *"No single component is the answer. The answer is what happens when all five operate together."*
- Closing body: Methodology without platform = binder on shelf. Platform without methodology = software in search of use case. All five must be designed, deployed, and supported together.

### Section 11: Dimensions Worth a Deeper Look (Close)

**Background:** Navy with marble texture overlay (`closing-bg.png`), gradient.

- Gold ornament: — ✦ —
- Label: *"What this conversation could become"*
- Heading: *"The dimensions worth a deeper look."*
- Body: "The pages above are a field perspective on a strategic problem and an operationalized solution to it. They do not describe a commercial proposal."
- **Three dimensions** (numbered, gold bold titles):
  1. **The integration architecture.** How a purpose-built workspace sits alongside what NM has already built, model-agnostic by design and composable across the firm's existing AI workflows.
  2. **The field readiness path.** How the methodology and Contnuum reach the advisors who serve this segment, keeping the wealth advisor operating as a wealth advisor.
  3. **The home office economics.** What the segment looks like at scale, how NM's infrastructure investment compounds when the field can use it consistently.
- Soft close: "The right next step is the one this conversation surfaces... The right rhythm is the one that fits Northwestern Mutual's process."
- Final line: *"The market is moving. The conversation worth having is what Northwestern Mutual chooses to do about it."*

### Section 12: Footer

**Background:** Navy.

- Brand: ETERNAL WEALTH PARTNERS · ESTATE & BUSINESS PLANNING
- Gold divider
- Contact: Becky Gustafson — CFP, MSFP, AEP, CAP, ChFC, CLU, RICP, CASL, LUTCF, CLTC
- Tagline: *"Twenty years in the field, prepared for the conversations that come next."*
- Full-width gold divider
- Disclaimer: Informational only, not financial/tax/legal advice, illustrative revenue figures, individual results vary.

---

## Responsive Behavior

### Tablet (max-width: 1024px)
- Hero: padding 60px 40px, headline 48px, stat numbers 36px, stats gap 32px
- Sections: padding 80px 40px
- Card rows stack vertically (single column)
- Quote text: 24px
- Spine: heading 38px, subhead 22px
- Pillars thesis: 26px
- Revenue table: single column, row headers hidden
- Market Reality grid: single column
- Flip cards: maintain 380px min-height

### Mobile (max-width: 640px)
- Hero: padding 40px 20px, headline 36px, stats stack vertically
- Sections: padding 60px 20px
- All section headings: max 28px
- Spine: heading 32px, subhead 19px, callout padding 28px 24px
- Pillars thesis: 22px
- Flip cards: expand to 460px min-height
- Four Questions: rows collapse to single column
- Dimension items: compressed grid (40px + 1fr), font 18px

---

## Key Statistics and Sources

| Statistic | Value | Source |
|-----------|-------|--------|
| Wealth in transfer | $124T through 2048 | Cerulli Associates |
| Boomer-owned businesses exiting | 12M | Industry standard |
| Business assets in motion | ~$10T | Industry standard |
| Boomer businesses projected to transact | $5T over next decade | McKinsey Institute for Economic Mobility, Feb 2026 |
| Small business exits by closure (2022) | 92% (~510,000 total exits) | McKinsey Institute for Economic Mobility, Feb 2026 |
| Advisors retiring | 37% of workforce | Industry standard |
| Advisor-controlled assets | $10.4T | Cerulli Associates |
| Advisors unsure of succession | 26% | Cerulli Associates |
| NM CFP holders | 1,498 | NM press release, Aug 14, 2024 (Financial Planning IBD Elite) |
| Post-exit regret rate | 76% | Exit Planning Institute, 2023 National State of Owner Readiness Report |

---

## Deployment Configuration

**package.json:**
```json
{
  "name": "ewp-practice-impact",
  "version": "1.0.0",
  "description": "EWP Practice Impact — Where the Business Owner Plan Lives",
  "scripts": { "start": "serve . -l $PORT -s" },
  "dependencies": { "serve": "^14.0.0" }
}
```

**railway.json:**
```json
{
  "$schema": "https://railway.com/railway.schema.json",
  "build": { "builder": "NIXPACKS" },
  "deploy": {
    "startCommand": "npx serve . -l $PORT -s",
    "restartPolicyType": "ON_FAILURE",
    "restartPolicyMaxRetries": 10
  }
}
```

---

## Voice Discipline

- No AI register (no rhythmic triplets, no academic hedging, no breathy adverbs)
- No em-dashes in body copy. Break to two sentences instead. This rule is load-bearing: multiple deployed fixes (Component 04, Spine callouts, earlier edits) trace to em-dash removal. Enforce on every future edit.
- No personal first names, no personal pronouns in methodology descriptions
- Dominant phrase: *process-backed methodology*
- NM AI vocabulary alignment: model-agnostic, integration-first, compose across workflows, scale safely — never directly quoted as NM's framework
- Buy-vs-build question never preempted in deployed copy
- $150M Future Ventures never referenced in deployed copy
- Sources cited where statistics appear
- PiroScope vocabulary does not appear

---

## Pinned Items

### Transferability / Business Readiness Diagnostic
**Status:** Deferred. Dependency: Continuum deliverable spec must inform design before formalization.

### Internal Tool Roadmap / Four-Year Window Basis
**Status:** Active. Anchors all timing language in Section 5.

**Context:** The "next four years are the window" language in Market Reality Paragraph 2 is tied to NM's active evaluation of next-generation business planning tooling for the broader business owner segment. The firm has acknowledged the gap exists and is evaluating what comes next. The four-year window reflects the period in which the operating layer for NM's business owner planning gets decided, before competitive alternatives and external platform migration make the decision for the firm.

**Why this is pinned:** Without this entry, the four-year window framing has no traceable basis in the build document. Any future revision that softens or removes the timing reference risks losing the urgency frame without realizing it is tied to a specific institutional event. The window language must not be revised without reviewing this pin first.

### NM AI Strategy Alignment
**Status:** Active. Vocabulary baked into deck; framework reference held for meeting.

### NM Four AI Priorities — Conversation Mapping (Not in Deck)

| NM Priority | What the methodology delivers |
|---|---|
| Consistent AI support across core workflows | Seven Pillars = core workflow architecture with defined inputs/outputs |
| Accelerate field growth and market impact | Business owner segment is highest-leverage growth segment |
| Reduce non-revenue-generating activity | Workflow collapses 20+ hours of case prep into guided compliant path |
| Unrivaled client outcomes at scale | Technical depth from multiple credentials unified into single workflow |

---

## Full Commit History

```
710383b Initial deploy: EWP Practice Impact standalone page
b391029 Add Lucide icons throughout all card sections
4215370 Sync full UI from Pencil design to HTML
5f9884e Add background textures for hero and closing sections
5ae8358 Rebuild site from NM Home Office revision spec
cd3d95a NM Build Spec revision with flip cards, integration architecture, Contnuum naming
1360d37 feat(market-reality): insert Market Reality section
c41ca6e feat(spine): add compliance posture and formula integrity callouts
91ad03a feat(pillars-intro): rewrite Seven Pillars intro with thesis + wealth advisor framing
afd7830 refactor(pillars): replace all seven flip card backs with workflow-focused copy
dc7d309 refactor: remove Integration Architecture section
1736469 feat(revenue-retention): insert Revenue and Retention section
71c8ef6 refactor: remove Home Office Economics section
b69db2b refactor: remove Structural Point pull quote section
d105fa8 refactor(close): replace 5-dimension close with 3-dimension soft close
2d9caa7 Center Seven Pillars intro block
00158f7 Center pillars thesis and framing blocks
bc94cbb Add investment and legacy plan reference to Pillar 06
99ea0df Simplify Pillar 07 gap statement
cfcbae2 Rewrite Revenue section intro
368f371 Remove 'in the field over twenty years' from Component 01
9fac575 Remove PX sentence from Component 03
23d04b0 Rename 'NM intranet GPT' to 'LinknetGPT' in Component 04
93e3937 Add access code gate (1857)
1fbb47f feat(spine): reframe Spine with operating-system thesis
90edf46 feat(market-reality): reframe with CFP evidence, four-year window, data sovereignty risk
43fe8f3 fix(citation): add Exit Planning Institute citation
d1d11a5 fix(register): replace "the math maths" with professional phrasing
44159e3 fix(close): remove explicit name reference
cf91862 docs: rebuild build document
7be4a94 docs: add Strategic Frame, copy guidance, IP boundary discipline
b401173 fix: institutional capability reframe across deployed copy
7ec5745 fix(four-questions): rewrite all four questions for institutional frame
7f5a2d0 feat(market-reality): add competitive context paragraph
3302bc1 fix: center Market Reality closing paragraph
015f6c2 refactor: shift to process-backed methodology with NM AI strategy alignment
132600f docs: update build doc with process-backed methodology changes
e21dc2a fix(market-reality): rewrite three cards with institutional gap framing
fa04cba feat(market-reality): add gold dash-diamond-dash ornaments to cards
d8d7a9e fix: center gold ornaments on Market Reality cards
641a20a docs: update build doc with Market Reality card reframe
7bf225e fix(hero): remove 'The pages that follow are the answer' tagline
4eaef2c fix(market-reality): rewrite 'The piece that exists' card body
bbeeb24 fix(market-reality): rewrite 'The environment that does not exist' card body
0b8b25b docs: update build doc with hero tagline removal and card body rewrites
47d0675 docs: rebuild build document from scratch
```
