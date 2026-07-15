# Attachments (Appendix)

Appendix is a deterministic product of artifacts from earlier phases - each attachment points to a source file, not duplicates it.

This review applies its own thesis to itself: the research apparatus (queries, criteria, coding scheme, screening path) is made available as an auditable set of artifacts, not described in general terms. The attachments below allow the corpus and coding to be reconstructed independently.

## Appendix A - Search strategy and search log

The full, executable query log (databases, search strings, dates, hit counts, layer-inclusion decisions) is located in `SEARCH_LOG.md` in this folder. Key facts:

- **Databases:** OpenAlex (primary), arXiv, Crossref - open APIs replacing paywalled Scopus/WoS/EconLit (rationale: procedure description in `../PROCEDURE.md`).
- **Thematic streams:** six layers (L1 preregistration, L2 multiverse, L3 reproducibility, L4 FAIR/provenance, L5 data/code policies, L6 AI-for-science) + citation anchors.
- **Time filter:** thematic queries from 1998 (no upper bound); earlier works enter only through anchors/citation expansion (corpus 1955-2026).
- **Screening method:** deterministic keyword dictionary applied to titles and abstracts (reproducible, recordable - not LLM classification).

## Appendix B - PRISMA-ScR flow diagram

The path from raw records through deduplication, title/abstract screening, to the included corpus (582 works) - `../figures/fig_corpus_v3_prisma.png` (PL) / `..._en.png` (EN). Layer distribution in the included corpus: L3 reproducibility 246, L1 preregistration 102, L2 multiverse 73, meta 67, L6 AI 46, L4 FAIR 33, L5 policies 15.

## Appendix C - Coding scheme and coded dataset

A scheme of 16 interpretive fields (credibility problem, control mechanism, moment, freezing unit, required artifacts, human/AI role, data/code/AI provenance, approach to exploration/confirmation/deviations, transferability to economics, risks, import to SDD) - `../data/coding_sheet.csv` (56 works shortlisted; **28 were coded in full text in the first coding round**, documented in the calibration and adjudication files here, and the coding was later extended to 41 works in full text, including a 13-work economics subsample, in the canonical coding_sheet.csv shipped in data/). Scheme calibration: `KALIBRACJA_kodowania.md` in this folder. Verification of medium-confidence fields: the citation verification process is described in `../PROCEDURE.md`. Adjudication decisions: `ADJUDYKACJA_decyzje.md` in this folder.

Coding quality control principle: **every citation is verified programmatically** - it must appear literally in the source text, otherwise it is rejected. Author attributions are pulled from OpenAlex (never from memory).

## Appendix D - Works not available in full text

A list of 27 works (of the 56 shortlisted for coding) for which automated full-text retrieval was not possible - mostly closed-access titles behind paywalls (Wiley/Econometrica, AEA, Nature, APA, Oxford, and others), i.e. not limited to Elsevier. These works entered the corpus and the coding on the basis of title, abstract, and metadata; their full-text coding requires manual institutional access. This is a stated limitation of the review (Section 8.6). Each work is locatable by its DOI.

### Economics venues

1. A Reality Check for Data Snooping (2000). *Econometrica*. https://doi.org/10.1111/1468-0262.00152
2. Transparency, Reproducibility, and the Credibility of Economics Research (2018). *Journal of Economic Literature*. https://doi.org/10.1257/jel.20171350
3. Star Wars: The Empirics Strike Back (2015). *American Economic Journal Applied Economics*. https://doi.org/10.1257/app.20150044
4. Viewpoint: Replication in economics (2007). *Canadian Journal of Economics/Revue canadienne d économique*. https://doi.org/10.1111/j.1365-2966.2007.00428.x
5. Methods Matter: p-Hacking and Publication Bias in Causal Analysis in Economics (2020). *American Economic Review*. https://doi.org/10.1257/aer.20190687
6. Reporting the Fragility of Regression Estimates (1983). *The Review of Economics and Statistics*. https://doi.org/10.2307/1924497
7. REPORTING GUIDELINES FOR META‐ANALYSIS IN ECONOMICS (2020). *Journal of Economic Surveys*. https://doi.org/10.1111/joes.12363

### Methodology, statistics, and psychology

1. Conducting Meta-Analyses in<i>R</i>with the<b>metafor</b>Package (2010). *Journal of Statistical Software*. https://doi.org/10.18637/jss.v036.i03
2. Power failure: why small sample size undermines the reliability of neuroscience (2013). *Nature reviews. Neuroscience*. https://doi.org/10.1038/nrn3475
3. The preregistration revolution (2018). *Proceedings of the National Academy of Sciences*. https://doi.org/10.1073/pnas.1708274114
4. Reproducibility and Replicability in Economics (2020). *Harvard Data Science Review*. https://doi.org/10.1162/99608f92.4f6b9e67
5. Replication and Scientific Standards in Applied Economics A Decade After the Journal of Money, Credit and Banking Project (1994). https://doi.org/10.20955/r.76.79-83
6. Increasing Transparency Through a Multiverse Analysis (2016). *Perspectives on Psychological Science*. https://doi.org/10.1177/1745691616658637
7. The ASA Statement on <i>p</i> -Values: Context, Process, and Purpose (2016). *The American Statistician*. https://doi.org/10.1080/00031305.2016.1154108
8. The case for motivated reasoning. (1990). *Psychological Bulletin*. https://doi.org/10.1037/0033-2909.108.3.480
9. The file drawer problem and tolerance for null results. (1979). *Psychological Bulletin*. https://doi.org/10.1037/0033-2909.86.3.638
10. A Simple Sequentially Rejective Multiple Test Procedure (1979). *Scandinavian Journal of Statistics*. https://doi.org/10.2307/4615733
11. Statistical Analyses and Reproducible Research (2007). *Journal of Computational and Graphical Statistics*. https://doi.org/10.1198/106186007x178663
12. Specification curve analysis (2020). *Nature Human Behaviour*. https://doi.org/10.1038/s41562-020-0912-z
13. Multiple Inference and Gender Differences in the Effects of Early Intervention: A Reevaluation of the Abecedarian, Perry Preschool, and Early Training Projects (2008). *Journal of the American Statistical Association*. https://doi.org/10.1198/016214508000000841
14. Adaptive linear step-up procedures that control the false discovery rate (2006). *Biometrika*. https://doi.org/10.1093/biomet/93.3.491
15. A Multiple Comparison Procedure for Comparing Several Treatments with a Control (1955). *Journal of the American Statistical Association*. https://doi.org/10.1080/01621459.1955.10501294
16. False-Positive Psychology (2011). *Psychological Science*. https://doi.org/10.1177/0956797611417632
17. HARKing: Hypothesizing After the Results are Known (1998). *Personality and Social Psychology Review*. https://doi.org/10.1207/s15327957pspr0203_4
18. Selective Publication of Antidepressant Trials and Its Influence on Apparent Efficacy (2008). *New England Journal of Medicine*. https://doi.org/10.1056/nejmsa065779
19. 1,500 scientists lift the lid on reproducibility (2016). *Nature*. https://doi.org/10.1038/533452a
20. A primer on provenance (2014). *Communications of the ACM*. https://doi.org/10.1145/2596628

## Appendix E - PRISMA-ScR checklist

The full checklist (Tricco et al. 2018 standard, 20+2 items) with the location of each item in the article - `checklista_PRISMA-ScR.md` in this folder.
