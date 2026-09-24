# Brand & Quality Standard — All Drops

This is a standing rule, not a one-time note. Every digital product this business ships — the Wealth Architect, the Savings Architect, the Dating Architect, and anything after it — is held to this bar. Read alongside `org/operating-model.md`.

## The bar

**100x the top-selling comparable product on Gumroad, not "good enough."** Before shipping any drop, the real test is: put it next to the best-selling thing in that category on Gumroad right now. If it doesn't clearly beat it on design, depth, and desirability, it's not done.

## Tone — every guide, every page

High-energy, direct-address, momentum-driven. The reader should feel like something is happening to them, not like they're reading a manual. No dry textbook voice, no hedging paragraph after paragraph, no "studies show" academic tone. Short punchy sentences mixed with longer ones for rhythm. Second person ("you"), always. This isn't optional per-product — it's the house voice.

## Covers — the emotional bar, not just the design bar

A cover is not done when it "looks clean." It's done when it makes someone feel **"I need this. This speaks to me. I want to be that person."** That's an identity/aspiration trigger, not a design checklist. Concretely:
- Aspirational, cinematic imagery over flat corporate/infographic style — evoke the outcome (freedom, status, confidence), not just the topic
- Bold, confident typography that reads as exclusive, not generic
- Never use real people's likenesses — silhouettes, symbolic imagery, or abstract cinematic scenes instead
- The cover should work as a thumbnail at small size (Gumroad grid, social post) — test legibility small, not just full-size

## Drops should feel exclusive

Every product page and every guide should read like the buyer got access to something insiders have, not a generic PDF anyone could produce. This shows up in: naming ("The [X] Architect System," not "[X] Guide"), scarcity/insider framing in copy where honest to do, and content depth that free versions circulating online don't match.

## Logos & marks — the standard, not the vibe

Researched against real top-rated Fiverr logo sellers before writing this rule (see `product/logo-design-research.md`): **glow, neon, particle, chrome, and gradient effects are an amateur/AI tell, not a premium signal.** They fail every real test a professional mark has to pass. A logo isn't done until it passes all of these:
- **Flat, 1-2 solid colors, no gradient/glow/bevel/drop-shadow** — ever, on the primary mark
- **Silhouette test:** still reads clearly as pure black on white, and pure white on black
- **Scalability test:** still recognizable shrunk to a 16px favicon
- **Single-color test:** every line is a clean closed stroke that would survive embroidery or one-color screen printing
- **Full set, not just one file:** primary lockup, icon-only mark, full-color, all-black, all-white/reverse, single-color version

A "hero shot" with lighting/glow/3D treatment can exist as a secondary marketing image (social posts, a website banner) — it is never the primary logo file, and the flat vector master must exist first.

## The Master Prompt — reusable formula for every future visual generation

This exists because getting the Wealth Architect HQ logo right took three rejected rounds (glow/neon, flat-but-boring, bold-but-still-wrong) before landing on the approved version. That's expensive. This section encodes what actually worked so the next room — HEARTH, CHALK, HOWL, INK, or whoever comes after — hits the bar on attempt one instead of six.

**Step 1 — Reference beats description, every time.** If an approved reference image exists (a previously-approved asset, or one PROTON sends directly), attach it via Higgsfield's image-upload pipeline (`media_upload` → upload the bytes → `media_confirm` → `generate_image` with the `image_references` role) instead of describing it in prose. Matching an actual image always beats matching an adjective.

**Step 2 — The material/lighting language that worked.** Keep this sentence structure, fill in the brackets:

> "[SUBJECT/CONCEPT], rendered in brushed and polished [MATERIAL] with realistic material reflections, dramatic clean studio lighting from above-left creating bright specular highlights on the raised surfaces, richer/darker tones in the shadowed recessed areas, subtle soft reflection on the ground beneath the object, on a plain [BACKGROUND COLOR] background, [ONE unified silhouette description] — no clip-art combination of separate symbols, one ownable continuous shape."

**Step 3 — One silhouette, not a collage.** The single biggest difference between the rejected rounds and the approved one: rejected versions combined multiple recognizable symbols as separate elements (compass + arrow + chart line, each doing its own thing). The approved version reads as one continuous, ownable shape. Before generating, state the single silhouette in one sentence — if it takes an "and" to describe the shape, it's still a collage, not a mark, and it isn't ready to generate yet.

**Step 4 — The dual-deliverable rule still applies, unchanged.** A dimensional hero-shot render (Steps 1-3) is the secondary marketing asset — a social post, a cover element, a banner. It is never the only file. The flat, 1-2 solid color, no-glow vector master (per the Logos & Marks standard above) still has to exist, either as its own flat-vector generation pass or by simplifying the hero shot's approved silhouette. Shipping the dimensional version alone and calling it done fails this whole section.

**When no reference exists yet:** skip Step 1, generate 2-3 options using Steps 2-3 language, and bring them to PROTON for a reference-quality pick before iterating further — never guess blind for multiple rounds hoping to land on the right direction by chance.

**Lesson from the actual shipped Wealth Architect HQ logo (learn this one, don't relearn it):** PRISM's lockup attempts placed the icon beside the wordmark, flat, side-by-side — none of them landed. The version PROTON actually shipped is a **contained badge/emblem**: the icon sits inside a bordered circular badge, with the wordmark as a banner underneath the icon, inside the same badge — not beside it. Badge/emblem format reads more premium and more "insider" than a side-by-side lockup, and matches the exclusivity bar in this file. Default to the badge/emblem structure for any future icon+wordmark lockup, not a side-by-side pairing.

## Applies going forward without being re-asked

Any new product drop, cover, or piece of sales copy in this repo should be built against this standard by default. If a draft doesn't clearly clear the bar, redo it before showing it, rather than shipping something merely adequate and waiting for feedback to fix it.
