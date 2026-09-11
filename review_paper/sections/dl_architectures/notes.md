# DL Architectures — Notes (Cycle 4, RQ2)

## Claims → IDs
- YOLO bulk (v2–v10, RT-DETR-era): P006 (v2-v5, v5s best tradeoff; v4 localization), P010 (FMA-v5s 79.41), P012 (v3+Attn), P013 (v5l vs RetinaNet), P014 (CBS 90.85/92.18), P015 (opt-v4 89%), P016/25 (v5/v10m), P017 (v8n-seg), P023 (v5 edge), P027 (v8-IS), P028 (v8s-LSKA 77.9), P029 (EFD-v8 edge), P030 (v8 87.2), P031 (v8n 0.992), P032 (v8 networked), P033 (v5x 94%), P034 (v7/v8 + dark-channel), P039 (v7-GFPN 86.3), P041 (v5-SIoU-softNMS 86.3), P042 (v8 hyacinth), P044 (Scaled-v4), P046 (v5s efficient).
- Faster R-CNN/RetinaNet: P007 (68.7%), P012 (43.4), P037 (SwAV backbone), P038, P043 (MP 71.39), P048 (benchmark).
- SSD: P035 (teacher-student), P049 (Deqing 91.1), P051 (UDA-SSD 82.2%).
- U-Net/DeepLab: P001 (DV3+ best), P004 (ResUNet50), P009 (U-Net3DE/DV3X), P017.
- Mask R-CNN: P047 (riverbank quant); ISDA-bottles excluded (non-aquatic).
- Transformers: P001 argues CNNs for small data (no transformer tested); TAUNet-marine excluded; DETR discussed in P001 text only (YOLO better small/dense per Yuan cited); Drone-DETR VisDrone excluded (generic). Gap: ~zero river-transformer studies.
- SAM/foundation: P017 (SAM baseline loses to custom v8n-seg); P026 (Stable Diffusion synthetic); P037 (SwAV foundational direction).
- Mamba: P035 Changemamba (first).
- Speed/accuracy: edge rows P023 (Pi), P028 (3.1ms), P029 (RK3588 30.5ms), P032 (TensorRT 100ms), P012 (Sep‡ 10× smaller).
