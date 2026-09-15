# Handoff prompt for Claude Design

Paste everything below the rule. Attach `ArabTechExport_Landing_Page.md` for the
copy and `DESIGN-SPEC.md` for the scene-by-scene object briefs.

---

Build a single-page scrolling landing page for **Arab Tech Export**, a pre-launch
education business that teaches Arab software engineers, indie hackers and AI
consultants how to sell AI products and services into the United States and Canada.

**Use your own design system.** Palette, type, spacing, components, all yours. The
attached spec references colour by role only, `accent`, `ink`, `surface`, `muted`,
`warning`. Map those to your tokens however you normally would. Do not wait for a
brand system and do not ask me for one.

## What this is

One continuous scroll. Sixteen scenes. No pagination, no arrow-key navigation, no
slide transitions. It is a landing page, not a deck. Somebody reads it alone, on a
phone, and scrolls past most of it in about 90 seconds.

**The page must be understandable by someone who reads none of it.** That is the
brief in one sentence. Every scene carries its argument in a 3D object, and the copy
is a caption to the object rather than the other way round.

## Non-negotiables

1. **Real 3D.** CSS 3D transforms, `perspective`, `preserve-3d`, `translateZ`. No
   WebGL, no 3D libraries. Crisp type matters more than shaders here, because the
   page is carrying numbers.
2. **Alive at rest.** Every object has an ambient state, ±0.3deg to ±0.5deg yaw on
   an 8 to 14 second loop. Nothing on this page is ever frozen. Nothing is ever busy.
3. **Illustrative, never decorative.** Delete any graphic. If nothing is lost, it
   comes out. Six scenes are marked **motion-as-claim** in the spec, where the
   movement *is* the argument. Build those first and give them the performance
   budget.
4. **Under 900 visible words** across the whole page at rest. The source copy is
   3,200. Part 3 of the spec says exactly where the rest goes: hover states, tap
   expands, accordions. When a scene runs over budget, cut copy, never the object.
5. **One `requestAnimationFrame` loop** for the entire page. No transform writes from
   scroll or pointer handlers. Damp scroll progress with a 0.12 lerp. Pause every
   object outside the viewport.
6. **Reduced motion ships the resolved end state**, not a static fallback. Under
   `prefers-reduced-motion`, gates are open, the ladder is built, slabs are flipped,
   the stack has landed. Opacity and colour transitions under 200ms still run.
   Nothing translates, rotates or scrubs.
7. **Never hijack the scroll.** No scroll-jacking, no snap-between-scenes, no smooth
   scroll library. At most three scenes pin, scenes 4, 7 and 8, and each releases
   after 100vh.
8. **Tabular figures for every numeral.** A number that reflows while it counts
   destroys the trust it was placed there to build.

## The spine

*The work is good enough. The paperwork is what fails, and you can see exactly which
piece.*

Carrying line: **Four departments decide. None of them were on the call.**
Carrying number: **30 percent**, withheld over one missing tax form.

## Register: objects land

This reader is spending their own money at a local income, and they are sceptical of
this entire product category. Objects have weight. They settle, they impact, they
come to rest. **Precision, not spectacle.** Nothing floats, nothing bounces, nothing
celebrates.

## Build these five scenes first

They carry the page. The other eleven support them.

- **Scene 1, The Four Gates.** Four planes receding in Z. A deal token travels
  forward, clears two gates, and **stops dead at the third** with a 90ms impact. Gate
  three is security, the gate this audience has never heard of. The object makes the
  argument before the headline does.
- **Scene 4, The Camera Orbit.** Reuses scene 3's four well-made blocks, then orbits
  180 degrees to the far side where they are **flat, unlit and unlabelled**. Same
  work, seen from the buyer's side, invisible. The page's best idea.
- **Scene 7, The Ladder.** Centrepiece, at 44 percent through. Four platforms rising
  and receding. A token climbs on scroll and **each platform only materialises as the
  token reaches it**, because most of this audience does not know the higher bands
  exist.
- **Scene 8b, The Sorting.** Six slabs physically sort into two groups, free to fix
  and costs money, then restack in blocking order. This is the product's core promise
  rendered as a physical sort.
- **Scene 11, The Empty Shelf.** Four testimonial frames rendered as dotted, unlit
  outlines. **They stay empty. Nothing ever fills them.** No shimmer, no skeleton, no
  "coming soon". Then four solid objects land beside them: the IRS source, the
  published method, the written terms, the capped cohort.

## The recurring motif

**Four ticks.** Four small vertical bars. Lit bars in `accent`, unlit in `muted` at
25 percent. The lit count is the band.

It appears in scenes 1, 4, 7, 15 and 16. **It is never labelled and never explained,
and there is no legend anywhere on the page.** By its third appearance the reader
reads it without help. Specify it once, use it five times.

## Where not to animate

Decks and pages fail from too much motion far more often than too little. Four
explicit restraints:

- **Scene 5, the crescendo, has no object at all.** No 3D, no parallax, no entry
  motion. It is the only still scene in the page and the centrepiece two scenes later
  only lands because the reader passed through stillness first. If you add a floating
  element here, scene 7 loses its impact and nobody will be able to say why.
- **Scene 3's four blocks do not move after entry.** They are the calm before the
  pain. The contrast with scene 4 is the whole point.
- **Scene 11's empty frames do nothing.** Any pulse or shimmer turns an honest
  statement into a tease.
- **Scene 16's token leaves quietly.** No burst, no confetti. Clearing procurement
  makes a vendor eligible, it does not win the deal, and a triumphant exit would be
  the page's only broken promise.

Also: the hero's four stat numbers **count up once, on first view, and never again.**
No looping counters.

## Honesty constraints, which are load-bearing

This business is pre-launch and the page says so out loud. These are not style
preferences, they are the product's own argument turned on itself.

- **No testimonials, no logos, no client names, no invented numbers.** There are
  none. Scene 11 exists to say that.
- **Scene 10's prices render as a blank underscore rule**, not as a number and not as
  the word "TBD". Pricing is genuinely undecided. An empty field reads as honest.
- **Scene 14's token board shows the true number of remaining places.** If that count
  is not known at build time, render a static twelve-socket board that shows the cap
  without implying a fill level. Do not show a nearly-full board.
- **Scene 15 never renders an example score.** The scorecard's design rule is that it
  never delivers a verdict, and a pre-filled result would break that before the reader
  answers anything.

## Mobile, which is most of this audience

No hover anywhere, every reveal has a tap equivalent that expands in place rather
than opening a modal. Pinned scenes shorten to 60vh. Depth reduces to three Z-layers.
The hero stat bar becomes a 2x2 grid, never a horizontal scroll.

## RTL

The page may ship in Arabic. Every object is direction-agnostic except the ladder in
scene 7 and the path in scene 6, both of which read left to right. **Mirror both
under RTL.** A ladder climbing away from the reading direction fights the reader.

---

Full scene-by-scene briefs, entry timings in ms, ambient loops, interaction states,
restraint notes and reduced-motion states are in `DESIGN-SPEC.md`. Copy is in
`ArabTechExport_Landing_Page.md`, and the spec's Part 3 says which parts of it are
visible at rest and which move into interaction.

Build the five named scenes first and show me those before continuing to the rest.
