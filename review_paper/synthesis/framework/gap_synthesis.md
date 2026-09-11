# GAP SYNTHESIS FRAMEWORK (Evidence-Based)

Purpose: Organize gaps identified in `synthesis/gaps/gap_analysis_framework.md` with actual evidence from `extraction_table/template.md`, `contradiction_tracker.md`, and `taxonomy/framework.md`. This is NOT speculative gap listing — it is evidence-based synthesis.

## Gap Summary (Based on Actual Evidence, Not Assumptions)

### 1. Data & Dataset Availability Gap (Evidence: P001, P011, P032)
- Evidence: P001 dataset public (Yes) but small (764 tiles, 2 rivers); P011 open dataset (Yes, hyperspectral); P032 dataset status unclear; most other papers (`P003` review, `P004` original) have private/unreleased datasets. Only ~3 out of 30 papers have public datasets.
- Taxonomy evidence: Level 10 (`datasetPublic`) shows mostly "No" or "TBD".
- Context support: Zhao 2024 (microplastic focus dominates literature; macroplastic datasets scarce), WIREs 2025 review (calls for standardization), Cook 2021 (citizen science data gaps).
- Synthesis point: Data availability is a major bottleneck. Public multi-river datasets (like P001's but larger; P011's open hyperspectral set) are valuable but rare. Recommendation: future studies should release annotated datasets (P011 model) and use standardized annotation formats.

### 2. Cross-Environment Generalization Evidence Gap (Evidence: C006, C007, C008, taxonomy Level 8 analysis)
- Evidence: Only P001 (A — cross-river), P009 (A — satellite cross-region), P025 (A — lab→field), P027 (A — 7-river), P037 (A — SSL cross-location), P032 (B — networked multi-river) have A-grade external tests. Most papers graded B/C/D (no appropriate external test or only indirect evidence). C006 highlights platform trade-off (satellite broad vs UAV detailed); C007 confirms architecture choice determines cross-condition performance; C008 exposes evaluation gap (detection metrics ≠ monitoring reliability).
- Taxonomy evidence: Level 8 (`generalizationType`) shows mostly 8A (same-environment) or 8F (model transfer only for P001); very few 8B (cross-river/region/environment) or 8C (cross-sensor/resolution) except P009, P011.
- Context support: P002 review notes limited studies; P003 review confirms sparse literature; Zhao 2024 and Blettler 2018 support freshwater data scarcity.
- Synthesis point: Cross-environment generalization is rarely demonstrated experimentally. Synthesis should clearly separate papers with A-grade evidence from those with claims only (C-grade), and identify conditions under which transfer succeeds (fine-tuning vs frozen; CNN vs SSL; multi-river training vs single-river).

### 3. Platform Diversity & Underwater Camera Gap (Evidence: P002 review, taxonomy Level 2, P011 hyperspectral)
- Evidence: P001 (UAV RGB), P002 (satellite/UAS/ground), P011 (hyperspectral fixed tripper), P032 (networked — details unclear). No underwater camera studies found in extraction table; P002 explicitly excludes underwater; P011 uses hyperspectral but not underwater deployment.
- Taxonomy evidence: Level 2 shows UAV (dominant), Satellite, Ground, Multi-platform; underwater absent.
- Context support: P002 review excludes underwater; WIREs 2025 notes underwater sensing is in early development; no underwater studies in seed/backward/forward tracking.
- Synthesis point: Underwater cameras represent a major unexplored platform for river waste monitoring, particularly for submerged or partially submerged waste. Recommendation: future studies should explore underwater sensing integration (possibly combined with UAV/surface sensors for full-column monitoring).

### 4. Architecture & Training Strategy Gaps (Evidence: P001 comparison, P037 SSL, P038 new architecture, C001, taxonomy Level 6/7)
- Evidence: P001 compares scratch/fine-tune/frozen; P006 uses frozen backbone (CNN); P037 introduces SSL (SwAV) with +12.7% AP cross-location; P038 introduces new architecture (flux quantification) with open data; P003 review notes CNN dominance; no transformer studies found in extraction table; SAM/ConvNeXt absent.
- Taxonomy evidence: Level 6 shows mostly CNN family; Level 7 shows mostly fine-tuning/scratch; SSL (P037) and synthetic data (P026) are emerging; domain adaptation rarely tested (only P001 transfer learning, P009 cross-region without fine-tuning).
- Context support: P001 notes transformer barriers (quadratic scaling, lack of inductive bias, need for more data); P037 shows SSL as alternative; P002 review mentions DL generally but not specific architectures.
- Synthesis point: CNN architectures (YOLO, DeepLab, U-Net) dominate; newer architectures (transformers, SSL, generative AI for data augmentation — P026) are emerging but not yet standard. Training strategy (fine-tune vs frozen) depends on dataset size and task. Synthesis should recommend: standard comparison protocols (same dataset, same metrics, same split) for architecture comparisons; SSL and synthetic data augmentation as future directions (supported by P026, P037 evidence).

### 5. Evaluation Standardization Gap (Evidence: C005, C008, taxonomy Level 9, P002 review call)
- Evidence: P001 has metric attribution errors (C005); P031 shows detection mAP 0.99 but counting 6/32 (C008); different papers use different metrics (mAP@0.5 vs IoU vs F1 vs precision/recall vs counting accuracy); no standardized comparison table exists across studies; P002 review explicitly calls for standardized protocols.
- Taxonomy evidence: Level 9 shows diverse metrics; no consistent reporting standard across studies.
- Context support: P002 review (standardization call); Cook 2021 (citizen science standardization gap); Zhao 2024 and Blettler 2018 (review-level calls for standard methods).
- Synthesis point: The lack of standardized evaluation metrics and reporting protocols is one of the most significant gaps (RQ6). Synthesis recommendation: future studies should adopt unified reporting (detection metrics + quantification metrics + generalization test conditions + dataset availability + code availability) to enable cross-study comparison.

### 6. Reporting & Reproducibility Gaps (Evidence: P001 TBD fields, P003 review, P002 review, P032 dataset status unclear)
- Evidence: P001 has missing fields (augmentation not stated, observation days TBD, exact dataset counts confirmed but release URL noted); P003 (review — no original data); P032 dataset status unclear; many papers (`P005-P008`, `P013-P017`, etc.) have TBD fields pending full text; `pending_extraction.md` shows many studies need full-text verification.
- Taxonomy evidence: Level 10 (`datasetPublic`) mostly "No" or "TBD"; only P001 (Yes), P011 (Yes, open dataset) confirmed.
- Context support: P002 review notes reproducibility details missing; P003 (Jia 2023) is a review summarizing studies but not providing original reproducible data; P032 networked system may have data but status unclear.
- Synthesis point: Data and code availability is limited. Only 2 studies (`P001`, `P011`) have confirmed public datasets; `P026` and `P037` have open code/data; most studies (`P004`-`P032`) have private or unclear availability. This severely limits reproducibility and meta-analysis potential (RQ6).

Agents / Writers: Before drafting `challenges_future/` or `conclusion/`, filter `extraction_table/template.md` by taxonomy levels and `rqMapping` to confirm gap claims are supported by actual evidence. Do NOT invent gaps that are not present in the data. If synthesis requires additional papers to fill evidence gaps, note them in `pending_extraction.md` or `improvement_flags.md` rather than inventing evidence.
