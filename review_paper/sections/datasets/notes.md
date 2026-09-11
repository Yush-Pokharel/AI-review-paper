# Datasets — Notes (Cycle 5, RQ1)

## Claims → IDs (master table columns: name/size/annot/cats/region/resolution/availability)
- P001: 764 tiles (343+421), YOLO-TXT + PNG masks, unified waste class, 256px, Nepal UAV, public GitHub.
- P004: 328/434/1846 patches 256px, pixel multi-class, Bosnia lake+river, not stated.
- P006: 500 tiles/site 256px 2m, YOLO boxes, Laos+Thailand, not stated.
- P008: 9,473 imgs, 4-level litter classes, NL canal, OPEN (TUD-GV).
- P009: multi-date Drina/LA/Yangtze pixel labels (water/debris/other), release TBD.
- P010: 2,400 imgs (1,920→4,800), 8 classes VOC boxes, waterway, not stated.
- P012: 13,500 imgs, 48,450 objs, boxes+masks, Lahore canals, Partial (URL).
- P013: Original + Public-PET + Random-PET (web Xinxiang), Asahi, not released.
- P016: lab flume 7 classes, 5,711 test; P025: +2,000 CCTV canal frames.
- P017: HRB-WD open + .pt weights, smartphone, Japan.
- P023: custom bottles, not stated. P024: 340 imgs Jakarta. P027: 7,356 + 3,802 WLGCAM, Japan. P030: PH custom imbalanced. P031: 4,162 + 1,005 bg, Korea. P033: ~800 Rhine patches. P036: PlanetScope-annotated → Sentinel-2, GEE app Partial. P038: open code+data (GitHub+Zenodo). P040/P010 shared 8-class scheme (lineage flag). P042: ~15k, 69k+57k. P048: FloW 2,000/5,271 + videos + radar (benchmark).
- Gaps: underwater none; geographic skew (Europe/E.Asia over-represented; Africa/S.America sparse per Atuhaire25); small/underwater/transparent items under-annotated; mass/flux labels rare.
