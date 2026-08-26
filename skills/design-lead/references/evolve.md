# evolve — improve a shipped surface without breaking it

The highest-frequency real job in a living portfolio: a surface that already works
needs to get better. The failure mode this mode exists to prevent is the **parallel
rebuild** — a fresh layout built beside the shipped one, which reads to its owner as
"far too many new things… measurably worse than what we already have." Evolution is
DELTAS applied to the shipped screens.

## 1. Audit before touching

Screenshot the live surface first — desktop AND ≈390px — and document:

- **Brand tokens:** colors, type stack, radii, signature treatments. These are the
  incumbent's identity; a locked direction in the project's notes makes them
  non-negotiable without the human's explicit call.
- **IA and conversion paths:** page tree, nav labels, slugs, form fields, analytics
  hooks. None of these change silently — renames break SEO, muscle memory, autofill,
  and tracking.
- **Patterns to preserve:** the signature moves, the recognizable hero, the copy voice.
- **Patterns to retire:** run the lint gate and the registry check on the LIVE surface;
  its hits are the work list.
- **The concrete problem** the human named, in one sentence. No problem stated → ask
  for one; "make it better" is not auditable.

## 2. Levers, in priority order

Apply the cheapest lever that solves the stated problem, then stop:

1. Spacing and rhythm.
2. Color recalibration within the incumbent palette.
3. Motion layer (only motion you can verify; motion you cannot ship verified gets
   dropped, not half-built).
4. Recomposition of the failing section — structure changes, identity stays.
5. Full block replacement — only when a block is unsalvageable, and stated as such.

Typography and palette replacement are not evolution levers; wanting them means the
direction itself is in question → route to `direction` with the human's consent.

## 3. Comp, gate, land

Build the deltas as a comp in scratch space against a copy of the live surface. Run
the SKILL.md check and the lint gate; annotate deliberate keeps (`data-slop-allow`)
where a flagged pattern is real identity — a numbered list whose order encodes an
actual sequence keeps its numbers; one whose order encodes nothing loses them to a
stronger anchor (replace, never delete).

Show the comp at both breakpoints with the evidence-first format (see
[critique.md](critique.md)): detector before/after on live vs comp, then your labeled
judgment of what each delta buys.

On approval: apply the deltas to the live files exactly as comped, re-run the lint
gate on every touched page, QA both breakpoints again on the real files, and record
in the project's notes what changed, why, and the approval. Content edits that carry
business meaning (claims, prices, names) land only with explicit sign-off, and
anything wired to a backend (form values, field names, endpoints) is verified
untouched or intentionally versioned — a cleaned-up label with a preserved submitted
value beats a broken whitelist.

Ship only on the user's word; deploying is theirs to trigger unless they've said
otherwise.
