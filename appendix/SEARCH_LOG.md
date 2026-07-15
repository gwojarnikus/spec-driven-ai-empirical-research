# Search log - corpus v1 (PRISMA-ScR appendix)

> Access date: 2026-07-04. Engine: OpenAlex (MCP `literature`), arXiv (MCP `literature`), Crossref (DOI verification). Databases unavailable: Scopus, Web of Science, EconLit (paywall); PubMed/PMC E-utilities (blocked by sandbox, request declined). Substitution rationale: OpenAlex in practice indexes a superset of Scopus/WoS and PMC content.

## 1. OpenAlex queries (free-text, `year_from=1998`, sort=cited_by_count, 40 rec./query)

| Tag | Query | api_total |
|---|---|---|
| L1_prereg | preregistration pre-analysis plan registered reports economics selective reporting | 599 |
| L2_multiverse | specification curve multiverse analysis garden of forking paths robustness multiple testing | 136 |
| L3_reproducible | reproducible research research compendium executable paper dynamic document | 1382 |
| L4_fair_prov | FAIR data RO-Crate workflow provenance research object reproducibility | 198 |
| L5_datapolicy | data code availability policy replication package computational reproducibility economics | 5062 |
| L6_ai_science | AI for science LLM agents automated scientific discovery reproducible human-in-the-loop | 3353 |
| econ_dof | researcher degrees of freedom p-hacking HARKing empirical economics finance credibility | 52 |

## 2. arXiv queries (sort=relevance, 30 rec./query)

| Tag | Query | api_total |
|---|---|---|
| arxiv_specdriven | abs:"spec-driven" AND (abs:science OR abs:"data analysis" OR abs:research) | 2 |
| arxiv_agentic | abs:"LLM agents" AND abs:"scientific" AND (abs:reproducible OR abs:autonomous) | 50 |

## 3. Anchors (targeted import, spec §11) - 11 DOI + 3 arXiv, all resolved

Kerr 1998 (10.1207/s15327957pspr0203_4) · Simmons 2011 (10.1177/0956797611417632) · OSC 2015 (10.1126/science.aac4716) · Nosek 2018 (10.1073/pnas.1708274114) · Ofosu 2020 (10.1257/pandp.20201079) · Ludwig 2019 (10.1257/pandp.20191070) · Steegen 2016 (10.1177/1745691616658637) · Simonsohn 2020 (10.1038/s41562-020-0912-z) · List 2016 (10.3386/w21875) · Gentleman 2007 (10.1198/106186007X178663) · Wilkinson 2016 (10.1038/sdata.2016.18) · ARIA (arXiv:2510.11143) · Agent Laboratory (arXiv:2501.04227) · AI Scientist (arXiv:2408.06292).

## 4. Citation graph expansion

For each of the 11 anchors in OpenAlex: backward references (≤60) + forward citing works (≤50, sort cited_by). Result: 682 unique works, of which 74 linked to ≥2 anchors (cross-cutting core).

## 5. Deduplication and screening

- Source contributions to the merge (with overlap): OpenAlex pilot 280 (7 tags × 40) + arXiv pilot 32 (2 tags) + anchors 14 (11 DOI + 3 arXiv) + expansion 682 = **1008 raw rows**; 1 row with an empty key (no DOI and no title) discarded → **1007 rows with a valid key** → after deduplication **965 unique** (key: DOI, failing that - normalized title).
- Title screening: deterministic dictionary rule (7 groups of inclusion phrases per spec §9 + an off-topic exclusion list). Result: IN + MAYBE + OUT = 965. Override: a work linked to ≥2 anchors is always IN.
- Methodological note: LLM classification of titles was originally planned; switched to a dictionary rule as more reproducible (recordable in the appendix) and free of token cost. LLM reserved for abstract screening on the Tier C set.
- Correction (2026-07-04, post-audit): the first version of the merge loop omitted 32 arXiv pilot records (31 unique), understating the pool to 934 and corpus v1 to 280. After the fix: pool 965, corpus v1 304. The recovered works are the core of layer L6 (ARIA, LMR-BENCH, ReproRepo, reproducibility agents) - L6 grew from 20 to 41.

## 6. Corpus layers (tiers)

- A_anchor (11): anchors.
- A_core (68): linked to ≥2 anchors.
- B_title_in (225): dictionary hit in title.
- C_abstract_pending (654): title without a keyword - awaiting abstract screening.
- OUT (7): off-topic (PLS-SEM, Gene Ontology, RCV1, Metaverse, GPT-4 Technical Report).

Sum: 11+68+225+654+7 = 965. Corpus v1 = Tier A+B = **304 works**. (Sections 4-6 describe the v1 state; section 7 describes the transition to v2.)

## 7. Closing the L5 gap → corpus v2 (2026-07-04)

The diagnosed gap (L5 = 2 works) closed via targeted selection of four economic anchors + ±1 citation expansion:

| Anchor | DOI | cited_by |
|---|---|---|
| Christensen & Miguel 2018 (*JEL*) | 10.1257/jel.20171350 | 435 |
| Stodden, Seiler & Ma 2018 (*PNAS*) - effectiveness of journal data/code policies | 10.1073/pnas.1708290115 | 374 |
| Vilhuber 2020 - reproducibility in economics (AEA Data Editor) | 10.1162/99608f92.4f6b9e67 | 39 |
| Anderson et al. 1994 - replication standards in applied economics | 10.20955/r.76.79-83 | 55 |

The AEA Data and Code Availability Policy itself and openICPSR are cited as institutional sources (pages per access date, spec §8), not as research works.

Expansion: 333 L5 records (4 anchors + 329 from citations) → 330 unique, of which 41 were already in the pool (confirming that the L5 anchors genuinely connect to the corpus), 289 new. Pool 965 → **1254**.

Dictionary update: extended **exclusively** the L5 group with vocabulary the pilot did not catch (`data editor`, `data archive`, `journal (data) policy`, `scientific standard`); the `meta` group unchanged relative to v1. The Protein Data Bank / crystallography family (PDBj and related) was added to the EXCLUDE list, having entered via "data archive" citation expansion - this is the same type of off-topic noise as Gene Ontology in the pilot. OUT: 7 → 19.

### Corpus v2 - numbers (historical snapshot, BEFORE abstract screening - current values in §9)

> Note: the tier distribution below describes the v2 state (before abstract screening). After screening (§9) the tiers are different: C_abstract_pending 824 → B_abstract_in 171 + C_screened_out 646 + OUT (+7); OUT 19 → 26. Current, authoritative distribution: see §9 and `pool_full_tiered.csv` (column `tier`).

- Pool (v2, historical): **1254** (tiers: A_anchor 16 + A_core 79 + B_title_in 316 + C_abstract_pending 824 + OUT 19 = 1254).
- Corpus v2 (A+B) = **411** (v1 was 304).
- Distribution by first matched layer: L3_repro 153, L1_prereg 72, meta 61, L2_multiverse 52, L6_ai 42, L4_fair 23, **L5_policy 8**.

### IMPORTANT caveat: layer label ≠ topic coverage (post-audit correction)

The layer label is the **first** dictionary rule matched in the title, checked in order L1→L6. This has two effects that make the count "L5_policy = 8" a **poor proxy** for economic coverage:

1. **Overstates in one direction:** the L5 label went mainly to general-science works on data-sharing (PLoS ONE, BMJ, Scientific Data), not economic ones. This is not 8 works on data/code policies in economics.
2. **Understates in the other direction:** the four targeted economic anchors (Christensen & Miguel 2018, Stodden et al. 2018, Vilhuber 2020, Anderson et al. 1994) fell into **L3_repro**, because their titles contain "reproducibility/replication," and L3 is checked before L5. The economic material is in the corpus - it is hiding under the L3 label.

**A fair metric (independent of the layer label):** corpus v2 contains **46 works with an economic venue** (AER, JPE, Economic Journal, NBER, JEL, Economic Inquiry...), of which **25 come from the targeted L5 selection**. This is the real result of closing the economic gap - not the "L5=8/9" figure. The `is_econ_venue` column in the corpus files allows this to be verified directly.

**Conclusion for the article:** the number on the L5 label is not suitable for the claim "layer L5 covered." The economic section should use the venue metric (46 works) and treat layer assignment as preliminary - final layer coding will occur in phase 02 from the full text, not from the title.

## 9. Tier C abstract screening (phase 02) - corpus update

Tier C layer numbered **824** works. Of these, **10 had no OpenAlex identifier** (records entered via citation expansion without a resolved W-id) - for these it was not possible to fetch an abstract, so they went straight to the screened-out layer, without screening. The remaining **814** works (with an identifier) were fetched directly from the OpenAlex API (batches of 50 identifiers, reconstructed from the inverted index): abstract available for 637 works, 177 without an abstract (OpenAlex does not provide one) - for these, screening was based on the title alone. The LLM token budget for the session was exhausted, so abstract screening was performed with the same deterministic dictionary rule as title screening (method consistency, full reproducibility), extended with vocabulary visible only in the abstract. The rule was calibrated on a sample: the overly general phrase "evidence-based" was removed (it introduced noise: Handbook of Behavior Change, AI in Dentistry), while unambiguously methodological phrases were retained (numerical reliability, econometric software, meta-research, data curation).

Result of screening 814 assessed works: **171 IN** (promoted from Tier C to the corpus), 7 OUT, **636 screened out** (abstract/title exists, no topical signal); 171 + 7 + 636 = 814. The screened-out layer additionally includes the 10 works without an identifier (unassessed), hence **C_screened_out = 636 + 10 = 646**. Tier reconciliation: A_anchor 16 + A_core 79 + B_title_in 316 + B_abstract_in 171 + C_screened_out 646 + OUT 26 = 1254.

### Corpus v3 - numbers

- Corpus included (A+B) = **582** (v2 was 411; +171 from abstract screening).
- Distribution by first matched layer: L3_repro 246, L1_prereg 102, L2_multiverse 73, meta 67, L6_ai 46, L4_fair 33, **L5_policy 15**.
- Years 1955-2026, median 2019, OA 75%, works with economic venue: 71.
- Diagram: `fig_corpus_v3_prisma.png` (PL) + `fig_corpus_v3_prisma_en.
