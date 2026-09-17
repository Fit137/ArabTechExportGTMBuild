# Arab Tech Export, landing page design spec, v2

**Supersedes v1.** The previous version built the page around a riddle headline and
had no ICP callout. A visitor had to read four sections before knowing whether the
page was for them. This version names the reader in the first ten words.

**Deliverable:** one continuous scroll. Thirteen scenes. Not a deck.

**Design system:** yours. Colour referenced by role only. The brand palette is green,
`#00A45C` primary, `#062B21` ink.

---

## Part 0, at a glance

| | |
|---|---|
| Scenes | 13, down from 16 |
| Visible words at rest | Under 700, down from 900 |
| Register | **Objects land.** Weight, settle, impact. Never float, never bounce |
| Reader | An Arab engineer who can build AI and has never sold to a US company |
| Job of the page | Tell them in five seconds that this is for them, then prove it |
| Centrepiece | Scene 8, the Band Ladder, at 61 percent |
| Motion | CSS 3D transforms, one `rAF` loop, no libraries |

**The arc:** *here is what you get → here is whether you qualify → here is what is blocking you → here is why now → here is the method → here is the way in.*

---

## The rule that changed

**v1 was too clever.** Every section headline was a claim that needed decoding. This
version says what each section is, plainly, and puts the cleverness in the objects
instead.

**Section headlines are labels. Objects carry the argument.** If a visitor reads only
the headlines, they should understand the offer. If they read none and only look,
they should understand the offer.

---

## The logo constraint, read this before building anything

The brand mark is a segmented pointed arch. **It appears in the navigation and the
footer, nowhere else.**

Do not use an arch, a gate, a portal or any arch-derived form as a page illustration.
v1 did this and it costs the mark its meaning: a logo that also appears as decoration
six times stops reading as a logo. Scarcity is what makes a mark a mark.

The page's own visual language is **tracks, checkpoints, stacks and sorts.** Not
arches.

---

## Scroll mechanics

| Behaviour | Scenes | Mechanic |
|---|---|---|
| **Reveal** | Most | `IntersectionObserver` at 0.35, play once, never replay on scroll-up |
| **Pin and scrub** | 3, 8 only | Sticks for 100vh, animation maps to scroll |
| **Ambient only** | 11 | Already at rest, breathing |

**Two pinned scenes maximum**, down from three. The page is shorter and pinning is
expensive attention.

**Rules.** Lerp scroll at 0.12. One `rAF` loop for the page. Only the active scene
animates. Play once. Never hijack scroll speed. 60fps on a mid-range Android.

**Mobile.** No hover, every reveal has a tap equivalent expanding in place. Pinned
scenes shorten to 60vh. Three Z-layers maximum. The hero stat row becomes 2x2.

**Reduced motion** ships the resolved end state of every object, not a static
fallback. Opacity and colour under 200ms still run.

---

## The recurring motif

**Four ticks.** Four small vertical bars, equal width, gap equal to bar width. Lit in
`accent`, unlit in `muted` at 25 percent. Lit count is the band.

Appears in scenes 1, 5, 8 and 12. Never labelled, no legend. Third appearance is when
the reader gets it.

---

# The thirteen scenes

---

### Scene 1 · Hero
**Job:** name the reader and the outcome before they scroll.

**On screen**
- Eyebrow: *For Arab engineers and AI builders*
- Headline: *Build an AI Services Company That Sells to America.*
- Two short lines. Two CTAs. Four stat tiles.

**Object, The Route.** **Motion-as-claim.**
- A horizontal track running left to right across the right half of the viewport.
  Left terminal is a small solid slab, the reader's work. Right terminal is a larger
  form, the US buyer.
- **The track starts plain.** At 600ms, **four checkpoints materialise along it**,
  evenly spaced, each labelled on its underside at small size: Procurement, Legal,
  Security, Finance.
- **Argument:** the path has structure you could not see. Not that you failed, that
  it was invisible.
- **Do not animate the token through the checkpoints in the hero.** That promises
  the outcome in the first five seconds and the page spends the next twelve scenes
  being careful not to. The token sits at the left terminal, waiting.
- **Ambient:** checkpoints drift ±0.4deg yaw, 11s, out of phase by 2.5s. The token
  pulses opacity 0.85 to 1.0, 3s.
- **Restraint:** **stat numbers count up once, on first view, 900ms, then never
  again.** A number that re-animates on scroll-back reads as a slot machine.
- **Reduced motion:** track and four checkpoints present, token at the left terminal.

---

### Scene 2 · This is for you if / not for you if
**Job:** qualify hard, in under four seconds. **The scene v1 did not have.**

**On screen**
- Two columns. Four green check items left, four muted cross items right.
- Each item: a bold three-to-six word head, one line under it.

**Object, The Sort.** **Motion-as-claim.**
- Eight small tokens arrive in a loose cluster at the centre, then **physically sort
  left and right**, four each way, 140ms stagger.
- Left tokens land lit, in `accent`. Right tokens land unlit and settle lower, with
  a heavier 120ms impact.
- **Argument:** the page is sorting the audience, openly, in front of them. A reader
  who belongs on the right learns it here instead of at checkout.
- **Restraint:** the right-hand column is **not** styled as failure. Muted, not red.
  No warning colour, no strikethrough. These are people the product does not serve,
  not people who are worse.
- **Reduced motion:** tokens already sorted.

**Copy diet:** this scene keeps all its words. It is the qualifier and shortening it
makes it vague, which defeats the purpose.

---

### Scene 3 · The problem is not your code
**Job:** name the mechanism and put a number on each failure.

**Behaviour: pinned, scrub 100vh.**

**On screen**
- Headline, then two beats.
- Beat one: *You send the proposal. It goes quiet.*
- Beat two: a six-row table, each row a blocker and its cost. Collapsed to bold
  figure plus three-word head.

**Object, The Stall and the Handoff.**
- **At 0 to 40 percent scrub:** the token from scene 1 travels right, reaches
  checkpoint 1, and **stops dead** with a 90ms impact and a 3px camera shake.
- **At 40 to 70 percent:** the camera pulls back to reveal **three more figures
  standing behind the checkpoint**, who were never on the call. They are plain
  forms, not characters. Small, unlit.
- **At 70 to 100 percent:** the six cost figures land beside the checkpoints they
  belong to, 90ms impact, 140ms apart. `30%` lands on Finance. `$25,000` on
  Procurement.
- **Argument:** the deal did not fail on the call. It failed in a room the reader
  was not in.
- **Interaction:** tap any figure to expand its full row in place. No modal.
- **Reduced motion:** ship the resolved frame. Token stalled, figures revealed,
  costs landed. No scrub.

---

### Scene 4 · Why this window is open now
**Job:** carry the market thesis in numbers, skimmable.

**On screen**
- Two clusters. *The budget arrived before the people did*, five figures.
  *They are already buying from outside*, three figures.
- Sources on hover or tap, never as visible text.

**Object, The Supply Gap.** **Motion-as-claim.** *Best object on the page.*
- Two extruded columns. Left is demand, 1.6M. Right is supply, 518k.
- **Both rise together from zero over 800ms. Demand keeps rising. Supply stops at 31
  percent of demand's height and visibly strains**, a 2px vertical judder over 400ms,
  then settles.
- Label the ratio `3.2 : 1` in the gap between them.
- The gap is not drawn. It is enacted.
- **Secondary:** a dot-field mass beside it for `$2.59T`, growing outward from one
  origin point, 900ms, then holding.
- **Ambient:** columns drift ±0.3deg, 12s. The mass has a slow internal shimmer, one
  point brightening at a time, 9s.
- **Restraint:** no axes, no gridlines, no legend anywhere in this scene. Two shapes
  and two numbers.
- **Reduced motion:** columns at final heights, mass formed.

---

### Scene 5 · What you learn
**Job:** show the six checks and which are free.

**On screen**
- Six rows. Number, three-word head, two column marks: free to fix, costs money.
- One line under: *Five of six are free.*

**Object, The Six, Sorted.** **Motion-as-claim.**
- Six slabs arrive in a column, then **split into two groups: five slide left into
  `accent`, one slides right and goes heavy and unlit.**
- Then the five restack **in blocking order**, not in the order they sorted. The
  reorder is the second half of the argument.
- **Argument:** this is the whole method in one motion. Most of what is missing is
  free, and the order matters.
- The four-tick motif appears beside the stack.
- **Restraint:** the paid item is not styled as bad. It is heavier and later, not
  wrong.
- **Reduced motion:** five stacked in order, one aside and heavy.

---

### Scene 6 · How it works
**Job:** three steps, achievable, sequenced.

**On screen**
- Three numbered steps. Verb, one bold *Stop X. Start Y.* line, one line under.

**Object, Three States of One Form.**
- **Diagnose:** a six-axis radar, tilted 20deg, filling unevenly over 700ms, two axes
  visibly short.
- **Build:** those six values detach and become the slabs from scene 5, re-sorted.
- **Apply:** a single document plane. Three marks land, 90ms each, 200ms apart. It
  then **duplicates into three copies that travel to three checkpoints.**
- **Restraint:** this must be a **transformation of the same matter**, never a fade
  between three illustrations. A fade makes it three unrelated pictures and the
  sequence loses its meaning.
- **Reduced motion:** three resolved states stacked vertically.

---

### Scene 7 · What you get
**Job:** make the offer concrete without a price.

**On screen**
- Three tier columns, nine feature rows, check marks.
- One line: pricing not set, founding terms permanent.

**Object, Three Cards in Depth.**
- Cards staggered in Z. Hover or tap pulls one forward and unfurls its rows.
- **`{TBD}` prices render as a visible blank underscore rule in `muted`.** Not a
  number, not the word TBD. An empty field reads as honest, and this page has a
  scene about honesty three scrolls down.
- **Ambient:** a sheen tracks the pointer across card faces. On touch, a slow
  automatic sheen, 9s.
- **Reduced motion:** cards flat in a row.

---

### Scene 8 · Your band decides everything, centrepiece
**Job:** the single idea the reader should remember.

**Behaviour: pinned, scrub 100vh.**

**On screen**
- Headline. One line: *Your band is what your setup can survive, not what you are
  bidding on.*
- Four band labels and deal sizes. Nothing else at rest.
- Bottom rail, quiet, small: *This makes you eligible. It does not win the deal.*

**Object, The Ladder.** **Motion-as-claim.**
- Four platforms rising in Y and receding in Z, so climbing is also moving away.
  Each carries the four-tick motif at 1, 2, 3, 4 lit.
- **A token climbs on scroll. Each platform materialises only as the token reaches
  it**, because most of this audience does not know bands 2 to 4 exist.
- At each platform, that band's checkpoint count appears: band 1 shows one, band 3
  shows four.
- The token's ticks light one at a time as it climbs.
- **Restraint:** **no particles, no trails, no glow on the climb.** The climb is the
  argument and it is already legible. Effects on top read as a game, and this reader
  is deciding whether to spend real money at a local income.
- **Restraint, second:** the token **stops at band 3.** It does not reach band 4 in
  this animation. Band 4 stays visible and unreached. Over-promising here undoes the
  bottom rail.
- **Interaction:** tap any platform to expand its requirements in place.
- **Reduced motion:** four platforms present and lit, token at band 1.

---

### Scene 9 · Compared to what you are doing now
**Job:** concede honestly, then name the gap.

**On screen**
- One table, three columns. Rows collapsed to two-word heads, full text on tap.

**Object, The Hinge.**
- Three planes on a shared vertical axis. The one being compared rotates to face the
  reader, the others recede to edge-on at 90deg.
- **Critical:** on rows where a competitor genuinely wins, **their plane lights in
  `accent` and rotates forward.** Marketplaces win on clients available today and
  payment protection. Free content wins on cost.
- **Restraint:** never rotate a losing option to invisible. Edge-on, still present.
  Disappearing an alternative reads as hiding it.
- **Reduced motion:** planes flat and forward, winning rows statically marked.

---

### Scene 10 · What we do not have yet
**Job:** the honesty scene. Structurally the second most important on the page.

**On screen**
- Headline. Four empty slots. Four things that stand in their place.

**Object, The Empty Shelf.** **Motion-as-claim.**
- Four testimonial-shaped frames, **dotted outlines, unlit, genuinely empty.** No
  skeleton shimmer, no "coming soon", no placeholder avatar.
- **They stay empty. Nothing ever fills them.**
- Below, four solid objects land with weight: the IRS source, the published method,
  the written terms, the capped cohort.
- **Entry:** frames draw first, 600ms, thin dotted stroke. **Then a 700ms pause,
  which is long and deliberate.** Then the four solid objects land, 90ms impact,
  160ms apart.
- **The 700ms pause is the scene. Do not shorten it.**
- **Restraint:** **no shimmer, no pulse, no loading state on the empty frames.**
  Anything suggesting they will fill later turns an honest statement into a tease.
- **Reduced motion:** frames empty, solid objects landed. Same outcome.

---

### Scene 11 · Questions
**Job:** answer objections without visual noise.

**Behaviour: ambient only.**

**On screen**
- Seven questions, collapsed. Short answers only.

**Brief**
- **No hero object.** The page has had nine. This is a working scene.
- Expansion: 280ms height, content fades at 180ms delayed 100ms.
- **Ambient:** the four-tick motif small in the corner, fully lit, doing nothing.
- **Restraint:** no 3D, no parallax, no scroll effects. Readers here are close to
  deciding and want answers, not atmosphere.
- **Reduced motion:** expansion instant.

---

### Scene 12 · Two ways in
**Job:** both CTAs, with the scarcity structural and true.

**On screen**
- Two panels. Founding cohort left, readiness check right.

**Object A, The Token Board.**
- Twelve sockets in a ring. **Renders the true remaining count.** If nine places
  remain, nine sockets are empty.
- **The brief forbids showing a nearly-full board when it is not.** Fake scarcity in
  a business selling credibility is a contradiction the reader will feel without
  being able to name it. If the count is not tracked, ship a static twelve-socket
  board that shows the cap and implies no fill level.
- Filled tokens drop in with 90ms impacts, 100ms apart.

**Object B, The Hexagon.**
- Scene 6's radar, now empty and outlined, rotating slowly.
- As the pointer crosses it, axes light in sequence, suggesting a score.
- **Never render a specific example score.** The instrument's design rule is that it
  delivers no verdict, and a pre-filled result breaks that before the reader answers.
- **Reduced motion:** board at true state, hexagon outlined and still.

---

### Scene 13 · Footer
**Job:** close quietly.

**On screen**
- Brand line, bilingual. One-line positioning. Contact.

**Object, The Route, Completed.**
- Scene 1's track returns at the same scale. **The token has moved past the fourth
  checkpoint and continues out of frame.** Its four ticks are lit.
- **Entry:** checkpoints fade up, token travels through, 160ms stagger.
- **Restraint:** **no celebration. No burst, no confetti, no flourish.** The token
  leaves quietly. Clearing the checks makes you eligible, it does not win the deal,
  and a triumphant exit would be the page's only broken promise.
- **Reduced motion:** token past the last checkpoint, ticks lit.

---

## Part 2, motion

| Event | Duration |
|---|---|
| Entry | 600 to 900ms |
| Stagger | 90 to 140ms |
| Impact | 90 to 120ms |
| Hover | 180ms |
| Expand | 280ms |
| Ambient loop | 8 to 14s |
| Scroll lerp | 0.12 |

**One easing curve for the page**, `cubic-bezier(.22,1,.36,1)`. What changes between
scenes is settle duration and impact weight, never the curve.

**Ambient amplitude** ±0.3deg to ±0.5deg yaw. Larger reads as broken.

**3D:** standard stage, rig, face, edge, side. Pointer parallax coalesced into the
single `rAF` loop, damped, capped ±6deg. **No WebGL, no 3D libraries.** A canvas
context costs crisp type and this page is carrying numbers.

**Tabular figures for every numeral, always.**

**Performance:** at most four `will-change` layers at once, released after. Pause
everything outside the viewport.

---

## Part 3, text diet

Source copy 1,763 words. **Page renders under 700 at rest.**

| Scene | Source | At rest | Remainder lives in |
|---|---|---|---|
| 1 Hero | 95 | 55 | Checkpoint labels |
| 2 Qualifier | 250 | **250** | Nowhere. Keeps everything |
| 3 Problem | 200 | 70 | Row tap expand |
| 4 Why now | 165 | 85 | Source attribution on hover |
| 5 What you learn | 150 | 75 | Row tap |
| 6 How it works | 105 | 55 | Step tap |
| 7 What you get | 130 | 60 | Card unfurl |
| 8 Bands | 175 | 60 | Platform tap |
| 9 Compared | 165 | 70 | Row expand |
| 10 Nothing yet | 95 | **95** | Nowhere. Needs its words |
| 11 Questions | 220 | 50 | Accordion |
| 12 Two ways in | 120 | 60 | Nowhere |
| 13 Footer | 45 | 45 | Nowhere |

**Two scenes keep everything.** Scene 2, because a vague qualifier does not qualify.
Scene 10, because shortening honesty reads as evasion.

**Rule:** if a scene exceeds budget, cut copy, never the object. The page is designed
to be understood by someone who reads none of it.

---

## Part 4, before you build

### Verified
Every figure traces to `PROOF-LEDGER.md` with a source and tier. The four-checkpoint
sequence comes from the Block 1 research, not from metaphor. The 30 percent figure is
IRS primary source. Band thresholds are written "about" everywhere because they are
inferred from contract-value tiers, not published policy.

### To settle
1. **The founding cohort count in scene 12.** Must render true. If untracked, ship
   the static cap version.
2. **Prices in scene 7.** Blank fields unless pricing is decided before build.
3. **RTL.** Scenes 1, 8 and 13 read left to right and **must mirror** under Arabic. A
   route running against the reading direction fights the reader.
4. **The founder FAQ answer** is `{TBD}` in the copy. The page ships with a visible
   gap there until it is filled, and that gap is in the most-read section.

### Invented, and what it costs
- **The route and checkpoints as a visual object.** The four-lane sequence is
  research. Rendering it as a track is a design invention, and it now appears in
  scenes 1, 3, 8 and 13. Changing it means rebuilding four scenes.
- **The four-tick motif.** Invented, never labelled. It needs to appear inside the
  product too or it reads as decoration the first time someone joins the community.
- **The empty shelf staying empty.** A deliberate commitment. If marketing later
  wants placeholder testimonials in those frames, the scene's argument inverts and it
  should be deleted rather than filled.
