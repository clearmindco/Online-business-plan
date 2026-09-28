# The Generational Wealth Prompt Vault — Product Plan

PROTON's idea, triggered by two real references: a "Master Claude" prompt-book ad (1900 prompts, 350 assistants) and a bookstore sales book pairing AI with a proven category ("The AI Edge"). Researched before committing to specifics, per the standing "research first, beat what's winning" rule.

## The market is real, not guessed

Two direct competitors already exist on Gumroad: an "AI Financial Freedom Prompt Library" (50+ prompts, pitched as replacing a $3K/year advisor) and a "Claude AI Prompt Library" (105 prompts across 7 categories), both from the same seller, priced $37-47. AI prompt packs are named as a top-selling 2026 Gumroad category, and finance-niche prompt products are named as able to command $37-47 without hesitation. ([conversionproplus.com](https://conversionproplus.com/blog/gumroad-trends-2026-what-s-selling-right-now), [digitalwealthwithsa.gumroad.com](https://digitalwealthwithsa.gumroad.com/l/claudeprompts), [aliteq.com](https://aliteq.com/make-money-selling-ai-prompts-2026))

## Why we beat the existing competitors, not just copy them

Their products are generic prompt dumps ("1900 prompts, 350 assistants" — spray and pray, no real curation). Ours is the AI companion to a brand people already trust: it grows directly out of the "AI Wealth Advisor" bonus already teased inside The Wealth Architect System, built out into its own full product under its own name, The Generational Wealth Prompt Vault. That's a real differentiator, not a marketing claim — the cross-sell is already built into the existing guide.

## Positioning in the funnel

The Wealth Architect System ($5.99, entry point) → **The Generational Wealth Prompt Vault** (this product, the upgrade) → future higher-tier offers. Classic value-ladder logic already used elsewhere in this business (`org/mission.md`'s DotCom Secrets chain: lead magnet → tripwire → core → profit maximizer).

## 7 categories (matches the benchmark competitor's structure, not its content)

1. **Budgeting & Cash Flow** — builds on the Wealth Split framework already in the main guide.
2. **Debt Payoff** — builds on the Debt Freedom Ladder framework already in the main guide.
3. **Income Growth / Side Hustles** — reuses the 5 business-starting prompts already built for the Instagram AI Prompt Playbook.
4. **Business & Offer Building** — offer creation, content planning, positioning, launch sequencing.
5. **Investing Basics (education only)** — prompts that ask AI to explain concepts (index funds, compound interest, risk tolerance), never to pick stocks or give specific financial advice. Same editorial line already locked in `product/wealth-architect-system.md`.
6. **Career & Income Negotiation** — salary negotiation prep, resume/interview prompts.
7. **Protecting What You Build** — insurance and estate-planning education prompts, always framed as "questions to bring to a professional," matching the existing not-licensed-advice disclaimer.

## Quality bar, not quantity bar

Competitors lead with volume (1900 prompts, 105 prompts) as the selling point. We lead with curation: roughly 60-80 prompts, each mapped to one real, specific outcome, each already following the exact prompt format proven in `product/instagram-content-plan.md`'s AI Prompt Playbook (a role, a clear ask, bracketed fill-ins). Fewer, better prompts is the actual differentiator, not a compromise.

## Pricing

Start at **$27**, below the $37-47 competitor band but well above the $5.99 entry guide — positions it as premium without being priced out of an impulse buy from someone who already bought the first guide. Same penetration-then-raise logic already proven on the main guide: raise once real sales validate it, not before.

## Build pipeline (reuses the existing Gumroad Content Engine, not a new process)

1. **SCRIBE** drafts all 7 categories — reuses the 5 already-written business prompts, writes the remaining ~55-75 fresh, each following the proven format.
2. **WARDEN** QA pass — every prompt reviewed for the same accuracy/legal line already enforced on the main guide (no specific financial/investment advice, no invented stats, disclaimer present).
3. **PRISM** designs cover + interior in the existing navy/gold brand identity, reusing the approved badge logo.
4. **FORGE** assembles via the proven `markdown_to_pdf` recipe, verifies via `pdf_properties`.
5. **HERALD** writes the Gumroad listing and the cross-sell email/IG post to existing Wealth Architect System buyers (the built-in audience for this exact upgrade).
6. **PROTON** does the final publish click, per the standing no-autonomous-publish rule.

## Where to sell it

PROTON's instinct ("every platform would be good") is directionally right but Gumroad is the correct first platform — it's where the existing audience and the direct competitors already are, and it's already our live storefront. Cross-listing to other platforms (Etsy digital downloads, etc.) is a real future step, not a day-one requirement — expanding to more platforms before proving the product on the one platform we already have set up would split effort without adding proof.

## Status

**Built.** PROTON gave the go-ahead on categories and the $27 launch price (2026-09-28). SCRIBE drafted all 70 prompts across the 7 categories in `product/generational-wealth-prompt-vault.md`, WARDEN passed it (no invented stats, investing category stays education-only with no stock/fund picks, disclaimer present, house style applied), PRISM generated the cover art, and FORGE assembled the final PDF.

**Cover art (PRISM):** two assets generated in the navy (#0b1220) / gold (#d4af7a) brand identity, built from a mountain-summit-at-sunrise concept (reaching the summit = reaching financial freedom), matching a reference PROTON sent of a competitor's book-ad mockup format but with our own brand, no other brand's marks:
- **Gumroad/marketing listing image** (3D hardcover book mockup on a desk): https://d8j0ntlcm91z4.cloudfront.net/user_3DRitQw0a8l5E8VtiHel0ReRB0I/hf_20260928_011233_ea2971c6-a0f8-4271-8ac6-249e00136534.png
- **PDF interior cover** (flat full-bleed art, same concept): https://d8j0ntlcm91z4.cloudfront.net/user_3DRitQw0a8l5E8VtiHel0ReRB0I/hf_20260928_011312_5f1f43ed-1de8-4977-8cf4-51781862feb8.png

Both had their baked-in title text visually verified correct before use (no spelling errors), per the standing spelling-check rule.

**Final PDF (FORGE):** 17 pages, Arial body font (matches the typography standard already used on The Wealth Architect System), navy chapter-header bands per category, full-bleed branded cover — download: https://to.adobe.com/Gsz0qYRFpDDlX5tKpcNLp40CAi8e

**Revision (2026-09-28, PROTON's catch):** the first version had two bugs PROTON found on his phone: the cover title was cropped at the top (fixed by switching the background image from `cover` to `contain` sizing so it can never crop), and prompt headings were getting orphaned at the bottom of a page while their prompt box flowed to the next page (fixed by wrapping every one of the 70 prompts in a `page-break-inside:avoid` block so heading and box always move together). Page count dropped 24 → 17 once the orphan-created blank gaps went away.

**Next step (PROTON):** review the PDF and cover art, then the one manual step per the standing no-autonomous-publish rule — upload to Gumroad. The manuscript itself is a plain PDF, so the same file works for any other platform (Etsy digital downloads, Payhip, etc.) once Gumroad is proven.
