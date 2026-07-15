# Coding calibration - 3 benchmark papers (for standard acceptance)

> This is the calibration batch of phase 02: 16 interpretive fields coded for 3 papers from different layers, each field with a **source quote** and **confidence** (high/medium). Goal: agree on the standard before I code the remaining 26 papers with full text. Check especially the fields marked _medium_ - there the interpretation is most debatable.

## L1 - preregistration (economics)
**Ofosu & Posner 2020, Do Pre-analysis Plans Hamper Publication?**

| Field | Coded value | Source quote | Confidence |
|---|---|---|---|
| Problem_wiarygodnosci | p-hacking/fishing and selective reporting in economic experiments; and the publication cost of preregistration discouraging it | „registering a PAP reduces researchers' latitude to fish for specifications” | high |
| Mechanizm_kontroli | pre-analysis plan (PAP) - prespecification of hypotheses and analyses before observing results | „scholars who register and adhere to PAPs”; „prespecified in a PAP” | high |
| Moment_kontroli | before analysis | PAP registered before data analysis (AEA/EGAP registries) | high |
| Jednostka_zamrozenia | analysis plan | „prespecified in a PAP”; freezes hypotheses and regression specifications | high |
| Artefakty_wymagane | registered PAP in a registry (AEA/EGAP), with prespecified hypotheses | „PAPs registered on the AEA and EGAP registries” | high |
| Rola_czlowieka | researcher writes the PAP before the data and adheres to it during analysis/writing | „scholars who register and adhere to PAPs” | high |
| Rola_AI | none - the paper predates the era of AI tools in this line of research | no mention of AI | high |
| Proweniencja_danych | secondary data: 8706 NBER working papers 2011-2018 + citations from Google Scholar | „NBER working papers between 2011 and 2018” | high |
| Proweniencja_kodu | not explicitly reported in this short P&P article | no code/replication section in the text | medium |
| Proweniencja_AI | not applicable | - | high |
| Podejscie_eksploracja | criticized - the PAP is meant to limit ex-post exploration | „latitude to fish for specifications” | high |
| Podejscie_konfirmacja | confirmatory: the PAP enforces prespecified hypotheses | „primary hypotheses that were prespecified” | high |
| Podejscie_odchylenia | deviations from the PAP are explicit; researchers admit that they "almost always deviate from the PAP" | „I almost always deviate from the PAP” | high |
| Transferowalnosc_ekonomia | very high - this is a strictly economics paper about the practice of top-5 econ journals | „top-five economics journals” | high |
| Ryzyka_ograniczenia | selection into preregistration; no control for significant vs null results; snapshot of a trend | „must be taken as only suggestive given the challenges of selection” | high |
| Import_do_SDD | PAP = archetype of freezing analytical decisions before the data (core of layer L1); + evidence that the publication cost is tolerable | observation: papers with a PAP are more often in top-5 and more often cited | high |

## L4 - FAIR data/artifacts
**Wilkinson et al. 2016, The FAIR Guiding Principles**

| Field | Coded value | Source quote | Confidence |
|---|---|---|---|
| Problem_wiarygodnosci | data and artifacts that are unfindable/unreusable → lack of transparency and reproducibility | „all components of the research process must be available to ensure transparency, reproducibility” | high |
| Mechanizm_kontroli | FAIR principles (Findable, Accessible, Interoperable, Reusable) for data AND algorithms/tools/workflows | „Findability, Accessibility, Interoperability, and Reusability” | high |
| Moment_kontroli | during writing / submission - at the stage of publication and data deposit | „after the data publication process”; management at the deposit stage | medium |
| Jednostka_zamrozenia | data (+ metadata + workflow as a research object) | „principles apply not only to data ... but also to the algorithms, tools, and workflows” | high |
| Artefakty_wymagane | globally unique persistent identifier, rich metadata, license, provenance | „F1. (meta)data are assigned a globally unique and persistent identifier” | high |
| Rola_czlowieka | data producer/publisher/steward implements FAIR | „guide to data publishers and stewards” | high |
| Rola_AI | machines as stakeholders - computational agents autonomously find/use data ("machine-actionable") | „enhancing the ability of machines to automatically find and use the data” | high |
| Proweniencja_danych | explicitly required: rich metadata + identifier | „F2. data are described with rich metadata” | high |
| Proweniencja_kodu | workflows/tools covered by FAIR as research objects | „analytical pipelines benefit from application of these principles” | high |
| Proweniencja_AI | provenance for machine agents: „keep an exquisite record of provenance” | „R1.2. (meta)data are associated with detailed provenance” | high |
| Podejscie_eksploracja | supports exploratory data integration by agents | „deeply and broadly integrative analyses” | medium |
| Podejscie_konfirmacja | not applicable - this is a data management framework, not hypothesis testing | - | high |
| Podejscie_odchylenia | not applicable | - | high |
| Transferowalnosc_ekonomia | medium/high - data/code policies in economics (data editors, replication packages) are an application of FAIR | domain-independent framework: „domain-independent, high-level principles” | medium |
| Ryzyka_ograniczenia | principles precede implementation, no enforcement, „good data management largely undefined” | „The Principles precede implementation” | high |
| Import_do_SDD | artifact with a persistent
