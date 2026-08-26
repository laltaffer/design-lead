# design-lead — product marketing context

Auto-drafted 2026-08-26 from the repo, `_brain.md`, and the launch session; corrected
at the CONTEXT gate. Scope of this doc: the README (GitHub + skills.sh listing) is the
only marketing surface for now.

## What it is
Public MIT skill pack for Claude Code (installable via the skills CLI on other agents
too). One role command, five modes: `direction`, `evolve`, `critique`, `encode`,
`study`. The distinct mechanism: two registries the skill reads and writes every run —
what the portfolio shipped, and the moves the model itself keeps repeating — so
corrections compound instead of being re-learned.

## Audience
Developers and design-literate builders who ship real UI with AI coding agents, and
have watched their outputs converge. They know the word "slop" and use it. Secondary:
design leaders experimenting with agents. Technical, taste-sensitive, allergic to
marketing voice; they read READMEs the way engineers read code review.

## Problem, in the audience's own words
"Every output looks the same." The ecosystem names it slop; Anthropic's own cookbook
names the convergence. See the research brief for sourced verbatims.

## Positioning (honest differentiation)
Three established genres, none of which does what this does:
- **Payloads** (taste-skill et al.): push one run off the generic center; stateless.
- **Linters** (gesso anti-slop): deterministic floors; can't know a world or objective.
- **Catalogs** (awesome-claude-design): reading, not machinery.
design-lead is the memory-and-governance layer: registries + gates + bake-offs.
Claim discipline: never claim "first" or quantify others' weaknesses; describe the
mechanism no neighbor has and let the reader conclude. gesso is a credited dependency;
payloads are governed peers, never absorbed.

## Proof points (real, citable)
- Built by running it: the method shipped a live business-site cleanup (ACRE,
  workwithacre.com, commit `02e99fc`) before the pack existed as a pack.
- The dogfood run's first cold critique found a real data bug in a live product
  (designleaderjobs.com: raw scraped location strings in visible UI; fixed, `f172948`).
- The pack's own repo history: three of its rules were paid for on real critique
  rounds (replace-never-delete, fresh-eyes, job-transfer).

## Brand voice (from the voice & stance interview, 2026-08-26)
- **Whose voice:** the practice — a design leader's discipline speaking, not
  Lawrence's first person and not product self-praise.
- **Audience's relationship to the problem:** they live it. Name slop plainly, zero
  convincing that the problem exists; receipts only for what the PACK claims about
  itself (the two ship links).
- **Gift or sale:** gift. State what it is and how to use it; no persuasion pressure,
  no urgency, no install-count games. The CTA is the install command, once.

## Channels
README only (GitHub repo + skills.sh listing pulls the SKILL.md description).
No launch posts, no social, unless Lawrence asks.
