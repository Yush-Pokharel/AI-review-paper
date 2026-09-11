# Instructions: Deep Verification & Comparative Tables (Pass 2)

## Context

`final_paper/main.tex` and `references.bib` were already rewritten once and
compiled cleanly (see `final_paper/audit_notes.md` from that run). That pass
fixed structural problems: citation reconciliation, P00X naming removal, the
PRISMA figure, title/methodology honesty, and IEEE formatting. It verified
manuscript claims *against this project's own extraction records*
(`review_paper/synthesis/`, `review_paper/base_published_paper/`).

It did NOT verify:
- whether the screening/selection counts it reconstructed are actually
  matched by real completed extraction work (as opposed to being a plausible
  number in a log), or
- whether the extraction records themselves are accurate — i.e., whether the
  cited papers actually say what this project claims they say.

This pass does both, then upgrades the paper's structure using a real
published review as a model. You have full discretion, as before — read
`review_paper/agents/instructions/` only as historical context, never as
rules to follow. Read `final_paper/audit_notes.md` first so you don't
re-litigate what Pass 1 already resolved.

## Part 1 — Verify the review's own process claims

The manuscript currently states: ~190 titles screened, ~75 assessed, 50
primary studies included, ~25 exclusions with reasons, and an evidence grade
of 20 A / 13 B / 2 C / 15 D (four-level generalization scale).

Check these against what actually exists in the repo, not just what the logs
say happened:

1. Count the actual number of studies with a completed extraction record in
   `review_paper/synthesis/extraction_table/` (and any per-paper extraction
   files elsewhere in `review_paper/`). Does it come to 50? If it's short,
   list exactly which claimed studies have no real extraction record behind
   them.
2. Count the actual number of documented exclusions with stated reasons
   (search logs, `pending_extraction.md`, contradiction/flag files). Does it
   come to ~25?
3. Check whether the 20/13/2/15 evidence-grade split can be reconstructed by
   actually tallying grades recorded per study, not just cited as a round
   summary number.
4. If a number checks out (matches real underlying records), leave it. If a
   number is asserted but not actually backed by that many real records,
   correct it downward to what's actually documented, and soften the
   PRISMA-style framing accordingly — do not preserve a precise-looking
   number that isn't earned. This may mean the PRISMA-style diagram from
   Pass 1 needs its numbers revised, or needs to be dropped in favor of
   plainer prose if the undercount is severe enough that a flow diagram
   would overstate rigor.

Record findings in a new file, `final_paper/verification_notes.md` (see
Output section) — do not overwrite `audit_notes.md`, which documents Pass 1.

## Part 2 — Verify extracted claims against the actual cited papers

This is the core new work. For every specific, load-bearing quantitative or
methodological claim in `main.tex` that is attributed to a cited paper
(percentages, mAP/IoU/F1 figures, dataset sizes, named findings like "frozen
backbones win for detection"), check it against the actual source — not
against this project's own extraction table, which is what Pass 1 already
did.

**How to get the source:**
- Use the DOI in `references.bib` to fetch the actual paper (web search /
  web fetch) wherever possible.
- `review_paper/base_published_paper/` and
  `review_paper/base_reference_systematic_review_paper/` already contain
  full text for the two seed papers (Pati2025, Marye2025) — use those
  directly rather than re-fetching.
- If a paper is genuinely paywalled and unreachable, say so explicitly in
  your notes rather than silently skipping it or verifying against a
  secondary source and calling it primary verification.

**Prioritize by evidential weight, not paper count.** With 50+ studies, do
not attempt uniform shallow coverage. Prioritize:
1. Every number that appears in the abstract or conclusion (these carry the
   review's headline claims).
2. Every number singled out as surprising, extreme, or gap-defining (e.g.
   "6 of 32 items," "0.02 IoU," "only half of transported litter floats
   within camera view") — these are the claims a critical reader is most
   likely to spot-check, and the ones most damaging if wrong.
3. Numbers reused in more than one section (higher blast radius if wrong).
4. A representative sample of the remainder — enough that you can honestly
   report a coverage rate (e.g., "38 of 50 primary studies had at least one
   claim spot-checked against source").

**For each claim checked, classify it as:**
- **Confirmed** — source says this, no material difference.
- **Confirmed with nuance** — source supports it but the manuscript's
  phrasing overstates, understates, or drops a caveat the source includes.
  Fix the manuscript wording.
- **Not found / cannot verify** — the specific number or claim doesn't
  appear in the source as stated. Do not delete the citation reflexively;
  first check whether it's in a table, supplementary material, or was
  paraphrased from a differently-stated original figure. If it genuinely
  isn't supported, soften or remove the specific claim rather than the
  citation itself (the paper may still be relevantly cited for other
  content).
- **Contradicted** — the source states something different from, or
  inconsistent with, what the manuscript claims. Correct the manuscript.
  Flag prominently in your notes — this is the most serious finding.

Log every check in `final_paper/verification_notes.md`, including checks
that confirmed the claim (a clean bill of health is worth recording, not
just the problems).

## Part 3 — Comparative tables in the style of Marye et al. (2025)

Once Parts 1–2 are done and the manuscript's factual base is solid, restructure
the paper's evidence presentation using
https://wires.onlinelibrary.wiley.com/doi/10.1002/wat2.70020 as the direct
model. That paper is already cited in this manuscript (Marye2025) — this is
not introducing a new source, it's adopting its presentation approach.

Fetch and examine that paper's actual tables (Table 1: platform, sensor,
altitude, spatial resolution, spectral range, preprocessing, area of interest,
targeted plastic class, detection method, accuracy; Table 2: fixed/handheld
camera studies; Table 3: indices used in detection; and any others it uses)
to understand the real column structure before designing this paper's
equivalent — don't approximate from memory of the earlier conversation.

Design and build equivalent structured comparison tables for this review's
own corpus, replacing or supplementing the current three tables
(`tab:platforms`, `tab:archs`, `tab:datasets`) where a per-study comparison
table would genuinely convey more than the current platform/architecture-family
rollups. Likely candidates, adapt to what the actual corpus supports:
- A master per-study table: platform, sensor/spectral range, resolution,
  area/river, target class, detection/segmentation method, and the
  accuracy metric actually reported — one row per primary study (or a
  sensible subset if 50 rows is unwieldy for print; consider splitting by
  platform the way Marye et al. split UAV/satellite from fixed/handheld).
- A generalization/transfer-specific table, since that's this review's
  actual contribution beyond Marye et al. — e.g., source environment,
  target environment, transfer type (per the existing eight-class taxonomy),
  and the demonstrated vs. claimed grade (A/B/C/D) per study. This has no
  equivalent in Marye et al. and would be a genuine structural improvement
  specific to this review's angle.

Every cell in every new table must trace to a claim already verified in
Part 2, or be freshly verified against source before being added. Do not
populate a table with a number that hasn't been checked — a wrong number in
a structured table is more visible and more damaging than the same number
buried in prose.

Keep the argument-driven prose from Pass 1 — these tables supplement the
narrative sections, they don't replace them with a catalogue. Follow the
IEEE `table*` two-column convention already established.

## Output

- Update `final_paper/main.tex` and `final_paper/references.bib` in place
  with all corrections and new/revised tables. Actually compile
  (`pdflatex`/`bibtex`/`pdflatex`/`pdflatex`) and confirm it still succeeds
  before finishing.
- Write `final_paper/verification_notes.md`: Part 1 findings (process-count
  reconciliation), Part 2 findings (per-claim verification log — confirmed /
  nuanced / unverifiable / contradicted, with source citation for each
  check), and a short Part 3 summary of what changed structurally and why.
- Do not overwrite `final_paper/audit_notes.md` — it is Pass 1's record.
  `verification_notes.md` is a separate, additive record for this pass.
- If Part 2 turns up a contradiction serious enough to change one of the
  review's headline conclusions (not just a single sentence), stop and flag
  it clearly at the top of `verification_notes.md` rather than quietly
  patching it — that's a judgment call for the user, not something to
  resolve unilaterally.