# generation shells — locked direction → reusable generation prompt

For projects that ship AI-generated imagery or video. Batches generated from prose
re-descriptions drift; batches generated from a shell don't. Compile the shell once,
at direction-lock; store it in the project's design docs; every asset request fills
slots, never rewrites the shell.

Anatomy (synthesized from working art-director practice — the production-call-sheet
school of prompting):

1. **Constants are the craft; brackets are the content.** The world's palette, light,
   composition rules, and medium physics appear VERBATIM in every generation;
   `[SUBJECT]`, `[SETTING]`, `[ACTION]` vary. If two assets from the shell look like
   different projects, the constants were too thin.
2. **Medium physics, never vibe adjectives.** Cash out every aesthetic claim as
   production traits: not "vintage photo" but "35mm look, slight grain, faded color
   response, soft contrast, natural light, documentary framing." Sample color values
   from the actual referent (a sunlit new leaf, not "green").
3. **Identity locks by enumeration.** A recurring character/product is pinned by
   listed invariant features (hair, glasses, materials, proportions) — never by "the
   same X as before."
4. **One job per reference image.** "Image 1 is the CHARACTER reference: match
   exactly. Image 2 is the LAYOUT reference: follow its sequence, do not invent,
   reorder, or merge." Unassigned references leak.
5. **Video adds a timeline contract.** Timestamped shots with camera grammar per shot,
   hard cuts declared, sound synced to timestamps, and continuity stated as physics
   ("momentum carries between cuts, same lighting direction in every shot").
6. **Close with inline anti-tell lint.** End the shell by negating the target model's
   known failures for this asset class ("no extra fingers, no morphing, no glossy
   retouching, no cartoon style") — the generation-time equivalent of the registry
   check.
7. **Verify against the genuine article.** Never let a model draw a real-world
   artifact class from memory (maps, tickets, forms, instruments) — source or trace
   the real thing; generated approximations of documented artifacts read as fake next
   to any authentic one.

Generated assets pass the same gates as any comp: registry check, human approval on
seen pixels, and honest labeling wherever a real photograph is what the audience is
being led to assume.
