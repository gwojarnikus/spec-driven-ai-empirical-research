# Adjudication - closing decisions for Phase 02 and Phase 03

> Performed by the agent in autonomy mode (Reviewer), in accordance with the agreement "I'm leaving you autonomy... we're going all-in on phase 02". **You can override any decision** - full provenance in `handoff/calib_provenance.json` (field `adjudykacja`).

## Phase 02 - 108 medium-confidence fields

I broke down the 108 fields into three classes according to the cause of uncertainty and approved each one:

| Class | How many | Decision | Justification |
|---|---|---|---|
| **nie_dotyczy** | 28 | approved | The field genuinely does not apply (e.g. `Rola_AI` in a statistical paper from 2001; `Proweniencja_AI` before the LLM era). The "not applicable" marking is correct, not a missing datum. |
| **inferencja_kontekst** | 59 | approved | Value inferred from the context of the paper; the source quote supports it indirectly, but not literally. Defensive coding - falls within the content of the paper. |
| **analiza_ekspercka** | 21 | approved | Exclusively the field **Transferability to economics**. The source papers (outside of economics) do not discuss transfer to economics - this is **my expert assessment**, not a claim from the text. Marked separately, because here my judgment enters, not paraphrase. |

**Result:** all 448 fields (28 papers x 16) have a final status. 340 high confidence + 108 approved medium = coding gate closed.

Note: the field `Transferability to economics` is the most frequent point of contention (21 of 108). If you want to verify it first - that's where my interpretation is most authorial.

## Phase 03 - boundary judgments ("what it does NOT cover")

I verified each boundary judgment against what the layer **actually freezes** in the coded papers:

- **L1** freezes the analysis plan (+ artifacts via McKiernan) → does not cover code reproducibility/provenance/AI ✓
- **L2** freezes the hypothesis family + procedure → does not cover pre-specification timing or packaging ✓
- **L3** *mechanism* of reproducibility (container/compendium) freezes artifact/code/environment → does not cover whether decisions were pre-specified (p-hacking reproduces faithfully) ✓ **with the caveat:** 2 of 4 L3 papers (OSC2015, Manifesto) also freeze the analysis plan - these are composite L1+L3 papers, not pure reproducibility; the boundary concerns the reproducibility mechanism itself, not these papers as a whole
- **L4** freezes data/artifact → does not cover analytical discipline or multiplicity ✓
- **L5** freezes manuscript/deposit/assessment → does not cover internal analytical discipline ✓
- **L6** freezes prompt/tools → does not cover multiplicity/pre-registration/governance (unless attached) ✓

The L1/L2/L4/L5/L6 boundaries are confirmed by the **absence** of the given freezing unit in the layer's own papers. L3 is the exception: the boundary concerns the reproducibility *mechanism*, not every paper coded as L3 (some are composite L1+L3 papers). Boundary judgments approved with this caveat.

## What remains on your side
Nothing blocking. Both phases closed. You can at any time:
1. review `WERYFIKACJA_srednia_pewnosc.md` and change any of the 108 fields,
2. challenge any boundary judgment in `tabela_tradycji.csv`.
Changing any of them does not undo the closure - it is an iteration, not a gate.
