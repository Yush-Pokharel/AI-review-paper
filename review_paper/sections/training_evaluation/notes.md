# Training/Generalization + Evaluation — Notes (Cycles 6-7, RQ3/RQ4/RQ5)

## Training claims → IDs
- Scratch vs fine-tune vs frozen: P001 (seg→fine-tune wins; OD→frozen wins; mIoU 0.867/0.869; mAP 0.857/0.844); P006 (fine-tune marginally > frozen (3% vs 1%), both >> scratch; YOLOv3-spp 0.59→0.81); P008 (full-layer FTAL > classifier-only FTC; flip best DA); P030 (SGD-0.001 best, early-stop patience 50).
- Transfer cross-river: P001 (0.849/0.841 mIoU); P006 (TT→HMH +3%); P034 (Jakarta→Sarno +17% w/ dark-channel); P009 (unseen-region OK, Yangtze fail); P007 (~50% AP similar-sites; 50-object few-shot 20→42%); P027 (7-river→WLGCAM); P025 (no-retrain preprocessing 0.74→0.85); P012 (cross-site A).
- SSL/synthetic/UDA: P035 (teacher-student 75.1→77.7); P037 (SwAV +12.7% zero-shot); P038 (SSL+SAHI, +45 small items); P026 (AIGC synthetic→real); P051 (CDA-SSD-FT +13.4/8.3/9.4).
- Augmentation: P010 (mosaic+expansion +2.18); P013 (GSD-matched web supplement helps only combined); P014 BTS? (CBS arch); P034 (dark-channel); P032 (tiling/blurring); P008 (flip).
- Data-centric: P025 (preprocessing w/o retraining); P036 (index-reduced general model); P048 (benchmark honesty).

## Evaluation claims → IDs (task-scoped metrics; no cross-task pooling)
- OD: mAP@0.5 65–94%; AP-S crisis (P012 2.7–5.2; P040 small-target gains).
- Seg: mIoU 0.5 (satellite) → 0.87 (UAV); IoU 0.61 debris (P009); Dice/F1 (P004 0.86–0.92; P001).
- Classification: acc 83–95% (P005/P008/P011/P018).
- Speed/cost: report where present (P028 3.1ms; P029 30.5ms edge; P032 100ms TensorRT; P023 Pi; P012 Sep‡ 10×); absence stated elsewhere.
- Counting collapse: P031 6/32; P032 dense-aggregation unquantifiable; P038 3–4× under human.
