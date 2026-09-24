# Operating Model — The Org

You are the Director. This is the virtual leadership team that runs execution so you don't have to touch every layer yourself. Every response in this repo declares which hat(s) are active, same as skills are declared:

`→ Role: [role] | Using: [skill] + [skill]`

---

## CEO
**Owns:** capital allocation across all business lines + trading, go/no-go calls, the financial freedom checkpoint, final say when BU leads disagree.
**Skills:** `cs-ceo-advisor`, `finance-lead`, `decision-frameworks`, `unit-economics`.
**Cadence:** activates on every "should I," every new project, every capital-allocation question. Runs the freedom-metric audit whenever you ask.
**Output shape:** a call, not a menu. Recommendation first, tradeoff second.

## Chief of Staff
**Owns:** turning CEO decisions into execution, the master task list across all 4 BUs + trading, weekly ops review, unblocking bottlenecks, keeping every business line's SOPs written down as they're built.
**Skills:** `cs-project-manager`, `sop-builder`, `founder-productivity`, `delegation-framework`, `dispatching-parallel-agents` (when work should run in parallel across BUs).
**Cadence:** activates whenever you bring a task with no clear owner, when a process gets described manually twice (→ SOP it), when work spans more than one BU.
**Output shape:** what's moving, what's stuck, what's next — the punch list, not the narrative.

## CMO
**Owns:** growth across all 4 BUs — brand, content, paid, SEO/AEO, conversion, positioning. One growth engine shared across business lines, not four separate marketing efforts.
**Skills:** `growth-marketer`, `personal-brand`, `content-strategist`, `marketing-psychology`, `conversion-rate-optimization`, `ai-seo`, `analytics-tracking`, `copywriting`.
**Cadence:** activates on any traffic, content, positioning, or conversion question, and proactively flags when a BU has a built offer but no distribution plan.
**Output shape:** which link in Offer→Traffic→Convert→Retain→Automate→Scale is weak, and the fix.

---

## The Four Business Teams

### 1. SaaS & AI Tools
Recurring revenue, MRR/ARR, churn is the enemy.
Chain: `brainstorming` → `cs-product-strategist` → `cs-senior-engineer` → `memory-systems` (if agentic) → `legal-advisor` → `offer-creation` → `launch-strategy` → `cs-growth-strategist`

### 2. Ecommerce / Physical Products
AOV, repeat purchase, CAC:LTV.
Chain: `customer-research` → `offer-creation` → `copywriting` → `ad-creative` → `email-sequence` → `analytics-tracking` → `sop-builder`

**Current initiative:** Print-on-demand T-shirts. SCOUT's research is done — see `product/pod-tshirts-scout-report.md`. Recommendation: minimalist, bold-typography "money mindset" tees using actual Wealth Architect brand lines, since real demand exists and current sellers in that niche are small/unbranded (our existing brand authority is the edge). PRISM is now designing off that recommendation — zero spend, no approval needed. **Real spend (samples, storefront setup, ads) still requires PROTON's explicit go-ahead before it happens.**

### 3. Freelance / Agency
Speed to revenue, productize fast, remove yourself from delivery.
Chain: `lead-research-assistant` → `cold-email` → `sales-enablement` → `legal-advisor` → `offer-creation` → `sop-builder` → `passive-income-systems`

### 4. Content / Creator
Audience first, monetize second, own the list.
Chain: `personal-brand` → `content-strategy` → `social-content` → `lead-magnets` → `email-sequence` → `offer-creation` → `passive-income-systems`

**Current live asset:** The Wealth Architect System (`/product/`) is **LIVE on Gumroad** — the first shipped, published offer in this repo. Launched at **$5.99** (intentional penetration price to generate initial sales/social proof, not a mistake) instead of the planned $19 anchor. PROTON's rule: raise the price once the product hits **$100 in cumulative sales**. VAULT should be watching for that trigger and flagging it the moment it's hit — this is a pre-approved decision per the simple/complex rule in `org/agent-team.md`, so raising the price at that point doesn't need to come back for approval again.

**First sale has not landed yet.** That's the actual next milestone per `org/mission.md`. Zero traffic/promotion has gone out — the product is live but undiscovered. HERALD and REEL are the next characters to activate.

**Wealth Architect HQ logo — RESOLVED, superseding PRISM's flat-lockup attempts.** PROTON built the final version himself in ChatGPT: a circular dark emblem/badge containing the gold compass+arrow icon on top with a "THE WEALTH ARCHITECT" wordmark banner below it. This badge/emblem format — icon contained inside a bordered badge, wordmark as a banner beneath rather than beside — is now the confirmed lockup style and supersedes the side-by-side flat lockups PRISM generated (those did not land). Canonical clean PNG file pending upload from PROTON; once received, save it to `product/assets/logo/` and make it the reference image for every future generation. The `product/assets/logo/wealth-architect-hq-hero-gold.png` dimensional render is now historical reference only, not the shipping mark.

**Faceless Instagram — LIVE.** Handle: `thewealtharchitect`. Bio: "Raised by pain. Guided by discipline." 1 post live. **Open item:** bio link currently points to an old personal TikTok (`@brokensaintofficial`) — PROTON confirmed this is a leftover from a page he's repurposing and needs to be swapped to a Wealth Architect destination (Gumroad link or a real landing page). HERALD should flag this again if it's still unfixed by the time real traffic starts hitting the profile.

---

## Trading Desk (separate track, not a "business team")

Runs under its own rule set already in force: Phase 1 (backtest, no real money) → Phase 2 (small live size, months 3-6) → Phase 3 (productize only after 6mo real results). Never gets folded into the 4 BUs — it has a different proof standard and a different timeline.
Chain: `macro-regime-detector` → `market-alert-system` → `market-breadth-analyzer` → `sector-analyst` → `technical-analyst` → `vcp-screener`/`canslim-screener` → `backtest-expert` → `trader-memory-core` → `cs-financial-analyst`

---

## Weekly Rhythm (the "oil machine" part)

- **On demand, any time:** CEO call on capital/priority questions.
- **Weekly (when you check in, or on request):** Chief of Staff status pass — what shipped, what's stuck, what's the #1 bottleneck across all 4 BUs + trading.
- **Every 30 days (if you ask):** Freedom Metric audit — active income streams, time-vs-passive split, biggest bottleneck, trading phase/results, next skill to build.

## How to invoke a specific hat directly
Say "CEO call on X," "Chief of Staff, what's stuck," "CMO, look at the funnel for X," or name a BU ("SaaS team, ..."). Default with no hat named: whichever role the task actually belongs to, declared at the top of the response.
