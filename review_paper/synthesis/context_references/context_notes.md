# CONTEXT / BACKGROUND REFERENCES (Not Primary Data)

These papers are cited in seed papers (P001, P002) or discovered during tracking, but serve as background/evidence for claims rather than primary extraction targets.

## Zhao et al. (2024) — Freshwater Plastic Pollution Trends
- Source: Cited in `base_reference_systematic_review_paper/` `.md` file (line ~47-48): "Research on freshwater plastic pollution has increased in recent years; however, much of the scientific focus remains on microplastics [Blettler et al. 2018; Gallitelli and Scalici 2022; Zhao et al. 2024]".
- Role: Context/reference — supports gap claim that macroplastic river studies are fewer than microplastic studies.
- Incorporation plan:
  1. Add as citation in `introduction/` when framing why macroplastic detection (not microplastic) is the review focus.
  2. Add as citation in `challenges_future/` when discussing the imbalance between microplastic and macroplastic research in freshwater.
  3. Do NOT add to `extraction_table/` unless full text confirms it is an original DL + aquatic experiment (unlikely — appears to be a review/trend analysis).
- Full citation (Phase 2 confirmed, P002 .md line 631): Zhao, B., R. E. Richardson, and F. You. 2024. "Microplastics Monitoring in Freshwater Systems: A Review of Global Efforts, Knowledge Gaps, and Research Priorities." *Journal of Hazardous Materials* 477:135329.
- Verdict: microplastics review → CONTEXT ONLY, confirmed NOT primary data (fails criteria_final #1 macro/waste-DL focus and #3). Never add as P-row; cite for RQ6 gap claims in introduction/ + challenges_future/ as planned above.

## Other Potential Context References (From P002 References Section)
- Blettler et al. (2018) — microplastic freshwater review
- Gallitelli and Scalici (2022) — freshwater plastic review
- Cook et al. (2021) — citizen science / freshwater standardization gap
- Winton et al. (2020) — freshwater monitoring limitations

## Blettler et al. 2018 — Microplastic Freshwater Review
- Citation: Blettler, M. C. M., M. A. Ulla, and A. I. Rabuffetti. 2018. "Freshwater plastic pollution: A global review." (Full citation to be confirmed; cited in P002 `.md`).
- Role: CONTEXT — supports trend claim (freshwater plastic pollution increasing; focus on microplastics).
- RQ links: RQ6 (gap), introduction framing.
- Note: Not primary DL data; do not add to `extraction_table/`.

## Gallitelli and Scalici 2022 — Freshwater Plastic Review
- Citation: Gallitelli, L., and F. Scalici. 2022. (Full citation confirmed via P002 reference list; freshwater plastic pollution review).
- Role: CONTEXT — complements Zhao 2024; supports standardization gap.
- RQ links: RQ6 (gap), `challenges_future/` (standardized protocols lacking).
- Note: Review/survey — not primary extraction target.

## Cook et al. 2021 — Citizen Science / Standardization Gap
- Citation: Cook, S., et al. 2021. "Goals and approaches in the use of citizen science for exploring plastic pollution in freshwater ecosystems: A review." (Cited in P002 `.md`; full citation to confirm).
- Role: CONTEXT — supports RQ6 gap claim (standardized methodologies for citizen science/recruiting/training lacking).
- RQ links: RQ6, `challenges_future/` (methodology standardization).

## Winton et al. 2020 — Freshwater Monitoring Limitations
- Citation: Winton, R. S., et al. 2020. (Full citation from P002 `.md`; freshwater plastic monitoring limitations).
- Role: CONTEXT — supports data scarcity and monitoring challenge claims.
- RQ links: RQ6, `datasets/` (limited spatial/temporal coverage).

## RiverWatch (2024) — Citizen-Science Approach to River Pollution Monitoring
- Source: User-provided URL / PRIN project reference: `https://riverwatch-prin.github.io/`
- Citation (to confirm from source): RiverWatch Project. 2024. "RiverWatch: A Citizen-Science Approach to Pollution Monitoring." Italian Ministry of University and Research (PRIN 2022MMBA8X).
- Role: CONTEXT — supports RQ6 claim (standardized citizen-science protocols for river monitoring are emerging but not yet harmonized globally; complements Cook 2021 gap).
- RQ links: RQ6 (`challenges_future/`: citizen-science standardization needs), `introduction/` (Nepal/river context — citizen science as future direction for resource-limited regions).
- Note: Not an original DL + aquatic waste experiment; context/background only. Do not add to `extraction_table/`.

## Rochman C. M. (2018) — Microplastics Research: Sink to Source
- Citation: Rochman, C. M. 2018. "Microplastics Research—From Sink to Source." *Science* 360, no. 6384: 28–29.
- Source: Cited in P002 `.md` (line ~31 reference chain: ecotoxicology/risk assessment literature).
- Role: CONTEXT — supports RQ6 gap claim (microplastic focus dominates health/ecotoxicology literature; macroplastic river sources less studied).
- RQ links: RQ6 (`challenges_future/`), `introduction/` (why macroplastic detection matters for source-tracking).
- Note: Short perspective/review — context only.

## Schmidt, Krauth, and Wagner (2017) — Plastic Debris Export by Rivers
- Citation: Schmidt, C., T. Krauth, and S. Wagner. 2017. "Export of Plastic Debris by Rivers Into the Sea." *Environmental Science & Technology* 51, no. 21: 12246–12253.
- Source: Cited in P002 `.md` (line ~26 reference; also cited in base paper `.bib` reference chain on riverine plastic emissions).
- Role: CONTEXT — provides quantitative baseline for riverine plastic emissions to oceans; supports RQ1 platform comparison claim (why river monitoring is critical for marine pollution sources).
- RQ links: RQ1 (`data_sources/`: river as transport pathway), RQ6 (`challenges_future/`: river-to-ocean flux measurement limitations), `introduction/` (global magnitude of river pollution).
- Note: Not DL + aquatic waste; quantitative review/modeling study — context only.

## Additional Context References (From P002 References / User Tracking)
- Mennekes et al. 2024 — freshwater plastic dynamics/sink behavior (P002 `.md` line ~31 reference chain)
- Oswald et al. 2025 — freshwater plastic dynamics (P002 `.md` line ~31)
- Hurley et al. 2023 — see full entry below (Connected-Papers batch; duplicate one-liner removed 2026-09-08)
- Lebreton and Andrady 2019 — flooding/plastic clogging risk (P002 `.md` line ~30 reference chain; Nepal context relevance)
- Jambeck et al. 2015 — global mismanaged waste baseline (P002 `.md` line ~20 reference chain)
- Meijer et al. 2021 — 1000 rivers account for 80% emissions (P002 `.md` line ~20; base paper `.tex` reference)

Note: These are cited extensively in P002 and base paper `.bib`; they serve as background evidence for gap claims and should be cited where relevant in synthesis sections (`introduction/`, `challenges_future/`, `datasets/`, `conclusion/`). They are NOT primary DL + aquatic waste studies and must NOT be added to `extraction_table/`.

Agents: When these are encountered, determine:
1. Is it an original experiment with DL + aquatic waste? → Add to extraction table.
2. Is it a review/survey/trend analysis? → Add to this file for citation in introduction/conclusion/gaps.
3. Does it provide unique dataset/method comparison data not covered by original sources? → Note in `extraction_table/template.md` `notes` field of relevant paper.

## Connected-Papers Context Batch, Part 2 — Vegetation, Hotspots, Geography (2026-09-08)

### Schreyers et al. 2024a/b + Lotcheris et al. 2024 — Hyacinth Retention/Transport (Saigon)
- Citations: Schreyers et al. 2024a (one-year Thu Thiem, up to 77% entrapped); Schreyers et al. 2024b (methods); Lotcheris et al. 2024 (GPS trackers, >80% trapped over 40km). (Full citations to confirm; P002 `.md`/P042 chains.)
- Role: CONTEXT — multi-study vegetation-entrapment evidence backing P042 (73% at 42km scale); transparent/hyacinth misses explain P038 flux underestimation.
- RQ links: RQ6 (`challenges_future/`: vegetation-confound as first-class detection challenge), `datasets/` (annotation must label entrapped vs free-floating).
- Note: Field studies, no DL detection experiment — context only; upgrades Schreyers-2021 already noted.

### Tasseron et al. 2024 — Hotspot Definition (STOTEN 173294)
- Citation: Tasseron, P., et al. 2024. "Defining plastic pollution hotspots." *Sci Total Environ* (doi 10.1016/J.SCITOTENV.2024.173294).
- Role: CONTEXT — hotspot definition framework for P036/P019/P020 accumulation-mapping claims; RQ6 quantification strand.
- RQ links: RQ6, `evaluation/` (what counts as a mappable hotspot).
- Note: Methods/framework — not a detection experiment.

### Atuhaire et al. 2025 — Freshwater RS Review (Sci African e02833)
- Citation: Atuhaire, C., et al. 2025. "Prospects of remote sensing for monitoring plastic litter in freshwater environments: A systematic review." *Scientific African* (doi 10.1016/j.sciaf.2025.e02833; 28 studies 2010–2024).
- Role: CONTEXT — third review voice; documents Africa/Australia/S.America gap + drone-GSD non-standardization + marine-derived spectra insufficiency for freshwaters.
- RQ links: RQ6 (geographic + protocol gaps), `introduction/` (literature landscape: P002, P003, Gnann22, Atuhaire25).
- Note: Review — context only; already in pending log.

### Global-South & Regional Field Set — Geographic-Gap Evidence (grouped)
- Studies (all field/monitoring, no DL detection → context only): Bago River Myanmar (sources/dynamics); Sabaki/Tana Kenya water-column + riverbank macro/mesoplastics (2024/25); Odaw River Ghana (transport dynamics; cf. P002 refs); Patagonia mountain streams (urban vs pristine riparian); Durance riverbank France; Rhine–Meuse Dutch delta riverbank; Swiss freshwaters land-use; Marseille urban river; Manila river mouths (temporary sinks); Chao Phraya estuary drifters (retention–remobilisation).
- Role: CONTEXT — geographic-diversity evidence for RQ6 gap claim (Asia/Europe/N.America over-represented; Africa/S.America sparse) + Nepal/Global-South framing (comparable monsoon-urban rivers: Bago, Odaw, Sabaki/Tana pair with P001/P006/P024 Asian contexts).
- RQ links: RQ6 (`challenges_future/`), `introduction/` (why Nepal-relevant review matters globally).
- Note: Full citations to confirm at synthesis; cite as a group ("field studies across X rivers in under-represented regions report...") never as detection evidence.

## Connected-Papers Context Batch (2026-09-08; source: resources/connected_papers/*.bib)

### Gnann et al. 2022 — Close-Range Macroplastic-ID Review
- Citation: Gnann, N., Baschek, B., and Ternes, T. A. 2022. "Close-range remote sensing-based detection and identification of macroplastics on water assisted by artificial intelligence: A review." *Water Research* 222:118902.
- Role: CONTEXT — second review voice on close-range/water AI identification; states ML/DL still in infancy vs visual monitoring on accuracy/detail despite promise; flags data availability/accessibility bottleneck.
- RQ links: RQ6 (`challenges_future/`: accuracy-vs-visual gap, data-availability barrier), `introduction/` (why rigorous comparison like P001 is needed).
- Note: Review — not primary data; complements P002 (platforms) + P003 (DL architectures) with close-range verdict.

### Olyaei et al. 2024 — River Hyperspectral Reflectance Database
- Citation: Olyaei, M. A., Ebtehaj, A., and Ellis, C. R. 2024. "A Hyperspectral Reflectance Database of Plastic Debris with Different Fractional Abundance in River Systems." *Scientific Data* (doi 10.1038/S41597-024-03974-X).
- Role: CONTEXT — open spectral library for river plastics at fractional abundance; underpins subpixel-detection claims (cf. Cerra unmixing note, P009/P019 resolution limits).
- RQ links: RQ1 (`datasets/`: spectral resources), RQ6 (subpixel/small-target gap).
- Note: Database, not a detection experiment; cite as resource, never as performance evidence.

### Garaba & Park 2023 — Fine-Pixel Satellite Riverine Monitoring (Guatemala/Slovakia)
- Citation: Garaba, S. P., and Park, Y.-J. 2023. "Riverine litter monitoring from multispectral fine pixel satellite images." *Environmental Advances* (doi 10.1016/j.envadv.2023.100451).
- Role: CONTEXT — statistical (non-learning) anomaly→fractional-abundance method; cross-sensor consistency R²=0.98, manual R²>0.99; transferability demo Guatemala + Slovakia; sub-daily revisit case.
- RQ links: RQ5 (`evaluation/`: transferability benchmark without DL), RQ6 (high-res commercial imagery access/cost gap vs Sentinel-2 rows P009/P019/P020).
- Note: No learning component — excluded as primary (cf. Cerra rule); cite for transferability/monitoring-design claims only.

### Alboody et al. 2023 — Aquatic-Drone Hyperspectral System (RS 15:3455)
- Citation: Alboody, A., et al. 2023. "A New Remote Hyperspectral Imaging System Embedded on an Unmanned Aquatic Drone..." *Remote Sensing* 15:3455.
- Role: CONTEXT — near-field (45cm) NIR–SWIR system on Jellyfishbot aquatic drone; ~90% polymer classification (lab marine-item benchmark); designed for confined waterways/estuaries/rivers.
- RQ links: `future_directions/` (aquatic-drone + hyperspectral platform novelty), RQ1 platform comparison (unmanned surface viewpoint; pairs P048 USV row).
- Note: Lab + marine-item focus — not primary; cite for platform-future claims, not river performance.

### Hurley et al. 2023 — Methods/Harmonisation/QC (Water Res 235:119902)
- Citation: Hurley, R., et al. 2023. "Measuring riverine macroplastic: Methods, harmonisation, and quality control." *Water Research* 235:119902. (Promoted from one-liner; P002 `.md` lines ~64/71 chain.)
- Role: CONTEXT — harmonised monitoring + QC standard; frames P001's metric inconsistencies (C004/C005) as field-wide problem.
- RQ links: RQ6 (`challenges_future/`: standardization), methodology discussion (reporting discipline).
- Note: Methods review — not DL data.

### Kataoka & Nihei 2020 — Classical Flux Baseline (Sci Rep 10:2198)
- Citation: Kataoka, T., and Nihei, Y. 2020. "Quantification of floating riverine macro-debris transport using an image processing approach." *Scientific Reports* 10:2198 (Edo River; difference-image + threshold + template matching; r=0.983 vs visual).
- Role: CONTEXT — pre-DL classical baseline for flux quantification; anchors P038/P031/P024 DL-flux advances (what DL replaced and what classical r=0.983 still sets as bar).
- RQ links: RQ6 (flux-quantification lineage), `evaluation/` (classical-vs-DL comparison point).
- Note: No learning — excluded as primary; cite for methods-lineage claims.

### Wolf et al. EGU22 — Bridge + Net, Submerged Fraction (Vietnam/Cambodia)
- Citation: Wolf, M., et al. 2022. EGU22-11959 (abstract; Cambodia-drone → Vietnam bridge action-cam lineage of P005 APLASTIC-Q).
- Role: CONTEXT — ~50% of litter transported at surface (rest submerged → AI-invisible); net-calibration design for total-transport extrapolation.
- RQ links: RQ6 (`challenges_future/`: submerged-blindness gap — pairs P038 hyacinth/transparency misses, P025 no-submerged limit), P005 lineage note.
- Note: Abstract only — cite numbers cautiously ("~50% reported in conference abstract, journal version pending").

### Balsi et al. 2025 — Drone SWIR Hyperspectral (RS 17:938) [REVERSED 2026-09-08]
- Citation: Balsi, M., Moroni, M., and Bouchelaghem, S. 2025. "Plastic Litter Detection in the Environment Using Hyperspectral Aerial Remote Sensing and Machine Learning." *Remote Sensing* 17:938.
- Role: CONTEXT — was P053 (provisional row, now removed). Full-text XML proved ML training is ALL land (grass/bare ground); only one seawater-floating demo; riverbanks cited as motivation only, no river experiment → fails criterion #2 for primary status.
- RQ links: `future_directions/` (SWIR modality + 1030nm no-recalibration deployment + LOO-across-flights protocol as methodological exemplar), RQ1 platform comparison (drone-SWIR vs RGB/multispectral rows).
- Note: Cite for modality-future claims only, never as river performance evidence. Count restored to 50/50.

## Zhao et al. 2024 — Incorporation Plan (Updated)
- Source: WIREs Water 2025 (`base_reference_systematic_review_paper/`) `.md` file (line ~47-48): "Research on freshwater plastic pollution has increased in recent years; however, much of the scientific focus remains on microplastics [Blettler et al. 2018; Gallitelli and Scalici 2022; Zhao et al. 2024]"
- Full citation: Zhao, Richardson & You 2024, Journal of Hazardous Materials, 477:135329 (`JHM` 2024, DOI: 10.1016/j.jhazmat.2024.135329). Confirmed via `.bib` / reference tracking.
- Role: CONTEXT / BACKGROUND reference (not primary data). Supports RQ6 gap claim: macroplastic river studies are fewer than microplastic studies.
- Incorporation:
  - `introduction/`: Frame macroplastic focus ("While freshwater plastic pollution research has grown [Zhao 2024; Blettler 2018], much focus remains on microplastics [Gallitelli 2022], leaving macroplastic river monitoring underexplored [WIREs 2025 review]").")
  - `challenges_future/`: Support gap claim ("Standardized macroplastic monitoring remains limited; most freshwater studies address microplastics [Zhao 2024], not floating macroplastics measurable by UAV/satellite [P002]").")
  - `datasets/`: Reference for dataset diversity gap (microplastic studies dominate literature; macroplastic river datasets like P001's are rare and not public [contrast with P001 datasetPublic Yes but small scale]").")
