---
status: planning
type: skill pack (public, publication is the goal)
stack: Markdown skills + registry templates; npx-wired lint dependency (gesso); no build step
github: https://github.com/laltaffer/design-dna (private until launch; flips public at v1)
prev_path: n/a — created in tree
---

# design-dna

## Overview
Public Claude Code skill pack packaging the taste-infrastructure system built across
2026-08-24→26: treat AI design quality as a compounding system, not a per-prompt trick.
POV in one line: prompt packs make one output better; this makes your hundredth output
better than your tenth, because the system remembers. Positioned against the two
existing pack genres — prompt payloads (taste-skill) and linters (gesso) — as the layer
above both: the referee and the memory, not another player.

## Scope
**V1 in:**
- Design DNA Registry + Typeface Registry as EMPTY TEMPLATES with seeding instructions
  (track shipped worlds/palettes/moves per project; differentiation check).
- Claude-tells discipline: personal catalog of your model's recurring moves grown from
  real critiques, with the replace-never-delete rule (lint, not brief).
- Moodboard pipeline, de-personalized: worlds, visual-choice-never-prose, tiered
  reference diet (Tier-1 contemporary web core / analog as flavor), fresh-eyes
  consumable screenshots, job-transfer rule, study mode, amend-mode deltas.
- Process gates: scratch-comp isolation + human approval; evidence-first critique
  (detector evidence, then judgment labeled as judgment); lint-gate wiring via
  `npx -y @gessobuild/anti-slop check` (credited dependency, never absorbed).
- Bake-off tool governance (results over mandates: contested tools run the same real
  brief; registries referee).
- Generation-shell anatomy for AI imagery (slot templates, medium physics, identity
  invariants, role-locked references, inline anti-tell lint).
- Manifesto doc carrying the POV.

**V1 out:** Lawrence's actual registry contents, taste memory, vetoes, client rows,
Design-Library content; third-party payloads (taste-skill/impeccable/refero stay
external peers the governance layer referees).

## Key Decisions
- **Ship mechanisms, not taste (2026-08-26).** Registries publish empty; users grow
  their own. Personal state lives in a gitignored LOCAL.md overlay — the pm-lead
  pattern (one public repo + local overlay), chosen over the cto publish.sh twin
  because growing the overlay IS the product.
- **Depend on, don't absorb (2026-08-26).** gesso stays an npx dependency with credit;
  taste-skill and friends stay outside as governed peers.
- **Private until launch (2026-08-26).** Repo created private; flips public when v1 is
  ready — nothing half-baked gets a URL.
- Working title `design-dna`; naming explicitly open, Lawrence decides at /cmo.
- Proof point in hand: first production ship of the stack was ACRE commit `02e99fc`
  (bake-off comp → approval → site-wide cleanup → gesso PASS ×4 → live-verified).

## Status
Created 2026-08-26. Scaffolded + pushed (private). Next: /pm-lead zero-to-one to lock
scope/audience/claims before any pack content is written; /cmo later for README and
launch positioning (what "first" claim is honest per the 2026-08-25 Threads/GitHub
survey — see design-prompt-libraries memory).

## Open
- Run /pm-lead zero-to-one (product definition: audience, jobs, honest differentiation
  vs taste-skill/gesso/awesome-claude-design, v1 cut).
- Then port + de-personalize: moodboard SKILL.md, registry templates, critique/gate
  wiring docs, generation-shell reference, manifesto.
- Naming decision (working title design-dna).
- Launch: flip repo public, /cmo positioning pass.
