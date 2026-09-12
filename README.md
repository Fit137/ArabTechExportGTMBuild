# Arab Tech Export, GTM input brief

The discovery input for running the `gtm-builder` skill on Arab Tech Export. arabtechexport.com

Arab Tech Export teaches Arab technology builders and companies to sell AI products and services into markets with higher demand and higher economic value, starting with the United States and Canada. It serves two buyers with the same subject, education: individual builders through a community, courses, one-on-ones, and AMA sessions, and enterprise companies through sales team training and market entry strategy.

Four files. No placeholders for an agent to fill, and nothing here waits on a build step.

| File | What it is |
|---|---|
| `GTM-BRIEF.md` | The skill's REQUIRED INPUTS, answered. Project information, competitor slate, service list, business context, and the claim constraints every phase has to respect |
| `SKILL-ADAPTATION.md` | How the nine phases change. The skill is written for B2B SaaS, this is services and education, and six phases need a substitution |
| `RESEARCH-PROMPTS.md` | The three external research steps, pre-filled and ready to paste, plus a Step 0 the skill assumes you already did |
| `.claude/skills/gtm-builder/SKILL.md` | The skill itself, checked in so a session opened on this repo can run it |

## How to run it

1. Push this repo, then open a Claude Code session on it.
2. Fill the four business context lines in `GTM-BRIEF.md` Section 4, and answer as many of the five open decisions as you can. Pricing and language matter most.
3. Run Step 0 in `RESEARCH-PROMPTS.md` to name your competitors. The skill assumes you already know them and this business has not named any.
4. Run Steps 1.1, 2.1, and 2.7 from the same file, then bring the findings back.
5. Invoke the skill. Point it at `GTM-BRIEF.md` and `SKILL-ADAPTATION.md` first.

Two runs, not one. Track B, individual builders, then Track A, enterprise. The skill builds one GTM per run and these are two different buyers with two different offers, two competitor slates, and two pricing models. `GTM-BRIEF.md` carries both and recommends Track B first.

## The one rule that governs the whole run

The business is pre-launch. No customers, no revenue, no results, no testimonials. Unknown numbers stay `{TBD}` and are never invented.

This bites hardest in Phase 6, which asks for a supporting proof point and a social proof headline nine times each. Eighteen invitations to make up a customer. The skill's own deck prompt already carries the rule. Apply it from Phase 1.
