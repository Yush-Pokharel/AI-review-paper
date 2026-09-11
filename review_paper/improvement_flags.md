# IMPROVEMENT FLAGS (Updated 2026-09-07 — Iterative Tracking)

## Resolved Flags (Human Confirmed)
- [2026-09-07] Scope ambiguity — RESOLVED: Rivers/ponds (Nepal context); aquatic/freshwater focus.
- [2026-09-07] Base paper type — RESOLVED: Comparative experimental/research study (Pati et al.); method blueprint for UAV + DL comparison.
- [2026-09-07] No PRISMA claim — RESOLVED: Methodology will be structured and transparent but will NOT claim protocol registration or full PRISMA compliance.
- [2026-09-07] Reference review integrated — RESOLVED: WIREs Water 2025 (Marye et al.) read; notes for agents created in `base_reference_systematic_review_paper/notes_for_agents.md`.
- [2026-09-07] Base paper files — RESOLVED: `main.tex` and `references.bib` present in `base_published_paper/`; folder cleaned (no separate figure/reference folders).

## Active Flags (Awaiting Resolution During Writing)
- [2026-09-07] Time range for included studies: Propose 2015-2026. Confirm with human before finalizing `methodology/`.
- [2026-09-07] Database selection: Propose Scopus, Web of Science, IEEE Xplore, Google Scholar. Confirm with human.
- [2026-09-07] Peer-reviewed vs. conference: Propose include reputable conferences (IEEE, CVPR, etc.). Confirm with human.
- [2026-09-07] Geographic scope: Global with Nepal context? Confirm with human.
- [2026-09-07] Section 6 (DL architectures): Must specifically compare architectures mentioned in base paper (DeepLabv3+, detection models) against broader literature (YOLO, Faster R-CNN, SSD, transformers, newer architectures). Agent must not miss this comparison.
- [2026-09-07] Section 8-9 (Training/Evaluation): Must synthesize base paper's training strategy comparison (scratch/fine-tune/frozen/transfer) across broader literature. This is a key unique contribution.
- [2026-09-07] Section 10-11 (Challenges/Future): Must reference both base paper's limitations (small dataset size, two rivers only, UAV-only) and WIREs review's identified gaps (standardization, underwater, newer architectures) to create a coherent gap map.
- [2026-09-07] Title refinement: Current draft includes "Nepal Context" — confirm if human wants this emphasized or kept as implicit context.

## Phase 1 Extraction Flags (2026-09-08)
- [2026-09-08] CONTRADICTION: template.md guessed P001 datasetPublic "likely No" — main.tex Data Availability Statement gives public GitHub URL (accessed 2025-05-31). Corrected to Yes; verify link live before methods section claims it.
- [2026-09-08] CONTRADICTION: main.tex line ~666 attributes Freeze-YOLOv5s precision 0.860 to "Bagmati dataset" — Table OD shows 0.860 is Bishnumati (Bagmati Freeze-YOLOv5s = 0.739). Typo; use table values.
- [2026-09-08] TYPO: Table ODvsIS lists Freeze-YOLOv7x Bishnumati recall 0.786 vs Table OD 0.789. Minor; use Table OD.
- [2026-09-08] ANOMALY: waste-size paragraph reports segmentation largest-predicted areas identical to OD numbers (9606.25/5942.48 cm²) and claims predictions "larger than ground truth" while OD paragraph says predictions "smaller than ground truth" — likely copy-paste error; quote cautiously.
- [2026-09-08] AMBIGUITY: two distinct Jia-2023 papers — P003 = Jia Water Research review (base .bib) vs P008 = Jia Frontiers in Water open-dataset study (WIREs). Never cite as "Jia 2023" without disambiguation.
- [2026-09-08] TYPO: main.tex line ~308 "Jakovljeic et al." — bib key Jakovljevic2020ADL spelling is correct.
- [2026-09-08] MISSING in main.tex: year/venue, flight dates/season, Emax/patience/LR values, augmentation list, IS/FCN backbone names, GSD-correction/ortho details. Marked TBD in P001; do NOT infer.
- [2026-09-08] PRETRAINING CORRECTION: P001 pretrained = MSCOCO (OD) / MSCOCO-subset-to-VOC (IS), NOT ImageNet as template pre-guessed.
- [2026-09-08] PROVISIONAL GRADES: P005/P006/P008 generalizationEvidence left TBD (summaries only); P007 graded provisional B — all require full-text confirmation; next agent must not inflate to A.
- [2026-09-08] P004 LOCATION: paper studies Lake Balkana + Crna Rijeka/Vrbas confluence (Mrkonjić Grad, Bosnia and Herzegovina) — WIREs Table 1 "river and reservoir" shorthand confirmed; GIM article once writes "Crna Rijeka and Drina" (likely error; paper says Vrbas). Use Vrbas.
- [2026-09-08] P004 EVIDENCE CAVEAT: graded A on Balkana→Crna Rijeka independent test (F1 0.73 vs 0.78 + 3.4% area error), but paper reports 80/20 train/val with no separate held-out test and trained a separate ResUNet on Dataset3 — next agent must verify Table 5 (was Crna Rijeka eval truly held-out?) from full-text PDF before synthesis cites it as A.
- [2026-09-08] P003 vs P008: confirmed distinct (Water Research review vs Frontiers in Water open-dataset study); P008 corroborated via Vallendar 2021 TU Delft thesis (DenseNet majority-vote 91%, YOLOv4 95.61% single-class) — thesis is grey literature, cite P008 paper not thesis.
- [2026-09-08] Zhao 2024 RESOLVED: Zhao, Richardson & You 2024, JHM 477:135329 — microplastics review, context-only, never a P-row.
- [2026-09-08] P004 A PARTIALLY VERIFIED: full-text sections confirm Balkana-trained ResUNet50 run on Crna Rijeka as independent scenario (F1 0.73 vs 0.78, 3.4% area error); residual: Table 5 separation + Dataset3-ResUNet distinction need PDF pass before synthesis cites unqualified A.
- [2026-09-08] P010 CONFLICT: WIREs Table 2 "2400 images" vs paper 1920→4800 — use paper value; WIREs imageSource "handheld" unconfirmed by paper text, needs full-text check.
- [2026-09-08] GRADE WATCH: P009/P011/P012 A-grades rest on abstract+repository evidence (unseen-region / lab→field / cross-site tests described with metrics); per-region tables need PDF pass; P010 stays C (robustness claim, no external test) — do NOT upgrade without new evidence.
- [2026-09-08] TITLE/JOURNAL BACKFILL: P013+ rows carry title+journal per expansion spec; P001–P012 lack them — backfill before synthesis (titles inferable from .bib/WIREs, low risk).
- [2026-09-08] NON-DL PRECEDENT: P011/P018–P022 included as CV+ML per criteria_final #3 ("CV and/or DL"); review title is DL-focused — synthesis must frame these as spectral/ML baseline strand, not DL evidence. Do NOT let ML rows dilute DL-generalization claims.
- [2026-09-08] SCHREYERS CONTEXT: excluded (no DL) but 78%-hyacinth-entrainment finding is key vegetation-confound evidence — route to challenges_future via context_notes, not extraction table.
- [2026-09-08] TBD VENUES/AUTHORS: P028 venue (doi 10.54097/t1napg15), P030 authors, P032 authors — retrieve from full text before synthesis cites them.
- [2026-09-08] P027 NUANCE: intermediate-weights-best (overfitting) + GSD-direction flip (small-GSD↔IS vs large-GSD↔OD) — synthesis must NOT claim "larger models / higher res always better."
- [2026-09-08] P001 VENUE FIX: published IEEE Access 2025, doi 10.1109/access.2025.3576295 — base_published_paper/README.md still implies unpublished manuscript; update at synthesis + cite P006→P001 lineage (Maharjan TT→HMH mirrors P001 cross-river design, same group).
- [2026-09-08] P036 PROVISIONAL: A rests on EGU abstract + iScience linkage (cross-river F1 79%) — full-text pass required before unqualified A.
- [2026-09-08] PREPRINT/THESIS RULE: Saddi25 (ESSOAr) + Cortesi24 (thesis) correctly held out per criteria #6 — do NOT promote without peer-reviewed versions.
- [2026-09-08] FINAL QC (50/50): IDs sequential, no duplicates; every row has rqMapping + generalizationType + evidence grade; all A-grades cite explicit test+metrics (caveats inline); provisional rows (P036/40/41/44/46/47/49/50/51/52) MUST pass PDF verification before synthesis cites them as anything stronger; non-DL rows (P011/P018–P022) framed as spectral/ML strand; P045 scoped adjacent (infrastructure, not litter detection); outline.md verified untouched.
- [2026-09-08] CONNECTED AUDIT (51/50): P053 added B-prov (river evidence thin — PDF pass before any synthesis use); Garaba23/Alboody23 correctly held as context (fails #3/#2). Grades now A18/B15/C2/D16.
- [2026-09-08] P012 VERSION CONFLICT: arXiv-v1 (easy-AP 48.1%) vs published ICONIP (mAP 35.1–45.8) — row uses published; synthesis must cite published numbers only.
- [2026-09-08] P053 REVERSAL: full-text XML proved land-only ML training (one seawater demo, rivers as motivation only) — row deleted, Balsi context entry added, 50/50 restored. Lesson: B-prov grades without river-isolated evidence must not survive contact with full text.
- [2026-09-08] FINAL GRADES: A20/B13/C2/D15 across 50 included. Provisionals remaining: P040/41/44/46/47/50 (D), P049/52 (B) need PDF pass; P043-platform, P010-camera, P028-rigor residual.
- [2026-09-08] ASSEMBLY NOTES: MPFasterRCNN2024 authors + JiaFlux2025 venue verified and fixed in bib; all \cite keys resolve; environments balanced; fig:problem created; NO LaTeX toolchain on this machine — human must compile (pdflatex + bibtex) and report errors back.
- [2026-09-08] WRITING QC: all 12 sections drafted as \input-ready IEEE fragments (no preamble); master references.bib built — keys/DOIs need verification pass before compiling (esp. MPFasterRCNN2024 authors, JiaFlux2025 misc-entry, Lin2021b unused key); fig:problem (intro) does not exist yet — needs creation or reference drop; fig:prisma exists as TikZ (needs compile check); abstract ≤250 words ok; conclusion introduces no new studies (checked).
- [2026-09-08] CYCLE-1 WRITING FLAGS: (1) methodology.tex cites keys (Pati2025 etc.) with NO master references.bib yet — build refs file or switch to author-year placeholders before compiling; (2) flow numbers (~180/~70) are best-estimate, confirm wording; (3) P028 + P045 inclusion confirmed by human? (flagged in notes.md open questions); (4) scope.md still lists items as "proposed" — needs one-line human-confirmed stamp.

## Guidelines for Agents (Updated)
- Read ALL of these before starting: `direction.md`, `scope.md`, `base_published_paper/README.md`, `base_reference_systematic_review_paper/notes_for_agents.md`.
- When drafting, ask: Does this reflect rivers/ponds? Does it reference the base paper's key findings appropriately? Does it acknowledge the WIREs review as state-of-the-art? Does it claim PRISMA? (It should NOT.)
- Add any contradictions, missing citations, or scope drifts here before finishing.
Expanded collection started. Writing blocked at <50 papers.
