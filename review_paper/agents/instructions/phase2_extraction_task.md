# PHASE 2 EXTRACTION — Option A (P003 + P004 Full Text) then Option B (P005–P008)

Status: IN_PROGRESS
Assigned: EXTRACTION AGENT (same agent as Phase 1, sequential handoff permitted)

## Task A: Confirm P003 (Jia 2023) — Full Text
- Source: `base_published_paper/references.bib` key `Jia2023DeepLF`; journal Water Research 231 (2023) 119632.
- Read full text (or abstract + method + results if full text inaccessible). Update `template.md` row P003: fill `country`, `waterBody`, `datasetSize`, `model`, `pretrained`, `transferLearning`, `performanceMetrics`, `crossLocationTesting`, `mainLimitation`, `generalizationEvidence` (likely D or B — it's a review, but check if it reports original cross-testing).
- Apply taxonomy levels (`taxonomy_framework.md`).
- Confirm `rqMapping`: likely RQ2 (DL approaches review), RQ6 (gaps), RQ1 (datasets/platforms if summarized).
- Note: This is a REVIEW (not primary experiment). `sourceType` = Review. Do NOT inflate `generalizationEvidence` to A unless original cross-testing data is reported.

## Task B: Confirm P004 (Jakovljevic 2020) — Full Text
- Source: `references.bib` key `Jakovljevic2020ADL`; Remote Sensing 12 (2020) 1515.
- Read full text. Fill `template.md` P004: country (likely Serbia? check text), waterBody (river/reservoir — check exact name), dataset size, model architecture, metrics, whether cross-testing performed.
- Apply `generalization_evaluation_guide.md`: likely A or D depending on whether cross-river/cross-dataset testing exists.
- Note: Original study (UAV + DL for plastic mapping). Likely `rqMapping` includes RQ1, RQ2, RQ4, RQ5.

## Task C (After A + B Complete): Option B — P005–P008 Provisional
- Read `pending_extraction.md`. For each paper listed:
  1. Check if full text is available (search engine or database access).
  2. Apply `criteria_final.md` (include only if DL/CV + aquatic + experiment + 2015-2026).
  3. If included: create new row in `template.md` (P009, P010, etc.), apply taxonomy, set `generalizationEvidence` strictly (no inference from claims alone).
  4. If excluded (e.g., Simpson 2022 SAR only — likely exclude per criteria): note exclusion reason in `pending_extraction.md`.
  5. Do NOT inflate provisional grades. Leave as TBD until full text read.

## Incorporating Zhao et al. 2024 (and Similar Context Papers)
- Papers like Zhao 2024 (cited in P002 `.md`: "freshwater plastic pollution has increased in recent years; however, much of the scientific focus remains on microplastics") are CONTEXT / BACKGROUND references.
- They are NOT primary data papers for the extraction table (unless they contain original DL + aquatic waste experiments — check first).
- Plan for incorporation:
  - **When**: During synthesis / writing phase, specifically for `introduction/` (trend framing) and `challenges_future/` (gap justification).
  - **How**: Cite as evidence for RQ6 gap claims (e.g., "Research on freshwater plastic pollution has increased, yet much scientific focus remains on microplastics [Zhao et al., 2024], leaving macroplastic river monitoring underexplored").
  - **Where**: Add a `context_references/` folder (create if needed) or note in `extraction_table/template.md` `notes` field for P002 that Zhao 2024 supports the geographic/temporal gap claim.
  - **Do NOT** add Zhao 2024 as P003/P004 replacement; it serves a different purpose (background trend vs. seed method comparison).

## Rules
- Sequential: Finish A, then B, then C.
- Update `agent_log.md` after each sub-task (A, B, C).
- Update `project_status.md` only after all 3 complete.
- Read `improvement_flags.md` before finishing; add any new contradictions found in P003/P004 full texts.
- If full text of P003 or P004 is inaccessible, note access limitation in `notes` and proceed with abstract-level data only (do not invent details).
