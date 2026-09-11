# RQ → SECTION MAPPING (Synthesis Framework)

Purpose: Ensure each review section directly addresses the 6 RQs defined in `synthesis/research_questions/rq_framework.md`.

## Mapping

### RQ1 — Datasets & Platforms
- Sections: `data_sources/` (UAV, satellite, ground, underwater comparison); `datasets/` (master comparison table using taxonomy Level 2, 3, 10)
- Key papers: P001 (UAV RGB, 764 tiles), P002 (satellite/UAS/ground review), P009 (satellite multispectral, cross-region), P011 (hyperspectral lab→field), P027 (7-river multi-platform)
- Taxonomy tags: Level 2 (platform), Level 3 (spectral), Level 4 (waste category), Level 10 (dataset availability)
- Synthesis table: dataset comparison (size, annotation, geographic diversity, public/private)

### RQ2 — Computer Vision & Deep Learning Approaches
- Sections: `detection_approaches/` (classification → detection → segmentation → instance); `dl_architectures/` (YOLO family, Faster R-CNN, SSD, U-Net, DeepLab, Mask R-CNN, transformers, newer architectures)
- Key papers: P001 (DeepLabv3+, YOLOv5/7; CNN preferred); P003 (review: CNN vs transformer barriers); P006 (Faster R-CNN + Inception, fixed camera); P010 (YOLOv5s + FMA attention; CNN only); P031 (YOLOv8n counting gap); P037 (SwAV SSL — new architecture category); P038 (flux quantification — new architecture category)
- Taxonomy tags: Level 5 (task), Level 6 (DL family: CNN, Transformer, SSL, Hybrid)
- Synthesis theme: CNN dominates river waste; transformers rare (P001 justification); SSL emerging (P037/P038); newer architectures (SAM, ConvNeXt) largely absent (gap)

### RQ3 — Detection vs Segmentation
- Sections: `evaluation/`; `detection_approaches/`; `challenges_future/`
- Key papers: P001 (DeepLabv3+ segmentation outperforms YOLO detection: precision 0.915 vs lower detection scores; mIoU 0.867/0.869); P031 (YOLOv8n detection mAP 0.99 but counting 6/32 — C008 contradiction: detection ≠ quantification)
- Taxonomy tags: Level 5 (task type comparison); Level 9 (metrics comparison: mAP vs IoU vs F1 vs counting accuracy)
- Synthesis theme: segmentation more accurate for pixel-level waste estimation; object detection faster/easier for density monitoring but quantification unreliable (C008); standard metrics insufficient for monitoring applications

### RQ4 — Training & Transfer-Learning Strategies
- Sections: `training_evaluation/` (scratch, fine-tuning, frozen, transfer learning, domain adaptation); `datasets/` (limited dataset sizes); `dl_architectures/` (pretrained vs scratch)
- Key papers: P001 (scratch vs fine-tune vs frozen backbone comparison; transfer learning cross-river improves mIoU 0.849/0.841); P003 (training strategy review); P006 (pretrained ImageNet, frozen backbone best for detection); P037 (SSL zero-shot +12.7% AP — new training category); P025 (Nunkhaw 2025 resolves P016 claim-only with lab→field evidence); P027 (intermediate-weights best — architecture/training interaction); P032 (networked multi-river system — cross-river training potential)
- Taxonomy tags: Level 7 (training strategy: scratch, fine-tune, frozen, transfer, domain adaptation, SSL); Level 8 (generalization: cross-river, cross-region, cross-environment, cross-dataset, model transfer, representation transfer)
- Synthesis theme: fine-tuning best for segmentation; frozen backbone best for detection (P001); transfer learning improves generalization but dataset size limits (P001 small dataset); SSL shows promise (P037) but needs larger datasets; cross-environment transfer rare (only P001, P025, P009, P027 demonstrate experimentally; most papers claim without external test — C-grade)

### RQ5 — Generalization Across Environments
- Sections: `evaluation/`; `challenges_future/`; `data_sources/` (cross-sensor comparison)
- Key papers: P001 (cross-river A — Bagmati↔Bishnumati); P009 (satellite cross-region A — multi-river→Yangtze); P025 (lab→field A — resolves P016 C); P027 (7-river A — cross-river + cross-resolution); P032 (networked multi-river B — potential cross-river but not fully tested); P037 (SSL zero-shot cross-location A — representation transfer); P038 (flux quantification A — open data)
- Contradictions: C006 (satellite cross-region vs UAV same-basin trade-off — not contradiction but modality difference); C007 (satellite ML degrades while DL holds — architecture matters for generalization); C008 (P031: detection mAP 0.99 ≠ quantification 6/32 — detection metrics don't predict monitoring reliability)
- Taxonomy tags: Level 8 (8A within-environment, 8B cross-river/region/environment, 8C cross-sensor/resolution, 8D cross-dataset, 8E methodological transfer, 8F model/domain adaptation, 8G representation/foundation); Level 9 (performance drop metrics: absolute/relative change across environments)
- Synthesis theme: Most papers claim generalization without external test (C-grade); only P001, P009, P025, P027, P032, P037 demonstrate experimentally (A-grade); cross-environment tests extremely rare; underwater cameras and newer architectures (transformers, SAM) largely absent (gaps); representation transfer (SSL, P037) is emerging but limited; domain adaptation explicitly tested very rarely

### RQ6 — Limitations & Research Gaps
- Sections: `challenges_future/`; `datasets/`; `methodology/` (quality assessment); `conclusion/`
- Evidence from extraction table + contradiction tracker + gap framework:
  - Data gaps: few public river datasets (P001 public but small; P011 open data; P032 dataset status unclear); underwater cameras underexplored (P002 excludes; almost no studies in extraction table); multi-river datasets rare (P001 2 rivers; P027 7 rivers is exception)
  - Methodology gaps: no standardized evaluation protocol (P002 calls for this; P001 metrics inconsistent — C005 attribution error); detection metrics (mAP, IoU) don't predict quantification reliability (C008 P031); augmentation rarely reported (P001 not stated); observation periods rarely reported (P001 TBD)
  - Generalization gaps: very few cross-river/cross-region tests (only P001, P009, P025, P027, P032); most studies claim robustness without appropriate external test (C-grade prevalence); cross-season/cross-weather missing; cross-sensor (UAV→satellite→underwater) almost absent
  - Platform gaps: UAV dominates; satellite studies limited to high-flow/large rivers (P002 notes); underwater cameras excluded (P002); ground cameras mainly fixed/handheld (P006, P012, P007)
  - Architecture gaps: transformers rarely applied (P001 notes barriers; no transformer study found in extraction table except discussion); newer architectures (SAM, ConvNeXt) absent from river studies; SSL emerging (P037) but very new (2024)
  - Geographic gaps: Nepal (P001), Bosnia (P004), Netherlands (P011), Jakarta/Indonesia (P024, P025), Italy (P027 multi-river), global satellite (P009) — Africa, South America, Southeast Asia underrepresented
  - Environmental condition gaps: season/weather/light/turbidity diversity almost never tested (P001 no season data; P025 lab→field different conditions but not systematic cross-season); cross-season studies absent
- Context references (`context_notes.md`): Zhao 2024 (microplastic dominance), Blettler 2018 (freshwater pollution increase), Gallitelli 2022 (standardization gap), Cook 2021 (citizen science standardization), Winton 2020 (freshwater monitoring limitations), RiverWatch 2024, Rochman 2018, Schmidt 2017, Mennekes 2024, Oswald 2025, Hurley 2023, Lebreton/Andrady 2019, Jambeck 2015, Meijer 2021
- Synthesis structure: group gaps by taxonomy level (data, method, generalization, platform, architecture, geography, conditions) with evidence from extraction table; reference contradictions (C001-C009) to show unresolved tensions; reference context papers for broader literature confirmation
