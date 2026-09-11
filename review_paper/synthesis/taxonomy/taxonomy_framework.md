# TAXONOMY FRAMEWORK — What Categories Must Be Extracted

Agents use this when reading papers to ensure consistent categorization.

## Taxonomy Levels

### Level 1: Environment (Water Body Type)
- River (named)
- Pond / Lake
- Canal / Channel
- Reservoir / Dam
- Estuary / Outflow
- Multiple (specify)

### Level 2: Imaging Platform (RQ1)
- UAV / Drone (low-altitude, high-resolution)
- UAV / Drone (high-altitude)
- Satellite (Sentinel-2, Pleiades, WorldView, etc.)
- Ground Camera — Fixed (bridge-mounted, bank-mounted)
- Ground Camera — Handheld
- Ground Camera — Mobile (vehicle-mounted)
- Underwater Camera (submerged, floating, ROV/AUV)
- Multi-platform (specify which)

### Level 3: Image Type / Spectral Range
- RGB (visible only)
- Multispectral (specific bands — note which)
- Hyperspectral
- SAR (Synthetic Aperture Radar)
- LiDAR
- Mixed / Fused

### Level 4: Waste Category (RQ1 / RQ6)
- Macroplastic (≥5mm, visible)
- Mesoplastic (5-25mm)
- Mixed plastic sizes
- Floating plastic specifically
- Non-plastic waste (organic, metal, glass — note if mixed with plastic)
- Unspecified waste / litter

### Level 5: Task Type (RQ2 / RQ3)
- Classification (image-level: waste / no waste, or multi-class)
- Object Detection (bounding box: single-class or multi-class)
- Semantic Segmentation (pixel-level: waste vs. background)
- Instance Segmentation (pixel-level + instance identity)
- Multi-task (e.g., detection + segmentation in one model)

### Level 6: Deep Learning Approach (RQ2)
- CNN family: YOLO (v3-v11, RT-DETR), Faster R-CNN, SSD, RetinaNet, etc.
- Segmentation: U-Net (and variants: U-Net++, Attention U-Net), DeepLab (v2/v3/v3+), FCN, PSPNet
- Instance Segmentation: Mask R-CNN, YOLACT, SOLO
- Transformer-based: ViT, Swin Transformer, DETR, Deformable DETR, SAM (Segment Anything)
- Hybrid / Newer: ConvNeXt, YOLO-World, etc.

### Level 7: Training Strategy (RQ4)
- From scratch (no pretraining)
- Fine-tuning (full model, pretrained weights — specify source: ImageNet, COCO, etc.)
- Fine-tuning with frozen layers / frozen backbone
- Transfer learning — cross-river (same domain, different location)
- Transfer learning — cross-region / cross-country
- Transfer learning — cross-dataset
- Domain adaptation (explicit method: adversarial, feature alignment, etc.)
- Data augmentation (list types: geometric, photometric, synthetic)
- Synthetic data / simulation

### Level 8: Generalization Type / Scope (RQ5 — BROAD DEFINITION)
Note: A single paper may demonstrate multiple types. Tag all that apply.

#### 8A — Within-Environment
- Same river / same dataset (no generalization tested — baseline)
- Same river / different area within river
- Same river / different season
- Same river / different weather / lighting / turbidity

#### 8B — Cross-Location / Cross-Environment
- Cross-river (same region, different river — e.g., Bagmati → Bishnumati)
- Cross-region / cross-country
- Cross-environment: river → pond / lake
- Cross-environment: river / freshwater → coastal / estuary / marine
- Cross-environment: river → canal / reservoir / dam outflow

#### 8C — Cross-Platform / Cross-Resolution / Cross-Sensor
- Cross-sensor: UAV → satellite (same area, different resolution)
- Cross-sensor: UAV → ground camera / handheld
- Cross-sensor: UAV → underwater camera
- Cross-resolution: high-res → low-res (or vice versa)
- Cross-resolution: same sensor, different GSD / altitude
- Multi-platform fusion (combining sources for generalization)

#### 8D — Cross-Dataset / Cross-Annotation
- Cross-dataset: different dataset, same environment type
- Cross-dataset: different annotation quality / format
- Cross-dataset: synthetic → real (or real → synthetic evaluation)

#### 8E — Cross-Model / Methodological Transfer
- Methodological transfer: detection approach developed for riverine waste adapted to coastal / marine / pond / other environment (same or different model architecture)
- Architecture comparison across environments: YOLO tested on river, YOLO tested on coastal — compare whether relative performance holds

#### 8F — Transfer Learning / Domain Adaptation
- Model transfer: weights from Source A fine-tuned / evaluated on Target B (explicit)
- Domain adaptation: feature-level / adversarial / alignment methods used to adapt across environments
- Frozen layers / partial fine-tuning as generalization strategy

#### 8G — Representation / Foundation / Self-Supervised Transfer
- Features learned from general vision (ImageNet, COCO) applied to waste detection (standard pretraining — note source)
- Self-supervised / contrastive pretraining on environmental images applied to waste
- Foundation model (SAM, etc.) applied to river waste without task-specific fine-tuning, or with light fine-tuning
- Cross-domain representation: features from marine/satellite pretraining used for river detection (or vice versa)

### Level 9: Performance Metrics Reported (RQ3 / RQ5)
- Classification: Accuracy, Precision, Recall, F1, AUC-ROC
- Object Detection: mAP (mean Average Precision), mAP@0.5, mAP@0.75, Precision, Recall
- Segmentation: IoU, mIoU, Pixel Accuracy, Dice Coefficient
- Generalization: Performance drop (absolute or % change) across environments
- Efficiency: Inference speed (FPS), model size (parameters), FLOPs, GPU memory

### Level 10: Dataset Availability
- Public (URL or repository)
- Private / Not released
- Partial (some images available, annotations private; or vice versa)
- Not stated

Agents: When extracting a paper, tag the row with relevant taxonomy levels (e.g., `Level 2: UAV`, `Level 6: DeepLabv3+`, `Level 7: Fine-tune frozen backbone`, `Level 8: Cross-river`).
