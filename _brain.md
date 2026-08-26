---
status: planning
type: skill pack (public, publication is the goal)
stack: Markdown skills + registry templates; npx-wired lint dependency (gesso); no build step
github: https://github.com/laltaffer/design-lead (PUBLIC since 2026-08-26)
prev_path: n/a — created in tree
---

# design-lead

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
- **Named `/design-lead` (2026-08-26, Lawrence's pick).** Named from the moment of
  use, not the concept ("calling /design-dna doesn't make sense" mid-project): it's a
  ROLE summoned at five moments, completing the C-suite pattern (cto/cmo/pm-lead/uxr —
  design was the missing chair). Symmetric with the public pm-lead pack. Invocation
  grammar: `/design-lead direction` (new visual world) · `evolve <surface>` (the
  ACRE-style preserve pass) · `critique <target>` (evidence first, judgment labeled) ·
  `encode "<rule>"` (correction → registries, permanently) · `study <subject>`
  (practice, no project). "Design DNA" survives as the REGISTRY component's name.
  Rejected: /taste-* (collides with Leonxlnx/taste-skill, reads derivative), /pd-lead
  (PD ambiguous publicly), /cdo (data-officer collision), /studio (not
  self-documenting).
- Proof point in hand: first production ship of the stack was ACRE commit `02e99fc`
  (bake-off comp → approval → site-wide cleanup → gesso PASS ×4 → live-verified).

## Status
Created 2026-08-26; **v1 built and pushed same day (commit `eededfb`)**. Layout is
skills-CLI installable (`npx skills add laltaffer/design-lead`): `skills/design-lead/`
with router SKILL.md (role + registries + invariants + mode table), five references
(direction w/ study variant, evolve, critique, encode, generation-shells,
tool-governance), templates (Design-Registry, Typeface-Registry — empty with
delete-me example rows under fictional "hollowtree-outfitters"; LOCAL.md.example),
plus MANIFESTO.md and README.md at root. De-personalization verified by grep (no
SecondBrain/Lawrence/project-name leaks); gesso credited as check-only npx dependency;
registries default to ~/.claude/design-lead/ and self-seed on first run. Earlier same
day: no pipeline gate per Lawrence ("more of a PD lead skill.. doesn't need to be tied
to either").

## Open
- ~~Dogfood before launch~~ — DONE 2026-08-26: ran the pack cold (critique + encode on
  designleaderjobs.com via its local dist build; registries seeded at
  ~/.claude/design-lead/ and grown with a real DLJ row + 2 tells). Three gaps exposed
  and fixed same day (commit `7c56f98`): critique now verifies the target is the real
  page (a Cloudflare challenge page PASSed the detector meaninglessly), chases every
  detector quote to source (a flagged "oversized number" was actually raw scraped
  location data visible in the UI — worse than the rule knew; a "585 slots in one
  row" hit was a parser artifact), and seeding deletes the template example rows.
  Direction/evolve modes not exercised in dogfood (evolve was validated pre-pack on
  ACRE; direction's method is the ported moodboard pipeline). The critique also
  produced real DLJ findings — handed to Lawrence in-session, DLJ fixes are that
  project's call.
- ~~Launch~~ — DONE 2026-08-26: repo PUBLIC; install path validated end-to-end
  (`npx skills add laltaffer/design-lead` lands SKILL.md + references + templates);
  listed on skills.sh (registration is install-telemetry — the validation install
  indexed it; listing at skills.sh/laltaffer/design-lead/design-lead, shows a pending
  Snyk audit flag, standard for new listings). Optional /cmo positioning pass for
  README/claims still available on Lawrence's ask.
- ~~Personal-stack migration (engine + overlay)~~ — DONE 2026-08-26, all four steps,
  with three deviations from the written plan:
  1. **Diff verdict:** the port carried more than expected — `evolve.md` already held
    the amend-mode discipline (screenshot-live-first, token preservation, the
    "measurably worse" verbatim), and study archival was generalized, not lost. Four
    real gaps upstreamed into `direction.md`: the mandatory-analog-reference rule with
    its why (the one source a web corpus can't regurgitate; design-specific archives,
    not fine-art museums), the "good enough to stop iterating on" hard-stop, the
    every-candidate-advances-together comp-round rule (sameness = failure; only the
    human kills a candidate), and study-archive mechanics (board + assets + index
    line). /moodboard retired — archived at `~/.claude/retired-skills/moodboard/`
    (untracked in the ~/.claude repo, so moved, not deleted; it keeps the dated
    PackOut/Cosmos verbatims).
  2. Symlink pre-existed (created earlier same day) — verified, left alone.
  3. LOCAL.md written beside the symlinked SKILL.md (gitignored, verified invisible
    to git): registry location + vocabulary mapping (Claude-tells = model-tells),
    PARA gate-write targets, taste-memory pointer, vetoes, approval conventions,
    reserved 03 signature pointer, LOCAL-ONLY rules, Refero/Mobbin/archive/harvest
    tooling, gesso caveats, p2nda pointer. **Unplanned but forced by one-home:** the
    dogfood-seeded `~/.claude/design-lead/` registries were merged into the Resources
    registries (DLJ row enriched; italic-interjection tell enriched with the DLJ
    catch + replacement; card-per-row tell added) and then deleted — LOCAL.md warns
    against recreating the default location.
  4. CLAUDE.md Web Design slimmed: moodboard bullet → /design-lead (engine + overlay
    named), the ~250-word Refero bullet → 3 lines pointing at direction.md +
    LOCAL.md + tool-governance.md, keeping only the registries-as-authority
    invariant. Mobile-first, nav, DNA/typeface checks, slop lint bullets untouched.
  Design-Registry's closing line now names /design-lead (was /moodboard) as the
  automatic check-runner.
