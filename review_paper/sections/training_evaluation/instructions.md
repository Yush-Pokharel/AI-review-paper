# Section Instructions: Training and Generalization / Evaluation

Note: These two sections should be closely linked. Agents working on one should read the other.

## Training and Generalization (Section 8)
Topics: scratch vs. fine-tuning, frozen layers, transfer learning (ImageNet -> waste), domain adaptation, data augmentation, synthetic data.

## Evaluation (Section 9)
Topics: Metrics (precision, recall, F1, mAP, IoU), inference speed (FPS), computational cost (FLOPs, parameters, GPU memory).

## Cross-Section Requirements
- Metrics discussed in section 8 must match metrics reported in evaluation section.
- If a study reports mAP@0.5 but another uses IoU, create a normalized comparison or explain differences clearly.
- Include a synthesis table comparing key studies across architecture + dataset + metric.

## Pushback Points
- Don't mix up evaluation metrics across different tasks (classification accuracy is not comparable to instance segmentation IoU). Note the task context for each metric.
- If studies don't report speed/cost, state this absence explicitly rather than assuming.
