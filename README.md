# design-lead

**A design leader with memory, for Claude Code.** Prompt packs make one output
better; this makes your hundredth output better than your tenth, because the system
remembers — what your portfolio shipped, what your model's own hands reach for, and
every correction you've ever given, verbatim.

Why that matters: AI design output converges on the same generic moves regardless of
brief. Payload skills push a single run off-center but keep no state; linters catch
"reads as generated" but can't know your world or your objective. design-lead is the
layer above both — the referee and the memory. The full argument:
[MANIFESTO.md](MANIFESTO.md).

## Install

```bash
npx skills add laltaffer/design-lead
```

Or clone and symlink `skills/design-lead` into `~/.claude/skills/`.

Optional but recommended: your personal overlay. Copy
`skills/design-lead/templates/LOCAL.md.example` to `LOCAL.md` beside the SKILL.md
(it's gitignored) and record your vetoes, conventions, and reserved signatures.

## Use — one role, five moments

```
/design-lead direction          # project needs a visual world: research → board → your gate
/design-lead evolve <surface>   # improve a shipped surface without breaking it
/design-lead critique <target>  # evidence-first review: detector facts, then labeled judgment
/design-lead encode "<rule>"    # your correction becomes permanent registry state
/design-lead study <subject>    # train the eye; no project needed
```

On first run it seeds two registries at `~/.claude/design-lead/`:

- **Design-Registry.md** — one row per project (world, shipped palette, signature
  moves) plus a *model-tells* list: the moves your AI repeats across projects, each
  paired with what to reach for instead. Grown from your critiques, checked against
  every comp.
- **Typeface-Registry.md** — shipped faces, look-alike checks, AI-darling callouts.

Every mode consults the registries before showing you anything, and every callout is
exactly that — a callout. You decide.

## What's inside

| Piece | What it does |
|---|---|
| [SKILL.md](skills/design-lead/SKILL.md) | the role, the registries, the invariants, mode routing |
| [direction.md](skills/design-lead/references/direction.md) | worlds → tiered reference research → visual board → approval gate |
| [evolve.md](skills/design-lead/references/evolve.md) | audit-first preservation pass: deltas on shipped screens, never parallel rebuilds |
| [critique.md](skills/design-lead/references/critique.md) | two-layer review: deterministic evidence, then judgment labeled as judgment |
| [encode.md](skills/design-lead/references/encode.md) | corrections → registry rows, verbatim, one home per fact |
| [generation-shells.md](skills/design-lead/references/generation-shells.md) | locked direction → reusable AI-imagery prompt shells |
| [tool-governance.md](skills/design-lead/references/tool-governance.md) | results over mandates: bake-offs, not bans |
| [templates/](skills/design-lead/templates/) | empty registries with seeding examples + LOCAL.md overlay |

## Plays well with

- **[@gessobuild/anti-slop](https://github.com/Gesso-Build/skills)** (MIT) — the
  deterministic 73-rule slop detector wired in as this pack's lint gate, via
  `npx -y @gessobuild/anti-slop check`. Used check-only, credited, never absorbed.
- Design payload skills (taste-skill, impeccable, and kin) and research MCPs — they
  stay external peers; the governance layer runs bake-offs between them and the
  registries referee the results.

## License

MIT.
