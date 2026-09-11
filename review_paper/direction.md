# STRATEGIC DIRECTION (Updated 2026-09-07)

## HUMAN CONTEXT CLARIFIED (New)
- **User origin**: Nepal — full of rivers/ponds. This gives the review a strong contextual anchor.
- **Scope**: Pollution in rivers and ponds (aquatic/freshwater focus, not marine/terrestrial only). Nepal context is a guiding example but review covers broader literature applicable to similar geographies.
- **Base paper** (`base_published_paper/main.tex`): "Leveraging UAV Data and Deep Learning Models for Detecting Waste in Rivers" — comparative experimental/research study comparing object detection and segmentation, evaluating training strategies (scratch, fine-tuning, frozen layers), and cross-river transfer learning in Bishnumati and Bagmati rivers. Uses UAV imagery.
- **Reference systematic review** (`base_reference_systematic_review_paper/`): WIREs Water 2025 (Marye et al.) — systematic review on remote sensing for macroplastics in rivers. Good model for structure but user does NOT want PRISMA claim.

## PUSHBACK / IMPROVEMENT AREAS FOR AGENTS TO MONITOR
1. **Scope Ambiguity — RESOLVING ITERATIVELY**: Confirmed rivers/ponds (Nepal context). Agents: Ensure every section reflects aquatic/freshwater focus, not generic urban waste. Flag any section that drifts to terrestrial-only or marine-only contexts.
2. **Base Paper Integration — RESOLVED**: The base paper is a **comparative experimental/research study** (not a survey). Agents must treat it as a methodological blueprint (training strategies, UAV datasets, river-specific evaluation) and cite it as an example of rigorous riverine DL comparison, not as the review's primary content source.
3. **No PRISMA Claim — RESOLVED**: Methodology should follow structured review practices (search strategy, inclusion/exclusion, screening) but must NOT claim PRISMA compliance or registration. Agents: Use `methodology/` to describe a transparent, reproducible process without implying formal systematic review protocol registration.
4. **Reference Review Integration**: The WIREs Water 2025 review is an excellent structural reference for remote sensing + river pollution + DL. Agents: Use it to confirm what is already covered in literature, identify gaps (e.g., this review may lack underwater cameras, newer transformers, or Nepal-specific studies), and position the new review's contribution.

## OUTLINE (Fixed — Updated Notes)
- abstract (write LAST; reference Nepal/rivers/ponds context briefly if relevant)
- introduction (story: Nepal river pollution; base paper's Bishnumati/Bagmati context; why CV; reference WIREs review for state-of-the-art framing)
- review methodology (structured, transparent, NO PRISMA claim; reference search strategy, criteria, screening process; include PRISMA-style diagram as organizational aid only)
- data sources (UAV, satellite, ground cameras, underwater cameras — emphasize UAV since base paper focuses on it)
- waste detection approaches (classification, object detection, semantic segmentation, instance segmentation — base paper compares detection vs. segmentation)
- deep learning architectures (YOLO, Faster R-CNN, SSD, U-NET, DeepLab, Mask R-CNN, transformers, newer architectures — base paper uses DeepLabv3+ and detection models; highlight this comparison)
- datasets (dataset size, annotation type, geographic diversity, waste categories, image resolution — include base paper's novel datasets for Bishnumati/Bagmati)
- training and generalization (scratch, fine-tuning, frozen layers, transfer learning, domain adaptation — base paper's key contribution: comparing these strategies)
- evaluation (precision, recall, f1, mAP, IoU, inference speed, computational cost — base paper reports these; review should synthesize across studies)
- challenges and research gaps (synthesize from studies + reference review gaps)
- future research directions
- conclusion

## AGENT WORKFLOW (Incremental, Human in Loop — Updated)
1. Agent picks section based on `outline.md` status.
2. Agent reads `direction.md`, `scope.md`, `base_published_paper/main.tex`, and `base_reference_systematic_review_paper/` files.
3. Agent drafts `.md` notes in section folder, then `.tex`.
4. Agent updates `outline.md` status, `agent_log.md`, and `improvement_flags.md`.
5. Human reviews `improvement_flags.md` and `agent_log.md` before next agent starts.
6. Human updates `direction.md` or `scope.md` as needed — iterative refinement encouraged.

## BASE PAPER DETAILS FOR AGENTS
- Title: Leveraging UAV Data and Deep Learning Models for Detecting Waste in Rivers
- Authors: Pati et al. (AI Research Center, Tribhuvan University, Nepal)
- Key contribution: Comparative evaluation of detection vs. segmentation; training strategies; cross-river transfer learning; novel UAV datasets (Bishnumati, Bagmati).
- Key results: DeepLabv3+ (fine-tuned) outperforms detection; frozen backbone better for detection; fine-tuning better for segmentation; transfer learning improves mIoU (0.849 Bagmati→Bishnumati, 0.841 reverse).
- Style: IEEE Access format (`ieeeaccess` class, `cite` package, structured abstract).

## REFERENCE REVIEW DETAILS FOR AGENTS
- Source: WIREs Water, 2025; "Remote Sensing for Monitoring Macroplastics in Rivers: A Review"
- Authors: Marye et al.
- Key contribution: Reviews remote sensing platforms (satellite, UAS, ground cameras), image analysis, DL/ML for macroplastic detection.
- Useful for: Confirming state-of-the-art, identifying what platforms/methods are covered, seeing gaps this new review can fill.
- Note: This reference review does NOT claim PRISMA protocol registration explicitly in the visible text; it uses "systematic review" terminology. Our review will be transparent but not claim formal PRISMA.

## TITLE — FINAL (Confirmed)
"Generalization of Deep Learning-Based Waste Detection Across Riverine Environments: A Systematic Review"

Note: The term "generalization" is used in the broadest sense:
- Same river / different area
- Cross-river / cross-location
- Cross-region / cross-country
- Cross-environment (river → pond → coastal / marine, and vice versa)
- Cross-season / cross-weather / cross-lighting
- Cross-sensor (UAV → satellite → ground → underwater)
- Cross-resolution / cross-scale
- Cross-dataset / cross-annotation
- Cross-model / architecture comparison (methodological transfer: detection approach developed for river adapted to coastal)
- Transfer learning (model weights)
- Domain adaptation (feature-level)
- Representation / foundation / self-supervised transfer (features learned elsewhere applied to waste)

Agents: When analyzing papers, tag which type(s) of generalization are demonstrated, proposed, or missing. Do not restrict to literal "trained A, tested B" model reuse.

## SEED PAPERS — CONFIRMED (4 Seeds)
1. P001 — User's base paper (Pati et al., `base_published_paper/`)
2. P002 — WIREs Water 2025 review (Marye et al., `base_reference_systematic_review_paper/`)
3. P003 — Jia et al. (2023) — Deep learning macroplastic literature
4. P004 — Jakovljevic et al. (2020) — Early river DL study
Agents: Start extraction from P001 and P002 (backward/forward). Then incorporate P003 and P004 references into extraction table.
