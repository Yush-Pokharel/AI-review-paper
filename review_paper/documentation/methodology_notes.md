# METHODOLOGY DOCUMENTATION NOTES (For Agents & Human Review)

This file tracks what was decided about methodology so that all agents follow the same protocol.

## Confirmed Decisions (2026-09-07)
- **Review type**: Structured review with transparent methodology — NO formal PRISMA protocol claim.
- **Time range**: Early 2015 to early 2026 (a decade).
- **Databases**: Any renowned (suggest Scopus, Web of Science, IEEE Xplore, Google Scholar, ScienceDirect, arXiv only if cited by seeds).
- **Inclusion criteria**: Confirmed in `criteria_final.md`.
- **Conference papers**: Included.
- **Geographic scope**: Global, with Nepal papers (including user's base paper) emphasized.
- **Language**: English preferred; others only if accessible/translatable.

## Search Strategy Approach
- **Seed-based expansion**: Start with 2 confirmed seeds (P001, P002), add 3-5 proposed seeds.
- **Backward tracking**: Read reference lists of seeds; extract all studies that meet criteria.
- **Forward tracking**: Search citation indexes for papers citing seeds; include those meeting criteria.
- **Keyword supplement**: Execute refined keyword search to fill gaps (especially newer papers 2023-2026 that may not cite older seeds).

## Data Extraction Protocol
- Every included paper gets a row in `synthesis/extraction_table/template.md`.
- Fields: See `template.md`. Key fields for synthesis: `rqMapping`, `imageSource`, `model`, `pretrained`, `transferLearning`, `crossLocationTesting`, `mainLimitation`, `datasetPublic`.
- Agents must note `TBD` for missing fields and explain in `notes`.

## Taxonomy Use
- Agents tag each paper with taxonomy levels (`synthesis/taxonomy/taxonomy_framework.md`).
- Taxonomy tags are used for grouping papers by RQ and identifying gaps.

## Synthesis Phase (After Extraction)
- Once ≥15 papers are extracted, begin contradiction tracking (`synthesis/contradictions/`).
- Once ≥20 papers, begin gap analysis (`synthesis/gaps/`).
- Only after synthesis is substantially complete should section writing (`sections/`) begin — this ensures the review is evidence-based, not outline-driven.

## Quality / Bias Notes
- Since this is not a meta-analysis (no effect size pooling), quality assessment is descriptive.
- Note limitations of included studies in `mainLimitation` field.
- Note missing data (e.g., dataset not public, no cross-environment testing) as implicit gaps.
