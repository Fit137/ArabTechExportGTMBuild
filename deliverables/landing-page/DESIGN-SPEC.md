# Arab Tech Export, landing page design spec

**Deliverable:** one continuous scroll page. Not a deck, not slides. No pagination, no
arrow keys, no presenter mode. The page is read alone, on a phone, in about 90
seconds of scrolling before anyone reads a word.

**Source copy:** `ArabTechExport_Landing_Page.md`. Every number traces to
`PROOF-LEDGER.md`.

**Design system:** yours. This document does not specify palette, type, spacing or
components. Colour is referenced by role only, `accent`, `ink`, `surface`, `muted`,
`warning`. Use your own tokens for all of it.

---

## Part 0, the page at a glance

| | |
|---|---|
| Format | One scroll, 16 scenes, no pagination |
| Motion | CSS 3D transforms plus one `requestAnimationFrame` loop. No 3D libraries |
| Register | **Objects land.** Weight, settle, impact. This reader is spending their own money at a local income. Precision, not spectacle |
| Text budget | Under 900 words visible at rest across the whole page. The rest lives in hover, tap and scroll states |
| Spine | The work is good enough. The paperwork is what fails, and you can see exactly which piece |
| Carrying line | **Four departments decide. None of them were on the call.** |
| Carrying number | **30 percent**, withheld over one missing form |
| Centrepiece | Scene 7, the Ladder, at 44 percent through |
| Loop | Scene 16 returns to scene 1's object with its state changed |

**The arc:** *your work is fine → four people you never met decide → here is what each checks → here is which part is free → here is the room → here is the door.*

---

## The one rule that governs every visual

Delete any graphic on this page. If nothing is lost, it was decoration and it comes
out.

Every object below carries a specific argument. Where the motion **is** the claim,
it is marked **motion-as-claim**. Those are the ones to build first and the ones
worth spending the performance budget on.

---

## Scroll mechanics, the part a deck spec does not cover

### Three scene behaviours, and nothing else

| Behaviour | Use when | Mechanic |
|---|---|---|
| **Reveal** | Most scenes | `IntersectionObserver` at `threshold: 0.35`, play once, never replay on scroll-up |
| **Pin and scrub** | Scenes 4, 7, 8 only | Scene sticks for 100vh of scroll, animation progress maps to scroll position |
| **Ambient only** | Scenes 5, 12 | No entry animation. The object is already at rest and breathing |

**Three pinned scenes maximum.** Four or more and the page feels like it is fighting
the reader's scroll, which is the most common way a page like this fails.

### Scroll rules

1. **Scrub with damping.** Lerp scroll progress at `0.12` per frame. Raw scroll
   position driving transforms reads as jittery on every trackpad.
2. **One `rAF` loop for the whole page.** Never a scroll or pointer handler that
   writes transforms directly.
3. **Only the active scene animates.** Objects outside the viewport get
   `animation-play-state: paused` and drop `will-change`.
4. **Play once.** Scrolling back up shows resolved states. Re-triggering on every
   pass is the fastest way to make a page feel cheap.
5. **Never hijack scroll speed.** No smooth-scroll libraries, no scroll-jacking to
   snap between scenes. The reader keeps control of the page at all times.
6. **Budget:** 60fps on a mid-range Android. If a scene cannot hold it, cut the
   scene's depth layers before cutting its idea.

### Mobile, which is most of this audience

- No hover anywhere. Every hover reveal has a tap equivalent that expands in place.
- Pinned scenes stay pinned but shorten to 60vh of scroll.
- Depth reduces: 3 Z-layers maximum instead of 5.
- The four-stat bar in scene 1 becomes a 2x2 grid, never a horizontal scroll.

### Reduced motion is a first-class state

Under `prefers-reduced-motion: reduce`, the page ships **the resolved end state of
every object**. Not a static fallback, the finished frame. The four gates are open.
The ladder is built. The stack has landed. Opacity and colour transitions under
200ms are still allowed. Nothing translates, rotates or scrubs.

---

## The recurring motif, specified once

**Four ticks.** Four small vertical bars in a row, equal width, gap equal to bar
width. Lit bars use `accent`, unlit use `muted` at 25 percent opacity.

The number of lit bars is the band. It is never labelled, never explained, and has
no legend anywhere on the page.

| Appears in | Lit state |
|---|---|
| Scene 1, beside the fourth stat | 1 of 4 |
| Scene 4, on the deal token | 1 of 4 |
| Scene 7, on each platform of the ladder | 1, 2, 3, 4 |
| Scene 15, in the scorecard result card | varies |
| Scene 16, footer | 4 of 4 |

By its third appearance the reader knows what it means. That is the whole point of
using it four times and explaining it zero times.

---

## Part 1, the sixteen scenes

Each scene gives: **what stays on screen**, **what moves into interaction**, and the
**object brief**. The copy diet is not optional. It is how the page gets to under
900 visible words.

---

### Scene 1 · Hero
**Job:** name the mechanism nobody told them about, in one line.

**On screen**
- Eyebrow, headline, one two-line sub, four stat tiles, two CTAs. Nothing else.

**Cut from the source copy**
- The three-paragraph framing block collapses to one line: *Procurement, legal,
  security and finance each check something different. The deal waits for all four.*
- The "Built for" line moves under the primary CTA at small size.

**Hero object, The Four Gates.** **Motion-as-claim.**
- **Construction:** four upright planes receding in Z at `translateZ(0, -140px, -280px, -420px)`, each rotated `rotateY(-6deg)` so the reader sees their faces and edges. Label each on its edge, not its face: Procurement, Legal, Security, Finance. Edge labels read at a glance and do not compete with the headline.
- **The token:** one small slab, `accent`, carrying the four-tick motif at 1 of 4 lit. It is the deal.
- **Entry, 1,400ms total:** gates fade up in sequence, 120ms stagger, from nearest to furthest. At 700ms the token enters from the reader's side and travels toward gate 1. It passes gate 1 at 900ms, gate 2 at 1,100ms, and **stops dead at gate 3 with a 90ms impact and a 3px camera shake**. Gate 3 stays closed. Gates 3 and 4 dim to `muted`.
- **Why it stops at three:** security is the gate most of this audience has never heard of. The object makes the argument before the copy does.
- **Ambient:** gates drift ±0.4deg yaw on a 11s loop, out of phase by 2.5s each. The stalled token pulses opacity 0.85 to 1.0 on a 3s loop. Nothing else moves.
- **Interaction:** hover or tap a gate to reveal its one-line check. Gate 3 reveals *"Can they assess your risk without a six week detour."*
- **Restraint:** **the four stat numbers count up exactly once, on first view, over 900ms, and then never again.** No looping counters. A number that re-animates when the reader scrolls back reads as a slot machine and destroys the trust the number was there to build.
- **Reduced motion:** gates present, token already stopped at gate 3, gates 3 and 4 already dim. Stats render final.

---

### Scene 2 · The Case: why export, why now, why AI, why you
**Job:** carry the whole thesis in four objects, readable without reading.

**On screen**
- Section headline. Four claim cards, each: a number, a three-word label, one line.
- **Sources render as a hover or tap, not as visible text.** Attribution is essential and it is not what the eye should land on.

**Cut from the source copy**
- Every bullet list. Each claim keeps one figure on screen. The rest lives in the card's expanded state.
- The "same capability is priced against what the buyer compares it to" line moves to the card back.

**Four objects, one per claim. All share a 14s ambient cycle, offset 3.5s.**

**2a, Why export. The Budget Mass.**
- A volumetric dot-field, roughly 2,000 points, forming a soft mass. It grows outward from a single origin point over 900ms on entry, then holds.
- Label: `$2.59T`, tabular figures.
- **Argument:** the budget is large and it is expanding. No comparison to anything, which is what keeps it inside the claim constraints.

**2b, Why now. The Supply Gap.** **Motion-as-claim.** *Build this one first.*
- Two extruded columns side by side. Left is demand, 1.6M. Right is supply, 518k.
- **Entry:** both rise together from zero over 800ms. Demand keeps rising. **Supply stops at 31 percent of demand's height and visibly strains**, a 2px vertical judder over 400ms, then settles.
- This is the single best visual on the page. The gap is not drawn, it is enacted.
- Label the ratio `3.2 : 1` between them.

**2c, Why AI. Two Growth Arcs.**
- Two arcs rising in Z, one at 63 percent, one at 117 percent. Not a chart. Two ribbons in perspective, the steeper one in `accent`.
- Restraint: no axes, no gridlines, no legend. Two shapes and two numbers.

**2d, Why you. The Screen That Does Not Filter.**
- A vertical mesh plane with many small apertures. Tokens approach from behind it and pass through freely.
- **Argument:** OFAC screening is entity based, not country based. The mesh is a screen that does not stop you. The object says "you are not excluded" without the page having to raise the doubt in words.
- **Restraint:** this must not read as a wall or a border. Apertures are wide, the plane is thin and semi-transparent, and tokens never slow down. Getting this wrong introduces an anxiety the copy is trying to resolve.

**Reduced motion for all four:** mass formed, supply column already short and settled, arcs drawn, tokens already through the mesh.

---

### Scene 3 · What you are already doing right
**Job:** validate, and plant four objects that scene 4 will reuse.

**On screen**
- Headline. Four blocks, each with a three-word label. One line each, at small size.

**Object, Four Solid Blocks.**
- Four extruded blocks, evenly lit, in `accent`. They should look **well made**. This is the only scene on the page where the objects are unambiguously good.
- **Entry:** they assemble into a neat row, 700ms, 90ms stagger, settling with a soft 60ms impact each.
- **Ambient:** almost none. A slow light sweep across all four, 12s loop.
- **Restraint:** **do not animate these beyond the entry.** This is the calm before the pain and it needs to feel settled. Scene 4 is where they move, and the contrast only works if this scene is still.
- **Continuity:** remember their positions exactly. Scene 4 reuses them.
- **Reduced motion:** four blocks present, assembled, lit. No entry, no sweep.

---

### Scene 4 · But you are still losing
**Job:** the same four blocks, seen from the buyer's side, where they are invisible.

**Behaviour: pinned, scrub over 100vh.**

**On screen**
- Headline. Five pains, each collapsed to a bold number plus a three-word head.
- `10-15%` platform commission, `30%` withheld, `$25k` threshold, `$50-200` card cap, and the unexplained loss.

**Cut from the source copy**
- Every explanatory paragraph. Each pain's full text lives in a tap-to-expand panel.
- The ASCII band comparison is deleted from the copy entirely and becomes the object.

**Object, The Camera Move.** **Motion-as-claim.** *This is the page's best idea.*
- Scene opens on scene 3's four blocks, in their exact final positions.
- **As the reader scrubs, the camera orbits 180 degrees to the far side.** From behind, the blocks are **flat, unlit, and unlabelled**. Same objects. No visible quality. Nothing to evaluate.
- **The argument:** you did the work correctly and the person deciding cannot see any of it. No copy makes this point as fast as the camera does.
- **At 60 percent scrub,** the four gates from scene 1 fade in behind the flat blocks, and the deal token stalls again.
- **At 85 percent scrub,** each of the five pain figures lands beside the relevant gate with a 90ms impact, one at a time, 140ms apart. `30%` lands on Finance. `$25k` lands on Procurement.
- **Ambient:** once resolved, the flat blocks breathe at 0.3 opacity, 4s loop.
- **Interaction:** tap any figure to expand its full pain copy in place, pushing the scene down rather than opening a modal.
- **Reduced motion:** ship the far side directly. Flat blocks, gates behind, five figures already landed. The orbit never runs.

---

### Scene 5 · Crescendo
**Job:** one quiet beat before the centrepiece.

**Behaviour: ambient only. No entry animation.**

**On screen**
- The crescendo copy, typeset large. That is all. No object.

**Brief**
- **This scene is deliberately empty of 3D.** The page has been dense and physical for four scenes. The centrepiece two scenes later only lands if the reader passes through stillness first.
- Background shifts to the page's lightest surface, the only light scene in a dark page, or the reverse if the system runs light.
- **Ambient:** an extremely slow light gradient drift across the type, 16s loop, amplitude low enough to be felt and not seen.
- **Restraint:** **no object, no parallax, no entry motion, no scroll effect.** If a builder adds a floating element here, the centrepiece loses its impact and nobody will be able to say why.
- **Reduced motion:** identical. This scene already qualifies.

---

### Scene 6 · The solution
**Job:** one origin, one destination, one route.

**On screen**
- Headline. The one-line value prop. The "This isn't, this is" disambiguation.

**Object, The Single Path.**
- A field of faint failed routes, five or six, rising toward a target and each stopping short in a different way. Then **one short direct path lights in `accent`** and connects.
- **Entry, 1,200ms:** failed routes draw first, 140ms stagger, each dimming as it fails. The connecting path draws last, 400ms, and holds lit.
- **Ambient:** the lit path pulses along its length, 6s loop, very low amplitude.
- **Restraint:** the failed routes are `muted` and thin. They must not look like a competitor attack. They are the reader's own previous attempts.
- **Reduced motion:** all routes drawn in their failed state, the connecting path already lit. No draw-on, no pulse.

---

### Scene 7 · The Ladder, centrepiece
**Job:** land the product in one object. This is the scene people will remember.

**Behaviour: pinned, scrub over 100vh.**

**On screen**
- Headline, *Move one band. Then the next.*
- One line: *Your band is what your setup can survive, not what you are bidding on.*
- Four platform labels. Deal sizes. Nothing else visible at rest.

**Cut from the source copy**
- The entire four-row band table. It becomes the object. Its content lives in each platform's expanded state.
- The four checkmark benefits move to scene 13.

**Object, The Ladder.** **Motion-as-claim.**
- Four platforms at increasing height and increasing Z-depth, so climbing is also moving away. Each carries the four-tick motif with 1, 2, 3, 4 lit.
- **Scrub behaviour:** as the reader scrolls, a figure-token climbs. **Each platform materialises only as the token reaches it.** Bands 2, 3 and 4 do not exist on screen until the climb reveals them, because most of this audience does not know they exist.
- **At each platform, the gates from scene 1 reappear at that band's difficulty:** band 1 shows one open gate. Band 3 shows four, three of them closed.
- **The token's ticks light one at a time as it climbs.** By band 4 the motif is fully lit, which is also its state in the footer.
- **Ambient:** platforms drift ±0.3deg, out of phase. The token idles with a 2s breathe.
- **Interaction:** tap any platform to expand what that band requires, in place.
- **Restraint:** **do not add particles, trails, or a glow to the climb.** The climb is the argument and it is legible. Effects on top of it will read as a game and this reader is deciding whether to spend real money.
- **Reduced motion:** all four platforms present and lit, token at band 1, gate states shown per band. No climb.

---

### Scene 8 · How it works, three steps
**Job:** make the method feel sequenced and achievable.

**Behaviour: pinned, scrub. Three sub-states across 100vh.**

**On screen**
- Three numbered steps. Each: verb, one "Stop X. Start Y." line, three-word bullets only.

**Cut from the source copy**
- All six dimension descriptions in step 1. They become the hexagon's labels.
- The "Real Example" paragraph moves to a tap state on step 3.

**Object, one per step, transitioning into each other.**

**8a, Diagnose. The Hexagon.**
- Six-axis radar in 3D, tilted 20deg. Six labelled vertices. A partial shape fills in over 700ms, uneven, with two axes visibly short.
- The four-tick motif appears beside it showing the resulting band.

**8b, Build. The Sorting.** **Motion-as-claim.**
- The six axis values detach and become six slabs. **They physically sort into two groups: free to fix, and costs money.** The free group is larger and lands first.
- **This is the split promise rendered as a physical sort.** It is the clearest expression of the offer anywhere on the page.
- Then the slabs restack **in blocking order**, not in the order they were sorted. The reorder is the second half of the argument.

**8c, Apply. The Document.**
- A single document plane. Three marks land on it, 90ms impact each, 200ms apart. Then it **duplicates into three copies that travel to three of the four gates.**
- The champion pack, rendered. The document going where the reader cannot.

**Ambient:** hexagon rotates ±0.4deg, 12s. Slabs settle and hold. Document edge catches a slow light sweep.

**Restraint:** the transition between 8a, 8b and 8c must be a **transformation of the same matter**, never a fade between three separate illustrations. If the builder fades, the sequence loses its meaning and becomes three unrelated pictures.

**Reduced motion:** three resolved states stacked vertically. Hexagon filled, slabs sorted and stacked, document marked and duplicated.

---

### Scene 9 · Versus the alternatives
**Job:** concede honestly, then name the gap. Counter-argument scene.

**On screen**
- Two comparison blocks, free content and marketplaces.
- **Rows collapse to their two-word head.** Full text on tap.

**Object, The Hinge.**
- Two planes joined on a vertical axis. Each rotates to face the reader as they scroll past it, while the other recedes.
- **Critical:** on the rows where the alternative genuinely wins, **the alternative's plane lights in `accent` and rotates forward.** Free content wins on cost and breadth. Marketplaces win on buyers available today and payment protection.
- **Argument:** the object concedes before the copy does. A comparison where our side lights on every row is one every reader has seen and discounted.
- **Ambient:** both planes drift ±0.3deg on a 10s loop, counter-phase, so the hinge
  reads as a live joint rather than a static fold.
- **Restraint:** never rotate a losing option to invisible. Rotate it to edge-on at 90deg so it remains present. Disappearing an alternative reads as hiding it.
- **Reduced motion:** both planes flat and forward, winning rows marked with a static indicator.

---

### Scene 10 · What it costs
**Job:** show the shape without inventing a price.

**On screen**
- Four tier cards. Names, what each carries you through, and the price field.

**Object, Four Cards in Depth.**
- Cards staggered in Z. The founding cohort card pulls forward on hover or tap and unfurls its terms.
- **The `{TBD}` prices render as a visible blank field, an underscore rule in `muted`, not as a number and not as the word "TBD".** An empty field reads as honest. A fake number would contradict the scene two scrolls below it.
- **Ambient:** a sheen tracks the pointer across the card faces. On touch, a slow automatic sheen, 9s loop.
- **Reduced motion:** cards flat in a row, founding card already forward.

---

### Scene 11 · What we do not have yet
**Job:** the honesty scene. Structurally the page's second-most important moment.

**On screen**
- Headline. Four empty slots. Four things that stand in their place.

**Object, The Empty Shelf.** **Motion-as-claim.**
- Four testimonial-shaped frames, **rendered as dotted outlines, unlit, genuinely empty.** No skeleton shimmer, no "coming soon", no placeholder avatar.
- **They stay empty.** Nothing ever fills them.
- Below, four solid objects land with weight: the IRS source, the published method, the written terms, the capped cohort. **Solid, lit, real.**
- **Argument:** the page tells the reader that buyers discount generic testimonials and demand attributable proof. Then it shows its own empty frames and does not fill them. The object is the credibility.
- **Entry:** empty frames draw first, 600ms, thin dotted stroke. Then a 700ms pause, which is long and deliberate. Then the four solid objects land, 90ms impact, 160ms apart.
- **The 700ms pause is the scene.** Do not shorten it.
- **Ambient:** empty frames do nothing at all. Solid objects have a slow light sweep.
- **Restraint:** **no shimmer, no pulse, no loading state on the empty frames.** Anything that suggests they will fill later turns an honest statement into a tease.
- **Reduced motion:** frames empty, solid objects landed. Identical outcome.

---

### Scene 12 · FAQ
**Job:** answer objections without visual noise.

**Behaviour: ambient only.**

**On screen**
- Seven questions, collapsed. Short answers only. Detailed answers on expand.

**Brief**
- **No hero object.** The page has had eleven. This is a working scene and it should feel like one.
- Expansion: 280ms height transition, content fades at 180ms delayed 100ms.
- **Ambient:** the four-tick motif sits small in the section corner, fully lit, doing nothing. Its fifth and final appearance before the footer.
- **Restraint:** no 3D, no parallax, no scroll effects. Readers arriving here are close to deciding and want answers, not atmosphere.
- **Reduced motion:** expansion becomes instant, no height transition. Everything else in this scene is already compliant.

---

### Scene 13 · Transform close
**Job:** sharpen the decision with contrast.

**On screen**
- Two columns. Old way, five items. The Arab Tech Export way, five items.

**Object, The Flip.**
- Five slabs laid flat, each carrying an old-way behaviour. **Each flips 180deg to reveal the new behaviour on its reverse.**
- Flip on scroll progress, 420ms each, 120ms stagger.
- **The flip is the argument.** Same slab, same position, different face. It is the same person and the same work, handled differently.
- **Ambient:** once flipped, a slow tilt ±0.3deg, 10s.
- **Reduced motion:** slabs already flipped, new-way face showing, old-way text rendered small above each.

---

### Scene 14 · Founding cohort
**Job:** make the scarcity structural and visible.

**On screen**
- Headline. Four benefit lines. One CTA.

**Object, The Token Board.** **Motion-as-claim.**
- Twelve sockets in a ring over a floor. Filled sockets carry a token, empty sockets are visibly empty.
- **The board renders the true current count.** If nine places remain, nine sockets are empty. **The brief forbids showing a nearly-full board when it is not.** Fake scarcity in a business selling credibility is a contradiction the reader will feel even if they cannot name it.
- **Entry:** floor fades up, sockets draw, then filled tokens drop in with 90ms impacts, 100ms apart.
- **Ambient:** filled tokens breathe slightly. Empty sockets are still.
- **Interaction:** hover or tap an empty socket, it lifts 4px and the CTA label pulses once.
- **Reduced motion:** board rendered at true state, no drops.

---

### Scene 15 · Scorecard CTA
**Job:** the low-commitment path, and it should feel like a gift.

**On screen**
- Headline. Six dimension names. One line: 7 questions, 6 dimensions, your band.

**Cut from the source copy**
- All six dimension descriptions. They live on the hexagon's vertices as hover or tap.
- The "receive instantly" list collapses to four icons with three-word labels.

**Object, The Hexagon Returns.**
- Scene 8a's hexagon, now empty and outlined, slowly rotating.
- **Interaction:** as the pointer moves across it, axes light in sequence, suggesting a score without producing a fake one.
- **Never render a specific example score.** A pre-filled result implies a verdict before the reader has answered anything, and this instrument's whole design rule is that it never delivers a verdict.
- The four-tick motif sits beside it, unlit, waiting.
- **Ambient:** the hexagon rotates continuously, ±0.5deg yaw and a slow 20s full
  rotation in place. It is the only object on the page that turns all the way round,
  because it is the only one inviting an action rather than making an argument.
- **Reduced motion:** hexagon outlined and still, axes unlit.

---

### Scene 16 · Footer, loop close
**Job:** close the visual loop opened in scene 1.

**On screen**
- Brand line. One-line positioning. Contact.

**Object, The Four Gates, Open.**
- Scene 1's four gates, at the same depths and the same angles. **All four now open.** The token passes through all four and continues past the last one, out of frame.
- Its four ticks are fully lit.
- **Entry:** gates open in sequence from nearest to furthest, 160ms stagger, 500ms each. Token travels through as they open. It does not stop.
- **Argument:** the page opened with a token stalled at gate 3. It closes with the same token through all four. Nothing is claimed in words. The loop makes the promise and the copy never has to.
- **Restraint:** no celebration. No burst, no confetti, no flourish on exit. The token leaves quietly. Clearing procurement makes you eligible, it does not win the deal, and a triumphant exit would be the page's only broken promise.
- **Reduced motion:** gates open, token past the last gate, ticks lit.

---

## Part 2, motion specification

Design system is yours. This is motion only.

### Timing

| Event | Duration |
|---|---|
| Scene entry | 600 to 900ms |
| Stagger between siblings | 90 to 140ms |
| Impact, land, settle | 90 to 120ms |
| Flip | 420ms |
| Hover response | 180ms |
| Expand, collapse | 280ms |
| Ambient loop | 8 to 14s |
| Scroll damping lerp | 0.12 per frame |

**One easing curve for the whole page.** `cubic-bezier(.22,1,.36,1)` unless your
system specifies otherwise. What changes between scenes is settle duration and
impact weight, never the curve.

### Ambient amplitude

±0.3deg to ±0.5deg yaw. Larger reads as broken. Every object that is not
deliberately still gets one. Nothing on this page is frozen, and nothing on this
page is busy.

### The 3D construction

Standard stage, rig, face, edge, side. `perspective` on the stage,
`transform-style: preserve-3d` on the rig, faces positioned with `translateZ`.
Pointer parallax coalesced into the single `rAF` loop, damped, capped at ±6deg.

**No WebGL. No 3D libraries.** CSS 3D transforms cover every object above. A canvas
context costs crisp type, and the numbers on this page are what it is carrying.

### Numerals

**Tabular figures for every numeral on the page, always.** `$2.59T`, `30%`, `3.2 : 1`,
`$25,000`. A figure that reflows while it counts destroys the trust the figure was
placed there to build.

### Performance

- Promote at most four layers with `will-change` at once. Release immediately after.
- One `rAF` loop. No transform writes from scroll or pointer handlers.
- Pause every object outside the viewport.
- Target 60fps on a mid-range Android. Cut depth layers before cutting ideas.

---

## Part 3, the text diet

The source copy is about 3,200 words. **The page renders under 900 at rest.** Here
is where the rest goes.

| Scene | Source | Visible at rest | Where the remainder lives |
|---|---|---|---|
| 1 | 180 | 60 | Gate hover reveals |
| 2 | 340 | 90 | Card expand, source attributions on hover |
| 3 | 120 | 40 | Nowhere. Genuinely cut |
| 4 | 420 | 70 | Tap to expand per pain |
| 5 | 90 | 90 | All of it. This scene is the copy |
| 6 | 110 | 50 | Nowhere |
| 7 | 260 | 60 | Platform tap states |
| 8 | 400 | 110 | Dimension labels, step 3 example on tap |
| 9 | 420 | 80 | Row expand |
| 10 | 120 | 60 | Founding card unfurl |
| 11 | 190 | 90 | Nowhere. This scene needs its words |
| 12 | 620 | 70 | Accordion. Questions visible, answers collapsed |
| 13 | 130 | 50 | Slab reverse faces |
| 14 | 90 | 50 | Nowhere |
| 15 | 220 | 60 | Hexagon vertex hover |
| 16 | 40 | 40 | Nowhere |

**Two scenes keep all their words on purpose.** Scene 5, the crescendo, where the
copy is the object. Scene 11, the honesty scene, where shortening it would make it
read as evasive.

**Rule for the builder:** if a scene's visible word count runs over its budget,
cut copy before cutting the object. The page is designed to be understood by
someone who reads none of it.

---

## Part 4, before you build

### Verified

- Every figure on the page traces to `PROOF-LEDGER.md` with a source and a tier.
- The gate sequence, procurement, legal, security, finance, comes from the Block 1
  research and is not a metaphor invented for this page.
- The 30 percent withholding figure is IRS primary source.
- The band thresholds are written as "about" everywhere, because they are inferred
  from contract-value tiers rather than published policy.

### To settle before build

1. **The founding cohort count in scene 14.** The board must render the true number
   of remaining places. If that number is not tracked anywhere, the scene cannot be
   built honestly and should be replaced with a static twelve-socket board showing
   the cap without implying a fill level.
2. **Prices in scene 10.** They render as blank fields. If pricing is decided before
   build, the scene works better with real numbers. If it is not, the blanks ship.
3. **Whether the page runs Arabic.** Every object above is direction-agnostic except
   the ladder in scene 7 and the path in scene 6, both of which read left to right.
   **Under RTL both must mirror.** A ladder climbing away from the reading direction
   fights the reader.
4. **The light scene in 5.** It assumes the rest of the page is dark. If your system
   runs light by default, invert it. The requirement is contrast against its
   neighbours, not a specific value.

### Invented for this page, and what committing costs

- **The four gates as a visual object.** The four-lane sequence is from the research.
  Rendering them as physical gates is a design invention. Cost: it becomes the
  page's central metaphor and appears in scenes 1, 4, 7, 8c and 16. Changing it later
  means rebuilding five scenes.
- **The camera orbit in scene 4.** The idea that the reader's good work is invisible
  from the buyer's side is an interpretation of the research, not a stated finding.
  It is the page's strongest moment and it is an argument by analogy.
- **The four-tick motif.** Invented. It has no meaning outside this page, which is
  why it is never labelled. Cost: it needs to appear in the product too, or it reads
  as decoration the first time someone visits the actual community.
- **The empty shelf staying empty.** A deliberate design commitment. If marketing
  later wants placeholder testimonials in those frames, the scene's entire argument
  inverts and it should be removed rather than filled.

Decide these before the build starts. Scenes 1, 4, 7 and 16 are one connected
system, and they are expensive to change once built.
