# GENERALIZATION EVALUATION CLASSIFICATION (Critical for RQ5)

Agents must classify every paper's generalization claim/evidence into ONE of the following categories. Do NOT infer from vague claims. Check the paper's actual experiments.

## Classification Categories

### A — Experimentally Demonstrated (Strongest)
The paper explicitly tests on a different environment, dataset, river, season, sensor, or resolution than the training set, and reports quantitative results.
- Example: P001 (Pati et al.) trains on Bagmati, tests on Bishnumati — reports mIoU drop.
- Example: Paper trains on Dataset A (UAV, River X), tests on Dataset B (UAV, River Y) — reports mAP.
- Must have: Explicit split/training-test description AND quantitative metrics on the external/test set.

### B — Indirect Evidence (Moderate)
The paper does not do a full cross-environment test, but provides evidence that supports generalization potential: large dataset diversity, multi-season training, multi-river combined dataset, extensive augmentation, or comparison showing model is stable across conditions.
- Example: Paper collects data across 3 rivers and trains a combined model, but only reports aggregated metrics without separate cross-river evaluation.
- Example: Extensive augmentation and multi-season data are used; authors claim this improves robustness but do not test on a separate season's data.
- Note: This is NOT demonstrated generalization. It must be labeled as indirect.

### C — Author Claim Without Appropriate External Test (Weak / Unverified)
The authors state the model is "robust," "generalizable," "scalable," or "works across environments" but do NOT perform an appropriate external test.
- Examples of inappropriate claims:
  - "Our model achieves high accuracy, therefore it should work on other rivers."
  - "We used data augmentation, so the model is robust."
  - "The model was tested with k-fold cross-validation, so it generalizes." (Cross-validation is within-dataset, not cross-environment.)
  - "We tested on 10% of the same dataset held out; the model is generalizable."
- Agents: If you encounter this, note the exact claim in `notes` and classify as C.

### D — No Generalization Evaluation (Absent)
The paper trains and tests on the same dataset/environment with no mention of generalization, cross-testing, or external validation.
- Most papers fall here. This is not a criticism — it is an observation of scope.

## How Agents Must Record This
In `extraction_table/template.md`, add / use:
- `generalizationEvidence`: A / B / C / D (must be one)
- `generalizationType`: The taxonomy categories that apply (8A-8G)
- `notes`: The exact evidence or claim that justifies the classification (quote or describe briefly).

Example entries:
- P001: A (cross-river model transfer; quantitative mIoU reported)
- P003 (if Jia 2023 is a review without original cross-testing): D (no original data) or B (if it synthesizes studies with cross-testing evidence)
- P004 (if Jakovljevic 2020 is original study without cross-testing): D or C (check paper text)

## Pushback Rule
If an agent classifies a paper as A (demonstrated) but the evidence is only within-dataset cross-validation or same-river testing, the next agent or human must flag this in `improvement_flags.md` and correct it to C or D.
