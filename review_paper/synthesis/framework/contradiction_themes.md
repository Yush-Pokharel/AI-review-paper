# CONTRADICTION THEMES FOR SYNTHESIS

Purpose: Organize contradictions (`contradiction_tracker.md`) into themes for writing `challenges_future/`, `evaluation/`, and `conclusion/`.

## Theme 1: Training Strategy — Fine-Tune vs Frozen (C001)
- Papers: P001 (segmentation: fine-tune best; detection: frozen best)
- Potential extension: P006 (frozen backbone preferred for detection); P027 (intermediate-weights best — newer finding)
- Synthesis point: Small datasets favor frozen backbone for detection to avoid overfitting; larger/more diverse datasets allow full fine-tuning. No universal best strategy — depends on dataset size and domain similarity.
- Section mapping: `training_evaluation/` (RQ4), `challenges_future/` (RQ6)

## Theme 2: Platform Trade-Off — UAV (High Res, Small Coverage) vs Satellite (Broad Coverage, Low Res) (C002, C006)
- Papers: P001 (UAV best for detailed river waste), P002 (satellite used in 20% studies but struggles with small items), P009 (satellite multi-river A — cross-region transfer works but resolution limits remain), P027 (multi-river UAV A — suggests UAV + multi-river training can match satellite coverage)
- Synthesis point: UAV provides high-resolution detail but is site-bound; satellite enables broad monitoring but misses small/dispersed waste; hybrid approaches (satellite + UAV fusion, e.g., P011 hyperspectral + UAV; P020 multi-sensor) are emerging but not standardized.
- Section mapping: `data_sources/` (RQ1), `evaluation/` (RQ5), `challenges_future/` (RQ6)

## Theme 3: Architecture Choice — CNN Dominance vs Transformer Potential (C003)
- Papers: P001 (CNN practical for small datasets; transformers lack inductive bias and need more data), P037 (SSL — new architecture representation), P038 (new architecture — flux quantification)
- Synthesis point: CNNs dominate river waste studies due to small, heterogeneous datasets; transformers show promise (P001 notes) but lack river-specific studies; newer architectures (ConvNeXt, SAM) not yet applied; SSL shows cross-environment potential (P037 +12.7% AP) — future direction.
- Section mapping: `dl_architectures/` (RQ2), `future_research/` (RQ6), `training_evaluation/` (RQ4 — SSL as new training strategy)

## Theme 4: Detection vs Quantification — Metrics Don't Guarantee Monitoring Reliability (C008)
- Papers: P031 (mAP 0.99 but counting 6/32 — massive gap), P001 (reports detection + segmentation metrics but no counting metrics), P024 (YOLOv3 counting but metric unclear), P012 (object detection AP only)
- Synthesis point: Most studies evaluate detection/localization (mAP, IoU) but do not evaluate quantification/reliability for monitoring applications. This is a major evaluation gap (RQ6). Synthesis recommendation: monitoring applications need combined metrics (detection + counting/reliability + temporal stability).
- Section mapping: `evaluation/` (RQ3, RQ5, RQ9 equivalent), `challenges_future/` (RQ6)

## Theme 5: Generalization Evidence — Most Claims Are Unverified (C-grade prevalence)
- Evidence: `extraction_table/template.md` shows most papers graded B/C/D; only P001, P009, P025, P027, P037 have A-grade with external tests.
- Synthesis point: Cross-environment generalization is the exception, not the rule. Most studies claim robustness without appropriate external tests. This reinforces the review's contribution: identifying which studies actually demonstrate generalization and under what conditions.
- Section mapping: `challenges_future/` (RQ6 — standard evaluation protocols needed), `evaluation/` (RQ5), `training_evaluation/` (RQ4 — transfer learning is rare but valuable)

## Theme 6: Internal Consistency — Data Reporting Issues (C004, C005)
- Papers: P001 (C004 size-direction contradiction; C005 metric attribution error)
- Synthesis point: Even well-cited studies have reporting inconsistencies. This highlights the need for standardized reporting protocols (RQ6) and careful verification in synthesis.
- Section mapping: `methodology/` (RQ protocol notes), `challenges_future/` (RQ6 — reporting standardization)

Agents / Writers: When drafting `evaluation/` or `challenges_future/`, reference these themes directly. Do not invent contradictions — use only those documented in `contradiction_tracker.md` (C001-C009).
