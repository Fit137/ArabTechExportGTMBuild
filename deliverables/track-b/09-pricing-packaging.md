# Track B, Phase 9. Pricing and Packaging

Steps 9.1 to 9.3. Runs as written per `SKILL-ADAPTATION.md`, with three changes the
adaptation specifies and one the research forced.

1. Per seat and per user are the same thing for a solo member. Scored per member,
   per cohort, and per access tier instead.
2. The outcome denominator is dropped. Pricing a training product on the member's
   earned outcome is an income claim with a payment schedule attached.
3. The affordability tension is held explicitly rather than discovered at launch.
4. **Added by the research:** billing shape is a conversion instrument, not an
   operations detail. See the payment rail constraint below.

**Every price is `{TBD}`** per `00-ASSUMPTIONS.md` decision 3. The structure, the
value metric, the expansion levers and the anchoring all stand without the numbers.

---

## Step 9.1. Value metric selection

| Denominator | Correlation to value | Scalability | Ease of measurement | Score |
|---|---|---|---|---|
| Per member | High. One member is one person receiving the value | High. Scales with the room | Trivial | **9.2** |
| Per cohort | Medium to high. Cohorts correlate with attention received | Medium. Capped by founder hours | Easy | **7.6** |
| Per access tier | High. Tiers map to how much founder time is included, which is the real scarce resource | High | Easy | **8.8** |
| Per usage, teardown slots | High. Directly tracks the scarce input | Medium. Discourages the behaviour that drives retention | Easy | **6.1** |
| Per capability, feature gating | Low. Gating knowledge in an education product is hostile | High | Easy | **3.4** |
| ~~Per outcome~~ | **Excluded, not scored** | | | **Dropped** |

**Why per outcome is excluded rather than scored low.** Pricing on what a member
earns is an income claim with a payment schedule attached. It is banned by
`GTM-BRIEF.md` Section 5 and it is a regulatory problem in several of the named
markets. It does not get a row.

**Recommendation**

- **Primary value metric: per member, per access tier.** The tier decides how much
  of the scarce resource, founder attention, the member receives.
- **Secondary metric: teardown slots per period.** Tracked and disclosed, used to
  define tiers, never billed per unit. Billing per teardown would suppress the one
  behaviour that keeps members alive past day 14.
- **Rationale:** the only genuinely scarce input is founder time, and Phase 1 showed
  it does not scale. Tiers that ration founder time honestly, with published caps,
  are both the correct economics and the correct trust signal in a category where
  access is the first thing to quietly disappear.

---

## Step 9.2. Pricing tiers

Decoy, Hero, Anchor. Prices `{TBD}`.

| Plan | Price | Access tier | Teardown slots | Position | Target share |
|---|---|---|---|---|---|
| **Checklist** | Free | Public assets, scorecard, email | None | Entry, not a tier | Ungated |
| **Room** | `{TBD}` | Community, course library, AMAs, peer deal review rubric | Peer review only | Decoy | 15 to 25 percent |
| **Deal** | `{TBD}` | Everything in Room, plus live deal teardowns and positioning review | `{TBD}` per month, published | **Hero** | 55 to 70 percent |
| **Direct** | `{TBD}` | Everything in Deal, plus one to one sessions | `{TBD}`, plus one to one, **slot count published and capped** | Anchor | 10 to 15 percent |
| **Founding cohort** | `{TBD}` | Deal tier access plus direct founder contact, permanent terms | Uncapped during the founding period | Separate. 8 to 12 people, closes | One time |

**The tiers now map to the bands.** Per `00-RESOLUTIONS.md` conflict 2, the offer is
the movement between bands, so the tiers should describe how far up a member is being
carried rather than how much content they receive.

| Plan | Carries a member | Note |
|---|---|---|
| Checklist, free | Nowhere. Shows the ladder | The scorecard returns a band. That is the hook |
| Room | Band 1 to band 2 | The free-to-fix half. Legibility, scope, champion enablement, the tax form |
| Deal | Band 2 to band 3 | Where the expensive half starts, and where a live deal is required |
| Direct | Band 3 and the edge of 4 | Founder hours on a specific procurement process |

This also fixes a weakness in the old tier logic. Room was justified only as a decoy.
It now has an honest job: it carries a member through the rungs that cost nothing but
knowledge, which is genuinely most of band 1 to 2. A member who never needs more than
that has still been served, which is a better retention story than a tier designed to
look wrong.

**Room is a genuine decoy.** It contains the commodity half of the offer, courses
and a room, which Phase 1 scored as table stakes and which free alternatives already
cover. Its job is to make Deal look correct. A member who buys Room and never brings
a deal is the member most likely to churn in 14 days, so Room should be priced close
enough to Deal that choosing it feels like a false economy.

**Direct exists to be mostly unavailable.** Phase 1 found one to ones are the worst
item in the set on delivery effort, and Phase 2 found founder access is the most
praised and first to vanish across the whole category. Publishing the slot count and
closing the tier when it fills is both the honest answer and the better commercial
one.

### Expansion levers

1. **Room to Deal, triggered by a live deal.** The upgrade prompt is the member
   posting about a real deal. That is a behavioural trigger, not a calendar one.
2. **Deal to Direct, triggered by a stalled deal.** A member whose deal is stuck
   after a teardown is the person for whom one to one is genuinely worth it.
3. **Monthly to annual, triggered by payment friction.** See below. This lever is
   unusual in that it improves the member's experience and the business's cash at
   the same time.

### The billing shape constraint

This is not a footnote. In Egypt, monthly USD card caps are reported as low as $50
to $200 and international card limits are reported suspended on debit cards. A
recurring monthly USD card charge is unreliable in one of the largest origin markets
by developer population, and it fails silently at renewal rather than at signup.

| Requirement | Why | Priority |
|---|---|---|
| Annual billing offered at every tier | One successful charge per year instead of twelve chances to fail | **Structural** |
| Fixed length cohort billing, one payment | Removes recurrence from the problem entirely | **Structural** |
| Local currency collection in the constrained markets | Removes the cross border conversion that triggers the cap | High |
| A non card route, bank transfer or wallet | For members whose cards will not clear at any amount | High |
| Payment failure tracked by market, not in aggregate | This failure is invisible in a blended conversion rate | **Day one** |

**Do not price this as a monthly USD subscription and plan to solve payments later.**
The tiers above should be quoted annually or per cohort first, with monthly as the
option rather than the default.

### The affordability tension, held rather than deferred

A price set against what the offer is worth in a target market is a significant
amount of money at a local income. A price set against local income will not sustain
the founder time the Deal and Direct tiers require. Both are true at once.

| Option | What it costs |
|---|---|
| Single global price | Simple, defensible, and prices out most of Egypt, Jordan and Morocco. Concentrates the business in the Gulf |
| Regional pricing by market | Reaches the audience. Leaks through VPNs and payment addresses. Creates resentment when members compare in the room, and they will, because they are in a room together |
| Cohort pricing with a scholarship allocation | Preserves one public price, admits some members below it, keeps the decision explicit and human. Slower and does not scale |
| Tier the access rather than the price | One price list. A constrained member buys Room, an unconstrained one buys Direct. Honest and it reaches fewer people |

**Recommendation: one public price list, plus a stated founding cohort rate, plus a
small explicit scholarship allocation.** Regional pricing inside a single visible
community is the option most likely to produce a public argument, precisely because
the members can see each other. This is a founder decision, not a model decision, and
it should be made before launch rather than after the first complaint.

---

## Step 9.3. ROI anchoring

**The skill's "one outcome pays for X years" calculator is dropped for Track B.**
`SKILL-ADAPTATION.md` is explicit: pricing a training product on the member's earned
outcome is an income claim. The calculator is that claim expressed as arithmetic. It
does not appear in this phase, in Phase 6, in Phase 8, or in the deck.

What replaces it is anchoring on cost and effort that can be stated without claiming
anyone's result.

### Anchor 1. Cost of the problem, stated without income figures

| Scenario | Cost without | Annual cost | Comparison |
|---|---|---|---|
| Time spent producing proposals that fail a check the member has never seen | `{TBD}` hours per proposal, member's own count | `{TBD}` | Stated in the member's hours, which they know and this business does not |
| Deals lost without a diagnosis, so the same mistake repeats | `{TBD}` count, member's own | `{TBD}` | The repetition is the cost, not the deal |
| Time to work out the buyer's checks alone, by trial | `{TBD}` months | `{TBD}` | Compressed, not eliminated |

Every cell is `{TBD}` and filled by the member, not by the business. The scorecard is
where this data comes from, which is one more reason it asks about deals rather than
about knowledge.

### Anchor 2. Alternative comparison

| Alternative | Their cost | What it does not do |
|---|---|---|
| Free content, Egypt FWD, Hsoub free library, YouTube | Zero | Stops before the commercial problem. Written mostly for a buyer the creator already had. No application to the member's own deal |
| A general freelancing or business course | Low, `{TBD}` | Teaches selling in general, not this buyer. No live deal review |
| Marketplace bidding, Upwork or Mostaql | Platform commission, commonly cited at 10 percent and up to 15 on Mostaql, on every project, forever | Gives access and takes price comparison with it. Recurring cost with no accumulation |
| Working it out alone | Time, `{TBD}` | Nothing accumulates from other people's attempts |

The marketplace row is the strongest one available and it is entirely factual. A
commission is a real, recurring, percentage cost that continues for as long as the
member uses the platform. Stating it is not an income claim.

### Anchor 3. Breakeven, restated

The skill's breakeven table asks for typical customer value, which is an income
figure this business must not supply. Restated as an effort breakeven.

| Plan | Annual cost | Breaks even when | Measurable by |
|---|---|---|---|
| Deal | `{TBD}` | The member stops sending proposals that fail a check they can now see | Their own proposal count |
| Direct | `{TBD}` | The member can run the six checks on their own work without help | Self assessed, re-taking the scorecard |

Both conditions are things the member can verify about themselves. Neither requires
anyone to state what they earned.

---

## Carried forward

| Output | Goes to |
|---|---|
| Per member per access tier | Phase 10 slide 10 |
| Billing shape as structural | Phase 7 stage 4, Phase 8 payment fallback asset |
| Affordability recommendation | Founder decision, before launch |
| Outcome calculator dropped | Do not reintroduce in any later asset |
