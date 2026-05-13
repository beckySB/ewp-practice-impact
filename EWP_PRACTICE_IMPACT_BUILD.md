# EWP Practice Impact — Build Document

**Live URL:** https://ewp-practice-impact-production.up.railway.app/
**Repository:** https://github.com/beckySB/ewp-practice-impact
**Deployment:** Railway (auto-deploy from `main` branch)
**Access Gate:** Code `1857` required before viewing content (sessionStorage-persisted)

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

### 3. Four Questions

- **Background:** Cream-warm (`#F5EFE3`) with top border
- **Label:** THE FOUR QUESTIONS THIS DOCUMENT ANSWERS
- **Content:** Four numbered question rows with decorative `?` marks
  - Q01: Planning, premium, and retention NM is leaving on the table in the business owner segment
  - Q02: What happens to the assets when the business sells
  - Q03: What happens to the client, and the business itself, across generations
  - Q04: What happens to that relationship as advisors retire and transition
- **Closing:** "The pages that follow answer each one in turn."

### 4. Market in Transition

- **Background:** Cream
- **Label:** THE MARKET IN TRANSITION - ANSWERING QUESTIONS 01 AND 04
- **Heading:** "The supply curve and the demand curve are crossing." (italic)
- **Lead paragraph:** Three demographic forces converging inside the next decade
- **Content:** Three stat cards
  - **$124T** — Wealth in Transfer: through 2048, 81% from Boomers, half from 2% of population
  - **12M** — Businesses Changing Hands: $10T in business assets, McKinsey projects $5T next decade
  - **37%** — Advisors Transitioning: $10.4T in client assets, 26% unsure of succession plan (Cerulli)
- **Closing:** "The convergence creates the opportunity. The fragmentation of the work prevents the field from capturing it."

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

### 6. Quote

- **Background:** Navy (`#1B2E4A`)
- **Content:** Decorative open/close quotes with italic Playfair Display text
- **Quote:** "The supply of advisors who can serve sophisticated business owner planning is shrinking at exactly the moment demand is reaching record highs."
- **Attribution:** "A field perspective on a structural problem."

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
| 01 | Values & Vision | Discovery exercises, vision statements, Growth/Liquidity/Control ranking | Gap: structured discovery needed. Workflow: guided path captures priorities. Thesis: conversation that anchors every later pillar actually happens. |
| 02 | Cash Flow & Balance Sheet | Eternal Wealth Snapshot, Guardrails, multi-year profitability trend | Gap: cash flow as living forecast, not snapshot. Workflow: living model with recommendations as inputs. Thesis: plan gets the sustainability it should have had. |
| 03 | Risk & Investment Audit | Buy-Sell, key person, executive carve-out, portfolio alignment | Gap: reading legal documents, modeling protection. Workflow: reads agreement, calculates gap, pre-populates recommendation. Thesis: case gets the depth it should have had. |
| 04 | Lifetime Tax-Efficient Strategy | RSU, ISO, NSO, ESOP, 83B, AMT, entity optimization | Gap: tracking tax events and planning calendar. Workflow: tracks events, surfaces implications. Thesis: plan gets the multi-year tax efficiency it should have had. |
| 05 | Business Valuation | Five Value Drivers, Transferability Score, Exit Gap, Value Acceleration | Gap: running valuation engine, scoring drivers. Workflow: runs assessment, calculates scores, produces roadmap. Thesis: case gets the analytical rigor it should have had. |
| 06 | Exit & Transition Planning | Exit Readiness, Strategy Options, Multi-Year Roadmap, Post-Exit Plan. 76% post-exit regret rate (EPI, 2023). | Gap: multi-year exit roadmap sequencing. Workflow: builds roadmap backward from desired exit date, sequences milestones. Advisor walks owner through path, and the investment and legacy plan for the assets. Thesis: exit gets the runway it should have had. |
| 07 | Legacy & Estate Planning | Wills, Trusts, Asset Ownership, Generation Skipping, Charitable Giving, Gifting Strategy | Gap: generation-skipping analysis, gifting strategy, charitable structures. Advisors are not estate attorneys. Workflow: generates estate diagram, models gifting, routes to Concierge Planning. Thesis: legacy gets the coherence it should have had. |

- **Back card pattern:** Gap statement (bold, what is hard) → Workflow description (what Contnuum does) → Thesis (italic, "The advisor stays a wealth advisor. The [domain] gets the [quality] it should have had.")

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
| 03 | The Planning Experience | Deliverables: Roadmap, Eternal Wealth Snapshot, Guardrails, Five Value Drivers Assessment, Exit Gap Calculation. Every artifact ties to a pillar. |
| 04 | The Platform Substrate - Contnuum | SOC2, FINRA/SEC audit-ready, single-tenant, explainable AI. Integrates with PX, AILA, LinknetGPT, NMGPT, NM Connect via API. |
| 05 | The Client-Facing Extension | In the spirit of NM Connect, for business owner clients. Owner sees plan, valuation, roadmap, progress. |

- **Closing quote:** "No single component is the answer. The answer is what happens when all five operate together."
- **Closing body:** Methodology without platform is a binder; platform without methodology is software in search of a use case. Five components must be designed, deployed, and supported together.

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
- Sources cited where statistics appear (Exit Planning Institute, 2023)
- The CFP count (1,498) is sourced to NM's August 14, 2024 press release citing Financial Planning's IBD Elite ranking

---

## Key Statistics and Sources

| Statistic | Value | Source |
|-----------|-------|--------|
| Wealth in transfer | $124T through 2048 | Industry standard (Cerulli) |
| Boomer-owned businesses exiting | 12M | Industry standard |
| Business assets in motion | ~$10T | Industry standard |
| McKinsey projection | $5T come to market next decade | McKinsey (cited in Fortune, Feb 2026) |
| Advisors retiring | 37% of workforce | Industry standard |
| Advisor-controlled assets | $10.4T | Cerulli |
| Advisors unsure of succession | 26% | Cerulli |
| NM CFP holders | 1,498 | NM press release, Aug 14, 2024 (Financial Planning IBD Elite) |
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
```
