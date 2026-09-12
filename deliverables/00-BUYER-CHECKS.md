# What a North American buyer checks, imported

Source: supplementary research Block 1, delivered 2026-09-12. Imported here as the
product's content spine. Nothing in the original run established what these checks
actually are, only that no competitor packages them.

**Read the source-quality note before putting any number in front of a customer.**

---

## Source quality, and why it limits what can be published

The research mixes two very different tiers of source, and the distinction matters
because this material becomes curriculum.

| Tier | Sources | Usable how |
|---|---|---|
| **Primary, strong** | IRS instructions for W-8BEN and W-8BEN-E, OFAC sanctions list service, Canada Treasury Board Directive on the Management of Procurement, Public Services and Procurement Canada industrial security | Teachable as fact. Cite the source |
| **Secondary, mixed** | Vendor onboarding blogs, procurement content marketing, sales-cycle benchmark aggregators | Teachable as pattern, not as statistic |
| **Conflicted** | The 78 percent SOC 2 Type II figure comes from a compliance vendor that sells SOC 2 readiness services | **Do not publish as a number.** Teach the direction, not the figure |

The tax, sanctions and Canadian procurement material is solid and citable. The
thresholds, cycle times and percentages come from content marketing and aggregators.
They are good enough to shape strategy and not good enough to print in a course
slide with a decimal point on them.

**Rule for every asset built from this file:** teach the mechanism, cite the primary
source where one exists, and describe secondary figures as "commonly reported"
rather than as measured fact.

---

## The single most important thing in this import

Every heavyweight item below is gated by deal size, and the gate sits at roughly
**$25,000 annual contract value**.

| Deal size | What the buyer actually does |
|---|---|
| Under about $15,000 | Minimal formal procurement. Manager-level approval. Reported 14 to 30 day cycles |
| About $15,000 to $25,000 | Procurement starts appearing. Some security review |
| Above about $25,000 | Procurement, legal review and a security questionnaire become normal |
| Above about $100,000 | Full enterprise process. Reported 90 to 180 plus day cycles, with 35 to 40 percent of elapsed time inside legal and procurement |

By headcount rather than deal size, reported cycles run about 38 days for a buyer of
1 to 10 people against about 185 days for a buyer over 10,000.

**This one table reorganises both tracks.** Most of what follows applies to buyers
above the $25,000 line. A solo builder selling a $6,000 project meets almost none of
it. See `00-CONFLICTS-TO-RESOLVE.md`, conflict 2.

---

## The buyer's actual sequence

Six stages, four owners. The original run guessed at this. Here it is.

| # | Stage | Who owns it | What happens |
|---|---|---|---|
| 1 | Intake | Business owner, the champion | Vendor, product, use case, data categories, integrations recorded. Inherent risk assessed, duplicates screened out |
| 2 | Risk triage | Procurement | Vendor tiered as commodity, standard, strategic or critical, by data sensitivity and financial exposure. **The tier decides how deep everything else goes** |
| 3 | Due diligence | Security, legal, finance in parallel | Tax and identity documents, sanctions screening, security evidence, privacy review |
| 4 | Contracting | Legal and privacy | MSA, NDA, DPA, SOW, SLA negotiated and signed |
| 5 | Operational setup | Finance and IT | Vendor master record, payment terms, banking, SSO and access configuration |
| 6 | Go-live | All four sign off | Every workstream must clear before the vendor is enabled. **A single incomplete lane holds the whole thing** |

The four lanes are procurement for commercial terms, legal and privacy for the
contract and DPA, IT and security for assurance and access, and finance for the
vendor master and payment.

**What this tells a vendor.** The stall is rarely the buyer changing their mind. It
is one lane waiting on one document, with nobody outside that lane aware of it.

---

## Stage 3, the foreign-vendor specific gates

The four things a domestic vendor never has to think about.

### 1. Tax documentation. Primary source, hard gate

| Item | Detail |
|---|---|
| Which form | **W-8BEN for a foreign individual. W-8BEN-E for a foreign entity.** Not interchangeable |
| Consequence of absence | The withholding agent may be required to withhold at **30 percent**, or payment is refused until a valid form arrives |
| What it must carry | FATCA classification, tax residence, and any treaty benefit claim. Incorrect FATCA status and the treaty section are the two commonly reported points of confusion |
| Validity | A signed W-8BEN-E is generally valid through 31 December of the third calendar year after signature, unless circumstances change |
| No TIN | A foreign individual still provides W-8BEN even without an EIN, ITIN or SSN, and even when claiming no treaty benefit. Payment is not issued until it arrives |
| When a US TIN is needed | An EIN may be expected for treaty claims or reduced withholding. An individual claiming treaty benefits on certain income types typically needs an ITIN |

This is the most teachable item in the entire import. It is primary-sourced, it is
binary, it is invisible until it bites, and it costs 30 percent of an invoice.

### 2. Sanctions and restricted-party screening. Primary source

- Screening runs against OFAC SDN and non-SDN consolidated lists, plus UN, EU, UK
  and Canadian lists. It is routine for **every** foreign vendor.
- **Sanctions are entity-based, not country-based.** No blanket prohibition was
  found on vendors from Egypt, Jordan, Morocco, Saudi Arabia or the United Arab
  Emirates, and no mainstream North American vendor policy singling those markets
  out was found.
- Confidence on the second point is **P to T**. Absence of a found policy is not
  proof of absence of friction.

Report this honestly to members. The answer appears to be that these five markets
are screened like everyone else and not excluded. That is reassuring and it should
be said plainly rather than avoided.

### 3. A United States entity is not legally required

Buyers can contract and pay a foreign entity directly, provided tax forms and
banking details are complete. No source found stated US incorporation as a legal
prerequisite. Some buyers prefer it for large or regulated contracts, or for dispute
resolution comfort, but that is a buyer preference rather than a rule.

Confidence **P**, trending **T** on the second half. This directly contradicts
widespread folk advice in this audience, which is exactly why it is worth teaching,
and exactly why it should be taught with the caveat attached.

### 4. Identity and entity verification

Business registration verified, beneficial owners identified, litigation history
checked for high-risk or high-spend vendors.

---

## Stage 3, security and privacy

### The evidence ladder

Buyers assess with SOC 2 or ISO 27001 certificates, a completed security
questionnaire, and a penetration test summary. Absence of these does not
automatically disqualify. It extends the review.

| Buyer segment | What is actually expected |
|---|---|
| SMB, under about $15,000 | Usually nothing formal |
| Mid-market | Structured security evidence. A questionnaire at minimum |
| Enterprise | SOC 2 **Type II** is widely treated as the baseline. Type I is commonly reported as insufficient, because Type II shows controls operating over 6 to 12 months |

### What a small vendor supplies instead of SOC 2

This is the practical heart of the section and it is genuinely useful to a small
foreign vendor.

1. A clear written **system boundary**. What the system is, what data it touches,
   where it runs.
2. A **recent penetration test report**.
3. **Control narratives** for access control, logging, and change management.
4. A **stated roadmap** toward SOC 2, with dates.
5. A **public security page** carrying the above in summary.

The consistent advice across sources is to answer questionnaires honestly, document
gaps with remediation plans, and avoid claiming a maturity the vendor does not have.
One source names this failure mode directly as audit theatre.

### Questionnaires in circulation

Shared Assessments **SIG** and **SIG Lite**, Cloud Security Alliance **CAIQ**, plus
buyer-specific questionnaires aligned to SOC 2 or ISO 27001 controls. They cover
access control, encryption, incident response and business continuity.

### Privacy and data

- **SCCs**, standard contractual clauses, for EU and UK personal data, with explicit
  data residency commitments in the DPA.
- **CCPA and CPRA** obligations for California resident data: data subject rights,
  disclosures, opt-out mechanisms, reflected in the DPA or a privacy addendum.
- A **DPA** must define processing scope and legal basis, data categories, security
  controls, sub-processor list, cross-border transfers, incident response and breach
  notification service levels, data residency, and audit rights.

### Insurance

| Coverage | Note |
|---|---|
| General liability | Commonly specified at **USD 1,000,000 per occurrence** or above |
| Professional liability, errors and omissions | Standard expectation for services vendors |
| Cyber liability | Increasingly requested where sensitive data is handled |
| Workers compensation | Listed in checklists, applicability varies by arrangement |

A certificate of insurance is frequently requested during onboarding. Whether a
vendor in the five origin markets can obtain policies a North American buyer will
accept was **not answered** by this research. It is a live open question and a
potentially expensive one.

---

## Stage 4, contracting

### The artifacts

MSA, NDA, DPA, SOW, SLA. A BAA where health data is involved. SCCs where EU data
crosses a border.

### The clauses foreign vendors mishandle

IP assignment or licence, confidentiality, governing law and venue, limitation of
liability, indemnity, non-solicitation. Buyers increasingly demand higher liability
caps and broader indemnity from vendors touching security, privacy, or **AI
decision-support functions**.

That last clause matters more than it looks for this audience. An AI services vendor
is in the category that attracts the enhanced liability terms.

---

## Stage 5, getting paid

| Item | Detail |
|---|---|
| Terms | Net 30, Net 45, Net 60 are the standard defaults. Procurement negotiating terms is reported to add roughly 16 days to a cycle |
| Mechanism | ACH and wire are primary for B2B services. Cards are for small subscriptions |
| Wire fees | Who bears them is set by contract. **No consistent norm was found.** Agree it explicitly or absorb it by accident |
| Invoice rejection | Tax identifier missing, legal name not matching the vendor master record, purchase order reference wrong or absent |

The invoice rejection line is worth teaching on its own. An invoice that does not
match the vendor master record exactly is held, and the vendor usually finds out by
noticing the money did not arrive.

---

## The soft checks, and the finding that reframes the product

### Why buyers go quiet after a good first call

The original run treated this as an unexplained loss the member never gets a reason
for. The research gives a mechanism, and it is a better story.

**The champion cannot sell the vendor internally.** Deals stall when the buyer-side
advocate has no proof assets they can hand to procurement, security and legal. The
positive first meeting was real. What followed was a champion who could not get the
vendor through four lanes with nothing to show each one.

Separately, long internal cycles in large organisations look identical to ghosting
from outside. A 90 to 180 day enterprise cycle with a vendor hearing nothing is a
normal cycle, not a rejection.

**What this changes.** The job is not to impress the buyer in the room. It is to
send the champion away carrying documents that survive being forwarded to three
departments that never met you.

### What buyers treat as proof

- Verifiable security pages with SOC 2 summaries and penetration test dates.
- Case studies with **named customers and concrete deployment detail**.
- Reviews carrying identifiable job titles, company sizes and specific use cases.
- Detailed implementation guides.

And what they discount: logo walls, generic testimonials, unattributed praise.

### Language and location

- **Quebec French obligations are statutory, not optional.** One source frames this
  as a core engineering commitment rather than cosmetic translation.
- Location is framed by buyers as data-jurisdiction risk, not nationality. The
  CLOUD Act is cited as a reason Canadian buyers scrutinise **United States**
  vendors, which is a risk a MENA vendor does not carry.

### Canada, where the advice partly reverses

- A federal **Buy Canadian** policy is reported to grant a 10 percent bid price
  reduction and 25 percent evaluation-score weight to Canadian suppliers.
- Canadian federal contracting limits: Public Services and Procurement Canada may
  enter competitive service contracts up to CAD 100,000,000 and non-competitive up
  to CAD 1,750,000. Other departments have lower limits. Pressing emergency allows
  non-competitive up to CAD 3,000,000. Primary source.
- Private-sector onboarding stages are materially the same in both countries. The
  differences are legal and jurisdictional, not procedural.

See `00-CONFLICTS-TO-RESOLVE.md`, conflict 4.

---

## The gaps foreign vendors most commonly have

Straight from the research, and this is the shortest useful summary of the entire
import.

1. Mature security evidence. SOC 2 Type II, penetration test summaries, a security page.
2. Accurate and complete W-8BEN or W-8BEN-E.
3. Documented insurance at expected limits.
4. Buyer-usable proof assets. Specific, attributable case studies and named references.

---

## What the research could not answer

Carried forward as open, not quietly closed.

- Exact private-sector thresholds by company size. The dollar figures above are
  inferred from annual contract value tiers and sales-cycle benchmarks, not from
  published procurement policies.
- Who bears international wire and ACH fees. No quantitative norm found.
- Whether vendors from the five named origin markets face documented friction
  beyond routine screening. Nothing found, which is weak evidence either way.
- Whether SOC 2 expectations differ for foreign against domestic vendors. Surveys do
  not disaggregate by vendor origin.
- **Added by this import:** whether a vendor in the five origin markets can obtain
  general liability, errors and omissions, and cyber policies that a North American
  buyer will accept. Not researched. Potentially a hard blocker and worth a Block 11.
