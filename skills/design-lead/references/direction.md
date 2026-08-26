# direction — research a visual world before pixels

Produce a **board**: a named world plus annotated references the human approves before
any design work starts. The board is the review artifact; design iterates only after
it is locked. A board contains references and swatches, never layouts — skipping ahead
to comps is the mode's failure state.

**Study variant:** same pipeline, no project required — only a subject ("worlds for a
hunting outfitter", "editorial registers for data products"). Run stages 1–4, skip the
lock: nothing is written to any project. Archive the board — the file, its image
assets, and an index line so future runs can find it — wherever the user keeps
reference material, so studies compound into future direction runs.

## 1. Frame

Read the project's design notes (its brain/README/design docs). If a locked direction
already exists, stop and say so — amending a locked direction is `evolve`'s job, and a
new-direction run over a locked world needs the human's explicit call.

Name the problem in one sentence — user pain, a business goal, a shipped surface
failing at its job. "This surface isn't in the world yet" is an aesthetic itch, not a
problem; if no problem can be stated, say so and offer a study instead. Then verify
the stated problem against the repo's CURRENT state, not just its notes — notes go
stale, and running a direction for a problem already solved in-tree wastes the run.
A recorded verdict that a surface is good enough to stop iterating on is a hard stop —
it outranks any note about remaining ceiling.

Privacy: for projects the user marks private/local-only, outbound research queries use
world vocabulary only — never the project, client, or employer name.

## 2. Worlds

Propose 2–3 candidate **worlds** — concept anchors that palette, type, and motifs
derive from (the register of: USGS quadrangle map, ghost-sign wall, engraving plate).
At least one candidate from outside web design: a physical artifact, print genre, or
place. A world names a real visual tradition with its own rules.

Adjectives in the brief — "fun", "premium", "bold" — are REGISTER requests, not prop
lists. Resolve them through the world and its mechanisms (type nerve, palette
register, motion timing, wordplay bound to the world), never through the props the
adjective conjures (confetti and tilted stickers for fun, gold and serif for
premium): those props are the model's priors showing, and most are registered
tells. Wit belongs in the bones, not on the surface.

**The choice is made visually, never from prose.** Run enough of stage 3 for EVERY
candidate to give each a small board section — 2–3 rendered references, real swatches,
type set in the actual faces — assemble them side by side in one board file, open it,
and only then ask which world wins (mark your recommendation on the board itself). The
full research pass then deepens the winner.

## 3. Research

Gather references for the confirmed world until the bar is met: **3–5 references from
at least two source types, at least one analog (non-web-design), every reference
carrying an image file and a one-line steal note** ("the way X handles Y" — the
specific move to take, not a vibe). Declare one
reference **dominant**; the rest contribute 1–2 borrowed details each. Synthesize,
never average — averaging references produces the safe middle this pack exists to kill.

**The reference diet (tiers):**

- **Tier 1 — the core, most of every board:** award-tier and cutting-edge contemporary
  web design (Awwwards, godly, siteinspire, styles.refero.design, category-defining
  brand sites). Structure, layout, and personality come from here.
- **Tier 2:** product-pattern corpora (Mobbin and kin) when the surface is an app.
- **Tier 3 — flavor only:** analog artifacts from design-specific archives (Letterform
  Archive, Fonts In Use, Library of Congress collections, Internet Archive specimen
  books). Palette, texture, register vocabulary — never the center of gravity. A board
  built analog-first produces museum pastiche with no web personality. One analog
  reference is still mandatory: it is the one source a web-trained corpus can't
  regurgitate. Stay in design-specific archives — fine-art museums read as museum,
  not cutting-edge.

Every candidate world needs Tier-1 evidence that it translates to modern web craft; a
world with only Tier-3 evidence is flagged **unproven on the web**.

**Fresh eyes:** reference screenshots are consumables. Harvest fresh ones each run —
new sites, new gallery pages, never the same site twice in a row — and delete captures
when the run ends. Steal-note TEXT persists; pixels don't. This forces the eye to keep
learning instead of recycling one harvest forever.

**Job transfer:** every structural reference does a job for ITS product. Name that job
before stealing the structure, and check this page shares it — a thumbnail wall that
sells curation stops selling anything when pasted onto a product that sells trips.
Every hero must answer: does this sell what the site sells?

**Borrow only from pixels you have looked at.** A prose description of a layout
invites model priors to fill the visual gap. Before taking a structural move from any
reference, view its actual image and copy its composition facts: quantity, scale,
spacing, ground. Motion is pixels too: when a reference's power is choreography —
transitions, scroll timing, a ground that reacts to content — watch it moving (a
scripted scroll recording read as a filmstrip works) before stealing from it. A
motion-led surface judged from stills gives up half its design.

**A palette is a system with a stated logic.** Before any palette goes on a board:
(1) its logic fits one sentence — tints of one hue plus a chromatic dark anchor, an
off-axis complementary pair, an ordered ramp; a palette that can't state its logic
reads random, however good the swatches. (2) Every color holds a locked role — an
accent that only ever marks action stays electric; spent everywhere, it's noise.
(3) Doses stay unequal — a quiet field with vivid micro-doses, or a full drench
with restraint; a 50/50 vivid split reads chaotic. (4) Chroma and lightness are
chosen against the surface's intended register: light + high-chroma reads playful,
light + muted reads calm, dark + restrained reads serious — and mid-lightness,
mid-chroma aged surfaces read dated in any world. (5) The ground may participate
(scene-by-scene recolors) only under the same one-line logic.

## 4. Registry check

Run the SKILL.md check (portfolio reuse, family resemblance, AI-tells, model-tells,
typeface registry) on the emerging direction. Carry every callout onto the board
verbatim — a callout is not a veto; the human decides at the gate.

## 5. Board and gate

Assemble one HTML board (stable path in scratch space; reruns overwrite): the world
named with its one-sentence story, each reference as image + steal note with the
dominant one marked, palette as real swatches with values, type candidates rendered in
the actual faces, and every registry callout verbatim. Open it for the human.

Iterate at the gate — swap references, re-run research — until approval. Every live
candidate advances together each round: never iterate one while the others sit, and
never build candidates on one shared skeleton — each candidate's structure comes from
its own Tier-1 references, and sameness across candidates is exploration's failure
state. Only the human kills a candidate. On approval (direction runs only):

1. Write the locked direction into the project's design notes: world, dominant
   reference, borrowed details, palette, type, and the human's rejections VERBATIM
   with the why — rejections are the registry's most valuable content.
2. Add or refresh the project's row in both registries.
3. If the project ships AI-generated imagery, also compile the locked direction into a
   generation shell — see [generation-shells.md](generation-shells.md).

Design work then proceeds from the locked direction. When it amends something already
shipped, hand off to `evolve` — deltas on the shipped screens, never a parallel
rebuild beside them.
