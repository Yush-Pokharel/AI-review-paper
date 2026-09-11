# EXPANDED COLLECTION PROMPT — P009–P012 + Backward/Forward Tracking

Hand off from previous agent. Read all previous outputs first.

## Pre-Read Checklist (Mandatory Before Starting)
- `agents/instructions/phase2_extraction_task.md`
- `synthesis/extraction_table/template.md` (check P001–P008 entries; note P004 caveat at line 171; note P003 vs P008 distinction at line 139/203)
- `generalization_evaluation_guide.md` (A/B/C/D — no claim inference)
- `taxonomy/taxonomy_framework.md` (Level 8: 8A–8G; apply to ALL new papers)
- `improvement_flags.md` (Phase 1 + Phase 2 flags; do not ignore)
- `pending_extraction.md` (batch list; note exclusions: Simpson 2022 SAR excluded)
- `synthesis/contradictions/contradiction_tracker.md` (C004/C005 preserved; add new contradictions if found)
- `synthesis/gaps/gap_analysis_framework.md` (actual evidence from P001/P002; confirm before inventing new gaps)
- `synthesis/context_references/context_notes.md` (Zhao 2024 resolved; do not conflate)

## Tweaks Based on Previous Agent Outputs (DO NOT IGNORE)
1. **P004 Caveat (line 171)**: Evidence A ONLY if full-text Table 5 verifies independent held-out test. If full text unavailable, downgrade to B (indirect: separate model on Dataset3, not cross-environment). Never claim unqualified A without verification.
2. **P003 vs P008 (lines 139/203)**: P003 = Jia 2023 Water Research (review). P008 = Jia 2023 Frontiers in Water (open dataset). Never cite as "Jia 2023" alone — disambiguate by journal.
3. **Provisional Grades**: P005–P008 remain TBD or B/C/D. Do NOT promote any to A without full-text external test evidence. If uncertain, leave TBD and explain in `notes`.
4. **Contradictions**: If new papers contradict P001 findings (e.g., full fine-tuning better than frozen for detection; transformers outperform CNNs with same dataset size), add to `contradiction_tracker.md` with full citation + resolution attempt.
5. **Generalization Classification**: Apply `generalization_evaluation_guide.md` strictly. Most papers will be D (no cross-testing) or B (indirect: augmentation, combined dataset). Only papers with explicit different-environment test + separate metrics = A.
6. **Taxonomy Tags**: Every new row must include `generalizationType` (8A–8G) and `rqMapping`. Do not skip.
7. **No Writing**: `outline.md` remains untouched. `project_status.md` notes 50-paper threshold. Writing blocked.

## Task: Expanded Batch P009–P012 (Priority Order)
1. **P009 — Solé Gómez et al. 2022** (`pending_extraction.md` line 6): Sentinel-2 + U-Net/U-Net3DE/DeepLabV3+; IoU ~0.5; Yangtze generalization drop noted. Check full text: is cross-environment (Yangtze) experimentally demonstrated with separate metrics? Classify A/B/C/D accordingly.
2. **P010 — Lin et al. 2021** (`pending_extraction.md` line 10): YOLOv5s + FMA attention; mAP 79.41% waterway floating plastics. Check: dataset public? Cross-testing? Generalization type?
3. **P011 — Tasseron et al. 2021/2022** (`pending_extraction.md` line 12): Lab + Waal River hyperspectral; SVM/SAM/SID. Check: cross-setting (lab→field) = A candidate; confirm metrics and separation.
4. **P012 — Tharani et al. 2021** (`pending_extraction.md` line 14): YOLOv3 + log-attention; AP 48.1% easy set; urban water-channel trash. Check if river/pond context applies (urban water-channel may be closely related freshwater per criteria_final).

After P009–P012, continue with remaining pending list (Geraeds 2019 — verify DL component; Schreyers 2021; Cortesi 2022 — borderline ML; Mohsen 2023; Sakti 2023; Iordache 2022; Pan 2022; Yang/Zailan/Nunkhaw 2022/2024; Gómez/Shijun 2022/2024).

Also: execute backward citation tracking from P003 (`base_published_paper/references.bib`) and P004 (check `.bib` key `Jakovljevic2020ADL` references) to discover additional papers not in WIREs review. Log in `search_protocol/search_log.md`.

## Deliverable Before Next Human Check
- `template.md`: P009–P012 rows filled (minimum `rqMapping`, `generalizationEvidence`, `notes`, `included`); provisional rows updated.
- `pending_extraction.md`: Updated with exclusions confirmed (Simpson 2022 excluded? Others included/excluded with reason).
- `contradiction_tracker.md`: Any new contradictions found (e.g., if P011 lab→field transfer contradicts P001 UAV-only limitation).
- `agent_log.md`: Updated with sequential A→B→C→expanded batch.
- `improvement_flags.md`: Any new flags from full-text verification (e.g., P004 Table-5 verification result; P009 cross-environment evidence confirmed/rejected).
- `outline.md`: STILL UNCHANGED. No section writing.

Confirm with one message when batch complete or if full text access blocked.