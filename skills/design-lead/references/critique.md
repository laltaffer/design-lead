# critique — evidence first, judgment labeled

A design review has two layers that must never blur. Blending them is how reviews
decay into vibes ("the colors could be more on-brand, some shadows feel heavy").

## Layer 1 — evidence

1. **Verify the target is the real page before measuring it.** A fetched URL can
   return a bot-challenge interstitial or an empty client-side shell — both PASS the
   detector meaninglessly. Sanity-check title and visible content; behind a
   challenge, use the project's local build or a rendered-DOM save instead, and say
   which artifact was measured.
2. Run the deterministic detector on the target (HTML file or directory):
   `npx -y @gessobuild/anti-slop check <target> --json`
3. Lead with the verdict line: **PASS** or **SLOP (severity N, M advisory)**.
4. One table row per finding: rule, hit count, the quoted occurrence, one line on why
   the pattern reads as generated. Report every finding that fired; invent none.
   Chase each quoted occurrence to its place in the page before repeating the
   detector's framing — a flagged number can turn out to be raw feed data leaking
   into visible copy (worse than the rule knew) or an implausible hit ("585 slots in
   one row") that is a parser artifact to report as such, not as fact.
5. Advisory-tier findings are genre calls — say whether the genre earns the pattern
   here (a numbered sequence on real process steps stays; on decorative sections it
   goes).
6. Add the registry check: reuse, family resemblance, AI-tells, model-tells, faces.
   Registry hits are evidence too — quote the registry row.

When the target isn't HTML (a screenshot, a native screen, a Figma frame), the
detector step is skipped and the review says so — the registry check still runs, and
"no detector coverage" is stated rather than papered over.

## Layer 2 — judgment, labeled as judgment

Open the section by saying these are opinions, not detector findings. At most five
observations, each anchored to something quotable on the surface, each answering one
question: **does this element do its job for this page's objective?** A business page
is a design for a business, not a piece of art — atmosphere that displaces content,
labels that tell the audience what it already knows, and imagery whose subject, age,
season, or setting contradicts the domain's reality are objective failures, not taste.

Close with the strongest single improvement you'd make, stated as a delta, and the
offer: any verdict worth keeping permanently → `encode` it.

## What a critique never does

A critique reports; it does not edit. If the human asks for the fixes, that's `evolve`
(shipped surface) or ordinary comp iteration (work in progress) — with the critique's
evidence table as the work list.
