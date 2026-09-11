# C008 — Detection Performance vs Quantification Reliability (P031 Lee 2025)

## Topic
Can high object-detection mAP guarantee reliable waste-quantification counts?

## Evidence
- P031 Lee 2025 (`P031` in extraction table): Object detection achieves `mAP 0.99` (near-perfect localization/classification) but counting accuracy `6/32` (~19%) — massive gap between detection performance and quantification reliability.
- This directly challenges any assumption in RQ3 that "good detection = good monitoring."

## Related Evidence (To Confirm From Other Papers)
- P001 Pati et al. reports both detection (mAP) and segmentation (mIoU/precision/recall) but does not report counting accuracy — could there be a similar hidden gap?
- P024 Putra 2021 reports YOLOv3 counting but metric is `mAP` (detection), not count accuracy — potential parallel gap.
- P032 B (networked system) may have counting metrics — verify.

## Resolution / Analysis for Synthesis
Not a contradiction between papers, but a gap in evaluation practices: most river-waste studies report detection metrics (mAP, IoU) without reporting counting/reliability metrics. P031 is one of the few that exposes this divergence.

## RQ Impact
- RQ3 (detection vs. segmentation comparison — if detection achieves high mAP but poor counting, segmentation or post-processing may be required for reliable quantification)
- RQ5 (generalization — if detection metrics don't generalize to counting reliability, cross-environment claims based only on mAP are weaker)
- RQ6 (major gap: lack of standardized quantification evaluation in addition to detection evaluation)

## Agent Note
Document this as a synthesis-level insight, not a contradiction between papers. When writing `evaluation/` section or `challenges_future/`, reference P031 as evidence that detection metrics alone are insufficient for monitoring applications.
