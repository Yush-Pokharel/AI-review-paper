# CONTRADICTION & SYNTHESIS TRACKING

Agents: When you find contradictions between papers, record them here with citations.
This is critical for RQ5 (generalization) — contradictions often reveal the limits of current evidence.

## Template for Each Contradiction
- **Contradiction ID**: C001, C002, ...
- **Topic**: What is being compared?
- **Paper A (Claim)**: Citation + specific claim/result.
- **Paper B (Contrary Claim)**: Citation + contrary result.
- **Resolution / Analysis**: Can the contradiction be explained by dataset differences, environment differences, model differences, or evaluation metric differences? If not resolved, note it as an unresolved tension in the literature.
- **RQ Impact**: Which RQ does this inform?

## Example Template Entries (Pre-populated with Expected Contradictions)

### C001 — Fine-tuning vs. Frozen Backbone
- Topic: Best training strategy for river waste detection.
- Paper A (P001 — Pati et al.): Fine-tuning pretrained weights best for segmentation; frozen backbone best for object detection.
- Paper B (Potential): [Agent to find paper claiming opposite or no difference.]
- Resolution: May depend on dataset size (small datasets benefit from frozen backbone for detection to avoid overfitting; larger datasets allow full fine-tuning).
- RQ Impact: RQ4, RQ5.

### C002 — UAV Resolution vs. Coverage Trade-off
- Topic: Whether UAV or satellite is better for river waste monitoring.
- Paper A (P001 — Pati et al.): UAV preferred for high-resolution river waste detection.
- Paper B (P002 — Marye et al. / included satellite studies): Satellite offers broader coverage but lower resolution; struggles with small dispersed items.
- Resolution: Not a contradiction but a trade-off. Both are valid depending on scale and objective.
- RQ Impact: RQ1, RQ5.

### C003 — Transformer Performance
- Topic: Whether transformers outperform CNNs for river waste detection.
- Paper A (P001 — Pati et al.): CNNs preferred for small, heterogeneous river datasets due to inductive bias and lower data needs.
- Paper B (Potential newer study): Transformer achieves higher mAP with sufficient data and augmentation.
- Resolution: Likely data-dependent. Note data size differences.
- RQ Impact: RQ2, RQ5, RQ6.

### C004 — P001 Internal Data Contradiction (Waste Size Prediction Direction)
- Topic: Does the model predict larger or smaller waste sizes than ground truth?
- Paper A (P001 OD paragraph): Predictions "smaller than ground-truth dimensions" (9606.25 cm² vs 6048.68 cm² is contradictory — likely copy-paste error from IS paragraph; note direction claim is opposite).
- Paper B (P001 IS paragraph): Predictions "larger than ground-truth dimensions" (same numbers quoted but opposite claim).
- Resolution: Unresolved contradiction within the same paper — likely copy-paste error in `.tex`. Agent should quote cautiously in review; verify with original dataset if possible. This undermines reliability of size-comparison claims.
- RQ Impact: RQ3 (detection vs. segmentation comparison — if size claims are contradictory, comparison is less reliable).

### C005 — P001 Metric Attribution Error
- Topic: Which river/site achieves specific OD performance?
- Paper A (P001 abstract / table text): Freeze-YOLOv5s precision 0.860 attributed to Bagmati dataset.
- Paper B (P001 Table OD): Freeze-YOLOv5s precision 0.860 = Bishnumati; Bagmati Freeze-YOLOv5s = 0.739.
- Resolution: `.tex` typo; use table values, not inline text. Agent must cite table, not inline attribution.
- RQ Impact: RQ3, RQ4 (training strategy comparison — if site attribution is wrong, conclusions about which strategy works best per site are unreliable unless corrected).

### C006 — Satellite Cross-Region Generalization vs UAV Same-Basin Scope (expanded batch, 2026-09-08)
- Topic: Which platform generalizes across geographies?
- Paper A (P009 — Solé Gómez et al. 2022): Sentinel-2 + DeepLabV3+ trained multi-river, correctly identifies debris in unseen regions (A; IoU ~0.5, debris acc ~80%).
- Paper B (P001 — Pati et al. + P002 narrative): UAV high-resolution models tested only cross-river within one basin; satellite portrayed as struggling with small/dispersed items.
- Resolution: Modality trade-off, not contradiction — multispectral + multi-river training enables coarse cross-region transfer; UAV high-res accuracy is site-bound by single-basin training. Synthesis should recommend multi-river UAV training (P009 lesson applied to P001 modality).
- RQ Impact: RQ1, RQ5.

### C007 — Satellite ML Degrades Across Conditions While Satellite DL Holds Cross-Region (auto-expansion, 2026-09-08)
- Topic: Does architecture choice determine cross-condition generalization on the same platform?
- Paper A (P019 — Mohsen et al. 2023): Sentinel-2 + SVC/RF/ANN collapses val F1 ~0.9 → unseen varying-hydro test F1 0.45–0.69.
- Paper B (P009 — Solé Gómez et al. 2022): Sentinel-2 + DeepLabV3+ holds ~80% debris accuracy on unseen regions.
- Resolution: Architecture + training-corpus difference (spatial-context CNN trained multi-river vs per-pixel ML trained single-river). Strengthens RQ2→RQ5 link: spatial models generalize better; do NOT pool satellite-ML and satellite-DL evidence as equivalent.
- RQ Impact: RQ2, RQ5.

### C008 — Detection Performance vs Quantification Reliability (P031 Lee 2025, Batch 4)
- Topic: Does high object-detection mAP guarantee reliable waste-quantification counts?
- Evidence: P031 reports mAP 0.99 (near-perfect detection) but counting accuracy only 6/32 (~19%).
- Impact: Challenges RQ3 assumption that good detection = good monitoring; suggests segmentation/post-processing needed for reliable quantification.

### C009 — AIGC Synthetic→Real Generalization Evidence (P026 Pan 2023)
- Topic: Does synthetic-to-real transfer demonstrate true generalization (A) or only training-set improvement?
- Evidence: P026 reports synthetic (Stable Diffusion AIGC) vs real benchmarks; metrics reported as aggregated F1-based results; separate synthetic→real transfer metrics not clearly isolated in available extraction data.
- Resolution: A-grade preserved with verification caveat — synthesis must quote with caveat that full separate metrics require deeper full-text verification; do not claim unqualified A for synthetic→real transfer without separate metric table.
- RQ Impact: RQ4 (training strategies, synthetic data), RQ5 (cross-dataset/generalization).

Agents: Add contradictions as you extract papers. Before final synthesis, review this file to identify themes.
