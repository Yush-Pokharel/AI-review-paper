# VERIFICATION PROTOCOL — P001–P032 (30 Papers)

Status: ACTIVE — Stop at 30 for verification before DB expansion to 50.

## Verification Rules (Strict)
1. **Retrieve/inspect primary paper** for each P001–P032 (full text, PDF, XML, or abstract + methods if full text unavailable).
2. **Compare `template.md` row** against paper content. Update ONLY fields confirmed by paper text (e.g., metrics, dataset size, cross-testing evidence, generalizationEvidence A/B/C/D).
3. **If evidence ambiguous / contradictory** (e.g., P025 A verification pending; P031 B counting vs detection gap; P004 Table-5 separation): DO NOT change grade or claim. Add/update `contradiction_tracker.md` or `improvement_flags.md`. Preserve ambiguity — do not resolve by assumption.
4. **Update `template.md`** only with paper-supported corrections (e.g., datasetPublic confirmed Yes/No; metric values corrected; generalizationEvidence confirmed/revised).
5. **Do NOT invent details** to fill `TBD` fields. If full text unavailable, mark in `notes`: "Full text unavailable; field TBD — requires access before final synthesis."
6. **Taxonomy tags (`taxonomy_framework.md`)**: Confirm or correct `generalizationType` (8A–8G) based on actual paper evidence, not summary claims.

## Batch Verification Order (Suggested)
- Batch A (P001–P012): Confirm base papers + seeds. Priority: P001 (full `.tex` verified), P002 (review — no primary data), P003 (Jia 2023 — review), P004 (Jakovljevic 2020 — Table-5 verification).
- Batch B (P009–P012): Expanded batch. Confirm P009 cross-region metrics, P011 dataset availability, P012 cross-site protocol.
- Batch C (P013–P022): Batch 1 + 2 papers. Confirm P019 separate metrics (A claim), P025 (A verification — lab→field separate metrics?), P031 (B — detection vs counting gap documented in C008).
- Batch D (P023–P032): New papers. Confirm grades, dataset details, missing fields.

## System Review / Bloat Check (Parallel)
Identify and fix:
- Duplicate files (e.g., `.pdf:Zone.Identifier` system files — safe to ignore, but confirm not needed)
- Unused templates (`prisma_diagram/template.md` — used? Keep for reference; no PRISMA claim)
- Outdated notes (`scope.md` time range / database questions — resolved; `direction.md` title confirmed; any leftover unresolved flags?)
- Redundant sections in instructions (check `agents/instructions/` for duplicates)
- Unused folders (`search_strategy/search_protocol/proposed_seeds.md` — seeds confirmed, file can be archived; `base_reference_systematic_review_paper/extracted_notes/` — empty? Check)

## After Verification Complete
- Confirm count still 30 (+ any new papers found during verification, minus any exclusions corrected).
- Confirm `outline.md` still untouched.
- Confirm `improvement_flags.md` updated with any new contradictions or unresolved evidence.
- Confirm `agent_log.md` has verification checkpoint.
- Then proceed: DB keyword search (`Scopus/WoS/IEEE/MDPI/open-access`) + forward citation tracking (`P001`–`P032`) to expand from 30 → 50.
