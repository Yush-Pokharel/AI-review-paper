# Data Sources — Notes (Cycle 2, RQ1)

## Claims → IDs
- UAV dominant, high-res (mm–cm GSD), costly/limited coverage → P001 (35m, 0.61cm), P004 (12–90m, 4–30mm), P006 (30m, 0.82cm), P018 (20–80m multispectral; precision collapses 89.7→33.9 with altitude), P027 WLGCAM fixed-cam network.
- Satellite: Sentinel-2 10–60m, broad coverage, small-item blind → P009 (unseen-region OK, Yangtze fail), P019 (val→test F1 collapse), P020 (riverbank API), P036 (3-river F1 79%, GEE app); commercial high-res (Pleiades 0.5m) as validator (P020).
- Ground/fixed: bridge/canal cameras, continuous, cheap, static FOV → P007 (Jakarta 5 rivers), P024 (Jakarta video + counting), P031 (Korea stream, counting collapse 6/32), P033 (Rhine bridge), P032 (pontoon + UAV dual).
- Handheld/phone: citizen-science potential, inconsistent → P008 (GoPro/Huawei), P012 (IoT nodes Lahore), P017 (smartphone HRB-WD), P030 (PH waterways).
- USV/boat: P048 (FloW USV + radar, first), P039 (unmanned boat), P032 (pontoon).
- Underwater: NONE in corpus (P002 scope-excluded; P004 shallow-water only) → state gap, no invention.
- Hyperspectral: P011 (lab→field SAM 93.6%), P018 (MAIA-S2 9-band), P022 (handheld MAIA), Alboody-context (aquatic drone).
- Multispectral: P018, P021 (MicaSense), P009/P019/P020/P036 (Sentinel-2 + indices).
