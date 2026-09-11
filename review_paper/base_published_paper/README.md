# BASE PUBLISHED PAPER (Updated 2026-09-07)

## Files Present
- `main.tex` — The full LaTeX source.
- `references.bib` — The bibliography file.
- Note: Figure folder and separate reference folder removed per user instruction. Only `.tex` and `.bib` are retained as core files.

## Paper Details for Agents
- **Title**: Leveraging UAV Data and Deep Learning Models for Detecting Waste in Rivers
- **Type**: Comparative experimental/research study (NOT a survey or review).
- **Authors**: Pati et al. (AI Research Center, ACEM, Tribhuvan University, Kathmandu, Nepal)
- **Context**: Nepal rivers (Bishnumati and Bagmati).
- **Data**: UAV-captured imagery; novel datasets for object detection and segmentation.
- **Key Methods Compared**:
  - Object detection models vs. segmentation models.
  - Training strategies: from scratch, full-model fine-tuning, fine-tuning with frozen layers.
  - Cross-river transfer learning (Bagmati → Bishnumati; Bishnumati → Bagmati).
- **Key Results**:
  - DeepLabv3+ (fine-tuned) best overall: precision 0.915 / recall 0.934 (Bagmati); 0.913 / 0.939 (Bishnumati).
  - Fine-tuning pretrained weights better for segmentation.
  - Frozen backbone layers better for object detection.
  - Transfer learning improves mIoU: 0.849 (Bagmati→Bishnumati), 0.841 (Bishnumati→Bagmati).
- **Format Style**: IEEE Access (`ieeeaccess` class, `cite`, structured abstract, keywords); DOI: 10.1109/access.2025.3576295 (2025) — venue confirmed via `.tex` metadata.
- **How to use**: Agents should reference this paper's methodology (training comparison, dataset construction, UAV setup) when discussing best practices. Cite it appropriately but do not treat it as the review's sole content source.
