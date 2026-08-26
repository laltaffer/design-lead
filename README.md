# design-lead

A design leader with memory, for Claude Code and any agent that speaks the skills CLI.

Every AI that designs converges on the same moves. The same hero anatomy, the same
three cards, the same safe serif, the same numbered section markers. You correct it,
it apologizes, and next session it does the thing again. The correction went nowhere.

design-lead gives corrections somewhere to go. It runs design work as a role with two
registries behind it: one recording what each of your projects actually shipped, one
recording the moves your model itself keeps reaching for. Every run reads both before
showing you anything and writes back what you decided. By the tenth project, the
registries know your portfolio's DNA and your model's habits.

## The loop, concretely

You catch your agent putting an italic serif flourish in a hero headline. You say so
once:

```
/design-lead encode "italic interjections in display lines read as an AI tell; use color-weight emphasis in the same face instead"
```

That becomes a row in the model-tells registry, with the correction verbatim and a
named replacement move. Every future comp, in every project, gets checked against it
before you see the work. A callout is never a veto; the registry flags, you decide.

## Install

```bash
npx skills add laltaffer/design-lead
```

First run seeds the registries at `~/.claude/design-lead/`. Optional: copy
`templates/LOCAL.md.example` to `LOCAL.md` beside the SKILL.md (gitignored) for your
own vetoes, conventions, and reserved signatures.

## One role, five moments

```
/design-lead direction          # project needs a visual world: research, board, your gate
/design-lead evolve <surface>   # improve a shipped surface without breaking it
/design-lead critique <target>  # detector evidence first, judgment labeled as judgment
/design-lead encode "<rule>"    # a correction becomes permanent registry state
/design-lead study <subject>    # train the eye, no project needed
```

The invariants hold across all five: no pixels before a named world, comps stay
quarantined until a human approves what they saw, choices get made from rendered
candidates instead of prose, and every HTML surface passes a deterministic lint gate
before it reaches you.

## What's inside

| Piece | Job |
|---|---|
| [SKILL.md](skills/design-lead/SKILL.md) | the role, the registries, the invariants, mode routing |
| [direction.md](skills/design-lead/references/direction.md) | worlds, tiered reference research, visual boards, the approval gate |
| [evolve.md](skills/design-lead/references/evolve.md) | audit-first improvement of shipped surfaces, deltas over rebuilds |
| [critique.md](skills/design-lead/references/critique.md) | two-layer review: deterministic evidence, then labeled opinion |
| [encode.md](skills/design-lead/references/encode.md) | corrections to registry rows, verbatim, one home per fact |
| [generation-shells.md](skills/design-lead/references/generation-shells.md) | locked directions compiled into reusable AI-imagery prompts |
| [tool-governance.md](skills/design-lead/references/tool-governance.md) | bake-offs over bans when design tools disagree |
| [templates/](skills/design-lead/templates/) | empty registries with seeding examples, plus the LOCAL.md overlay |

The rules inside were paid for on real work, and the file for each says what it cost.
The one worth repeating here: **replace, never delete.** Tells are common because
they work. A round of comps mechanically stripped of every flagged pattern came back
unanimously worse; the registry pairs every tell with a stronger move to reach for,
because design by avoidance leaves holes where the power was.

## Where this sits

Three kinds of design tooling already exist for agents, and this pack depends on one
of them. Payload skills (taste-skill and its kin) push a single run away from the
generic center, and they work, per run, with no state between runs. Deterministic
linters catch what reads as generated; design-lead wires one in directly, running
[Gesso's anti-slop](https://github.com/Gesso-Build/skills) (MIT, credited, check-only)
as its lint gate. Catalogs collect reference prompts to read. design-lead is the layer
that remembers: registries above the payloads, governance that runs bake-offs between
them on real briefs, and an encode loop that turns your taste into accumulating state.

Two receipts from before this was a pack: the method's first production run shipped a
live business-site cleanup ([workwithacre.com](https://workwithacre.com), commit
`02e99fc` in that repo), and its first cold dogfood critique found a real data bug on
a live job board (raw scraped location strings rendering in visible UI, fixed the
same day).

## License

MIT. The manifesto behind the design: [MANIFESTO.md](MANIFESTO.md).
