# Progress Computational Evidence

Read this reference for a `computational` Progress workstream and for every computational stage of a `hybrid` workstream. Do not load it merely because the scientific subject is biological; the current claim must depend on code, data processing, an algorithm, or a software state.

## Process execution ledger

For every process that may appear in the deck, record:

| Field | Required content |
|---|---|
| Audience object | What enters this stage, in audience-readable language |
| Implemented operation | What the inspected source or contract implements |
| Execution evidence | Run command, run record, configuration/hash, log, or other evidence that this exact work executed the operation |
| Result artifact | The output that demonstrates the operation's observed result |
| Allowed claim | The strongest wording jointly supported by implementation, execution, and result |
| Excluded claim | A plausible overstatement that the evidence does not support |

Code presence, recorded execution, and result evidence are three different facts. A method found only in source is `implementation-only`; do not describe it as part of the completed run. If current source differs from the executed snapshot, state which behavior is established by the run artifacts and which is only current implementation. Do not import a stage merely because it appears in an older deck.

Treat a reference deck as two separate sources: it may govern visual identity, teaching depth, or useful explanatory patterns, but its scientific content is subordinate to current contracts, run records, and results.

## Parameter evidence ledger

Record each exact parameter or decision rule that matters to the audience as:

`role → value/formula → source → alternatives actually executed → affected scope → evidence class → wording boundary`

Use the narrowest applicable evidence class; use more than one only when they describe different scopes and keep those scopes explicit:

- **data-derived** — estimated from current data through a fixed formula; the formula's multiplier may still be untested;
- **full rerun comparison** — alternatives reran every downstream stage that the parameter can affect;
- **local endpoint comparison** — alternatives changed only a local diagnostic such as recall, not the final axis or model;
- **fixed-axis slice** — thresholds were applied to one already frozen axis or assignment;
- **perturbation stability** — the fixed method was challenged by a grid shift, deletion, resampling, or similar perturbation;
- **diagnostic/nonbinding** — computed or checked but not used to make the current decision, or far from its stopping limit;
- **untested frozen constant** — one value was executed with no direct alternative comparison.

Never collapse these classes into the generic word “sensitivity.” In particular, a fixed-axis slice is not a full pipeline sensitivity test, and deleting data from a frozen result is not the same as refitting without those data. Use “optimized,” “blind-selected,” “preregistered,” “validated,” or “generalizable” only when the source and comparison scope support that exact word.

Separate three layers whenever transfer is discussed:

1. the reusable algorithmic rule or invariant;
2. the dataset-specific quantity that must be re-estimated;
3. the current dataset's numerical instance or example.

An illustrative candidate or current feature count may teach the method, but it must not become the rationale for the method or a target used to tune parameters.

## Computational teaching ladder

Before allocating slides to a primary method-heavy workstream, list its prerequisite concepts in dependency order:

`data object and analysis unit → stage input → operation and intuition → formula or decision rule when needed → stage output → next-stage dependency → execution evidence → boundary`

Use one audience-level conceptual jump per slide. A simple result may need one slide; a multi-stage method may need several. Do not impose a nominal page cap when that would skip a prerequisite, introduce a parameter before its role, or jump from one intermediate representation to a later decision.

- Introduce what is counted, compared, shifted, grouped, or assigned before presenting its statistic.
- State the unit and construction of folds, groups, windows, or held-out sets; do not replace their design with a convenient but inaccurate label.
- For a non-intuitive chart, define both axes, the statistic, the analysis unit, and the reading direction.
- Introduce a general rule before a current numerical example. Label current values as current instances, not universal constants.
- Put a main-deck formula only where it advances the stage logic. Define every symbol on the slide, give one plain-language purpose, and explain selection order in prose before a compact optimization expression. Move full derivations and dense parameter inventories to backup.
- If a term does not let a first-time listener identify the object, operation, and decision, rewrite it in ordinary Chinese or define it before using the short form. Internal names and untranslated English are not substitutes for explanation.
- Keep the physical or scientific object connected to its computational representation: identify which observations belong to one sample, which are pooled, and what each row, index, range, or state refers to. Explain how the current range or grouping is constructed before describing a faster lookup.
- For unfamiliar arithmetic, walk through a small input, intermediate values, and output. State what an index or boundary counts before subtracting it; show how a running quantity changes at each step before naming cumulative operations. Put necessary intermediate reasoning in notes and split the visual when one page skips a prerequisite.
