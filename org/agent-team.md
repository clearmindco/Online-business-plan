# The Product Factory — Agent Team

This is the automated pipeline that turns "we should sell X" into a finished, brand-standard product ready to upload — with each role doing one job, handing off a finished file, and nothing advancing until the current stage passes its own test.

Read alongside `org/operating-model.md` (the roles), `org/brand-standards.md` (the quality bar every stage is tested against), and `org/mission.md` (the actual reason this exists — every role should know it).

## How it runs

Say **"New drop: [topic]"** (e.g. "New drop: The Savings Architect" or "New drop: The Dating Architect for Men") and the pipeline below runs in order. Each stage's output lands as a file in `product/[drop-name]/`. A stage doesn't start until the prior stage's file exists AND passes its test — that's the literal mechanism behind "bots that don't move on until they finish their test."

I run Script Writer and Visual Designer as dedicated subagents (via the Agent tool) so each one stays focused on exactly one job, the same way a real team member would — this is the "bots talking to each other" part: their output is the handoff.

---

## The roles

### 1. Idea Intake — you + CEO hat
**Job:** lock the concept before any work starts.
**Test to pass:** one sentence — the dream outcome, and who it's for. ("A guide that gets a man his first real date in 30 days, for guys who freeze up talking to women.")
**Output:** a one-line brief. No brief, no pipeline.

### 2. Script Writer Agent — the smartest one on the team
**Job:** writes everything that's actually words — the full guide content, the sales page copy, the product description, later the launch emails. Runs on `copywriting` + `offer-creation` + `marketing-psychology`, in the house voice locked into `brand-standards.md` (energetic, direct-address, no textbook tone).
**Test to pass:**
- Reads like a human wrote it fired up about the topic, not like AI output
- Every factual claim is either evergreen-true or explicitly hedged (no numbers that go stale, no guarantees that can't be kept)
- Structured for the Assembler (chapter headers, clear sections, no walls of text)
**Output:** `product/[drop-name]/script.md`

### 3. Visual Designer Agent
**Job:** cover art + supporting infographics + brand consistency. Runs on `banana`/image generation, tested against the aspiration bar in `brand-standards.md` ("I need this," not just "looks clean").
**Test to pass:**
- Cover triggers desire at thumbnail size, not just full-size
- Palette and typography match the established brand (or a deliberate, approved new palette for a new product line)
- No real people's likenesses; legible when small
**Output:** `product/[drop-name]/visuals/` (cover + infographics)

### 4. Assembler
**Job:** merges script + visuals into the final sellable PDF using the proven `markdown_to_pdf` recipe (documented in `product/wealth-architect-system.md`'s technical section) — full-bleed cover, branded chapter headers, framed images, correct page breaks.
**Test to pass:** verified with `pdf_properties` — correct page count, no blank pages, images actually embedded (file size confirms it), fonts render as intended.
**Output:** the final PDF, verified.

### 5. QA / Brand Gate
**Job:** the last check before anything reaches you. This is the stage that exists specifically so nothing false or risky goes out under Javier's name.
**Test to pass — all of these, every time:**
- **Accuracy check:** every factual/numeric claim in the script is either evergreen-true or clearly hedged as a rule of thumb, not stated as certain or guaranteed. Nothing that could embarrass or expose Javier if a reader fact-checked it.
- **Brand check:** matches `brand-standards.md` — tone, cover desirability, depth.
- **Legal check** (`legal-advisor`): disclaimer present, no guaranteed-outcome language, refund/sales-final policy stated correctly and consistently between the product and the sales page.
**Output:** a pass/fail note. On a fail, name the exact stage and the exact fix, framed forward, never as blame — "Script Writer, Chapter 3's second claim needs a hedge — here's the fix" not "this is wrong." See `org/mission.md` for the full feedback-style rule. Fail = only the named stage redoes its part, the whole pipeline doesn't restart.

### 6. Email / Launch Agent
**Job:** once QA passes, writes the Gumroad product description, launch social posts, and (later) email sequence — pulled from the *actual finished* content, not generic templates.
**Test to pass:** copy is ready to paste with zero edits needed.
**Output:** `product/[drop-name]/launch-copy.md`

### 7. CEO — you
**Job:** final go/no-go. Everything above is built to arrive at your desk needing a yes/no, not more work.

### 8. Post-First-Sale Retro (required, not optional)
**Job:** the moment the first real sale lands on a drop, the whole team stops and looks at what actually happened — every role checks its own stage against what worked and what nearly broke.
**Test to pass:** each stage names one thing to keep doing and one thing to fix before the next drop. No stage skips this by saying "it was fine."
**Output:** notes added to this file or a `product/[drop-name]/retro.md`, so the next drop starts smarter, not from scratch.

## Team norms (how the roles actually work together)

- **Cross-agent help is expected, not exceptional.** If a role notices another is overloaded or better suited to solve something outside its own lane, it says so directly and takes the task — and states clearly what it took and why, so nothing silently falls through a gap.
- **Feedback is always forward, never blame.** "Here's what we can fix, and how" — never "you failed." See `org/mission.md`.
- **New roles get proposed by naming the trade-off:** which existing role's plate gets lighter, and how it moves the whole system faster — not automation for its own sake.

---

## What's already true today vs. what needs a decision

**Already buildable, right now, in this same session:** every step above except the actual click-by-click upload to Gumroad — I don't have a connected browser in this session, so that last physical step is still yours (or I can walk you through it live like we've been doing).

**The real decision:** do you want this pipeline to run **inside sessions like this one**, on your command ("New drop: X"), with me orchestrating the sub-agents and reporting back at each gate — or do you want **fully autonomous bots running without you or me in the loop at all** (e.g., on a schedule, triggered by a calendar/trigger, publishing without a human checkpoint)?

The first option works today, costs nothing extra, and keeps a human check before anything goes live. The second option is a bigger build — it means wiring real automation infrastructure (scheduled triggers, possibly external tools) and removing the human approval gate, which I'd want to be deliberate about before setting up, especially for anything that spends money or publishes publicly on its own.

**My recommendation: start with the first.** Run the pipeline on-demand for each new drop, keep the CEO gate, and only talk about full autonomy once you've seen the pipeline work end-to-end a few times and trust it.
