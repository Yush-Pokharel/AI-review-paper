# REVIEW QUESTION & RESEARCH QUESTIONS (Confirmed)

## Overarching Review Question (RQ-R)
How well do deep-learning-based waste detection systems generalize beyond the environment in which they were trained?

This frames the review around cross-environmental generalization — not just listing methods, but evaluating whether and how they work across rivers, regions, imaging platforms, and environmental conditions.

## 6 Research Questions

### RQ1 — Data & Platforms
What datasets and imaging platforms have been used for automated riverine waste detection?
- Covers: UAV, satellite, ground cameras, handheld/fixed cameras, underwater cameras; RGB, multispectral, hyperspectral.
- Maps to outline sections: data_sources, datasets (partially).

### RQ2 — Approaches
What computer vision and deep learning approaches have been used for riverine waste detection?
- Covers: classification, object detection, semantic segmentation, instance segmentation; CNNs, transformers, etc.
- Maps to: detection_approaches, dl_architectures.

### RQ3 — Detection vs. Segmentation
How do object detection and segmentation approaches compare for riverine waste monitoring?
- Direct comparison of bounding-box vs. pixel-level approaches.
- Maps to: base paper's core comparison (Pati et al.); evaluation section.

### RQ4 — Training & Transfer
What training and transfer-learning strategies are used to address limited riverine waste datasets?
- Covers: scratch, fine-tuning, frozen layers, transfer learning, domain adaptation, augmentation.
- Maps to: training_evaluation (section 8); directly builds on base paper findings.

### RQ5 — Generalization
How well do existing models generalize across rivers, geographic regions, environmental conditions, and datasets?
- The core of the review question. Cross-river, cross-region, cross-dataset performance.
- Maps to: evaluation (section 9), challenges, future directions.

### RQ6 — Gaps & Limitations
What are the major limitations and unresolved research gaps in automated riverine waste detection?
- Synthesis of data scarcity, annotation challenges, environmental variability, hardware constraints, lack of standardization.
- Maps to: challenges_future, conclusion.

## How RQs Guide Structure
- Sections are written to answer these RQs, not as generic headings.
- Each section's `.md` notes should reference the RQ it addresses.
- The extraction table (`extraction_table/`) is organized so that data can be filtered/grouped by RQ.
