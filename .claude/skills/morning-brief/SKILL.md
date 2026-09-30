---
name: morning-brief
description: Produces a short, real CEO-style morning briefing for Javier's business — revenue, mission status, what moved, what's blocked, what needs him, and one recommendation. Use when Javier says "run my morning brief", "brief me", "what's on my plate", or asks for a status check on the business.
---

# Morning Brief

This skill is fully self-contained — it has no memory of any prior conversation, so every source it reads and every formatting rule is spelled out here explicitly. Adapted from the real "build your own JARVIS" pattern (routines/skills with no memory between runs), applied to this business's actual data instead of a generic template.

## Sources to read, in this order

1. `org/revenue-ledger.md` — real revenue per product, all-time. Never state a number that isn't in this file.
2. `org/agent-status.md` — real current status per character (working/idle/blocked). This is the persistent source of truth; conversation memory is not.
3. `product/instagram-content-plan.md` — the "## Status" section, for the current Instagram/Metricool state.
4. `org/gumroad-content-engine.md` — the Topic Queue, for what's next in the pipeline.
5. `org/mission.md` — for Mission 001's real definition ("first real sale") if it needs restating.

## Output format

Write 6–8 short lines, direct address, no filler, matching the house voice in `org/brand-standards.md` (energetic, human, no unnecessary em dashes). Structure:

1. **Mission status** — one line: is Mission 001 (first real sale) complete or not, and the real confirmed revenue number.
2. **What moved** — 1–2 lines on what actually shipped or changed since the last brief (pull from `org/agent-status.md`'s "Working"/recently-completed entries — never invent activity that isn't in that file).
3. **What's blocked** — name it plainly if anything in `org/agent-status.md` has a real blocker (e.g. TikTok Shop proof-of-address, BROKER waiting on Shopify login). If nothing is blocked, say so — don't manufacture a blocker to sound busy.
4. **Requires Javier** — list any real pending decision. If there are none, say "0 decisions pending," not a vague prompt to check something.
5. **One thing to know** — a single real signal worth surfacing (a queue item about to run dry, a trigger about to fire, a number close to a threshold like the $100 price-raise trigger).
6. **Close with one recommendation**, not a menu — the single highest-leverage next action, stated plainly ("Do X because Y"), same as `org/operating-model.md`'s CEO output-shape rule.

## Hard rules

- Never state a projected or estimated number as if it were confirmed revenue. `org/revenue-ledger.md` is the only source of truth for money.
- Never invent an agent's activity that isn't recorded in `org/agent-status.md`. If that file is stale, say so plainly rather than guessing what's current.
- This is a read-and-report skill. It never sends an email, posts anything, or spends money on its own — those stay real decisions surfaced to Javier, per `org/mission.md`.
- If this brief is being written to an external surface (a Notion page, a file), update `org/agent-status.md`'s "Last updated" line at the same time so the two never drift apart silently.
