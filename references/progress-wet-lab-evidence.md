# Progress Wet-Lab Evidence

Read this reference for an `experimental` Progress workstream and for each experimental stage of a `hybrid` workstream. It applies when the claim depends on physical manipulation, preparation, treatment, acquisition, or measurement. Use it as a planning lock, not a checklist to place on slides.

## Core evidence lock

Freeze each claim-bearing experiment as:

`scientific contrast → independent unit → performed procedure → valid measurement → observed result → repetition/corroboration → boundary`

A planned protocol, a performed experiment, a QC-passed measurement, an observed contrast, an independent repeat, and an orthogonal confirmation are different facts. The claim cannot be stronger than the weakest necessary stage. Keep a consequential unknown as `unknown`; never complete it from custom or plausibility.

## Minimal experiment ledger

Record only fields that can change interpretation:

| Field | Required content |
|---|---|
| System, contrast, controls | What was studied, groups compared, and what each relevant control rules out |
| Units and counts | Smallest independently assigned or sampled unit, nested observational/technical units, definition of an independent repeat, exact `n` and its basis when decision-relevant, pooling, attrition, and exclusions |
| Performed execution | Authoritative plan, evidence of what actually ran, and consequential deviations or failed runs |
| Bias and confounding | Allocation, blocking, order, blinding, batch, operator, instrument, or resource identity when relevant; otherwise not applicable or unknown |
| Choice provenance | Basis of a consequential dose, duration, time point, dilution, cutoff, or stopping rule; alternatives actually compared and whether selection preceded the target result |
| Measurement validity | Raw artifact, measured quantity, processing/normalization and denominator, applicable controls, usable range, run-level QC, and summary/test at the correct unit |
| Evidence maturity | Protocol optimization, one QC-passed observation, independent repetition, orthogonal corroboration, or external replication |
| Claim boundary | Strongest supported wording and the closest plausible overstatement |

Keep interpretation-changing items on the slide or in notes; preserve the rest in `progress_map.md` and the source manifest.

## Interpretation rules

- Define independence from the design and intended inference, not from the number of rows or plotted marks. Cells, fields, wells, sections, reads, and repeated measurements from one source are nested unless the design supports another level.
- Technical repeats describe measurement variation; they do not by themselves establish experimental or biological replication. State what `n` counts, including assignment level, pools, repeated measures, and counts lost before analysis.
- Controls are claim-dependent. A passing control or run-level QC establishes assay validity only for its scope. If condition is aligned with day, plate, cage, batch, operator, or acquisition order, the biological contrast may remain confounded.
- Report what was planned and what was performed. Separate prespecified exclusions from decisions made after seeing data, and verify only key resources whose identity or variability can materially change the result.
- Distinguish raw measurement, normalization, derived endpoint, and summary. A representative image shows the displayed field; prevalence, effect size, and reproducibility require defensible selection, quantification, and independent units.
- Independent repetition, rescue, orthogonal measurement, and external replication address different uncertainties. Name the alternative each one addresses; none automatically proves the full mechanism.
- For a consequential experimental choice, use precise wording such as source-established, constrained, pilot-compared, dose/time-response compared, feasibility-chosen, conventional but untested here, adaptive/post hoc, or diagnostic. Do not say “optimized,” “prespecified,” or “validated” beyond the actual comparison.

## Conditional modality prompts

Use only the prompt needed by the claim:

| Claim-bearing modality | Additional question |
|---|---|
| Imaging or cytometry | Were selection/gating, sample nesting, and acquisition/processing comparable across groups? |
| Gel, blot, or amplification assay | Are identity, controls, normalization, usable range/saturation, and independent repeats adequate for the claim? |
| Cell line, engineered system, organism, or regulated material | Can source/identity, assignment unit, relevant biological variables, attrition, oversight, or key environmental conditions change interpretation? |
| High-throughput specimen generation plus custom analysis | Route as `hybrid`: this lock governs preparation/acquisition and the computational lock governs processing/analysis. |

Do not invent missing modality details. A consequential absence becomes a boundary or a question.

## Experimental teaching ladder

Teach a primary design-heavy workstream in dependency order:

`contrast → system and controls → independent unit and n → performed procedure → readout and QC → result → repetition/corroboration → boundary`

Use one audience-level conceptual jump per slide. Combine stages when they remain clear; expand only when unfamiliar controls, nested units, or multiple readouts are necessary to interpret the result. Do not turn the protocol into a slide-by-slide recipe.
