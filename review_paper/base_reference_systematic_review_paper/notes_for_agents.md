# REFERENCE SYSTEMATIC REVIEW — EXTRACTED NOTES FOR AGENTS

## Source Details
- **Title**: Remote Sensing for Monitoring Macroplastics in Rivers: A Review
- **Authors**: Marye et al. (2025)
- **Journal**: WIREs Water (Wiley Interdisciplinary Reviews: Water)
- **DOI / URL**: https://doi.org/10.1002/wat2.70020
- **Type**: Systematic review (structured, literature synthesis — but no explicit PRISMA protocol registration mentioned).
- **Files in this folder**: `.pdf` (original), `.md` (extracted text from PDF), `.pdf:Zone.Identifier` (system file — ignore).

## Key Themes (For Agents Using This as Reference)
1. **Scope**: Buoyant macroplastics in river systems only. Excludes underwater, marine, terrestrial ecosystems, microplastics.
2. **Platforms Covered**: Spaceborne (satellite), airborne (UAS/drones), ground-based (fixed and handheld cameras).
3. **Sensors**: Primarily visible spectral range; some multispectral; one hyperspectral; one active sensor.
4. **Image Analysis**: Traditional visual observation, physical interception (nets, booms), remote sensing + ML/DL.
5. **DL Coverage**: Mentions CNNs, but focus is broader on remote sensing platforms rather than deep architecture comparison.
6. **Geographic Coverage**: Studies from various global regions; diverse settings.
7. **Methodology Transparency**: Uses bibliographic search (Web of Science + Google Scholar), keyword combinations, duplicate removal, exclusion criteria (marine/other size categories excluded), full-text evaluation.

## Gaps This Review Can Fill (Agent Guidance)
The WIREs Water review provides excellent platform comparison but may have gaps our review can address:
- **Underwater cameras**: Explicitly excluded from WIREs review. Our review includes this.
- **Deep architecture comparison**: WIREs mentions DL generally; our review compares YOLO, Faster R-CNN, DeepLab, Mask R-CNN, transformers, etc. in detail.
- **Dataset comparison**: WIREs summarizes studies but may not have a standardized dataset comparison table like ours.
- **Training/generalization strategies**: Our base paper (Pati et al.) provides a rigorous comparison of scratch/fine-tune/frozen/transfer — this is a unique contribution to synthesize.
- **Nepal context**: Base paper provides Nepal-specific data; our review can highlight South Asian / developing-country river contexts.
- **No PRISMA claim**: Our review should be transparent without overclaiming.

## How Agents Should Use This File
- Read the `.md` extracted text before drafting `data_sources/`, `detection_approaches/`, or `challenges_future/`.
- Note which studies/platforms are already covered to avoid duplicating synthesis work without adding value.
- If our review finds studies not in WIREs (e.g., newer 2024-2026 papers, underwater studies, transformer-based river studies), highlight these as our contribution.
