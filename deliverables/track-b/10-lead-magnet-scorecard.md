# Track B. Lead Magnet Specification, Buyer Readiness Scorecard

For ScoreApp.com. Runs as written per `SKILL-ADAPTATION.md`, which calls this the
single deliverable in the run that does the most work for Track B.

Reference: Phase 1 Step 1.6 demand driver.

**The design rule that governs every question below.** The scorecard reveals an
access gap. It never tests knowledge and it never implies the respondent is
unskilled. A builder scoring low is being shown which parts of reaching a North
American buyer they have never had to handle. That distinction is the whole design
and it is the same distinction `GTM-BRIEF.md` Section 5 protects.

---

## Scorecard overview

| Element | Specification |
|---|---|
| Scorecard name | Buyer Readiness Check. Arabic title `{TBD}`, write it in Arabic, do not translate |
| Target ICP | Phase 4 both levels. Level 1 is the volume, Level 2 is who gets invited to the room |
| Problem it reveals | That deals are lost on legibility to the buyer rather than on capability, and which of six dimensions is weakest |
| Immediate value to user | The buyer's six checks, plus their own position on each. Most have never seen the list |
| Conversion path | Result page, then a four email sequence segmented by weakest dimension, then the walkthrough, then Room or Deal. Level 2 respondents route to a founding cohort conversation instead |

### The six dimensions

**Rebuilt on evidence.** Conflicts 1 and 7 resolved in `00-RESOLUTIONS.md`. The
previous six were reasoned. These come from `00-BUYER-CHECKS.md`, and each one's
answer options are the rungs of that dimension's ladder, so the result is a band
position rather than an impression.

| # | Dimension | What the buyer is checking | Free to fix, or has to be built |
|---|---|---|---|
| 1 | Legibility | Can they tell what you do in one line, in their category language | **Free** |
| 2 | Proof | Is there anything attributable they can verify without asking you | **Free to start, costs time to accumulate** |
| 3 | Scope | Is the work defined so they know what they are buying and when it ends | **Free** |
| 4 | Paperwork readiness | Tax form, contract template, invoicing that matches their records, insurance | **Mixed. The tax form is free. Insurance is not** |
| 5 | Security and compliance readiness | Can they assess your risk without a six week detour | **Has to be built, and it is the expensive one** |
| 6 | Champion enablement | Can your advocate carry you through four departments that never met you | **Free, and almost nobody does it** |

The fourth column is the split promise from conflict 3, built into the instrument
itself. A respondent sees not only where they are weak but which weaknesses cost
money to close.

**What changed and why.** Pricing frame was removed. It is a real problem and it is
not something a buyer verifies, so it has no place in an instrument that claims to
report what buyers check. It moves into the teaching. Security and compliance
readiness replaces it, because it is the dominant gate above band 2 and the previous
version had no dimension for it at all. Follow-through became Champion enablement,
which is the mechanism the research actually describes.

---

## Questions

Seven questions. Six dimensions plus the segmentation signal. Options are ordered low
to high and score 0, 4, 8, 12, 16.

| # | Question | Answer options | Scoring | What it reveals |
|---|---|---|---|---|
| 1 | When a buyer in the United States or Canada lands on your profile, what do they see in the first line? | (a) My job title and stack (b) A list of technologies (c) A description of what I build (d) A specific problem I solve, for a specific kind of company (e) That, plus who it is not for | 0 / 4 / 8 / 12 / 16 | **Legibility.** Most technical people describe capability. Buyers scan for a problem |
| 2 | If a buyer wanted to check you out without contacting you, what would they find? | (a) Nothing findable (b) A code profile (c) A portfolio of work (d) Work plus a written explanation of how you approach it (e) That, plus a named client, their job title, and what you actually did | 0 / 4 / 8 / 12 / 16 | **Proof.** Option (e) is the research's own standard: attributable, specific, verifiable. A code profile proves you can build, which was never in doubt |
| 3 | How do you define the work before it starts? | (a) We agree as we go (b) A verbal or chat outline (c) A written list of tasks (d) A written scope with what is excluded (e) That, plus milestones, an end point, and what happens if it changes | 0 / 4 / 8 / 12 / 16 | **Scope.** Undefined scope is where a target market buyer stops replying after the first call |
| 4 | Which of these do you already have ready to send? | (a) None of them (b) An invoice (c) A completed W-8BEN or W-8BEN-E (d) That, plus a contract template you did not write from scratch (e) That, plus insurance certificates | 0 / 4 / 8 / 12 / 16 | **Paperwork readiness.** Replaces the old vaguer question. A missing or invalid W-8 form means 30 percent withholding or no payment at all, and most respondents will not know what it is |
| 5 | If a buyer asked how you handle their data and access, what could you send today? | (a) I would answer in an email (b) A written explanation of my setup (c) That, plus a recent security test (d) That, plus a page they can read without asking (e) A formal report, SOC 2 or equivalent | 0 / 4 / 8 / 12 / 16 | **Security and compliance readiness.** The dominant gate above band 2, and the most expensive to close. Option (a) is not a failure at band 1 and is fatal at band 3 |
| 6 | After a good call, what does the person you spoke to have in hand to show their colleagues? | (a) Nothing, they have my email (b) A proposal (c) A proposal plus references (d) That, plus answers to the questions their legal and security people will ask (e) I ask who else has to approve it and give them something for each | 0 / 4 / 8 / 12 / 16 | **Champion enablement.** The single most actionable question here, and the one nobody expects. It is free to fix and almost nobody does it |
| 7 | How many live or imminent conversations do you have with a buyer in the United States or Canada right now? | (a) None (b) One, early (c) One, active (d) Two or three (e) More than three | 0 / 4 / 8 / 12 / 16 | **The segmentation signal.** Sorts Level 1 from Level 2 and decides which path the respondent is sent down |

**Question 6 is the one to watch.** It is the newest, it comes directly from the
research finding that deals stall because the champion cannot sell internally, and
almost every respondent will answer (a) or (b). It is free to fix, it needs no
purchase, and demonstrating it in the result email is the strongest possible argument
that this instrument knows something the respondent does not.

**Question 7 still does the commercial work.** Respondents answering (c), (d) or (e)
go to a founding cohort conversation regardless of total score. Respondents answering
(a) go to the email sequence and stay there until something changes.

## Results tiers

Total range 0 to 112. Bands map to the deal bands in `00-RESOLUTIONS.md`, so the
result tells a respondent what size of deal their current setup can survive.

| Score | Band | Message | CTA |
|---|---|---|---|
| 0 to 39 | **Band 1. Direct work only** | You can build. That is not what this measures. What it shows is that your setup currently works only where one person decides and no formal process runs. That is most marketplace and referral work, and it is a real place to be. Your weakest dimension is `{dimension}`. Nothing here is about your ability | Soft. Read the buyer's checklist. Free, no gate |
| 40 to 74 | **Band 2. Clears a light review** | You would survive a buyer who does a little checking and stall at one who does it properly. Your weakest dimension is `{dimension}`, and it is the one that decides whether the second conversation happens. Some of what is missing is free to fix. Some of it is not, and we will tell you which | Medium. Watch the buyer evaluation walkthrough, then the four email sequence |
| 75 to 112 | **Band 3. Clears procurement, mostly** | You clear most of what a buyer verifies. At this level the losses are narrow and specific, usually one dimension applied to one deal. Yours is `{dimension}` | Strong. Bring a live deal. Founding cohort conversation if question 7 is (c) or above |

**Wording discipline, and it survives the rebuild.** The low band message still opens
by conceding capability, because that is the premise of the business. It now also
does something the old version did not: it says band 1 is a real place to be rather
than a deficiency. An audience earning a living on marketplaces is not failing, and
telling them they are loses them in the first sentence.

**The stated absence, conflict 5.** The result page carries a plain line that Arab
Tech Export has no published results yet, and what stands in its place. An audience
sceptical of this category reads an unexplained absence as concealment.

**Never:** a risk framing, a grade, a percentile against other respondents, or any
number about money. Scores are per dimension plus a band, never a single verdict. The
band describes what process a setup can survive. It never implies an income.

## Post-scorecard email sequence

Four emails, Arabic. **Segmented by weakest dimension**, not sent flat. A single
sequence to everyone throws away the qualification the scorecard just performed.

| # | Day | Subject line | Content focus | CTA |
|---|---|---|---|---|
| 1 | 0 | Your six results | Result delivery and interpretation. Per dimension breakdown, weakest dimension named, what that dimension means to a buyer. No pitch, no offer | Read the checklist |
| 2 | 2 | What they do after the call ends | Deeper insight on their weakest dimension specifically. One concrete example of that dimension failing, and what passing looks like. Six variants, one per dimension | Watch the walkthrough |
| 3 | 5 | Applying it to a deal you actually have | Introduces the distinction between knowing the checks and applying them to live work. This is where the offer appears for the first time | See how the room works |
| 4 | 8 | Last one from me on this | Final. Recaps their weakest dimension, states plainly what the room does and does not do, includes the "who this is not for" exclusions and the published terms | Join, or stay on the weekly note |

**Email 4 disqualifies on purpose.** It carries the exclusions from Phase 8 and the
terms from Phase 6 RTB 3.3. In a category with a justified trust problem, and against
a buyer whose internal decision maker is asking whether this is another course, an
email that tells people not to buy is the one that converts the people who should.

### Segmentation map

| Weakest dimension | Email 2 variant | Routes toward | Free or costs money |
|---|---|---|---|
| Legibility | How a buyer reads one line and stops | Positioning review | Free |
| Proof | What counts as verifiable, and what gets discounted | The proof gap. Longest nurture, because it needs a client to exist first | Free, slow |
| Scope | Where scope goes wrong after the yes | Teardown, scope half | Free |
| Paperwork readiness | The form that withholds 30 percent of your invoice | The build list. **Strongest single email in the sequence** | Mixed |
| Security and compliance readiness | What to send when you do not have SOC 2 | The build list, expensive half | Costs money |
| Champion enablement | The three people your champion has to convince without you | Teardown, champion half | Free |

**The paperwork variant is the sequence's best asset.** It carries a primary-sourced,
checkable, financially specific fact that almost no respondent knows, it costs nothing
to act on, and it is verifiable against the IRS rather than against us. For a
pre-launch business with no proof of its own, an email that is right about something
expensive is the closest thing to a credential available.

**Security readiness routes carefully.** A respondent weak here at band 1 does not
have a problem yet. The variant should say so rather than manufacture urgency, then
show what the ladder looks like. Selling SOC 2 anxiety to someone bidding $4,000
projects is the churn event Phase 7 warns about, dressed as a conversion.

## Implementation notes for ScoreApp

| Item | Specification |
|---|---|
| Question count | 7. Do not add more. Completion rate is the metric, per Phase 7 stage 2 |
| Result type | Six dimension breakdown plus band. Never a single score alone |
| Capture point | Email before result, which is standard, but state the exchange plainly on the question before it |
| Language | Arabic interface, per `00-ASSUMPTIONS.md` decision 1. Write natively |
| Required field | Country. Needed for the payment routing above and for Phase 4's rail split |
| Integration | Email platform, segmented by weakest dimension and by question 7 answer |
| Tracking | Starts, completions, completion rate by question, drop-off question, question 7 distribution, and **band distribution**. Question 7 distribution and band distribution together are the most useful numbers this business will have in month one: they say whether the audience being reached is at a band the offer can serve |

---

## Why this converts

It hands over the buyer's checklist for free and in full, which is the thing the
audience most wants and cannot get anywhere in the verified competitor set. The
checklist is now evidenced rather than asserted, which is what the Block 1 research
bought. Then it shows the respondent their own position against it, in their own
words, before anything is sold.

What it cannot hand over is the application of that checklist to the respondent's own
live deal, because that requires a person looking at a specific document. That is the
paid offer, and the scorecard makes the boundary obvious without having to argue it.

**What the rebuild added.** The band result gives the respondent somewhere to go. The
old version told them what they were missing. This one tells them what size of deal
their setup currently survives and what the next rung costs, which is a reason to stay
in touch even when they are not ready to buy. That is the ladder working as
positioning, per `00-RESOLUTIONS.md` conflict 2.

**What it must never imply.** That clearing these checks wins the deal. It makes a
vendor eligible. Phase 3 flags this as the claim most likely to be crossed later, and
a scorecard that returns a band is exactly where someone would cross it.
