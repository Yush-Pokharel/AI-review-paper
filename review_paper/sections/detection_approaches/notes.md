# Detection Approaches — Notes (Cycle 3, RQ2/RQ3)

## Claims → IDs
- Classification (image-level; density/level labels): P005 (PLD low/high + PLQ 11 sub-classes, 83/71%), P008 (4 litter-level classes, DenseNet 91.7%), P011 (pixel classification SAM 93.6%), P018/19/20/21/22, P036 (hotspot RF), P045 (blockage state, scoped adjacent).
- Object detection (boxes; dominant): P006/7/10/12/13/14/15/23/24/25/27-32/33/34/39/40/41/43/44/46/47/48/49/50/51/52 (YOLO family bulk).
- Semantic segmentation (pixel masks): P001 (DeepLabv3+ best), P004 (ResUNet50), P009 (U-Net/DV3+).
- Instance segmentation (mask + ID; emerging, 2 rows): P017 (YOLOv8n-seg custom beats COCO/SAM), P027 (YOLOv8-IS 7-river + WLGCAM).
- OD-vs-IS comparison on same data: P001 (seg wins precision/recall), P027 (GSD-direction flip: small-GSD→IS, large-GSD→OD), P012 (both heads, attention + separable-conv + focal).
- Tracking/counting overlay: P016/P024/P025/P031/P032/P047 (DeepSORT, counter-line, SAHI).
