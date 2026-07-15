# How to deposit the replication package on Zenodo

This package meets the Journal of Economic Surveys hard requirement that data and
code be reproducible from a public repository with a persistent identifier (DOI).
Two routes are given. Route A (GitHub linked to Zenodo) is recommended because it
gives free versioning; Route B (direct upload) is the fastest one-off.

The Zenodo DOI it produces is the identifier that goes into the manuscript's
data-availability statement (replacing the current placeholder). This is
independent of SSRN - do not wait for the SSRN preprint DOI.

---

## Route A - GitHub linked to Zenodo (recommended)

Gives a versioned deposit: each GitHub release becomes a new Zenodo version, and a
stable "concept DOI" always points to the latest.

1. **Create a public GitHub repository** and push the contents of this `zenodo/`
   folder to its root (so `README.md`, `.zenodo.json`, `CITATION.cff`, `data/`,
   `appendix/`, `figures/`, `manuscript/`, `docs/`, `references.bib`, `LICENSE.md`
   are at the top level).
2. Go to **https://zenodo.org**, sign in (ORCID or GitHub login), open
   **Account -> GitHub**, and flip the switch **ON** next to the repository.
3. Back on GitHub, create a **release** (e.g. tag `v1.0`, title
   "Replication package v1.0"). Zenodo detects the release automatically.
4. Zenodo reads `.zenodo.json` and pre-fills the deposit (author, ORCID,
   affiliation, license CC-BY-NC-4.0, keywords, link to the SSRN note). Review it,
   then it publishes and mints the DOI.
5. Copy the **DOI** (the version DOI for citing this exact release; the concept DOI
   for "latest") and paste it into the manuscript's data-availability statement.

Note: the GitHub switch must be ON *before* the release is created - Zenodo only
captures releases made after linking.

---

## Route B - Direct upload (no GitHub)

Fastest if you do not want a public GitHub repo.

1. Go to **https://zenodo.org**, sign in, click **New upload**.
2. Upload `zenodo_replication_package.zip` (or the loose files).
3. Fill the form - or, if uploading the loose files, Zenodo does NOT auto-read
   `.zenodo.json` on manual uploads, so enter by hand:
   - **Resource type:** Dataset
   - **Title:** Spec-Driven Artificial Intelligence for Empirical Research: A Scoping Review and an Architecture of Epistemic Control - Replication Package
   - **Creator:** Wojarnik, Grzegorz - ORCID 0000-0001-6946-547X - University of Szczecin, Institute of Economics and Finance
   - **License:** Creative Commons Attribution-NonCommercial 4.0 (CC-BY-NC-4.0)
   - **Keywords:** reproducibility; meta-science; preregistration; research transparency; AI-assisted research; spec-driven development
   - **Related identifier:** "is supplement to" DOI 10.2139/ssrn.6853581 (the FSAIM position note)
   (all of these values are in `.zenodo.json` for copy-paste)
4. Click **Publish**. Zenodo mints the DOI.
5. Paste the DOI into the manuscript's data-availability statement.

---

## After you have the DOI

The DOI must replace the placeholder in:
- the manuscript data-availability statement (`statements.md`),
- `compliance_reporting_guidelines.md`,
- and be re-compiled into the Wiley PDF on Overleaf.

Send the assigned SSRN preprint DOI (once granted) to the editorial office
separately, per the cover letter's preprint disclosure.
