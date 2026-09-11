# AUTOMATIC COLLECTION EXPANSION — Agent Prompt

Status: ACTIVE (Sequential from Phase 1/2/Batch P009-P012)
Trigger: User confirmed "automatic collection expansion"
Threshold: 50 papers before writing (`outline.md` untouched)
Criteria: `resources/inclusion_criteria/criteria_final.md` (2015-2026; aquatic + CV/DL + experiment; peer-reviewed/conference; exclude manual-only, non-CV, out-of-range, pure opinion/review unless providing unique data)

## Sources (Priority Order)
1. **Backward citation tracking**: Read reference lists of P001 (`references.bib`), P003 (`references.bib`), P004 (`references.bib`). Extract studies meeting criteria. Log in `search_protocol/search_log.md`.
2. **Forward citation tracking**: Search Google Scholar / Scopus for papers citing P001, P003, P004, P009, P011. Note which meet criteria.
3. **WIRE review (`base_reference_systematic_review_paper/`)**: Extract studies from `.md` reference list not yet added (pending_extraction.md list: Geraeds 2019, Schreyers 2021, Cortesi 2022, Mohsen 2023, Sakti 2023, Iordache 2022, Pan 2022, Yang/Zailan/Nunkhaw 2024, Gómez/Shijun 2024, etc.). For each, apply criteria_final.md. If included, create new row (`P013+`). If excluded (e.g., Simpson 2022 SAR-only; no DL), note exclusion with reason.
4. **Open access databases**: Scopus, Web of Science, IEEE Xplore, Google Scholar, MDPI (Remote Sensing, Entropy, Water, etc.), WIREs Water (Wiley), ScienceDirect, arXiv (ONLY if study is original DL + aquatic waste and within time range — treat with extra scrutiny; note source clearly).
5. **Cross-reference existing seeds**: Any study cited in P001, P002, P003, P004 that meets criteria should be added regardless of database source.

## Documentation Sufficiency (Addressing User Concern)
Yes — any agent can find papers unambiguously. Each row includes:
- `paperID` (unique: P013, P014...)
- Full `authors`
- `year`
- Full `title` (from paper or citation)
- `journal` / `source` (from citation or `.bib` file)
- `notes` with full citation details if ambiguous
- `rqMapping` linking to research questions
Agents are instructed: if paper identity is unclear, check `.bib` file (`base_published_paper/references.bib`) or search the `paperID` + author in `search_log.md`. No paper should be unfindable.

## Workflow (Automatic — No Human Approval Per Paper)
For EACH paper found:
1. Check `criteria_final.md`.
2. If included: create new row in `template.md`. Fill all available fields. Use `TBD` for unknown fields. Add to `notes`.
3. Apply `taxonomy/taxonomy_framework.md` (Level 1-10 tags; mandatory `rqMapping` and `generalizationEvidence`).
4. Apply `generalization_evaluation_guide.md` (A/B/C/D — never infer; quote paper's actual experiment description).
5. If excluded: add to `pending_extraction.md` with exclusion reason (e.g., "Simpson 2022 — SAR only, no DL component; criteria #3/#4 fail").
6. Update `search_protocol/search_log.md` with search query, database, results count, included/excluded.
7. Update `agent_log.md` (batch updates sufficient; no per-paper log required unless contradiction found).
8. Add contradictions to `synthesis/contradictions/contradiction_tracker.md` if paper claims differ from P001 (e.g., training strategy, architecture performance, generalization evidence).

## Quality Control Rules (From Previous Flags)
- Do NOT inflate provisional grades to A. Only papers with explicit external test + separate metrics = A.
- Do NOT invent dataset sizes, metrics, or augmentation details. Mark `TBD`.
- P003 vs P008 distinction maintained (different journals: Water Research vs Frontiers in Water).
- P004 caveat preserved (Table 5 verification required for unqualified A claim).
- All papers include `generalizationType` taxonomy tags (8A-8G).
- Writing blocked (`outline.md` untouched) until 50 papers.

## Target
Continue until `template.md` contains ≥50 included papers (P001 to P050+). Report progress every ~5 papers or when significant contradiction/gap discovered.
