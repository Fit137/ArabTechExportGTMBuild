# GTM run output

The `gtm-builder` skill, v3.1, run against `../GTM-BRIEF.md` with the substitutions
in `../SKILL-ADAPTATION.md`. Two runs, Track B first as the brief recommends.

Executed 2026-09-12.

## Read in this order

| # | File | What it is |
|---|---|---|
| 1 | `00-RESEARCH-FINDINGS.md` | The three external research steps plus Step 0, executed rather than handed back. Named entities, working URLs, confidence marks, and what came back thin |
| 2 | `00-ASSUMPTIONS.md` | Section 4 and the five open decisions, answered as stated assumptions. Every dependent file is named |
| 3 | `track-b/` | Run 1, individual builders. Nine dashboards, lead magnet, deck |
| 4 | `track-a/` | Run 2, enterprise. Same structure |

## Track B, individual builders

| Phase | File |
|---|---|
| 1. Service and Offer Matrix | `track-b/01-service-offer-matrix.md` |
| 2. Competitive Market Analysis | `track-b/02-competitive-analysis.md` |
| 3. Positioning | `track-b/03-positioning.md` |
| 4. ICP | `track-b/04-icp.md` |
| 5. Buying Committee | `track-b/05-buying-committee.md` |
| 6. Value Proposition | `track-b/06-value-proposition.md` |
| 7. Customer Journey Funnel | `track-b/07-customer-journey.md` |
| 8. Assets and Collaterals | `track-b/08-assets-library.md` |
| 9. Pricing and Packaging | `track-b/09-pricing-packaging.md` |
| Lead magnet | `track-b/10-lead-magnet-scorecard.md` |
| 10-slide deck | `track-b/11-gtm-walkthrough-deck.md` |

## Track A, enterprise

| Phase | File |
|---|---|
| 1. Service and Offer Matrix | `track-a/01-service-offer-matrix.md` |
| 2. Competitive Market Analysis | `track-a/02-competitive-analysis.md` |
| 3. Positioning | `track-a/03-positioning.md` |
| 4. ICP | `track-a/04-icp.md` |
| 5. Buying Committee | `track-a/05-buying-committee.md` |
| 6. Value Proposition | `track-a/06-value-proposition.md` |
| 7. Customer Journey Funnel | `track-a/07-customer-journey.md` |
| 8. Assets and Collaterals | `track-a/08-assets-library.md` |
| 9. Pricing and Packaging | `track-a/09-pricing-packaging.md` |
| Lead magnet | `track-a/10-lead-magnet-diagnostic.md` |
| 10-slide deck | `track-a/11-gtm-walkthrough-deck.md` |

The decks are the skill's Gamma AI output. Paste either file into Gamma or any slide
generator. Markdown, ten slides, `---` separators, no tables, no em dashes.

## Format note

The skill's output map calls for XLSX and DOCX. These are Markdown, because the
deliverables live in a git repository where a diff is the point and a binary file is
not reviewable. Every table is a Markdown table and pastes into Sheets, Docs or Gamma
directly. Export to XLSX or DOCX once the content is settled, not before.

## Constraints held throughout

Checked mechanically across all 22 files.

| Rule | Status |
|---|---|
| No em dash | 0 occurrences |
| Banned word list from `GTM-BRIEF.md` Section 5 | 0 occurrences in content. 2 in explanatory notes about a renamed skill field |
| Unknown metrics stay `{TBD}` | 115 marks. No number is invented anywhere |
| No testimonial, client count, income figure, or guarantee | None. Phase 6 leaves 18 fields blank in each track rather than filling them |
| No superlative the research does not support | The "only provider" claim is explicitly refused in `00-RESEARCH-FINDINGS.md` |

## The six things to answer next

Ranked by how much output changes. Full detail in `00-ASSUMPTIONS.md`.

1. **Founder's stateable background.** Fills 18 blocked fields per track and unblocks
   funnel stage 3 in both. Highest value unblock in the run
2. **Language per channel.** Arabic or English. Assumed Arabic top of funnel, English
   work product
3. **Which free content creators this audience actually watches.** Probably
   competitor number one, and the open web could not answer it
4. **Named origin markets.** Assumed Egypt, Jordan, Morocco, Saudi Arabia, UAE
5. **Runway.** Decides whether Phase 8 can afford the long form asset
6. **Pricing.** Assumed deferred. Structure stands without the numbers
