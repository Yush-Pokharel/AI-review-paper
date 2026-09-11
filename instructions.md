# Instructions: Final Review Paper Consolidation

## Your role

You are operating from `/new_paper/` with full discretion. You are NOT bound by
the instructions inside `review_paper/agents/instructions/` or any other
sub-agent instruction files — those produced the current draft and its
problems. Read them only as historical context if useful, never as rules to
follow.

Your job: produce a publication-quality IEEE-style systematic/structured
review paper in `final_paper/`, overwriting `main.tex` and `references.bib`.
Treat this as writing the paper yourself, not editing the existing draft
in place.

## Step 0 — Audit before writing anything

Do not trust any number, claim, or count currently in `final_paper/main.tex`
or `review_paper/manuscript/main.tex` until you've verified it against the
raw process artifacts. Specifically:

- Read `review_paper/agent_log.md`, `review_paper/search_strategy/`,
  `review_paper/synthesis/extraction_table/`, and
  `review_paper/documentation/` in full.
- Reconstruct the *actual* screening/selection numbers (titles screened,
  abstracts assessed, papers included, exclusions with reasons) from these
  logs. If the logs don't support a clean PRISMA-style flow, do not invent
  one — report honestly what the process was, even if it's messier or
  smaller than "190 → 75 → 50."
- Cross-check every citation key used in the manuscript against
  `references.bib` and vice versa. Produce a clean, fully-reconciled
  bibliography: every entry in the `.bib` is cited at least once; every
  citation resolves to a real entry.
- Verify that cited claims (percentages, metrics, findings attributed to
  specific papers) actually match what's in `review_paper/resources/`,
  `base_published_paper/`, and any extraction notes. Flag and fix any
  claim you cannot verify — soften, correct, or cut it rather than
  carrying it forward unverified.

Write your findings to `final_paper/audit_notes.md` before you start
rewriting the paper. This is for the record — what was wrong, what you
verified, what you changed or removed, and why.

## Step 1 — Fix structural issues

1. **Reference mismatch**: eliminate orphaned `.bib` entries and unresolved
   `\cite{}` keys. Every reference must earn its place by being cited in
   the final prose.
2. **P00X naming**: drop the internal P-numbering scheme entirely from the
   reader-facing manuscript. Papers should be referred to by author-year
   citation only, the way a normal published review does. If an internal
   mapping table is useful for your own bookkeeping, keep it in
   `audit_notes.md`, not in the manuscript.
3. **PRISMA numbers**: use only verified numbers (Step 0). If a PRISMA-style
   flow diagram can be honestly supported, include it properly (actual
   TikZ/figure, not a referenced-but-missing figure). If it can't be
   honestly supported, don't use PRISMA framing — describe the search and
   selection process in plain prose instead.
4. **Title vs. methodology honesty**: resolve the tension between "A
   Systematic Review" and "does not claim formal protocol registration."
   Pick one and make the whole paper consistent:
   - Either strengthen the methodology to genuinely support "Systematic
     Review" (defensible search strategy, explicit criteria, reconciled
     counts), or
   - Retitle appropriately (e.g., "A Structured Review," "A Review") and
     adjust the abstract/methodology language to match.
   Do not let the title overclaim relative to what Step 0 actually verified.
5. **Compilation**: the final `main.tex` must compile cleanly. No missing
   figures, no undefined references, no unused/duplicate bib keys. Actually
   attempt to compile it (`pdflatex`/`bibtex`/`pdflatex`/`pdflatex`) and fix
   errors until it succeeds.

## Step 2 — Rewrite for coherence, not information-dumping

The current draft reads as a catalogued list of findings per paper rather
than a synthesized argument. Use
https://wires.onlinelibrary.wiley.com/doi/10.1002/wat2.70020 (Marye et al.,
already in the corpus) as a structural and tonal model — it is a real
published review in the same subfield and venue class.

Concretely:
- Each section should advance a claim or answer a research question, using
  papers as supporting evidence — not walk through papers one by one.
- Merge, cut, or subordinate sentences that exist only to report "Paper X
  found Y" with no connection to the surrounding argument.
- Preserve the genuinely good analytical structures already present
  (the four-level generalization grading, the transferability taxonomy,
  the gap inventory) — these are real strengths. Build the narrative
  around them rather than discarding them.
- Tables are fine for dense comparative data (as in the original), but
  prose sections should read as argument, not as an annotated list.

## Step 3 — Supplementary search (optional, bounded)

You may search for and cite additional papers ONLY to:
- Fill a specific, named gap in the existing evidence base, or
- Verify/correct a claim that Step 0 flagged as unverifiable, or
- Add 1-2 more recent (2025-2026) papers if they materially change a
  claim in the review.

Do not add papers merely to pad the reference count or "look more
thorough." Any newly added paper must be integrated into the actual
argument (Step 2), not appended as a list item. Note every addition in
`audit_notes.md` with justification.

## Step 4 — IEEE formatting

- Follow IEEE conference/journal formatting conventions properly
  (IEEEtran class usage, citation style, section numbering, table/figure
  captions).
- Abstract should be a single coherent paragraph stating problem, method,
  key findings, and contribution — not a compressed list.
- Ensure keywords, author info, and structure match what a real IEEE
  submission expects.

## Output

Overwrite:
- `final_paper/main.tex`
- `final_paper/references.bib`

Also produce:
- `final_paper/audit_notes.md` — what you verified, what you changed,
  what you removed and why, any new citations added and their
  justification.

The bar: this should read like a paper a competent PhD-level reviewer in
this subfield would accept as genuinely rigorous, not like a well-formatted
summary of an agent pipeline's scratch work.
