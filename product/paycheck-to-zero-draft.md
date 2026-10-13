# The Paycheck-to-Zero System — DRAFT, pending PROTON's approval

Source: Javier's "MASTER PROMPT — The Wealth Architect Sales System," built from Muse's research
(`b0966c24-what-s-selling-on-instagram-tiktok-and-shopify.html`). This file is the Step 3 deliverable
set from that prompt — drafts only. **Nothing here is built, scheduled, published, or sent.** Per the
prompt's own hard rule and this repo's standing no-autonomous-publish rule, this waits for PROTON's
explicit go-ahead before FORGE builds the sheet/PDF, PULSE schedules anything in Metricool, or HERALD
sends a single message.

## Status
**DRAFT — awaiting approval.** Registered 2026-10-13. Not yet in `org/revenue-ledger.md` (nothing to
log until it's real).

---

## (a) Hero product outline — SCRIBE + PRISM

**Product:** "Paycheck-to-Zero" — a budgeting + debt-payoff spreadsheet system, minimum build per the
prompt's explicit instruction (2 tabs only, nothing more until this validates).

**Tab 1 — Monthly Budget.** Income in, fixed bills, variable spending, a 4-way split (Needs / Savings /
Debt / Freedom — same split language already shipped in `product/generational-wealth-prompt-vault.md`'s
prompt 1.1, kept consistent rather than inventing new terminology). Auto-calculates what's left.

**Tab 2 — Debt Payoff.** List each debt (name, balance, APR, min payment), shows both the avalanche order
(highest interest first) and the snowball order (smallest balance first), and computes a debt-free date
from an extra-monthly-payment input.

**Dummy household (demo data only, labeled "SAMPLE DATA — fictional household" on the sheet itself, never
presented as a real user):** reuses the exact figures already shipped in the Vault's worked examples
(`product/generational-wealth-prompt-vault.md`, prompts 1.1 and 2.1) instead of inventing new numbers:
- Take-home: $4,200/month. Fixed bills: rent $1,400, car $320, insurance $150, phone $80, subscriptions $45.
- Debts: Credit Card A $3,200 @ 24% APR (min $95), Credit Card B $1,100 @ 19% APR (min $35), Car Loan
  $8,400 @ 6% APR (min $310).

**Walkthrough guide:** 10-12 page faceless PDF, FORGE's existing `markdown_to_pdf` recipe, screenshots of
the sheet with captions. No face, no voice, same as every other product.

**Price (PROTON's call, band is $19-29 per the prompt):** recommend **$19** — same penetration-pricing
logic already used on The Wealth Architect System ($5.99 instead of its $19 anchor, to earn initial
sales proof before raising).

**Checkout page copy (draft):**
> **Stop Guessing Where Your Paycheck Goes.**
> The Paycheck-to-Zero System: one spreadsheet that organizes your budget and shows your real
> debt-free date.
>
> Inside: a monthly budget tab, a debt-payoff tab (avalanche + snowball, both shown), and a short
> walkthrough guide.
>
> Get instant access — $19.
>
> *Educational and organizational tool only. Not financial, investment, or tax advice.*

The one claim this product is allowed to make, per Section 7 of the prompt: it **organizes your budget
and shows your debt-free date.** Never "get out of debt fast," never a guaranteed outcome.

---

## (b) 7 launch-week post hooks — PULSE

Ivory (#F7F3EA) background, navy (#0B1220) headline text, gold (#D4AF7A) accent only, "LINK IN BIO"
printed on the post itself below the headline with clear space. Heavier on demo/offer than the normal
1-in-5 ratio — a deliberate launch-week exception, not the new standing cadence.

1. **(Demo/offer)** "What if your budget showed you the exact day you'll be debt-free?"
2. **(Framework teaser)** "The 4-way paycheck split, now in a spreadsheet that does the math for you."
3. **(Mindset)** "You don't need a better plan. You need to see the plan."
4. **(Demo/offer)** "Watch me plan an entire paycheck in under 3 minutes." *(screen-demo hook)*
5. **(Identity/aspiration)** "The version of you that has it together has one thing you don't: a system,
   not a guess."
6. **(Mindset)** "A budget you don't look at isn't a budget. It's a guess with extra steps."
7. **(Demo/offer, launch close)** "Snowball or avalanche? The sheet shows you both — and your real
   debt-free date."

Per the prompt's own rule: these are hooks only. PROTON writes or approves the final caption copy.

---

## (c) 3 sales templates — HERALD (flagged: new function, no existing direct owner)

`org/agent-team.md` has no character who owns real-time DM/objection-handling sales conversations today —
HERALD owns launch copy and is the closest fit, taking this for now. If this becomes a sustained function
rather than a one-off, it's a CHIEF call on whether it earns its own Room Manager later — not decided here.

**1. New DM greeting + closing flow**
> Opening: "Hey! Thanks for reaching out about Paycheck-to-Zero 🙌 Quick question so I point you to the
> right thing — are you looking to organize your monthly budget, get a clear debt payoff order, or both?"
>
> Closing (after they answer): "That's exactly what Paycheck-to-Zero does — [one line matching their
> answer]. Here's the link: [checkout link]. Let me know if anything's unclear before you grab it."

**2. Abandoned-checkout follow-up** — *flagged unusable today: no Gumroad connector exists in this
session to detect an abandoned checkout at all (see Setup Check below). Drafted for when that connector
exists, not for sending now.*
> "Hey — saw you were checking out Paycheck-to-Zero earlier. No pressure, just wanted to make sure the
> link worked okay. If you had a question that stopped you, happy to answer it here."

**3. Objection reply — "isn't this just a free template?"**
> "Totally fair question. The free templates get you a blank sheet — this one's pre-built with the
> debt-payoff math (avalanche vs. snowball, with your real debt-free date) already done for you, plus a
> short walkthrough so you're not guessing how to fill it in. It's $19 one-time, no subscription."

---

## Setup Check (THE MECHANIC) — what's actually connected

- **Gumroad:** no MCP connector in this session at all. Cannot read live products, prices, orders, or
  abandoned checkouts. Everything about Gumroad in this plan comes from what's logged in
  `org/revenue-ledger.md` (PROTON's own self-reported updates), not a live feed.
- **Shopify:** the MCP server is present but returned "needs you to sign in again" when queried — not
  authenticated to a real store right now. No live Shopify data available, and per
  `org/operating-model.md` no Shopify store exists yet anyway.
- **Messaging/sales channel:** no ManyChat connector, no Instagram DM/automation connector. Metricool is
  connected but is analytics + post scheduling only — it cannot read or send DMs and has no concept of
  an abandoned checkout.

**Net effect:** the "24/7 sales operator" role in Section 5 of the prompt cannot run live as specified —
missing Gumroad read access and a messaging channel. Per the prompt's own hard rule, this is being
reported, not worked around or faked.

## Store audit (VAULT) — real numbers, from the ledger, not live-pulled

| Product | Price | Status | Units/Revenue |
|---|---|---|---|
| The Wealth Architect System | $5.99 | Live on Gumroad | $0 / 0 |
| The Savings Architect | $6.99 | Live on Gumroad | $0 / 0 |
| The Generational Wealth Prompt Vault | $27 | Live on Gumroad | $0 / 0 |
| The Dating Architect | $6.99 | **Packaged, not yet uploaded** | $0 / 0 |

Confirmed total revenue across every product: **$0.** Zero real traffic has been pushed through any of
them yet (per `org/operating-model.md`). That's directly relevant to Section 4's validation plan — there's
no existing funnel data to analyze, so the Day 1-2 audience poll is the right first move, not a step to
skip.
