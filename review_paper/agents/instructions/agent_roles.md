# AGENT ROLE CARDS

These describe how different agent instances should behave when working in this project.

---

## SEARCH & SCREENING AGENT
**Trigger**: Methodology section needs actual database results / screening numbers.
**Tasks**:
- Execute searches using `resources/search_strategy/search_strategy.md`.
- Track numbers for PRISMA diagram in `resources/prisma_diagram/template.md`.
- Apply `resources/inclusion_criteria/criteria.md`.
**Output**: Updated `methodology/` `.tex`, updated `agent_log.md`.
**Rules**: Always double-check duplicates. Never invent screening numbers.

---

## ARCHITECTURE AGENT
**Trigger**: Section 6 (`dl_architectures/`) needs drafting or updating.
**Tasks**:
- Analyze YOLO, Faster R-CNN, SSD, U-Net, DeepLab, Mask R-CNN, transformers, newer architectures.
- Compare specifically for waste detection (small objects, underwater, aerial).
**Output**: Updated `dl_architectures/` `.tex` and `.md`, comparison table.
**Rules**: Read `base_published_paper/main.tex` first. Cite actual studies, not just architecture papers.

---

## DATASET AGENT
**Trigger**: Section 7 (`datasets/`) needs drafting.
**Tasks**:
- Extract dataset details from studies found by Search Agent.
- Create master comparison table.
- Note geographic and category diversity gaps.
**Rules**: If dataset info is missing from a paper, note absence — don't assume.

---

## EVALUATION AGENT
**Trigger**: Sections 8-9 (`training_evaluation/`) need drafting.
**Tasks**:
- Extract metrics (precision, recall, F1, mAP, IoU, speed, cost) per study.
- Create synthesis table comparing studies across architectures/datasets.
- Flag metric inconsistencies.
**Rules**: Note the task context for each metric. Don't mix classification accuracy with segmentation IoU without explanation.

---

## SYNTHESIS AGENT
**Trigger**: Sections 4-5 (`data_sources/`, `detection_approaches/`) or final synthesis.
**Tasks**:
- Ensure cross-section consistency.
- Check that claims in one section are supported in another.
**Rules**: Read all previous sections. Add contradictions to `improvement_flags.md`.
