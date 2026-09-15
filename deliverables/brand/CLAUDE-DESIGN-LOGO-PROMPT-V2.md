# Claude Design prompt, logo rebuild. Supersedes Task B of the previous prompt

Upload `logo/prototype.html` and the five SVGs in `logo/` alongside this prompt.

---

## Stop. The previous mark is rejected and the reason is not aesthetic

The last attempt built an eight point star from two squares at 0 and 45 degrees,
rendered in blue. **That direction is dead.** An eight point khatam is authentic
Islamic geometry and that argument is worthless, because a mark that needs
explaining has already failed. Angular, centred, in blue, in front of an Arab
audience, it reads the way it reads. The blue made it worse.

**Hard bans, no exceptions, in every direction and every exploration:**

| Banned | Why |
|---|---|
| **Any star form.** Six point, eight point, any point count, any construction | Non-negotiable. Do not attempt to make a "safe" star |
| **Two overlapping squares, or two overlapping triangles**, at any rotation | This is how the last one happened |
| **Blue in any role**, including tints, hairlines and accents | Wrong for this brand and compounds the above |
| Camels, lamps, domes, minarets, flags, calligraphy used as ornament | Costume, not culture |

**Where to take the culture instead: Islamic architecture, not Islamic starwork.**
Arches, arcades, portals, thresholds, screens, vaulting, tiling that is not star
based. These carry the same mathematical rigour and none of the risk.

---

## The palette is decided. Green

| Token | Value | Role |
|---|---|---|
| `brand-green` | `#00A45C` | Primary. CTAs and the mark |
| `brand-green-bright` | `#00C767` | On the deep band only |
| `brand-green-deep` | `#047A46` | Inline links, pressed states |
| `brand-green-soft` | `#E3F5EC` | Featured tier tint, success badges |
| `ink` | `#062B21` | Deep band, footer, body text |

Deliberately not MongoDB's `#00ED64`, which is a neon spring green and one of that
company's most recognisable assets. These sit deeper and read institutional rather
than developer-tool. Close enough to keep the fork's character, far enough that
nobody mistakes the page. **Do not propose palette alternatives. This is settled.**

---

## The wordmarks, exact

- **Latin:** Arab Tech Export
- **Arabic:** مُصدرين التكنولوجي العرب

Use the Arabic **verbatim**, including the damma on the first letter. Do not correct
it, do not re-spell it, do not substitute a synonym. It is the client's own name.

---

## Direction 1, The Gate. Build this one

The attached prototype has it. **Take the geometry as given and refine, do not
restart.**

```
Mark path, viewBox 0 0 120 120
M29,96 A70,70 0 0 1 60,33 A70,70 0 0 1 91,96
stroke-width 17, butt caps, no fill
stroke-dasharray "32.5 5.2" with pathLength="150"  →  four segments, three gaps
```

**What it means.** A pointed arch, open at the base. Not a badge, a passage. The band
splits into four segments, which are the four departments that decide whether a
foreign vendor gets paid, and the four bands of the product's own ladder. It is a
gate you go through.

**Why it holds.** Two arcs and a stroke. No fill, no curves needing optical
correction, no gradient. It reproduces in one colour, in embroidery and in engraving
without redrawing, and it cannot be mistaken for a star from any distance.

**Responsive reduction.** Below 24px the segmentation drops and it becomes one clean
arch. That is a reduction of the same mark, not a second mark.

### What I want you to do with it

1. **Tune the segmentation.** The dash values are a first pass. Set the gaps so the
   apex sits inside a segment rather than inside a gap, because a broken keystone
   reads as damage rather than as rhythm.
2. **Test the arch proportion.** Try three ratios of height to span and pick one.
   Taller reads more formal, wider reads more approachable. Show all three.
3. **Decide the terminals.** Butt caps currently. Try a small chamfer. Do not round.
4. **Resolve the baseline question.** It is currently open at the bottom. Test a
   version with a thin threshold bar across the base and say which is stronger. Open
   says passage. Closed says gate. Argue it.

---

## Direction 2, The Arcade. Develop as the alternate

Three pointed arches receding, brightening toward the destination. A riwaq, the
arcaded walk of a caravanserai, the roadside inn that trade routes were built around.
Trade, passage and hospitality in one form.

**Two problems to solve or abandon it:** the opacity ramp collapses in one colour and
in embroidery, and the whole form must mirror under RTL or the route runs backwards
against the reading direction.

---

## Direction 3, The Weave. Included, and I would not ship it

Two bands interlacing, girih strapwork without a star. **It is one step from the
shape we are avoiding**, because a rotated square over a square approaches the same
silhouette. It is on the table for comparison only. If you recommend it, the argument
has to be very good.

---

## Deliverables for the chosen direction

1. Primary lockup, horizontal, Latin
2. Primary lockup, horizontal, Arabic, **mark on the right**, whole lockup mirrored
3. Bilingual lockup, Latin leading, Arabic set at roughly 1.06 optical to match
4. Stacked lockup, both scripts
5. The mark alone, working with no wordmark
6. Monogram and favicon, legible at 16px
7. Responsive reduction ladder with the pixel breakpoint for each step
8. Construction sheet: the arc geometry, the ratios, the segmentation maths
9. Clear space, as a ratio of the stroke width, never an absolute
10. Minimum sizes, screen and print, both scripts
11. Colourways: on light, on the deep band, one colour, reversed, and a
    single-weight version for embroidery and engraving
12. **Misuse board, at least ten**, and it must include: do not fill the arch, do not
    round the terminals, do not add a star inside it, do not add a flag, do not
    recolour to blue, do not stretch the Arabic, do not substitute a different Arabic
    face inside the wordmark
13. **Motion signature.** The arch **draws itself from both springpoints upward and
    meets at the apex**, under 900ms, using the emilkowalski skill. Construction, not
    a fade. The four segments arrive in sequence, lowest first, because that is the
    ladder. Specify the `prefers-reduced-motion` resolved state

---

## Typography, unchanged from the earlier prompt

Latin: a geometric sans in the Euclid Circular A register.
Arabic: recommend one of IBM Plex Sans Arabic, Tajawal, Almarai, Cairo or Noto Kufi
Arabic, and give the optical size correction and per-script line-height overrides.
The prototype uses IBM Plex Sans Arabic as a placeholder, not as a decision.

---

## Everything else from the previous prompt still stands

`DESIGN.md` rework, the brand book's nine sections, and all seven guardrails,
including: no testimonials or logo walls because this business is pre-launch,
ambition stated as ambition and never as a promise about anyone's outcome, never
compare markets on readiness or income, and no triumphalism in motion.

---

## Output

1. The chosen direction, fully built, all thirteen deliverables
2. The two rejected directions with one line each on why
3. `DESIGN.md` updated with the green palette above and the mark

**Show me the four proportion and segmentation tests before building the lockups.**
That decision propagates into every asset and it is cheap to change now.
