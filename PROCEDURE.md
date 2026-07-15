# Research Procedure

This scoping review was produced under the **FSAIM** methodology (spec-driven AI for empirical research), announced in the position note: Wojarnik, G. (2026), SSRN, DOI [10.2139/ssrn.6853581](https://doi.org/10.2139/ssrn.6853581). The procedure had six steps:

1. **Scope freeze.** The thesis, five research questions (RQ1-RQ5), and scope boundaries were fixed and frozen before analysis (analogue of layer L1 - preregistration applied to the review itself).
2. **Search.** Two streams: (a) topical queries in OpenAlex + arXiv + Crossref for the six control approaches (L1-L6), filtered from 1998; (b) a citation-anchor import (14 seed works) expanded through the citation graph, with no lower year filter. Full log: `appendix/SEARCH_LOG.md`.
3. **Screening.** A deterministic keyword dictionary over titles and abstracts (reproducible, not LLM classification). Result: 582 works included. Flow: `figures/fig_corpus_v3_prisma_en.png`.
4. **Coding.** 56 works were shortlisted; 41 were coded in full text against a 16-field interpretive schema (`data/coding_sheet.csv`, 69 rows), including a 13-work economics subsample. Every quote was verified programmatically - it must appear verbatim in the source text. Author attributions come from OpenAlex, never from memory.
5. **Synthesis.** Mapping the six approaches onto seven control layers (L1-L7), a comparison matrix (`data/tables/tab_synthesis_matrix.csv`), identification of four gaps, and construction of the SDD framework.
6. **Control and redaction.** A four-question consistency test on each section plus adversarial control; redaction following scientific-prose rules. Every process step is documented (layer L6 - AI-involvement disclosure).

**Human gates.** At key points (scope freeze, coding acceptance, economics claims, submission decision) a human author made the decision; the AI could not bypass them.

**Reproducibility.** The data in `data/` together with the log in `appendix/SEARCH_LOG.md` let you reconstruct the corpus and coding independently. Full texts of the works are not included here (copyright); locate each work by its DOI in `data/corpus_screened_in.csv` and `references.bib`.
