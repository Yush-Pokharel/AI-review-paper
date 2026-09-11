# OUTLINE TEMPLATE — Section Status Tracker

Agents: Before editing any `.tex`, check this file. Update the status line.

## Sections

### 1. abstract
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Must summarize entire review; write LAST. Reference all other sections.

### 2. introduction
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Story arc: river pollution visual evidence -> limitations of manual monitoring -> computer vision promise -> deep learning advancements. Include diagram reference for river pollution.
Dependencies: Must reference base paper's motivation section.

### 3. review methodology
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Needs protocol.md finalized first. PRISMA diagram in `resources/prisma_diagram/` must match actual screening numbers.

### 4. data sources
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Compare UAV, satellite, ground cameras, underwater cameras. Create comparison table.

### 5. waste detection approaches
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Classification -> Object Detection -> Semantic Segmentation -> Instance Segmentation. Progressive complexity.

### 6. deep learning architectures
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: YOLO family, Faster R-CNN, SSD, U-Net, DeepLab, Mask R-CNN, Vision Transformers, newer architectures (SAM, etc.). Must reference base paper architectures if relevant.

### 7. datasets
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Size, annotation type, geographic diversity, categories, resolution. Propose comparison table.

### 8. training and generalization
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Scratch vs. fine-tuning vs. frozen vs. transfer learning vs. domain adaptation.

### 9. evaluation
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Metrics table (precision, recall, F1, mAP, IoU, speed, cost). Must be consistent with methodology.

### 10. challenges and research gaps
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Synthesize from all previous sections. Not just listing — must identify gaps that are NOT covered by current literature.

### 11. future research directions
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Based on gaps. Must include concrete recommendations (e.g., multi-modal fusion, underwater low-light architectures).

### 12. conclusion
Status: DRAFT WRITTEN 2026-09-08 (awaiting human review)
Agent assigned: AUTO-AGENT
Notes: Summarize findings from sections 4-11. Reiterate contribution.

---

## Agent Handoff Protocol
1. Pick a section with status NOT STARTED or IN PROGRESS.
2. Read `direction.md`, `scope.md`, `base_published_paper/main.tex`.
3. Edit section `.md` first (draft notes), then `.tex`.
4. Update this file's Status line.
5. Append to `agent_log.md`.
6. Add any concerns to `improvement_flags.md`.
7. Stop — wait for human approval before starting next section (unless explicitly told to continue).
