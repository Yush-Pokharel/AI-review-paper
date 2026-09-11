# SEARCH STRATEGY — SEED SET & CITATION TRACKING

## Philosophy
We start with a known seed set and expand via backward (references cited by seed papers) and forward (papers citing seed papers) citation tracking. This ensures we capture the literature network around our key references rather than relying solely on keyword searches.

## Seed Papers (Confirmed)

### Seed 1: Base Published Paper
- Title: Leveraging UAV Data and Deep Learning Models for Detecting Waste in Rivers
- Authors: Pati et al. (2025/2026 — check publication year in `.bib` or `.tex`)
- Source: User's published paper (`base_published_paper/`)
- Why seed: Core comparative study; introduces datasets, training strategies, transfer learning across rivers.
- Backward tracking: Read its `references.bib` for papers it cites (this gives the historical/network base).
- Forward tracking: Search Google Scholar / Scopus for papers that cite Pati et al. (newer studies building on it).

### Seed 2: Base Reference Systematic Review
- Title: Remote Sensing for Monitoring Macroplastics in Rivers: A Review
- Authors: Marye et al. (2025)
- Source: `base_reference_systematic_review_paper/`
- Why seed: Comprehensive review of remote sensing + river macroplastic monitoring; excellent source list.
- Backward tracking: Read its references (the review already synthesized many studies — extract those studies directly if accessible).
- Forward tracking: Search for papers citing Marye et al. (2025) — these are newer studies responding to or extending the review.

### Seed 3-5: Additional Key Papers (Proposed — Agent Suggests/Confirms)
Agents should scan the seed papers' reference lists for commonly cited high-impact papers in river waste + DL. Propose 3-5 additional seeds based on frequency and relevance. Examples likely include:
- Jia et al. (2023) — Deep learning for macroplastic litter (cited in base paper)
- Jakovljevic et al. (2020) — Deep learning approach (cited in base paper)
- Wolf et al. (2020) — UAS studies (cited in reference review)
- Geraeds et al. (2019) — Early UAS + DL river study
- Any highly cited transformer/UAV study from 2022-2024

Agents: Propose seeds in `search_protocol/proposed_seeds.md`. Human confirms before expanding search.

## Search Protocol Steps
1. Extract all references from `base_published_paper/references.bib` (backward from Seed 1).
2. Read `base_reference_systematic_review_paper/` `.md` file and note all cited studies mentioned in text (backward from Seed 2).
3. Search Google Scholar / Scopus for papers citing Seed 1 and Seed 2 (forward tracking).
4. Execute keyword searches using refined strategy in `search_strategy.md`.
5. For each candidate paper, check inclusion/exclusion (`criteria_final.md`).
6. If included, extract data into `extraction_table/`. If excluded, note reason.

## Tracking File
Agents must maintain `search_protocol/search_log.md` with:
- Search date, database/search engine, query used.
- Number of results returned.
- Number screened, number included, number excluded (with reasons).
- Seed papers processed (backward/forward counts).
