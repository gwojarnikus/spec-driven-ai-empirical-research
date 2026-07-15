# Documentation (EN) - how to reproduce the results

This folder is a **replication package**: the source data and a procedure description behind the scoping-review article on the FSAIM methodology. It is not a copy of the whole workshop - only what is needed to understand and reproduce the results.

## What is where

- **`PROCEDURE.md`** - a single document with the entire research procedure in six steps (scope freeze → search → screening → coding → synthesis → control). Start here.
- **`data/corpus_screened_in.csv`** - the screened corpus: 582 works with DOI, title, year, assigned layer (L1-L6), venue, and open-access status. This is the basis of the approach map.
- **`data/coding_sheet.csv`** - the coding sheet: 69 rows; 41 works coded in full text against 16 interpretive fields (control mechanism, timing, unit of freezing, human/AI role, import to SDD, etc.), including a 13-work economics subsample.
- **`data/tables/`** - result tables used in the article: synthesis matrix, approaches table, RDF in economics, SDD→finance mapping.
- **`appendix/`** - Appendices A-D from the article (`Appendix.md`) plus their source files: `SEARCH_LOG.md` (full query log, App. A), `KALIBRACJA_kodowania.md` and `ADJUDYKACJA_decyzje.md` (coding quality control, App. C), `checklista_PRISMA-ScR.md` (PRISMA-ScR checklist, App. D). The list of works not automatically retrievable is documented in Section 8.6 of the manuscript; all DOIs are in `data/corpus_screened_in.csv`.
- **`figures/`** - the PRISMA-ScR flow diagram (path from raw records to 582 included), PL and EN.
- **`manuscript/`** - the reference article in PDF (PL and EN), to see how the data translate into conclusions.

Note: appendix filenames are kept in their original Polish form (e.g. `KALIBRACJA_kodowania.md`) to match the article's provenance chain; their contents are in English.

## How to reproduce

1. Read `PROCEDURE.md` - learn the method.
2. Open `appendix/SEARCH_LOG.md` - you get the exact queries and hit counts.
3. Repeat the search in OpenAlex/arXiv/Crossref, or use the ready `data/corpus_screened_in.csv`.
4. Check the coding in `data/coding_sheet.csv` (every quote is verifiable against the source text).
5. Trace the synthesis in `data/tables/tab_synthesis_matrix.csv`.

Full texts of the works are not here (copyright) - locate them by DOI.
