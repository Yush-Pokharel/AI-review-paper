# GAP ANALYSIS FRAMEWORK (To Be Filled After Synthesis)

This file guides how research gaps will be identified. Agents must not invent gaps before synthesis — they must emerge from the extraction table, contradiction tracker, and taxonomy.

## How Gaps Are Identified (Process)
1. Filter `extraction_table/` by taxonomy levels (e.g., `Level 8: Cross-river` = very few papers).
2. Check which RQs have sparse evidence (few papers with `rqMapping`).
3. Read `contradiction_tracker.md` — unresolved contradictions indicate knowledge gaps.
4. Check dataset availability (`datasetPublic` = No for most) — data scarcity gap.
5. Check geographic diversity (`country`) — over-representation of Europe/US/Nepal? Lack of Africa, South America, Southeast Asia?
6. Check `transferLearning` — how many papers actually test cross-environment generalization?
7. Check `imageSource` — underwater cameras rarely used? Confirm.
8. Check `Level 6` (model families) — are newer architectures (SAM, ConvNeXt) absent from river studies?

## Expected Gap Categories (Based on Base Paper + Reference Review)
1. **Data Gaps**: Few public river waste datasets; limited underwater camera datasets; limited multi-river datasets.
2. **Methodology Gaps**: Lack of standardized evaluation protocols; inconsistent metrics across studies; few studies comparing detection vs. segmentation on same dataset.
3. **Generalization Gaps**: Most studies train and test on same river/environment; very few cross-river, cross-region, or cross-season studies (except P001).
4. **Platform Gaps**: UAV dominates; underwater cameras underexplored; satellite studies limited to high-flow or large rivers.
5. **Architecture Gaps**: Transformer studies scarce in river waste; most studies use older CNN architectures (YOLO, DeepLab, U-Net); newer architectures (SAM, ConvNeXt) rarely applied.
6. **Geographic Gaps**: Most studies from Europe, North America, or South Asia (Nepal); fewer from Africa, Southeast Asia, South America.
7. **Environmental Condition Gaps**: Limited studies across seasons, weather conditions, turbidity levels, lighting conditions.

Agents: Once extraction is substantial (≥15 papers), begin filling actual gap evidence in this file. Do not copy these expected categories blindly — confirm with data.

## Actual Evidence (Phase 1 — P001 + P002 Only)
- P001 confirms: dataset is public (Yes) — contradicts expected data scarcity; but only 2 rivers, 1 country (Nepal), UAV-only, no season/weather diversity, no underwater, no cross-dataset (only cross-river within same basin). Small size (764 tiles, ~1.3 objects/tile).
- P001 confirms: only CNN architectures tested (YOLO, DeepLab, FCN); no transformers, no SAM, no newer architectures.
- P001 confirms: cross-river transfer demonstrated (A) but cross-region, cross-season, cross-environment, cross-sensor absent.
- P002 confirms: underwater cameras excluded from review scope; satellite studies use moderate resolution (Sentinel-2 10m) with detection challenges; ground cameras fixed/handheld account for ~33% of studies.
- P002 confirms: only 16 studies met strict criteria; indicates literature is sparse.
- P001 + P002 combined: no studies comparing detection vs. segmentation across different rivers; P001 is the only seed with this comparison.
- P001 flags: augmentation not stated, observation days missing, some metric inconsistencies — indicates reporting gaps in the literature.

Conclusion (preliminary): Even with just 2 seeds, gaps 3 (generalization — mostly absent), 4 (platform — underwater absent), 5 (architecture — transformers/newer absent), 7 (conditions — season/weather absent) are strongly supported. Gap 2 (methodology standardization) is supported by P002's call and P001's metric inconsistencies.
