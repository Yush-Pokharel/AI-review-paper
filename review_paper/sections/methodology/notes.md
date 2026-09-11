# Methodology — Draft Notes (Cycle 1, 2026-09-08)

## Claims → evidence mapping (every claim below traces to an ID or log)

1. Structured-but-not-PRISMA design → instructions.md (NO PRISMA CLAIM rule); report the exact disclaimer sentence in .tex.
2. Seed-anchored collection (P001 experimental blueprint + P002 review-of-record) → direction.md; P001 IEEE Access 2025 doi ...3576295; P002 WIREs Water 12:e70020.
3. Sources actually used (descriptive, not prescriptive): base .bib backward tracking; WIREs .md Tables 1–2; connected-papers .bib ×3 (~122 titles); targeted web retrieval as proxy for Scopus/WoS/IEEE/MDPI/ScienceDirect (Searches 5–17 in search_log.md); NO full DB keyword pass and NO Scholar/Scopus forward tracking (deferred — state openly).
4. Scope (human-confirmed 2026-09-08, applied descriptively): 2015–2026; Scopus/WoS/IEEE/Scholar (+MDPI/ScienceDirect hits via web); conferences included; global-with-Nepal-context. Corpus check: all 50 rows fall 2019–2025; venues peer-reviewed journals + conferences (P028 low-index venue flagged, cited thinly); preprints/theses held out (Saddi25, Cortesi24).
5. Flow numbers (honest, agent-screened): ~122 connected titles + ~60 keyword/backward hits title-screened (~180); ~70 abstract/full-text assessed; 50 primary included (P001 + P004–P052); ~25 documented exclusions with reasons (pending_extraction.md: SAR-only, manual-only, marine-only, land/non-aquatic, classical-no-learning, micro-only, venue quality); P053 reversal (land-only training) as QC anecdote.
6. Extraction schema → template.md fields (40 fields; paperID/title/journal/notes/rqMapping mandatory); taxonomy 8A–8G + A/B/C/D grading per guides; grades A20/B13/C2/D15.
7. Quality handling: single-agent screening + human log/flag review (NOT double-blind → limitation, route to challenges_future); provisional rows quarantined (P040/41/44/46/47/49/50/52 + P028/P043 residuals); arXiv-vs-published rule (P012 conflict as example); non-DL rows framed as spectral/ML strand; P045 scoped adjacent.
8. PRISMA-style diagram = organizational aid only → fill resources/prisma_diagram numbers here; reference figure in .tex without compliance language.

## Open questions for human review
- Are the ~180/~70 flow estimates acceptable as stated, or soften further ("over 150 titles screened")? > find the estimate based on the data you have.
- Keep P028 (low-index venue) + P045 (adjacent) in the 50, or drop to 48 fully-clean? > keep the two just use sparrigly when required.
- Confirm IEEE Access section-fragment convention (this .tex is \input-ready, no preamble).  > do as you need.
