# PROJECT STATUS (Updated 2026-09-07 — Human Confirmed Updates)

## What's Confirmed
- Scope: Rivers/ponds (Nepal context, freshwater focus).
- Base paper: `base_published_paper/main.tex` + `references.bib` — comparative experimental study (Pati et al., UAV + DL for river waste).
- Reference review: `base_reference_systematic_review_paper/` (WIREs Water 2025, Marye et al.) — systematic review on remote sensing for macroplastics in rivers.
- No PRISMA claim: Confirmed.
- Iterative process: Confirmed.
- Agent roles, handoff protocol, pushback system: All in place.

## What's Updated Today
- `direction.md`: Added base paper details, reference review details, updated title draft, no PRISMA clarification, agent rules updated.
- `scope.md`: Resolved scope (rivers/ponds, Nepal); remaining open questions (time range, databases, peer-reviewed vs. conference, geographic scope) clearly listed.
- `base_published_paper/README.md`: Detailed paper info for agents.
- `base_reference_systematic_review_paper/notes_for_agents.md`: Extracted notes and gap analysis.
- `improvement_flags.md`: Resolved flags marked; new active flags listed (time range, databases, architecture comparison requirements, etc.).
- `agent_log.md`: Updated with all changes.
- `methodology/instructions.md`: Explicit no-PRISMA-claim language added.
- `data_sources/instructions.md`: Updated to emphasize expansion beyond UAV-only base paper.
- `outline.md`: Unchanged but references updated files.

## What Remains for Human to Confirm Before Agents Start Writing
1. Study time range (suggest 2015-2026).
2. Databases for search (suggest Scopus, WoS, IEEE Xplore, Google Scholar).
3. Include conference papers? (Suggest yes for DL papers.)
4. Geographic scope for included studies (suggest global with Nepal context emphasized).
5. Title confirmation: "Deep Learning for Automated Waste Detection in Rivers and Ponds: A Structured Review with Focus on UAV-Based Approaches and Nepal Context" — or adjust?

## Phase 1 Extraction Update (2026-09-08)
- P001 fully extracted from main.tex full text (A: cross-river transfer; datasetPublic corrected to Yes via GitHub).
- P002 confirmed D (review); backward tracking yielded P005 Wolf 2020, P006 Maharjan 2022, P007 van Lieshout 2020, P008 Jia-Frontiers 2023 (provisional, full text pending) + P003/P004 citation rows; pending_extraction.md created.
- search_log.md, agent_log.md, improvement_flags.md updated. outline.md unchanged — no section writing (extraction only).

## Phase 2 Extraction Update (2026-09-08) — Sequential A→B→C complete
- Task A: P003 Jia 2023 review confirmed (B; RQ1/RQ2/RQ6).
- Task B: P004 Jakovljevic 2020 confirmed original study (A with Table-5 caveat; RQ1/RQ2/RQ4/RQ5; Bosnia: Balkana + Crna Rijeka/Vrbas).
- Task C: P005–P008 criteria PASS at summary level; Simpson 2022 excluded; next-batch priority set (Solé Gómez, Lin, Tasseron, Tharani).
- Zhao 2024 plan confirmed in synthesis/context_references/context_notes.md (JHM 477:135329, context-only).
- outline.md unchanged — no section writing.

## Expanded Collection Update (2026-09-08) — P009–P012 complete (12 papers total)
- P009 Solé Gómez 2022 A (satellite cross-region); P010 Lin 2021 C (claim-only robustness); P011 Tasseron 2022 A (lab→field hyperspectral, open data); P012 Tharani 2021 A (cross-site canal).
- C006 added (satellite cross-region vs UAV same-basin trade-off). Backward P003/P004: no new in-scope beyond pending list. 50-paper threshold: 12/50 — writing still blocked.
- outline.md UNCHANGED — no section writing.

## Automatic Expansion Update (2026-09-08) — 20/50 included
- Batch 1 (base .bib DL): P013 A, P014 B, P015 D, P016 C, P017 B (first IS/YOLOv8/open-weights row).
- Batch 2 (WIREs spectral/ML): P018 A-8C, P019 A (generalization DROP), P020 B, P021 B, P022 D.
- Excluded: Geraeds 2019, Schreyers 2021 (manual-only). C007 added (satellite ML-drop vs DL-hold).
- Next: Sio 2022, Putra 2021, Panwar 2020, marine-verify queue (Fulton/Kylili/Garcia-Garin/Kako/Mifdal/Deng), land-verify queue (Cordova/Patel/Kumar), Nunkhaw 2025 + Pan 2023 candidate rows.
- Next: forward tracking; full DB keyword pass (awaiting confirmations); PDF verification bundle.
- outline.md UNCHANGED — writing blocked (30/50).

## Automatic Expansion Update (2026-09-08) — 30/50 included
- Batch 4: P026 A (AIGC synthetic→real), P027 A (7-river IS + WLGCAM), P028 D, P029 D, P030 D, P031 B (counting collapse), P032 B (3-river networked system).
- Backfill: P001–P012 titles/journals in Documentation Addendum. No spec changes in automatic_expansion.md.
- outline.md UNCHANGED — writing blocked (34/50).

## Automatic Expansion Update (2026-09-08) — 34/50 included
- Batch 5: P033 D, P034 A (cross-country + dark-channel RQ4), P035 D (semi-supervised first), P036 A-prov (3-country satellite).
- Upgrades/fixes: P006→A (Laos↔Thailand); P001 = IEEE Access 2025 (doi ...3576295).
- 16 to go: full DB keyword pass (awaiting confirmations), forward tracking, PDF bundle.
- Batch 6 (2026-09-08): 38/50 — P037/P038 SSL A-rows, P039/P040 D-rows, P008→B. 12 to go.
- Batch 7 (2026-09-08): 41/50 — P041 D-prov, P042 B (hyacinth flagship), P043 D (Yellow River). 9 to go: Tomas22, Li23-DaiLake, Haris23-Rasau, Li22-JCleanPro leads + forward tracking + PDF bundle.
- Batch 8 (2026-09-08): 47/50 — P044 D-prov, P045 A (scoped), P046/P047 D-prov, P048 D (FloW benchmark), P049 B-prov. P007→A. 3 to go: Li23-DaiLake, Li22-JCleanPro, Renfei-UDA/multicam companions (or verified substitutes).
- Batch 9 FINAL (2026-09-08): 50/50 THRESHOLD REACHED — P050 D-prov, P051/P052 B-prov, P005→B. Verification pass complete (counts/grades/contradictions/consistency). outline.md UNCHANGED. Awaiting human authorization to begin section writing + PDF verification bundle.
- Connected batch 10 (2026-09-08): 51/50 (cap-exception) — P053 Balsi25 B-prov. Garaba23/Alboody23 → context queue. Context batch next (Gnann22, Olyaei24, Tasseron24-hotspots, field-transport set).
- Context batch DONE (2026-09-08): 11 context entries written. Collection phase closed: 51 primary + 2 seed reviews + ~23 context refs. outline.md UNCHANGED — awaiting writing authorization.
- PDF bundle DONE (2026-09-08): 7 resolved, 5 residual (need PDF downloads). Grades now A19/B15/C2/D16 (P036→A). outline.md UNCHANGED.
- User-PDF reconciliation DONE (2026-09-08): P004→unqualified A; P009 enriched; P012 corrected (version conflict flagged); P010 resolved; P051→A; P053 reversed to context. 50/50 restored, grades A20/B13/C2/D15. outline.md UNCHANGED — ready for writing authorization.
- MANUSCRIPT ASSEMBLED (2026-09-08): manuscript/main.tex + references verified + figures wired. Needs human compile (no local toolchain).
- ALL CYCLES COMPLETE (2026-09-08): 12/12 sections drafted (notes + .tex) + references.bib + prisma diagram. All statuses DRAFT WRITTEN. Awaiting human end-review.

## Next Step (When Human Confirms Above)
Agent can begin drafting `sections/introduction/` and `sections/abstract/` (abstract written last, but introduction can start with the river pollution story, Nepal context, base paper reference, and WIREs review framing).

## Pushback Reminders (Active)
- Agents must always check `improvement_flags.md` before finishing a section.
- Agents must not invent data for underwater cameras or geographic diversity gaps.
- Agents must reference the base paper's key results (training strategies, transfer learning, DeepLabv3+ performance) in relevant sections.
- Agents must reference the WIREs review as state-of-the-art but identify where this review goes further (underwater cameras, deeper architecture comparison, Nepal-specific context, training strategy synthesis).
