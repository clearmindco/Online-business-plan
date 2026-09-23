# THE WEALTH ARCHITECT
### An Energetic, No-BS Guide to Breaking Down Your Paycheck, Killing Debt, and Building Real Wealth — Plus an AI System That Builds Your Personal Plan

This is the source content for the PDF product. The actual sellable file is generated via Adobe's markdown_to_pdf tool with a full-bleed cover, navy/gold branded chapter headers, and 3 custom infographics — see the latest generated PDF link in conversation/session notes, not this markdown directly.

Tone: energetic, empowering, direct-address ("you"), short punchy sentences — think Tony Robbins' momentum-and-decision framing, not a dry finance textbook. Still fully accurate — no invented numbers, no dollar/percentage claims that go stale or vary by employer/plan.

Editorial rule locked in by the founder: **do not go deep into 401(k)/retirement-account mechanics or cite specific match percentages.** Employer plans vary too much (the founder's own is 3%) to generalize — mention retirement accounts exist and that any employer match is worth grabbing, then point the reader to their own plan documents or a professional. Depth belongs to a licensed advisor, not this guide.

Editorial rule: **no refund guarantee.** This is an instant-download digital product — all sales final. The "not licensed financial/tax/legal advice" disclaimer stays regardless; that protects the founder legally and is unrelated to the refund policy.

---

## STRUCTURE (current version)

1. Cover (full-bleed image, no text overlay needed — title is baked into the generated cover art)
2. "This Is Not Another Boring Finance PDF" — energetic intro + what's inside
3. Chapter 1 — The Wealth Split (50/20/20/10 paycheck framework + infographic)
4. Chapter 2 — The Debt Freedom Ladder (4-step payoff order + infographic, match language kept generic/percentage-free)
5. Chapter 3 — Where Money Grows (emergency fund, retirement accounts — kept brief per editorial rule, index funds, real estate, own skills + infographic)
6. Chapter 4 — The Order of Operations (8-step sequence)
7. Chapter 5 — The Habits That Make This Stick
8. Chapter 6 — Money Myths That Keep People Broke
9. Chapter 7 — Your 30-Day Quick-Start (checklist)
10. Bonus — The AI Wealth Advisor (9-phase master prompt + fill-in profile)
11. Closing — "You're Not Waiting For Permission"

## ASSETS USED

- Cover: gold/navy "THE WEALTH ARCHITECT SYSTEM" cover art
- Infographic 1: "THE WEALTH SPLIT" donut chart (50/20/20/10)
- Infographic 2: "THE DEBT FREEDOM LADDER" 4-step staircase
- Infographic 3: "WHERE MONEY GROWS" 5-column icon graphic

All three infographics and the cover were generated to match brand (navy #0b1220 background, gold #d4af7a accents) and are reused as-is across PDF revisions.

## KNOWN GOOD TECHNICAL RECIPE (for regenerating the PDF)

`markdown_to_pdf` (Adobe MCP) renders via an HTML2PDF engine that:
- Honors a `<style>@page{margin:...} body{font-family:...}</style>` block at the top (confirmed: switched embedded font from Times New Roman to Arial)
- Honors inline `style` attributes on raw `<div>`/`<img>` tags mixed into markdown (used for full-bleed cover, navy chapter header bands, framed images with box-shadow, and `page-break-after:always` section breaks)
- Does NOT reliably support GFM `- [ ]` checkboxes — use a literal `☐` character in a normal markdown bullet instead
- Force page breaks ONLY between major chapters, not mid-chapter — stacking two breaks close together with little content between them produces a fully blank page

Verify every regeneration with `pdf_properties` (check `page_count` and `fonts` list) before sending to the user — do not assume a change took effect without checking.
