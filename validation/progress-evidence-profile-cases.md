# Progress Evidence-Profile Adversarial Cases

## Status and limitation

This rubric and case set were fixed before the experimental-profile workflow was finalized. It is an internal forward test, not independent evidence that the workflow performs well on real laboratory decks. A future real deck remains the required held-out validation.

The cases target claim calibration and routing behavior. They do not test `ppt-master` rendering.

## Rubric

For each case, audit these invariants:

| ID | Invariant |
|---|---|
| R1 | The workstream is routed by claim dependency as computational, experimental, hybrid, or general; the rationale is explicit. |
| R2 | Planned method, recorded execution, measured output, and observed result remain separate facts. |
| R3 | Experimental, observational, and technical-repeat units are distinguished; exact `n` is attached to the correct level. |
| R4 | Controls, assignment/order, exclusions, and batch or other plausible confounders limit the claim when relevant. |
| R5 | Raw evidence, processing/normalization, assay validity, and run-level QC are sufficient for the displayed claim. |
| R6 | Optimization, one QC-passed observation, independent repetition, and orthogonal corroboration are not conflated. |
| R7 | The allowed claim is no stronger than the weakest necessary stage in the evidence chain. |
| R8 | Conditionality is preserved: irrelevant wet-lab checks do not burden a computational or general workstream. |

R2–R7 are critical when applicable. A pass requires all applicable critical invariants, correct routing, and no invented fact. “Unknown” must remain visible when the source cannot resolve a consequential item.

## Fixed cases

### C1 — Biological dataset, current work begins from a frozen matrix

The current contribution is a new analysis pipeline over an already generated matrix. No sample preparation or instrument run is being reported.

Expected: computational. Biological subject matter alone must not trigger the experimental lock.

### C2 — Six wells from one culture preparation

A treatment and control each have 3 wells derived from one culture preparation. The draft graph labels each group `n=3` and calls the result independently replicated.

Expected: experimental. Wells are nested measurements of one preparation unless the design establishes another independent unit. The workflow must block the independent-replication claim.

### C3 — Treatment assigned by cage

Eight cages contain 4 animals each. Treatment is assigned to cages, but the draft analysis and slide call `n=32` independent animals.

Expected: experimental. The treatment-assignment unit and nesting must be surfaced; the slide cannot silently use 32 independent treatment assignments.

### C4 — Representative microscopy fields

One specimen per group yields many fields. Two visually clear fields are selected after inspection and used to claim that the phenotype is common across samples.

Expected: experimental. The images may illustrate appearance, but prevalence or reproducibility requires a selection rule, quantification, and independent units.

### C5 — qPCR technical triplicates

One RNA extraction per condition is measured in 3 qPCR wells. The plotted error bars use the wells, while assay controls, normalization basis, and usable measurement range are not documented.

Expected: experimental. Technical wells cannot establish biological replication; missing assay validity and normalization information constrain the claim.

### C6 — Sample preparation plus sequencing analysis

Donor samples are processed in laboratory batches and then analyzed with a custom pipeline. A group difference could be affected by either sample/batch handling or a computational decision.

Expected: hybrid. The experimental and computational stages must each receive their own evidence lock, while donor/sample and derived observations remain distinct.

### C7 — Reagent dilution optimization

Several dilutions are compared in one run and one condition gives the clearest signal-to-background separation. No biological hypothesis is independently tested afterward.

Expected: experimental. The supported status is protocol optimization in the tested run, not validation of a biological effect or universal optimality.

### C8 — Software-only review interface

The workstream changes how users review and save results but makes no claim about assay performance or a biological intervention.

Expected: computational/software. The wet-lab lock must not be loaded.

### C9 — Treatment and batch are aligned

All controls were processed on day 1 and all treated samples on day 2. The readout passes within-run QC and the draft attributes the difference to treatment.

Expected: experimental. Treatment is confounded with processing day; passing assay QC does not recover the causal contrast.

### C10 — Mixed Progress deck

One independent workstream reports an intervention experiment, another reports a software release, and a third reports specimen generation followed by custom analysis.

Expected: experimental, computational/software, and hybrid respectively. Routing is per workstream and, for the hybrid workstream, per stage; the deck receives no single global profile.

## Mutation challenges

The final workflow must reject these transformations:

1. replace the experimental unit with the number of cells, fields, wells, or repeated readings;
2. rename technical repeats as independent replication;
3. convert a representative image into evidence of prevalence or reproducibility;
4. omit actual exclusions or attrition while retaining the original `n`;
5. call one selected dose, time, or dilution “optimized” without a relevant comparison;
6. call an assay-valid run a confirmed biological result without the required independent units;
7. claim that a computational stage ran because its code exists;
8. apply only one evidence lock to a hybrid claim whose conclusion depends on both stages;
9. load the full experimental checklist for a software-only workstream;
10. fill a missing control, randomization, blinding, or resource-validation fact from plausibility.

## Evidence basis

The generic invariants were derived from the Nature Portfolio life-sciences reporting summary, NIH rigor/reproducibility and key-resource authentication guidance, ARRIVE 2.0 for animal research, and MIQE 2.0 for qPCR. Modality-specific requirements remain conditional; they are not converted into universal slide fields.

## Observed internal forward test

The finalized router and conditional references were applied to the fixed cases without changing the cases or rubric.

| Case | Route produced | Claim decision produced | Result |
|---|---|---|---|
| C1 | computational | Audit the frozen input, code/run, parameters, and result; do not request wet-lab execution evidence for the current contribution. | pass |
| C2 | experimental | Treat the wells as nested observations of one preparation unless another independent unit is documented; block “independently replicated.” | pass |
| C3 | experimental | Surface cage-level assignment and animal nesting; block an unqualified `n=32` independent-treatment claim. | pass |
| C4 | experimental | Allow the selected fields to illustrate appearance only; block prevalence or reproducibility without selection, quantification, and independent units. | pass |
| C5 | experimental | Treat qPCR wells as technical repeats; keep assay validity, normalization, and independent biological evidence unresolved rather than inventing them. | pass |
| C6 | hybrid | Apply the experimental lock to donor/sample preparation, batch, acquisition, and QC, then the computational lock to pipeline execution and decisions; bound the claim by both. | pass |
| C7 | experimental | Report a pilot-compared operating condition in one run; block biological validation and universal optimality. | pass |
| C8 | computational | Apply the software release and execution evidence rules; do not load the wet-lab reference. | pass |
| C9 | experimental | Preserve the QC-passed observation but identify treatment/day confounding and block causal attribution to treatment. | pass |
| C10 | per-workstream; hybrid by stage | Route the intervention, software, and specimen-plus-analysis workstreams separately; apply both locks only to the third. | pass |

All 10 routing/claim decisions satisfied their applicable critical invariants. This is a same-agent forward application, so the result demonstrates rule coverage and internal coherence rather than independent generalization.

## Mutation audit result

All 10 fixed mutations were rejected by a decision-bearing rule:

| Mutations | Guard that rejected them |
|---|---|
| 1–2 | Independence is defined by design; nested observations and technical repeats cannot silently become independent `n`. |
| 3 | Representative appearance is separated from quantified prevalence and reproducibility. |
| 4 | Allocation, acquisition, and analysis counts must be reconciled with exclusions and attrition. |
| 5–6 | Choice provenance and evidence maturity separate optimization, assay validity, observed effect, and independent repetition. |
| 7 | Computational implementation, recorded execution, and result artifact remain separate. |
| 8 | A hybrid claim must pass both stage-specific evidence locks. |
| 9 | The dependency router loads only the relevant conditional reference. |
| 10 | Unknown experimental facts remain unknown and constrain the claim. |

The audit found no reason to add a universal wet-lab checklist or a new planning artifact. The compact experimental ledger remains conditional inside the existing `progress_map.md`.

### Post-hoc false-positive challenge

A simple wet-lab experiment that uses routine instrument acquisition, file export, and standard plotting was tested after the main audit. It remained `experimental`, not `hybrid`; the computational lock activates only when a processing/version/parameter decision materially supports the conclusion or is itself reported progress. This check was added after, and is not counted among, the 10 fixed cases.
