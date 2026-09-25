# The Gumroad Content Engine — Standing SOP

This is the process PROTON asked for: Claude working "in the background" as a coworker, keeping a pipeline of new Gumroad drops moving continuously, instead of waiting to be asked for each one. Read alongside `org/mission.md` (the no-autonomous-publish rule this respects) and `org/brand-standards.md` (the quality bar every drop below is held to).

## How publishing actually works (PROTON confirmed: both)

1. **Right now, and the default going forward:** Claude runs the entire pipeline below — topic, research, writing, design, multi-pass fact-check — end to end, unattended, and hands PROTON a finished, ready-to-upload package. PROTON's part is the upload click on Gumroad, not a review project. This keeps the human check-before-publish rule in `org/mission.md` intact — the rule exists specifically to catch a hallucinated or false claim before it reaches a paying customer, which is the exact risk PROTON flagged when asking for this engine.
2. **Queued for later, not built yet:** Gumroad has a real OAuth 2.0 REST API (`edit_products` scope — create a product, upload its file via S3 multipart, publish) per [gumroad.com/api](https://gumroad.com/api). True autonomous publishing would mean registering an OAuth app under PROTON's Gumroad account and building an integration against that API — never handing raw Gumroad login credentials to Claude, which is a standing security rule regardless of automation level. THE MECHANIC owns evaluating this once the weekly cadence below has proven itself across a few real drops (same standard `org/mission.md` already sets for autonomous publishing generally).

## Cadence

**Starting cadence: weekly.** PROTON's stated goal is daily — the aggressive end is on record and this SOP works toward it, not away from it. But a genuinely new, fully-researched, fact-checked, designed guide every single day is not a real commitment to make on day one; claiming it now would be exactly the kind of overpromise this whole engine exists to avoid. The concrete plan: run weekly for the first 3-4 drops, track actual time-to-ship and whether quality holds at `org/brand-standards.md`'s bar, then revisit cadence with real data instead of a guess. If weekly proves fast and clean, moving to twice-weekly or daily is a scheduling change, not a rebuild.

A recurring trigger fires automatically on this cadence (no message from PROTON needed) to keep the next drop moving — see "Automation" below.

## The pipeline (per drop)

1. **Topic** — pull the next item from the Topic Queue below, or CHIEF proposes a new one if the queue runs dry, checked against what's already selling well in that category (same "research first, beat what's winning" standard as every other room).
2. **Research & write** — SCRIBE drafts the guide against real information; no invented statistics, no invented percentages, no claims that can't be sourced or are safely generalized (see the 401k-percentage lesson already in `product/wealth-architect-system.md`'s notes).
3. **Design** — PRISM (or the relevant niche designer) builds cover + interior visuals per `org/brand-standards.md`'s cover/tone standard, using the typography standard below.
4. **QA — multiple passes, no exceptions:** WARDEN reads the full draft at least twice, specifically hunting for (a) factual claims that aren't safely generalized or sourced, (b) tone drift from the house voice, (c) design/typography inconsistency with the standard. A pass that finds nothing is still a pass — it doesn't get skipped because the draft "looks fine."
5. **Package** — FORGE assembles the final PDF via the known `markdown_to_pdf` recipe, verifies page count/fonts via `pdf_properties`.
6. **Hand-off** — Claude reports the finished product to PROTON with: what it is, what it claims, what was checked, and the direct file ready for upload.
7. **Publish** — PROTON uploads to Gumroad (the one manual step, by design — see above).
8. **Log** — VAULT logs the new product into `org/revenue-ledger.md` the moment it's live, at $0 until a real sale lands (same no-projection rule as every other room).

## Typography standard (locked / pending)

- **Headings, covers, chapter titles: Omnes SemiBold** (Joshua Darden, Darden Studio) — **CONFIRMED** by PROTON.
- **Body text: pending.** PROTON is sending a reference image of his own research (Arial, Calibri, Inter, Roboto were the names mentioned) — decide once that lands. Do not lock a body font before then. Whichever is chosen, verify it actually embeds correctly in the `markdown_to_pdf` output via `pdf_properties` before treating it as final — the same verification discipline used for every past PDF change.

## Topic Queue (Content/Creator BU, Gumroad drops)

**SCOUT researches new candidate topics on its own recurring cadence (roughly every 3 days — cron day-stepping, so it can drift near month boundaries) and appends them here** so this queue never runs dry before the weekly pipeline needs the next one. SCOUT does research only, never writes the guide itself.

Pull from the top. Add new ideas to the bottom instead of losing them in conversation.

1. **The Savings Architect** — already named as the next planned drop in `org/brand-standards.md` and `org/agent-team.md`.
2. **The Dating Architect** — already named as a planned drop in `org/brand-standards.md`.
3. **The Debt Freedom Architect** (SCOUT, added 2026-09-25) — a full standalone deep-dive on the Debt Freedom Ladder framework, which is already the specific chapter used in Instagram content. Real signal, not a guess: narrow, single-problem guides outsell broad ones 3-5x on Gumroad, and this expands proven interest rather than starting cold. ([Inkfluence AI](https://www.inkfluenceai.com/blog/ebook-ideas-that-sell-2026))
4. **The Side Hustle Architect** (SCOUT, added 2026-09-25) — narrow guide on starting one AI-assisted income stream, directly reusable with the AI Prompt Playbook content already built for Instagram. Personal finance and business/side-income guides are named among the best-selling Gumroad ebook categories for 2026, and the $30-49 price band converts better than sub-$10 pricing. ([Accio](https://www.accio.com/business/gumroad-top-selling-ebooks), [Inkfluence AI](https://www.inkfluenceai.com/blog/ebook-ideas-that-sell-2026))
5. *(open — CHIEF proposes the next topic once the above are in motion, checked against real Gumroad category performance first)*

## Status reporting

Every drop that moves through this pipeline gets reported to PROTON in plain terms: what stage it's at, what's been verified, what's next — so he can see multiple income streams actually building, not just hear that they are.
