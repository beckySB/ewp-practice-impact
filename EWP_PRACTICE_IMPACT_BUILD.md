# EWP Practice Impact — Build Document

**Live URL:** https://ewp-practice-impact-production.up.railway.app/
**Repository:** https://github.com/beckySB/ewp-practice-impact
**Deployment:** Railway (auto-deploy from `main` branch)
**Access Gate:** Code `1857` required before viewing content (sessionStorage-persisted)

---

## Strategic Frame (Governs All Copy)

This document is a field perspective delivered to Northwestern Mutual home office. It is not a commercial proposal, a product pitch, or a personal practice showcase. It exists to surface a strategic problem and demonstrate that a working operating model for sophisticated business owner planning has been built and tested inside the firm.

### The one-sentence positioning

> A structured operating model for sophisticated business owner planning, built and tested inside NM, designed to be replicable, and aligned to the firm's compliance and product architecture.

Every section serves this sentence. Every paragraph defaults to the language patterns below.

### What the deck is, and what it is not

**The deck is** a field perspective on a structural strategic problem and a demonstration that a working operating model exists. It surfaces the problem in a way home office cannot unsee, demonstrates that the methodology answers a piece of it, and creates the pull so the reader arrives at the deployment question on their own. The intended outcome is the reader asking, in their own words, *how does this reach the field*.

**The deck is not** a software pitch, a product proposal, or a commercial solicitation. The methodology lives inside the firm's compliance and product architecture. The deployment conversation, when it surfaces, is initiated by the firm and structured through proper internal channels.

### What must not appear anywhere in deployed copy

- Software, AI, platform, or technology described as something built outside the firm
- Continuum referenced as a separate commercial product or external service
- Pricing, licensing terms, deal structures, or proposal language
- Any phrasing that could read as soliciting an outside business arrangement
- Personal first names of the practitioner
- Anecdotes, case stories, or "what I do with clients" framing
- PiroScope or operational-diagnostic vocabulary (customer concentration, operational maturity, leadership bench, churn cohorts, unit economics, organizational architecture)

### The protagonist hierarchy

The protagonist of this document is the **operating model** — the methodology, the framework, the workflow, the components. Not the practitioner who built it. The personal pronoun is the enemy of the institutional sale. Strip it from all deployed copy.

| Stop saying | Start saying |
|---|---|
| My methodology | The methodology / This operating model |
| What I do with clients | The advisor workflow / The case process |
| My process | The structured process / The defined framework |
| I've developed | Has been built and tested / EWP has developed |
| My approach to discovery | The structured discovery sequence |
| My deliverables | The standardized deliverables |
| What works for me | What the case data shows |
| Clients I've worked with | Cases run through the framework |
| In my practice | Within the EWP operating environment |
| I've found that | The framework produces |

### The capacity asymmetry thesis

The macro stats establish *scale*. The strategic point is *asymmetry*. The wave of business owner transitions hits Northwestern Mutual's sophisticated planning bench at exactly the moment that bench is thinnest, because tenured advisors are themselves part of the boomer cohort. This is a structural capacity problem, not an open market opportunity.

The Market in Transition and Market Reality sections reinforce that asymmetry rather than celebrate market size. Every macro stat earns its place by connecting to a capacity, retention, or production implication for the firm.

### The macro stat hierarchy and the gap thesis

The $10T and $5T numbers serve different jobs and must not be presented as if they are interchangeable.

- **$10T** represents all boomer-owned business assets transitioning across all transition types (sales, family transfers, ESOPs, closures, liquidations) over roughly twenty years. The gross pool.
- **$5T** is the McKinsey projection of boomer-owned small businesses that will actually transact (be sold) over the next decade. The transactable slice.

The gap between the two is the more powerful story and the direct setup for the methodology's reason to exist. **Roughly half of boomer business value never reaches a buyer.** Of the approximately 510,000 small and medium-sized US businesses that exited the market in 2022, 92% exited via closure, only 5% via sale, and 3% via transfer (McKinsey Institute for Economic Mobility, 2026). Transferability is the difference between a transition and a payout. The methodology exists to close that gap by making businesses transactable.

### The five strategic vulnerabilities the document surfaces

These are the conditions the deck names (directly or indirectly) so the reader recognizes the strategic problem as their own.

1. **The capacity cliff in sophisticated planning.** The most complex planning is delivered by the most tenured advisors, who are themselves retiring into the same wave they were built to serve.
2. **The book transition problem.** Sophisticated business owner clients churn at higher rates during advisor handoffs than mass affluent clients. AUM, premium, and multi-generational relationships are at risk in every transition event.
3. **The competitive squeeze.** RIAs, family offices, and PE-backed wealth platforms are targeting the same demographic with planning-led front doors. A product-led brand is a liability in this segment.
4. **The compliance throughput ceiling.** Sophisticated planning at scale strains existing compliance review architecture. Advanced case volume cannot grow on current rails.
5. **The advisor recruiting story.** Top candidates choose firms based on infrastructure for complex cases. The firm needs a narrative that says *built for the complexity wave*, not *we will train you on it*.

### The CFO and Chief Field Officer language pattern

This audience does not buy demographic education or thought leadership. They buy production per advisor, retention impact, override impact, capacity solutions, and frictionless compliant delivery. Every section that touches the firm's economics speaks in those terms. The methodology is positioned as the operating arm that converts the transition wave into measurable, repeatable advisor production without adding headcount, without rebuilding compliance, and without depending on advisor talent variance.

### The credential paradox

The CFP, MSFP, AEP, CAP, ChFC, CLU, RICP, CASL, LUTCF, CLTC stack establishes technical depth. It does not establish that scaling the methodology requires replicating the practitioner.

Credentials are framed as *what the methodology codifies and operationalizes into a workflow advisors can execute*, not as *what makes the practitioner uniquely capable*. The intended read is that the methodology captures the technical depth typically scattered across multiple advanced credentials into a unified workflow that scales across advisors who hold a working subset of those designations.

### The "create the pull" close posture

The deck demonstrates a working operating model and ends on a question, not a proposal. The intent is to lead the reader to ask *how does this reach the field*, and to leave that question with them. The follow-up conversation, structured through proper firm channels, is where deployment architecture gets discussed.

A methodology that reads as *evolving* and *building* signals a working system. Static methodologies look dead. The deck reflects a living, developing capability — not a finished product looking for a buyer.

### The "system, not artistry" pattern

Show artifacts. Name components. Describe workflows. Avoid anecdotes, case stories, and "what I do" framing. Every methodology section earns its place by featuring a named framework or visible deliverable, not by demonstrating skill.

The methodology slide is a product catalog of operating components, not a portfolio of personal techniques.

### IP Boundary Discipline (Cross-Project Working Principle)

Continuum and PiroScope are independent products with non-overlapping audiences and non-overlapping problem domains.

- **Continuum:** Built for financial advisors serving sophisticated business owner clients. Wealth management and exit planning operating system. Audience: NM home office (the strategic deployment buyer) and NM advisors (the end users).
- **PiroScope:** Built for business owners and operators directly. Operational diagnostics on the business itself. Different audience, different buyer, different problem domain.

The two products will not integrate. They are not on a shared roadmap. The shared demographic context (business owners) does not constitute product adjacency. They should never be presented together, cross-referenced, or described as part of the same product family. The vocabulary firewall between them must remain clean.

This principle applies across both project folders.

---

## Architecture

| Layer | Technology |
|-------|-----------|
| Type | Static single-page HTML site |
| Hosting | Railway via `npx serve . -l $PORT -s` |
| Build System | Nixpacks (Railway default) |
| Fonts | Google Fonts (Playfair Display, Nunito) |
| Images | Local (`images/hero-bg.png`, `images/closing-bg.png`) |
| Responsive | CSS media queries at 1024px and 640px breakpoints |
| Access Control | Client-side code gate (1857), sessionStorage persistence |

### File Structure

```
ewp-practice-impact/
├── index.html                          # Single-file site (HTML + embedded CSS + JS)
├── EWP_PRACTICE_IMPACT_BUILD.md        # This build document
├── package.json                        # Dependency: serve ^14.0.0
├── railway.json                        # Railway deploy config
├── .gitignore                          # node_modules/, .DS_Store
└── images/
    ├── hero-bg.png                     # Dark navy waves with golden thread texture
    └── closing-bg.png                  # Navy/gold marble texture
```

---

## Design System

### Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--navy` | `#1B2E4A` | Primary dark backgrounds, text |
| `--navy-light` | `#243B5A` | Card backgrounds on navy sections |
| `--gold` | `#C9A962` | Accent, labels, borders, ornaments |
| `--cream` | `#FAF8F5` | Light section backgrounds |
| `--cream-light` | `#FAF6F0` | Card backgrounds |
| `--cream-warm` | `#F5EFE3` | Four Questions background |
| `--white` | `#FFFFFF` | Alternate section backgrounds |
| `--light-teal` | `#E8F4F6` | Spine callout backgrounds, flip card backs |
| `--teal` | `#2A7F8C` | Spine callout accents, eyebrow text |
| `--teal-deep` | `#1F5E6A` | Spine subhead, thesis text |
| `--text-dark` | `#1B2E4A` | Headings |
| `--text-body` | `#6B6560` | Body text |
| `--text-body-alt` | `#5A5550` | Darker body text |
| `--text-muted` | `#8A8580` | Muted labels |
| `--text-light` | `#C8C0B8` | Light text on dark backgrounds |
| `--text-cream` | `#E0DCD6` | Cream text on dark backgrounds |
| `--border` | `#E8E2D8` | Card and divider borders |

### Typography

| Element | Font | Weight | Size |
|---------|------|--------|------|
| Hero headline | Playfair Display italic | 400 | 72px |
| Section headings | Playfair Display | 700 | 44px |
| Spine heading | Playfair Display | — | 56px |
| Spine subhead | Playfair Display italic | — | 30px |
| Pillars thesis | Playfair Display | 600 | 32px |
| Quote text | Playfair Display italic | — | 36px |
| Flip card titles | Playfair Display | — | 28px |
| Body text | Nunito | 400-600 | 14-22px |
| Section labels | Nunito | 600 | 16px, 3px letter-spacing |
| Stat numbers | Playfair Display | 700 | 68px |
| Eyebrows | Nunito | 700 | 11-13px, 2-3px letter-spacing |

---

## Page Sections (11 Total)

### 1. Access Gate

- **Type:** Fixed overlay (`z-index: 9999`)
- **Background:** Navy (`#1B2E4A`)
- **Content:** "ETERNAL WEALTH PARTNERS" eyebrow, "Access Code" heading, 4-digit numeric input
- **Code:** `1857` — auto-submits on 4th digit, fades overlay on success
- **Persistence:** `sessionStorage` key `ewp-access` — survives page refresh within same tab
- **Error state:** "Invalid code" message with 2-second fade on wrong 4-digit entry

### 2. Hero

- **Background:** Golden wave texture (`hero-bg.png`) with multi-stop gradient overlay
- **Gradient:** `#1B2E4AE0` (0%) → `#1B2E4ACC` (50%) → `#1B2E4ABB` (70%) → `#243B5A90` (88%) → `#FAF8F5` (100%)
- **Layout:** Full viewport height, centered content
- **Content:**
  - Gold-bordered badge: "Eternal Wealth Partners - A Field Perspective for Northwestern Mutual Home Office"
  - Headline: "Where the Business Owner Plan Lives"
  - Subhead: "Twenty years in the field, one operating system for the most under-served, most lucrative segment we serve."
  - Supporting stats: $124T wealth transfer, 12M businesses exiting, 37% advisors retiring
  - Ornament: — ✦ —
  - Tagline: "The pages that follow are the answer."
- **Copy guidance:** The Hero establishes that what follows is a field perspective on an institutional problem — not a sales pitch and not personal advocacy. The phrase "one operating system" signals the methodology as a defined system, not as the practitioner's style.

### 3. Four Questions

- **Background:** Cream-warm (`#F5EFE3`) with top border
- **Label:** THE FOUR QUESTIONS THIS DOCUMENT ANSWERS
- **Content:** Four numbered question rows with decorative `?` marks
  - Q01: Planning, premium, and retention NM is leaving on the table in the business owner segment
  - Q02: What happens to the assets when the business sells
  - Q03: What happens to the client, and the business itself, across generations
  - Q04: What happens to that relationship as advisors retire and transition
- **Closing:** "The pages that follow answer each one in turn."
- **Copy guidance:** The Four Questions structure the deck as a response to home-office concerns the reader already holds. Q01 frames the economic vulnerability (production, retention, override). Q04 frames the capacity vulnerability (advisor transition). Q02 and Q03 frame the client durability vulnerability (post-event AUM, multi-generational continuation). The document is read as the answer to questions the reader already has, not as an outside argument being made.

### 4. Market in Transition

- **Background:** Cream
- **Label:** THE MARKET IN TRANSITION - ANSWERING QUESTIONS 01 AND 04
- **Heading:** "The supply curve and the demand curve are crossing." (italic)
- **Lead paragraph:** Three demographic forces converging inside the next decade.
- **Content:** Three stat cards
  - **$124T** — Wealth in Transfer: through 2048, 81% from Boomers, half from 2% of population (Cerulli)
  - **12M** — Businesses Changing Hands: $10T in motion. Only $5T transacts. McKinsey projects roughly half of boomer business value never reaches a buyer. 92% of small business market exits today occur through closure, not sale (McKinsey Institute for Economic Mobility, *The Great Ownership Transfer*, 2026). Transferability is the difference between a transition and a payout.
  - **37%** — Advisors Transitioning: $10.4T in client assets, 26% unsure of succession plan (Cerulli)
- **Closing:** "The convergence creates the opportunity. The fragmentation of the work prevents the field from capturing it."
- **Copy guidance:** The 12M card carries the deck's gap thesis. The contrast headline — *$10T in motion. Only $5T transacts.* — is the lede. The 92% closure stat earns the methodology its reason to exist. The transferability line connects the macro problem directly to what the methodology does. This is the slide that justifies every subsequent section. Avoid framing this section as opportunity celebration; frame it as a structural problem the firm has a narrow window to solve.

### 5. Market Reality

- **Background:** White
- **Label:** WHAT IS HAPPENING IN THE FIELD RIGHT NOW
- **Heading:** "The build is happening with or without us."
- **Content:** Three body paragraphs establishing the gap, timing, and data sovereignty risk:
  - **Paragraph 1:** Names the 1,498 CFP base (most in the IBD channel, sourced to NM August 14, 2024 press release). Frames "the talent and the credential are there. The operating layer is not."
  - **Paragraph 2:** Names the firm's gap acknowledgment (white-labeled valuation platform, actively evaluating next-gen tooling) without naming proprietary internal tools. Lands "the next four years are the window."
  - **Paragraph 3:** Names three dimensions of data sovereignty risk: regulatory responsibility, commercial asset, strategic moat.
- **Three-card grid:**
  - **Pillar 05** — Business Valuation: partially answered by white-labeled platform
  - **The Other Six Pillars** — Values, Cash Flow, Risk, Tax, Exit, Legacy: not built
  - **The Integration** — One Workspace, Seven Pillars: not built
- **Closing paragraph:** Operating-layer language — "who builds it, and whether the operating layer that results is built deliberately for the firm Northwestern Mutual has spent decades becoming."
- **Pull quote:** "The market is moving. The question is what version of this story Northwestern Mutual writes." (centered, gold ornaments)
- **Copy guidance:** This section reframes the macro from market-size to capacity-asymmetry. The firm has invested in the credential base; the operating layer that lets that base actually deliver sophisticated planning at scale has not been built. The argument is institutional, not proprietary. The pull quote leaves the strategic problem in the reader's hands without prescribing the solution.

### 6. Quote

- **Background:** Navy (`#1B2E4A`)
- **Content:** Decorative open/close quotes with italic Playfair Display text
- **Quote:** "The supply of advisors who can serve sophisticated business owner planning is shrinking at exactly the moment demand is reaching record highs."
- **Attribution:** "A field perspective on a structural problem."
- **Copy guidance:** The quote crystallizes the capacity asymmetry thesis in one sentence. The attribution is generic ("a field perspective") rather than personal, reinforcing the institutional frame.

### 7. The Spine

- **Background:** Cream
- **Label:** THE SPINE OF THIS DOCUMENT
- **Heading:** "The Seven Pillars are the methodology." (56px Playfair Display)
- **Subhead (thesis):** "Contnuum is the operating system that lets a firm built for advanced planning actually deliver it at scale." (30px Playfair Display italic, teal-deep)
- **Body paragraphs (2):**
  - Paragraph 1: Names NM's investment posture — CERTIFIED FINANCIAL PLANNER base, Sophisticated Planning Strategies team, Estate and Business Planning Specialists, Schools at home office. "The firm has built itself to be a sophisticated planning firm."
  - Paragraph 2: Names the missing operating layer and defines Contnuum's role. "The Seven Pillars are the methodology that delivers sophisticated business owner planning. Contnuum is the operating system that runs the methodology across the field force."
- **Three callouts** (teal-bordered, light-teal background):
  - **What the system does:** Three jobs — deepens client relationship, drives plan implementation, makes team's job easier
  - **Built for the firm's compliance posture:** SOC2 architecture, FINRA and SEC audit-ready, single-tenant data sovereignty, explainable AI, complete audit trail
  - **Why one workspace matters:** "One methodology. One workspace. The math reconciles across pillars." — formula integrity argument, PX integration, "The plan holds up. The numbers hold up across pillars."
- **Copy guidance:** Contnuum is referenced as an operating-system concept that sits inside the firm's architecture, not as an external commercial product. The Spine establishes that the firm's existing investment in sophisticated planning infrastructure is the precondition for the methodology working at scale, and that the missing piece is the operating layer that ties it all together. No commercial framing.

### 8. Seven Pillars with Flip Cards

- **Background:** White
- **Label:** THE METHODOLOGY - ANSWERING ALL FOUR QUESTIONS
- **Heading:** "Seven Pillars, Seven Flip Panels."
- **Axis display:** BUSINESS ← YOU → FAMILY (centered, teal, uppercase)
- **Thesis:** "The Seven Pillars are the methodology. Contnuum is the workflow that lets a great wealth advisor deliver them." (centered, 32px Playfair Display)
- **Framing paragraphs (centered):**
  - NM advisors are exceptional at relationships; methodology + Contnuum remove the demand to operate as CPAs, attorneys, analysts
  - "Each card flips to show what changes for the advisor and the team when the workflow runs."

**Flip Card System:**
- CSS 3D transforms: `perspective: 1400px`, `rotateY(180deg)`, `backface-visibility: hidden`
- Toggle via `onclick` → `.is-flipped` class
- Front: cream-light background, navy left border
- Back: light-teal background, gold left border

| # | Pillar | Front Summary | Back Structure |
|---|--------|---------------|----------------|
| 01 | Values & Vision | The EWP Discovery Sequence, vision statements, Growth/Liquidity/Control ranking | Gap: structured discovery needed. Workflow: guided path captures priorities. Thesis: conversation that anchors every later pillar actually happens. |
| 02 | Cash Flow & Balance Sheet | Eternal Wealth Snapshot, Guardrails, multi-year profitability trend | Gap: cash flow as living forecast, not snapshot. Workflow: living model with recommendations as inputs. Thesis: plan gets the sustainability it should have had. |
| 03 | Risk & Investment Audit | Buy-Sell, key person, executive carve-out, portfolio alignment | Gap: reading legal documents, modeling protection. Workflow: reads agreement, calculates gap, pre-populates recommendation. Thesis: case gets the depth it should have had. |
| 04 | Lifetime Tax-Efficient Strategy | RSU, ISO, NSO, ESOP, 83B, AMT, entity optimization | Gap: tracking tax events and planning calendar. Workflow: tracks events, surfaces implications. Thesis: plan gets the multi-year tax efficiency it should have had. |
| 05 | Business Valuation | Business Valuation, Transferability Score, Exit Gap, Value Acceleration | Gap: running valuation engine, scoring drivers. Workflow: runs assessment, calculates scores, produces roadmap. Thesis: case gets the analytical rigor it should have had. |
| 06 | Exit & Transition Planning | Exit Readiness, Strategy Options, Multi-Year Roadmap, Post-Exit Plan. 76% post-exit regret rate (EPI, 2023). | Gap: multi-year exit roadmap sequencing. Workflow: builds roadmap backward from desired exit date, sequences milestones. Advisor walks owner through path, and the investment and legacy plan for the assets. Thesis: exit gets the runway it should have had. |
| 07 | Legacy & Estate Planning | Wills, Trusts, Asset Ownership, Generation Skipping, Charitable Giving, Gifting Strategy | Gap: generation-skipping analysis, gifting strategy, charitable structures. Advisors are not estate attorneys. Workflow: generates estate diagram, models gifting, routes to Concierge Planning. Thesis: legacy gets the coherence it should have had. |

- **Back card pattern:** Gap statement (bold, what is hard) → Workflow description (what Contnuum does) → Thesis (italic, "The advisor stays a wealth advisor. The [domain] gets the [quality] it should have had.")
- **Copy guidance:** Each pillar is presented as a named operating component with a defined deliverable, not as a description of what the practitioner personally does well. Front summaries name *frameworks and artifacts*. Back panels describe *what changes for the advisor and the team when the workflow runs* — institutional language, not personal practice language. The pillar architecture is the methodology catalog; the flip mechanic is the systematization proof. Pillar 05 language stays inside wealth and exit vocabulary (Business Valuation, Transferability Score, Exit Gap, Value Acceleration). Operational-diagnostic vocabulary does not appear here.

### 9. Revenue and Retention

- **Background:** Cream
- **Label:** ANSWERING QUESTION 01 - WHY THIS COMPOUNDS
- **Heading:** "Why business owner relationships compound where personal planning relationships do not."
- **Lead paragraph:** "The work that compounds for clients also compounds for the firm."
- **Comparison table:** Personal Planning vs. Business Owner Relationship across 6 dimensions:

| Dimension | Personal Planning | Business Owner |
|-----------|------------------|----------------|
| First-year insurance premium | $2K to $5K | $30K to $150K+ |
| Insurance sale events over 20 years | 1 to 2 | 4 to 7 |
| Pre-event AUM accumulation | $500K to $2M | $1M to $10M+ |
| The liquidity event | None (gradual drawdown) | $5M to $50M+ deposited |
| Post-event AUM | Decumulating | Compounding into next generation |
| Multi-generational continuation | Sometimes | Almost always |

- **Retention argument:** "Retention runs in both directions." — structural stickiness for both client and advisor
- **Pull quote:** "Multiplied across the field force, the segment economics are an order of magnitude larger than any single practice." (centered, gold ornaments)
- **Copy guidance:** This section translates the methodology into the language home office economics actually buys — production per advisor, retention impact, override impact, and the compounding nature of business owner relationships across generations. The comparison table speaks in the language of activity standards and production lift, not practitioner skill. The pull quote signals scale without proposing scale architecture; it leaves the deployment question with the reader.

### 10. Five Components

- **Background:** Cream
- **Label:** FULLY OPERATIONALIZED - ANSWERING ALL FOUR QUESTIONS
- **Heading:** "Five components, one operating model."
- **Lead paragraph:** Methodology requires integrated operating model, not just a training program
- **Five component cards** (gold top border):

| # | Component | Description |
|---|-----------|-------------|
| 01 | The Methodology | Seven Pillars, validated and stress-tested. Documented, repeatable, same shape for every client. |
| 02 | The Client Journey | Discovery, valuation, multi-year roadmap, quarterly review, exit readiness, post-exit. Same for every client. |
| 03 | The Planning Experience | Deliverables: The Eternal Wealth Plan, Eternal Wealth Snapshot, Guardrails, Transferability Score, Exit Gap Calculation. Every artifact ties to a pillar. |
| 04 | The Platform Substrate - Contnuum | SOC2, FINRA/SEC audit-ready, single-tenant, explainable AI. Integrates with PX, AILA, LinknetGPT, NMGPT, NM Connect via API. |
| 05 | The Client-Facing Extension | In the spirit of NM Connect, for business owner clients. Owner sees plan, valuation, roadmap, progress. |

- **Closing quote:** "No single component is the answer. The answer is what happens when all five operate together."
- **Closing body:** Methodology without platform is a binder; platform without methodology is software in search of a use case. Five components must be designed, deployed, and supported together.
- **Copy guidance:** The Five Components frame demonstrates that the operating model exists as a coherent whole. Contnuum is referenced as the platform substrate that runs the methodology, sitting inside the firm's existing tool architecture, never as a separate commercial product. The four named methodology components (Discovery Sequence, Guardrails, Lifetime Tax-Efficient Strategy, Eternal Wealth Plan) are reflected here as the deliverables that comprise Component 03. The fifth methodology component (a formal transferability diagnostic) is in active development and not named in this catalog; if asked, the answer is that transferability is a core analytical lens within the methodology and the formal scored diagnostic is in development as the next component.

### 11. Dimensions Worth a Deeper Look (Close)

- **Background:** Navy with marble texture overlay (`closing-bg.png`)
- **Ornament:** — ✦ —
- **Label:** WHAT THIS CONVERSATION COULD BECOME
- **Heading:** "The dimensions worth a deeper look." (52px Playfair Display italic)
- **Intro paragraph:** Field perspective on a strategic problem and operationalized solution; not a commercial proposal
- **Three numbered dimensions:**
  1. **The integration architecture.** How a purpose-built workspace sits alongside what NM has already built.
  2. **The field readiness path.** How the methodology and Contnuum reach the advisors who serve this segment, keeping the wealth advisor operating as a wealth advisor.
  3. **The home office economics.** What the segment looks like at scale, how NM's infrastructure investment compounds when the field can use it consistently.
- **Soft-close paragraph:** "The right next step is the one this conversation surfaces. I am happy to follow up in whatever form would be most useful: a longer working session, a written response to specific questions, or time with a smaller group to go deeper on any of the three dimensions. The right rhythm is the one that fits Northwestern Mutual's process."
- **Final line:** "The market is moving. The conversation worth having is what Northwestern Mutual chooses to do about it." (gold, italic)
- **Copy guidance:** The Close is the deck's pull mechanism. It names three dimensions where the conversation could go deeper without proposing how the firm should engage. The deck ends on a question the firm chooses to answer — or not — on its own terms. No commercial framing, no proposal language, no implied next step beyond the firm's own process.

### 12. Footer

- **Background:** Navy
- **Brand:** ETERNAL WEALTH PARTNERS - ESTATE & BUSINESS PLANNING
- **Contact:** Becky Gustafson — CFP, MSFP, AEP, CAP, ChFC, CLU, RICP, CASL, LUTCF, CLTC
- **Tagline:** "Twenty years in the field, prepared for the conversations that come next."
- **Disclaimer:** Informational only, not financial/tax/legal advice, illustrative revenue figures

---

## Responsive Behavior

### Tablet (max-width: 1024px)
- Hero padding collapses to 60px 40px, headline to 48px
- All section padding reduces to 80px 40px
- All card rows/grids stack vertically (single column)
- Stat numbers shrink to 48px
- Quote text to 24px
- Spine heading to 38px, subhead to 22px
- Pillars thesis to 26px
- Revenue table collapses to single column (row headers hidden)
- Market Reality grid stacks to single column
- Flip cards maintain 380px min-height

### Mobile (max-width: 640px)
- Hero headline to 36px, padding to 40px 20px
- Hero stats stack vertically
- All section padding reduces to 60px 20px
- All section headings cap at 28px
- Spine heading to 32px, subhead to 19px
- Pillars thesis to 22px
- Flip cards expand to 460px min-height
- Dimension items compress grid to 40px + 1fr
- Four Questions rows collapse to single column
- Market Reality pull quote text to 19px

---

## Deployment Configuration

### `package.json`
```json
{
  "name": "ewp-practice-impact",
  "version": "1.0.0",
  "description": "EWP Practice Impact — Where the Business Owner Plan Lives",
  "scripts": {
    "start": "serve . -l $PORT -s"
  },
  "dependencies": {
    "serve": "^14.0.0"
  }
}
```

### `railway.json`
```json
{
  "$schema": "https://railway.com/railway.schema.json",
  "build": {
    "builder": "NIXPACKS"
  },
  "deploy": {
    "startCommand": "npx serve . -l $PORT -s",
    "restartPolicyType": "ON_FAILURE",
    "restartPolicyMaxRetries": 10
  }
}
```

---

## External Dependencies

| Dependency | Source | Purpose |
|-----------|--------|---------|
| Playfair Display | Google Fonts | Heading typography |
| Nunito | Google Fonts | Body typography |
| serve | npm | Static file server for Railway |

---

## Voice Discipline (Deployed Copy)

- No em-dashes in body copy (only decorative `&mdash;` in ornaments)
- No AI register (no rhythmic triplets, no academic hedging, no breathy adverbs)
- No proprietary NM internal tool names (no "BPA", no "BizEquity")
- No personal first names in deployed copy
- No personal pronouns in methodology descriptions ("my methodology" → "the methodology")
- Sources cited where statistics appear (Cerulli, McKinsey Institute for Economic Mobility, Exit Planning Institute)
- The CFP count (1,498) is sourced to NM's August 14, 2024 press release citing Financial Planning's IBD Elite ranking
- Operational-diagnostic vocabulary does not appear (customer concentration, operational maturity, leadership bench, churn cohorts, unit economics, organizational architecture all belong to PiroScope's product domain, not this deck)

---

## Pinned Items (Cross-Project Tracking)

### Transferability / Business Readiness Diagnostic

**Status:** Deferred. Not building yet.

**Why deferred:** Component design needs to be informed by Continuum's deliverable architecture before formalization. Building it now risks creating an EWP artifact that won't align with the Continuum-driven intake redesign coming downstream.

**Dependency chain:** Continuum deliverable spec → Transferability diagnostic design → EWP Discovery Sequence revision

**Working principle:** EWP intake forms are currently optimized for human-advisor-driven discovery. Continuum will require structured, machine-readable, consistently-scored inputs. The intake redesign and the diagnostic build are the same project, executed together, not separately.

**Verbal answer if asked in the room:** *Transferability is a core analytical lens within the methodology. The formal scored diagnostic is in active development as the next component, designed to integrate with the existing discovery architecture.*

---

## Key Statistics and Sources

| Statistic | Value | Source |
|-----------|-------|--------|
| Wealth in transfer | $124T through 2048 | Cerulli Associates |
| Boomer-owned businesses exiting | 12M | Industry standard |
| Business assets in motion (gross pool) | ~$10T | Industry standard |
| Boomer businesses projected to transact | $5T over next decade | McKinsey Institute for Economic Mobility, *The Great Ownership Transfer: A New Era of Business Stewardship*, February 2026 |
| Small business exits by closure (2022) | 92% (5% sale, 3% transfer; ~510,000 total exits) | McKinsey Institute for Economic Mobility, *The Great Ownership Transfer*, February 2026 |
| Advisors retiring | 37% of workforce | Industry standard |
| Advisor-controlled assets | $10.4T | Cerulli Associates |
| Advisors unsure of succession | 26% | Cerulli Associates |
| NM CFP holders | 1,498 | NM press release, August 14, 2024 (Financial Planning IBD Elite) |
| Post-exit regret rate | 76% | Exit Planning Institute, 2023 National State of Owner Readiness Report |

---

## Commit History (Chronological)

```
710383b Initial deploy: EWP Practice Impact standalone page
b391029 Add Lucide icons throughout all card sections
4215370 Sync full UI from Pencil design to HTML
5f9884e Add background textures for hero and closing sections
5ae8358 Rebuild site from NM Home Office revision spec
cd3d95a feat: NM Build Spec revision with flip cards, integration architecture, and Contnuum naming
29d5b45 chore: add playwright-cli and screenshots to gitignore
--- v6 spec execution (branched from cd3d95a, merged to main) ---
1360d37 feat(market-reality): insert Market Reality section
c41ca6e feat(spine): add compliance posture and formula integrity callouts
91ad03a feat(pillars-intro): rewrite Seven Pillars intro with thesis + wealth advisor framing
afd7830 refactor(pillars): replace all seven flip card backs with workflow-focused copy
dc7d309 refactor: remove Integration Architecture section
1736469 feat(revenue-retention): insert Revenue and Retention section
71c8ef6 refactor: remove Home Office Economics section
b69db2b refactor: remove Structural Point pull quote section
d105fa8 refactor(close): replace 5-dimension close with 3-dimension soft close
--- post-v6 surgical edits ---
2d9caa7 Center Seven Pillars intro block (axis, thesis, framing)
00158f7 Center pillars thesis and framing blocks with margin auto
bc94cbb Add investment and legacy plan reference to Pillar 06 flip card
99ea0df Simplify Pillar 07 gap statement
cfcbae2 Rewrite Revenue section intro to remove NM-specific language
368f371 Remove 'in the field over twenty years' from Component 01
9fac575 Remove PX sentence from Component 03
23d04b0 Rename 'NM intranet GPT' to 'LinknetGPT' in Component 04
93e3937 Add access code gate (1857) before viewing site content
--- Spine + Market Reality operating-layer reframe ---
1fbb47f feat(spine): reframe Spine page with operating-system thesis
90edf46 feat(market-reality): reframe with CFP evidence, four-year window, data sovereignty risk
--- Three-change addendum (citation, register, close) ---
43fe8f3 fix(citation): add Exit Planning Institute citation to 76% post-exit regret stat
d1d11a5 fix(register): replace "the math maths" with "the numbers hold up across pillars"
44159e3 fix(close): remove explicit name reference, replace with institutional language
--- Institutional capability reframe ---
cf91862 docs: rebuild EWP_PRACTICE_IMPACT_BUILD.md to reflect current deployed state
[pending] fix(market-in-transition): integrate Option A on 12M card (gap thesis, 92% closure stat, McKinsey 2026 primary citation, transferability line)
[pending] fix(pillar-01): rename "Discovery exercises" to "The EWP Discovery Sequence" on flip card front
[pending] fix(pillar-05): replace "Five Value Drivers" with "Business Valuation" on flip card front
[pending] fix(component-03): replace "Roadmap" with "The Eternal Wealth Plan" in deliverables list
[pending] fix(component-03): replace "Five Value Drivers Assessment" with "Transferability Score" in deliverables list
```
