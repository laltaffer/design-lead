# Research brief — README positioning (scoped)

2026-08-26. Sources: the 2026-08-25 ecosystem survey (Threads + GitHub, recorded in
the design-prompt-libraries memory) and primary documents re-read during it. All
quotes verbatim with sources; nothing invented.

## The pain, in real language

- Anthropic, frontend-aesthetics cookbook (anthropics/claude-cookbooks): "You tend to
  converge toward generic, 'on distribution' outputs. In frontend design, this
  creates what users call the 'AI slop' aesthetic."
- awesome-claude-design README (rohitg00), summarizing launch-week community reaction
  to Claude Design: "The single biggest community complaint: every Claude Design
  output looks the same."
- Same README, quoting a community review: "Just tested it. This is only hype for
  people that never worked with real UX/UI designers. Another slop feature that will
  burn tokens."
- Gesso anti-slop README (Gesso-Build/skills): "'Slop' is the set of visual tells
  that make generated UI read as generated."

Trigger moment: the second or third project where the builder recognizes their own
AI's habits — the same hero, the same three cards, the same serif — and realizes the
prompt isn't the variable.

## Objections to preempt (honestly)

1. "Another design skill?" — the genre fatigue is real; the README must differentiate
   by mechanism (state), not by adjectives.
2. "My payload skill already fixes this." — payloads are stateless; acknowledge they
   work per-run and position as the layer above, not a replacement.
3. "Will it fight my setup?" — governance stance: depends on gesso (credited),
   referees payloads, absorbs nothing.
4. "Is the memory real or a gimmick?" — show the loop concretely (correction →
   registry row → next run consults it) and the two ship links.

## Competitive angle map

| Genre | Exemplar | Their own claim | What they don't do |
|---|---|---|---|
| Payload | taste-skill (Leonxlnx, ~80K stars) | "gives your AI good taste. stops the AI from generating boring, generic slop" | no state between runs |
| Linter | gesso anti-slop | deterministic critique, "exact detectors, idempotent auto-fixes" | floors only; no world, no objective, no memory |
| Catalog | awesome-claude-design | DESIGN.md prompts by aesthetic family | reading material, not machinery |

Angle: the uncontested word is **memory** (with **compounding** as its consequence).
Claim discipline: never "first," never disparage — each neighbor is good at its layer,
one is a dependency, and the audience can smell a straw man.

## Insight to hang the asset on

The audience already believes the problem (they named it "slop" before any vendor
did). The README's job is not persuasion; it is a precise description of a mechanism
they haven't seen: an agent that writes down what you rejected and checks it next
time. Specificity of the loop is the whole pitch.
