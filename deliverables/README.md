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

## Exports

`exports/` holds the XLSX and DOCX files the skill's OUTPUT FORMAT MAPPING calls
for, generated from the Markdown by `../tools/export.py`.

| Skill mapping | Files |
|---|---|
| 8 XLSX | Phases 1, 2, 4, 5, 7, 8, 9 and the lead magnet, per track |
| 4 DOCX | Phase 3, Phase 6, the Phase 2 positioning summary, and the lead magnet, per track |
| 1 MD | The 10-slide deck, per track. Markdown is the skill's specified format for Gamma AI |
| Extra | `00-research-findings.xlsx`, the competitor slate in a sheet. Not in the skill's map, added because Phase 2 reads from it |

Every workbook opens with an `About` sheet carrying the prose, then one sheet per
table named from its step. The Phase 1 workbooks carry a live scatter chart plotting
demand against competitiveness, which is what the skill's Step 1.3 asks for.
`{TBD}` cells are highlighted so the gaps are visible at a glance.

**The Markdown is the source of truth.** Edit `track-b/` or `track-a/` and re-run:

```
python3 tools/export.py
```

`exports/` is rebuilt from scratch each time, so anything edited directly in a
spreadsheet or document is lost. The skill's metadata says 7 XLSX where its own
mapping table implies 8. The mapping table is followed here.

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
