# Claude Design prompt: design system revision plus full brand identity

Paste everything below the rule as one message.

---

## Step 0. Install these two skills first, before anything else

```
npx skills add emilkowalski/skill
npx skills add Leonxlnx/taste-skill
```

Read both before you touch a file.

- Apply the **emilkowalski** skill to everything motion: logo animation, the mark's
  build-on, transitions, easing, and the interaction states in the design system.
  Motion craft is a first-class part of this identity, not a finishing pass.
- Apply the **taste-skill** to every decision where more than one answer is
  defensible: which logo direction survives, where to stop adding, what to delete.
  Use it hardest on the logo. Most brand marks fail by accumulation.

Tell me in one line what each skill changed about your approach. If either fails to
install, say so and continue.

---

## Who this is for

**Arab Tech Export.** It teaches Arab software engineers, indie hackers, AI
consultants and technology companies how to sell AI products and services into the
United States and Canada.

The thesis in one line: *the capability is already here. What is missing is knowing
what a North American buyer verifies before they can award work.*

**The mission behind it:** to open a route for the Arab technology community, and to
help produce at least 100 leading Arab AI companies and more unicorns from the
region. That ambition is the reason this brand needs weight. It is not a course
brand. It is infrastructure for an export lane that does not exist yet.

**Current state:** pre-launch. No customers, no results, no testimonials. This
matters for the brand more than it sounds, see Guardrails.

---

## What already exists

I have a `DESIGN.md` in this project, forked from MongoDB's design system. It carries
MongoDB's palette, Euclid Circular A, pill buttons, 12px cards, dark teal hero bands,
the full component taxonomy.

There is also a landing page design spec for this project that references colour by
role, `accent`, `ink`, `surface`, `muted`, and a motif called **four ticks**: four
small vertical bars where the number lit indicates a level. That motif needs to
become part of the brand system, not stay a one-page device.

---

# TASK A. Rework `DESIGN.md` in place

**Edit the existing file. Do not create a new one.** Keep its structure, its token
naming convention, its component taxonomy and its discipline. Those are the reasons
to fork a mature system and they are worth keeping.

### A1. Re-pitch the palette, keep the architecture

The current file carries MongoDB's own brand colours. Those are MongoDB's most
recognisable asset. A business that sells credibility to North American buyers cannot
afford to look derivative of a database company, and there is a trademark exposure in
carrying a signature brand hue wholesale.

**Keep:**
- The dual-mode structure: deep dark brand bands against stark light surfaces
- The token architecture and every variable name pattern
- The restraint rule that saturated colour appears in exactly two places, the primary
  CTA and a small category-encoding set
- The full ramp discipline: brand, accent, surface, hairline, text, semantic

**Change:**
- Re-pitch the brand hue away from MongoDB's green. Propose **three** candidate brand
  colours with reasoning, each holding 4.5:1 against both the dark band and the light
  canvas, each still reading as a confident single-hue signal. Show them applied to a
  CTA pill, a badge and a featured card so I can judge them in context, not as swatches.
- Re-pitch the deep band hue. It should still be a dark, near-black, saturated
  anchor, and it should not be MongoDB's teal.
- Keep the category accent set at four hues, but re-derive them to sit under the new
  brand hue rather than under MongoDB's.

**Add a colour-meaning map.** One line per colour saying what it *means* in this
system, not where it appears. For example: the brand hue carries the ask, ink carries
the argument, the category set carries level and never carries emotion. This is what
keeps the system legible when someone applies it without reading the file.

### A2. Add Arabic typography. This is the largest gap in the file

The current file specifies Euclid Circular A, which has no Arabic support. This brand
ships Arabic for its entire top of funnel. **A Latin-only type system is not usable
for this project.**

Specify a bilingual type system:
- Keep a geometric Latin display face in the Euclid Circular A register
- Pair it with an Arabic face that holds the same weight, contrast and geometric
  temperament. Evaluate at minimum IBM Plex Sans Arabic, Noto Kufi Arabic, Tajawal,
  Almarai and Cairo. Recommend one and say why, including how its counters and
  stroke contrast behave against the Latin at the same optical size
- Give the **optical size correction** between the two faces. Arabic almost always
  needs a size and line-height adjustment to sit evenly beside Latin. Specify it as a
  ratio in the type table
- Add line-height overrides per script. Arabic needs more leading than the Latin
  values in the current table
- Specify how mixed-script lines set, since product terms like "W-8BEN-E", "SOC 2"
  and "Net 30" stay Latin inside Arabic sentences

### A3. Add RTL to the layout and component sections

Every component in the file needs a mirroring rule. Cover at minimum: what mirrors,
what never mirrors (numerals, logos, code blocks, progress that encodes time),
padding and border-radius flips, icon direction, and how the four-tick motif orders
under RTL.

### A4. Add motion tokens

The file's Known Gaps section admits animation timings were never extracted. Fill it
using the emilkowalski skill.

Specify: one easing curve for the whole system, durations for entry, hover, press,
expand, impact and ambient, stagger ranges, and a `prefers-reduced-motion` rule that
ships resolved end states rather than nothing.

**The register is "objects land."** Weight, settle, impact. Not float, not bounce.
This audience is spending their own money at a local income and is sceptical of this
product category. Precision, never spectacle.

### A5. Add the four-tick motif as a system primitive

Specify it once, properly: geometry, spacing, lit and unlit states, sizes, and its
behaviour under RTL. It becomes a component, not a page decoration.

---

# TASK B. The logo system

Not a wordmark. A full mark with a reason to exist.

### What it has to carry

| Value | Where it comes from |
|---|---|
| **A route with two ends** | The whole business is one origin and one destination. Not a generic arrow. A specific passage |
| **Passage and clearance** | Being let through. The product is about clearing a process, not about speed |
| **Method and construction** | The offer is rigour, not motivation. The mark should look built, not drawn |
| **Level and progression** | The four-tick motif. Movement between levels is the product |
| **Arab, without costume** | Authentic, structural, contemporary. Never a camel, never a lamp, never a minaret silhouette, never a calligraphic flourish standing in for a culture |
| **Scale of ambition** | 100 companies, not one course. The mark should hold at the size of an institution |

### Three directions to develop, then cut to one

Develop each far enough to judge. Then use the taste-skill and **recommend one**,
with the reasoning for cutting the other two.

**Direction 1, Girih construction.**
Build the mark from the Islamic geometric system: compass and straightedge, an
underlying polygon tiling, a derived star or knot. This is the strongest cultural
route because it is **mathematical rather than decorative**. Girih is a construction
method, and this brand sells method. Explore whether the derived form can also read
as an aperture or a passage. Show the construction geometry, not only the result.

**Direction 2, The aperture.**
A gate, threshold or opening seen straight on. Negative space does the work. A form
that reads as closed at a glance and open on a second look, or the reverse. This
is the most direct translation of the product and the easiest to make cold.

**Direction 3, The lane.**
Two points and the path between them, built with the same geometric discipline as
direction 1 so it does not become a generic swoosh. The four ticks could live inside
this as the path's segments.

**A note on combining.** The strongest outcome is probably a girih-derived form whose
geometry also resolves as a passage. Do not force it. A mark carrying one idea
cleanly beats one carrying three.

### Deliverables for the chosen direction

1. **Primary lockup**, horizontal, Latin
2. **Primary lockup**, horizontal, **Arabic**
3. **Bilingual lockup**, both scripts, with the hierarchy rule stated
4. **Stacked lockup**, both scripts
5. **The mark alone**, and it must work with no wordmark at all
6. **Monogram and favicon**, 16px legible
7. **Responsive reduction**: full lockup, reduced lockup, mark, monogram, with the
   pixel breakpoint for each step
8. **Construction and geometry**: grid, ratios, how the form is derived
9. **Clear space** as a ratio of a mark element, never an absolute
10. **Minimum sizes**, print and screen, both scripts
11. **Colourways**: full colour on light, full colour on dark, single colour, reversed
    out, and a one-colour version for embroidery and engraving
12. **Misuse board**, at least eight, including the culturally specific ones:
    do not add a flag, do not stretch the Arabic, do not substitute a different
    Arabic face in the wordmark
13. **Motion signature**, using the emilkowalski skill. How the mark builds on. It
    should **construct** rather than fade in, because construction is the brand's own
    argument. Under 900ms. Specify the reduced-motion resolved state

**Test the mark cold.** Render it at 16px, in one colour, on a light background, with
no wordmark, beside three unrelated marks. If it stops being legible or stops being
distinct, it is not finished.

---

# TASK C. The brand book

One document. Every section below.

**1. Strategy.** Purpose, positioning, the thesis in one line, values, personality,
what the brand refuses to do.

**2. Voice.** Peer to peer, specific, never guru. Include the banned word list below
and give five before-and-after rewrites so the rule is demonstrated rather than
asserted. Cover Arabic voice separately, since a translated English sentence carries
English rhythm and reads as imported.

**3. Logo system.** Everything from Task B.

**4. Colour.** The revised palette, the colour-meaning map, accessibility pairs with
contrast ratios, and what each colour is forbidden from doing.

**5. Typography.** The bilingual system, the full scale, the optical size correction,
mixed-script rules.

**6. Brand elements.** This is where a brand book earns its length:
- **Pattern system** derived from the mark's own geometry, tiling at three densities.
  Not decoration, a system with rules for where it may and may not appear
- **Iconography**: stroke weight, terminal style, grid, and a starter set of twelve
  covering the product's actual concepts, including a gate, a level, a document and
  a route
- **The four-tick motif** as a brand element, with its full behaviour
- **Data and diagram style**, because this brand's entire argument is numbers and
  process. Specify how a figure is set, how a process is drawn, how a comparison is
  shown
- **Illustration direction**: geometric, constructed, never stock, never 3D-render
  gloss. Say what it is, and show one example
- **Photography direction**, if photography is used at all. Consider recommending it
  is not, and say why

**7. Motion identity.** The system-wide easing, the logo build, the "objects land"
register, reduced motion.

**8. Applications.** Social avatars and covers for X, LinkedIn and YouTube, an email
signature, a presentation template opener, a document header, a community space
avatar, a certificate or completion artifact, and one merchandise item.

**9. Governance.** File naming, formats, what needs approval, and a one-page quick
reference someone can use without reading the rest.

---

# Guardrails, all of them load-bearing

**1. This business is pre-launch and the brand must not pretend otherwise.**
No testimonial slots. No logo wall. No customer-count placeholders. No "trusted by"
anything. If a template has a social-proof slot, design the version that works
without one, because that is the version that will actually ship.

**2. Ambition is stated as ambition, never as a promise.**
"100 leading Arab AI companies" is a mission and the brand should carry it with
weight. It must never be phrased so a reader hears a promise about their own outcome.
The brand may say what it is *for*. It may not say what any individual will *get*.

**3. Never compare markets on readiness or income.**
This brand's audience is Arab builders. Copy about them is read by them. Compare
buyer economics if you must. Never compare capability, ambition, readiness, or what
anyone earns. No "escape", no "finally", no rescue narrative. These are competent
professionals with an access problem.

**4. No triumphalism in motion.**
The product's honest promise is that clearing a buyer's checks makes you *eligible*.
It does not win the deal. Nothing in this identity should burst, celebrate or launch.
The landing page's closing animation deliberately ends quietly for this reason, and
the brand has to match it.

**5. Banned words**, across every surface:
leverage, unlock, empower, seamless, robust, streamline, revolutionise, cutting-edge,
transform (outside a headline where it earns its place), supercharge, elevate, delve,
harness, world-class, game-changing, next-generation.

**6. No em dashes anywhere.** Commas, periods or parentheses.

**7. Cultural specificity, not signalling.**
Girih geometry is welcome because it is a construction system with real mathematical
content. Flags, camels, lamps, domes, and calligraphy used as ornament are not. If a
form only reads as "Arab" through a stereotype, it has failed.

---

# Output

1. **`DESIGN.md`, edited in place.** Tell me every section you changed and why.
2. **The logo canvas.** Three directions explored, one recommended, full deliverable
   set for the chosen one.
3. **The brand book**, all nine sections.
4. **A decisions log**: what you chose, what you rejected, and what you need from me.

**Do Task A first and show me the palette candidates before continuing.** The colour
decision propagates into the logo, so I want to settle it before you build a mark on
top of it.
