# SEARCH LOG — To Be Filled During Extraction Phase

Agents must log every search action here. Use the format below.

## Format
```
[Date] [Agent] [Search Type] [Source/DB] [Query / Seed] [Results Returned] [Screened] [Included] [Excluded] [Notes]
```

## Entries

### Search 1: Backward Citation Tracking — Seed 1 (Pati et al.)
- [2026-09-07] HUMAN [Setup] [Seed Backward] `base_published_paper/references.bib` [Extracted references — count TBD] [TBD] [TBD] [TBD] [Awaiting agent extraction]
- [2026-09-08] PHASE1-AGENT [Seed Confirm] references.bib keys Jia2023DeepLF (Water Res 231:119632, review) + Jakovljevic2020ADL (Remote Sens 12:1515, original) confirmed as P003/P004 citation-only rows [2] [2 screened] [0 full extractions] [0] [Full-text read pending; WARNING two distinct Jia-2023 papers exist — see improvement_flags]

### Search 2: Forward Citation Tracking — Seed 1
- [2026-09-07] HUMAN [Setup] [Seed Forward] Google Scholar / Scopus — papers citing Pati et al. [TBD] [TBD] [TBD] [TBD] [Not yet executed]

### Search 3: Seed 2 (Marye et al.) Backward + Forward
- [2026-09-07] HUMAN [Setup] [Seed Backward/Forward] `base_reference_systematic_review_paper/` `.md` file [Review cites ~16 studies] [TBD] [TBD] [TBD] [Agent to extract cited studies and check forward citations]
- [2026-09-08] PHASE1-AGENT [Seed Backward] P002 .md Tables 1-2 + text scan [~16 studies identified] [8 summarized] [4 new rows P005-P008 + P004 details enriched] [Geraeds/Schreyers/Simpson visual-or-nondescript studies deferred to pending_extraction.md] [Full texts still required for all P005-P008 metric/site confirmation; forward citation tracking NOT executed]

### Search 4: Keyword Search — Databases
- [TBD] AGENT [Keyword] Scopus / IEEE Xplore / Web of Science [Query from `search_strategy.md`] [TBD] [TBD] [TBD] [TBD] [Awaiting confirmation of search terms from `scope.md` / `direction.md`]

### Search 5: Expanded Batch P009–P012 (web full-text verification)
- [2026-09-08] EXPANDED-AGENT [Targeted Retrieval] TU Delft repo / PMC / WUR / arXiv [Solé Gómez 2022; Lin 2021; Tasseron 2022; Tharani 2021] [4 retrieved at abstract+methods level] [4 screened] [4 included: P009 A, P010 C, P011 A, P012 A] [0] [Per-region/site metric tables still need full-text PDF pass]

### Search 6: Backward Tracking from P003/P004 Corpora
- [2026-09-08] EXPANDED-AGENT [Seed Backward] P003 34-paper corpus + P004 reference set (FIG 2019 precursor, MDPI citations) [overlap with WIREs set: van Lieshout 2020, Tasseron 2021, Lin 2021 already captured] [~6 screened] [0 new in-scope river+DL papers beyond pending list] [marine-only P003 corpus papers out of scope] [Forward tracking NOT executed — no DB access]

### Search 7: Automatic Expansion Batches 1–2 (web full-text verification)
- [2026-09-08] AUTO-AGENT [Targeted Retrieval] J-Stage / MDPI / Frontiers / Nature / ISPRS / Wiley [Pan 2022; Yang 2022; Zailan 2022; Nunkhaw 2024; Pan 2024; Cortesi 2022; Mohsen 2023; Sakti 2023; Iordache 2022; De Giglio 2021] [10 retrieved at abstract+methods level] [10 screened] [10 included: P013 A, P014 B, P015 D, P016 C, P017 B, P018 A-8C, P019 A, P020 B, P021 B, P022 D] [0] [Geraeds 2019 + Schreyers 2021 verified EXCLUDED (manual-only, fail #3)] [Forward tracking still deferred]

### Search 8: Automatic Expansion Batch 3 (include candidates + verify queues)
- [2026-09-08] AUTO-AGENT [Targeted Retrieval] IEEE / BEEI / MDPI [Sio 2022; Putra 2021; Panwar 2020; Nunkhaw 2025] [4 retrieved] [4 screened] [3 included: P023 D, P024 B, P025 A] [1 excluded: Panwar 2020 marine-only] [Marine queue (Fulton/Kylili/Garcia-Garin/Kako/Mifdal/Deng) + land queue (Cordova/Patel/Kumar) excluded at title/abstract level — all fail criteria #1; reversible on challenge] [Forward tracking still deferred]

### Search 9: Automatic Expansion Batch 4 (generative + 2024–2025 keyword sweep)
- [2026-09-08] AUTO-AGENT [Targeted + Keyword] J-Stage / web [Pan 2023 AIGC; YOLOv8 river 2024; Kataoka 2024; Liu 2025; EFD-YOLO 2025; WCSE 2024; Lee 2025; FrontEnvSci 2025] [7 retrieved] [7 screened] [7 included: P026 A, P027 A, P028 D, P029 D, P030 D, P031 B, P032 B] [0] [P001–P012 title/journal backfill done] ### Search 10: Keyword Sweep A + Forward-Cite Check (P004/P006 lineage)
- [2026-09-08] AUTO-AGENT [Keyword + Forward] web (MDPI/IEEE/SPIE proxies for Scopus/WoS/IEEE/MDPI) [UAV river plastic YOLO 2023-24; citing Jakovljevic 2020; Sentinel-2 debris DL 2024-25; citing Maharjan 2022] [~10 screened] [4 included: P033 D, P034 A, P035 D, P036 A-prov] [excluded: Cerra 2024 (rule-based, no learning), DEEP-PLAST + TAUNet (marine), Saddi-2025 preprint + Cortesi-2024 thesis (noted, not rows)] [P006 upgraded A, P001 venue fixed via hits] [Full DB keyword pass still deferred]

### Search 11: Sweep C/D — Pond/Lake/Canal + Backward (P008-team SSL lineage, P027/P031 refs)
- [2026-09-08] AUTO-AGENT [Keyword + Backward] web (MDPI/WUR/J-Stage proxies) [pond lake debris DL; Armitage vessel; de Vries Noria; Rhine bridge YOLO] [~8 screened] [4 included: P037 A, P038 A, P039 D, P040 D-prov] [excluded: Armitage marine, Clausiuspress venue] [P008 upgraded TBD→B via Frontiers full text; P027 corroborated via Frontiers full text] [Forward tracking + full DB keyword pass still deferred]

### Search 12: Batch 7 — Chen Lead + Geographic-Gap Sweep + Backward Leads
- [2026-09-08] AUTO-AGENT [Targeted + Keyword] web (MDPI/IOP/JOCA/SciAfrican proxies) [Chen23 Soft-NMS; Africa/S.America river DL; Tomas22; Li23 Dai Lake] [~7 screened] [3 included: P041 D-prov, P042 B, P043 D] [excluded: Drabinski (manual), Torregroza (coastal micro)] [context: Atuhaire25 review (geographic-gap evidence)] [leads left: Tomas22, Li23-DaiLake, Haris23-Rasau, Li22-JCleanPro] [Forward tracking + full DB keyword pass still deferred]

### Search 13: Batch 8 — NICS/IEEA/ICCV Backward (Vandaele + FloW citations) + Underwater Check
- [2026-09-08] AUTO-AGENT [Backward] web (IEEE/ACM/CVF/SPIE proxies) [Tomas22 IEEA; NguyenTran22 + Trinh22 NICS; FloW21 ICCV; Renfei Deqing; Hegde21; Kataoka-Nihei20] [~9 screened] [6 included: P044 D-prov, P045 A, P046 D-prov, P047 D-prov, P048 D, P049 B-prov] [excluded: Jaikumar21 (non-aquatic), Kataoka-Nihei20 (classical), Haris23 (OBIA), Hegde21 (marine)] [P007 upgraded B→A via WUR thesis Exp II] [3 to 50: Li23-DaiLake, Li22-JCleanPro, Renfei-UDA/multicam companions]

### Search 14: Batch 9 FINAL — Li22-JCleanPro + Wolf-Vietnam lineage + Renfei companions
- [2026-09-08] AUTO-AGENT [Targeted] web (Elsevier/IOP/DFKI proxies) [Li22 JCleanPro; Wolf Vietnam journal; EAAI-UDA] [~4 screened] [3 included: P050 D-prov, P051 B-prov, P052 B-prov] [P005 enriched to B (Cambodia open-data + multi-country lineage)] [50/50 THRESHOLD REACHED] [Deferred: full DB keyword pass, Scholar/Scopus forward tracking, PDF verification bundle — listed in pending_extraction.md]

### Search 15: Connected-Papers Audit (.bib ×3 → verification of 3 leads)
- [2026-09-08] AUTO-AGENT [Connected Audit] resources/connected_papers/*.bib (41+41+40 titles, dedup vs P001–P052) [~122 titles screened] [1 included: P053 Balsi25 B-prov] [Garaba23 → context (no learning); Alboody23 → context (lab-marine)] [51/50 cap-exception] [Context batch (Gnann22, Olyaei24, Tasseron24-hotspots, field-transport set) queued next]

### Search 16: PDF Bundle (human-authorized verification)
- [2026-09-08] AUTO-AGENT [Verification] web full-text/PMC/IOP/WUR [P036, P042, P030, P032, P051, P040, P028] [7 resolved: P036→A, P042/P030/P032-authors, P051-citation, P040-authors, P028-venue-flagged] [residual PDF-only: P004-T5, P009-regions, P010-source, P012-city, P043-platform] [leads, not rows: ROD-MCY-2026 (out of range), Ramya-ICICT25 (thin)]

### Search 17: User-PDF Reconciliation (blocked_files: 2 PDFs + 3 XMLs + 1 TXT)
- [2026-09-08] AUTO-AGENT [User Files] Jakovljevic-XML (full text: Table-5 held-out CONFIRMED); SoléGómez-PDF (full text: rivers/hyperparams/Table-4/cross-val/temporal); Tharani-PDF (Lahore, 48,450 objs, published mAP, URL; arXiv conflict flagged); Lin-XML (2,400 total resolved); Balsi-XML (land-only training PROVEN → P053 reversed to context); P051-TXT (CDA-SSD-FT metrics → P051 B-prov→A) [50/50 restored; grades A20/B13/C2/D15]

## Human Confirmations Needed Before Full Search Launch
- Confirm database list (any renowned — confirmed, but specify which ones agent should prioritize).
- Confirm proposed additional seeds (3-5 papers from reference lists).
- Confirm whether to include preprints (e.g., arXiv) — user said "renowned databases" and conference papers yes; preprints not explicitly mentioned. Suggest excluding arXiv unless specifically relevant and cited by seed papers.
