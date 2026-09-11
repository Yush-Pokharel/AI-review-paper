# PHASE 1 EXTRACTION — AGENT INSTRUCTION

Status: IN_PROGRESS (Started 2026-09-07)
Assigned agent role: DATASET / EXTRACTION AGENT (see `agents/instructions/agent_roles.md`)

## Task 1: Complete P001 (Base Paper) Extraction
File to read: `base_published_paper/main.tex`
File to update: `synthesis/extraction_table/template.md`

Actions:
1. Read `main.tex` carefully. Extract: exact dataset sizes (image counts for each of the 4 datasets), augmentation types, model architectures (detection models used besides DeepLab), backbone names, training hyperparameters if mentioned, exact metrics table, observation periods.
2. Fill ALL missing fields in the P001 row of `template.md`.
3. For `generalizationEvidence`: Confirm A (demonstrated). Note: The base paper does cross-river transfer (Bagmati→Bishnumati, Bishnumati→Bagmati) with quantitative results. This is A.
4. For `rqMapping`: Confirm RQ1, RQ2, RQ3, RQ4, RQ5.
5. For `datasetPublic`: Check `.tex` text — is dataset release mentioned? If not, mark No.
6. Append to `agent_log.md`: "[Date] P001 EXTRACTION [Agent] Completed P001 extraction; filled [X] fields; flagged [issues]."
7. If any contradictions or ambiguities are found in `.tex` (e.g., metric values that don't match abstract claims), add to `improvement_flags.md`.

## Task 2: Begin Backward Tracking — P002 (WIREs Review)
File to read: `base_reference_systematic_review_paper/WIREs Water - 2025 - Marye - Remote Sensing for Monitoring Macroplastics in Rivers  A Review.md`
File to update: `synthesis/extraction_table/template.md` (new rows for studies cited within P002 that meet criteria)

Actions:
1. Scan the `.md` file for studies mentioned with sufficient detail (platform, model, dataset, location, metrics).
2. For each cited study that appears to be an original study (not a review), create a new row in `template.md` with paperID P005, P006, etc.
3. If the cited study is only mentioned briefly without sufficient data, note it in a separate `synthesis/extraction_table/pending_extraction.md` list rather than creating an empty row.
4. For P002 itself: The pre-filled row exists. Confirm `generalizationEvidence`: D (no original data — it's a review). Confirm `rqMapping`: RQ1, RQ2, RQ6.
5. Append to `agent_log.md`.

## Task 3: Prepare P003 and P004 Tracking
Files: `search_strategy/search_protocol/proposed_seeds.md`
Action:
1. Confirm P003 = Jia et al. (2023), P004 = Jakovljevic et al. (2020).
2. Search `base_published_paper/references.bib` for their full citation details.
3. Note in `search_protocol/search_log.md` that seeds 3 and 4 are confirmed and their backward/forward tracking is pending.

## Task 4: Update `project_status.md`
Add: Phase 1 extraction started; P001 in progress; P002 backward tracking started; 4 seeds confirmed.

## Rules to Follow During Phase 1
- Read `generalization_evaluation_guide.md` before assigning A/B/C/D.
- Do NOT infer from abstract claims alone. If the paper only claims "robust" without cross-testing, classify as C.
- Every new paper gets a sequential ID (P005, P006, ...).
- If `main.tex` has ambiguous or missing information, mark `TBD` and explain in `notes`.
- Before finishing this phase message, update `agent_log.md`, `improvement_flags.md` (if any issues), and confirm `outline.md` status remains unchanged (writing sections not started yet — extraction comes first).

## Expected Deliverable
- `template.md` with P001 fully completed.
- `template.md` with at least 3 new rows from P002 citations (if available).
- `search_protocol/search_log.md` updated.
- `agent_log.md` updated.
- `improvement_flags.md` updated (only if issues found).
