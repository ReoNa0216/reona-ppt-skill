# Workflow: Progress Update

Use for lab-meeting recent-work reports, project updates, analysis status, software/tool development, and completed-output summaries.

## Audience question

> 最近做了什么？最强证据是什么？结果可信到什么程度？哪些已经完成，哪些仍然需要判断或决策？

Do **not** force independent workstreams into one causal scientific story.

## Planning artifact: `progress_map.md`

For each workstream record:

| Field | Required content |
|---|---|
| Workstream | Audience-readable name, not folder/module name |
| Audience priority | primary / secondary / backup, plus the one takeaway the audience must retain |
| Starting premise | The observation, prior result, operational friction, or preset hypothesis that started the workstream |
| Scientific/operational question | What this workstream is trying to establish or remove |
| Authoritative source order | Which current sources govern the premise, methods, result, release state, and limitations |
| Since last report | What materially changed |
| Strongest completed result | The most decision-relevant result already supported by the work |
| Displayed evidence | The figure, table, or screenshot that most directly supports that result |
| Analysis unit | cell / patient / event / project / software release etc. |
| Boundary | What the result does not establish |
| Status | completed / ongoing / blocked / validation needed |
| PI decision needed | include only when a real decision exists; otherwise omit |

## Workstream truth lock

Complete `Starting premise`, `Authoritative source order`, `Strongest completed result`, and `Displayed evidence` before choosing slide titles or layouts.

- Treat folders, repository names, old slide decks, and internal labels as locators, not as audience-facing descriptions or scientific premises.
- Read enough of the authoritative project sources to distinguish the original question, the preset expectation or candidate definition, the strongest completed result, and the main limitation.
- Do not select the most visually convenient figure and then reverse-engineer the workstream conclusion from it. The displayed evidence must answer the actual workstream question.
- Lead with the strongest defensible achievement. Keep a necessary limitation close to the result, but do not let a catalogue of caveats obscure what was completed.
- Assign `primary / secondary / backup` before storyboarding. Give explanation depth to the user's priorities; do not let adjacent completed work consume equal space merely because it exists.

## Computational method and parameter lock

Use this section of `progress_map.md` when a workstream teaches an analysis pipeline, algorithm, data-processing method, or scientific software behavior. Keep it conditional; ordinary result updates do not need it.

### Process execution ledger

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

### Parameter evidence ledger

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

## Method teaching ladder

Before allocating slides to a primary method-heavy workstream, list its prerequisite concepts in dependency order:

`data object and analysis unit → stage input → operation and intuition → formula or decision rule when needed → stage output → next-stage dependency → execution evidence → boundary`

Use one audience-level conceptual jump per slide. A simple result may need one slide; a multi-stage method may need several. Do not impose a 1–2 slide cap when that would skip a prerequisite, introduce a parameter before its role, or jump from one intermediate representation to a later decision.

- Introduce what is counted, compared, shifted, grouped, or assigned before presenting its statistic.
- State the unit and construction of folds, groups, windows, or held-out sets; do not replace their design with a convenient but inaccurate label such as “two halves.”
- For a non-intuitive chart, define both axes, the statistic, the analysis unit, and the reading direction.
- Introduce a general rule before a current numerical example. Label current values as current instances, not universal constants.
- Put a main-deck formula only where it advances the stage logic. Define every symbol on the slide, give one plain-language purpose, and explain selection order in prose before a compact optimization expression. Move full derivations and dense parameter inventories to backup.
- If a term does not let a first-time listener identify the object, operation, and decision, rewrite it in ordinary Chinese or define it before using the short form. Internal names and untranslated English are not substitutes for explanation.

## Narrative grammar

Default order:

`starting premise / workstream question → strongest completed result → displayed evidence → conclusion boundary → status`

Let audience priority and conceptual dependency determine slide count. Compress repeated evidence, not missing logic. Workflow detail belongs where it is required to understand the result, reproduce the claim boundary, or distinguish a full comparison from a local diagnostic.

Name each workstream by the audience-facing achievement or question, not by its directory, repository, package, or internal acronym. Independent workstreams may remain independent; use a brief transition instead of inventing a causal progression.

When a workstream begins with an internal discovery or preset candidate definition and then tests it in external data, use this optional validation grammar:

`internal discovery or preset premise → candidate-definition lock → role of each external dataset → primary-unit result → independent-unit result → boundary`

Use only the stages that exist. Do not imply that a localization dataset supports longitudinal comparison, or that a cell-level result has been independently validated at the patient, sample, or replicate level.

For software, use:

`user friction → one concrete review flow → evidence that the interface removes the friction → save/handoff behavior`

Do not lead with implementation facts, file formats, test counts, or internal module names.

The interface state shown must support the claimed convenience. If a capability cannot be demonstrated by the screenshot, verify it from the current release/source contract in the notes or remove the claim.

Before handoff, freeze one software release snapshot inside `progress_map.md` or the source manifest:

- official repository and branch/tag/commit;
- release maturity and displayed version;
- exact screenshot version and interface state;
- whether the screen uses real, demo, fixture, or synthetic data.

The slide, screenshot label, notes, and source manifest must use the same snapshot. An older interface image may be retained only when explicitly approved and must not serve as evidence for a newer interaction. Field counts, schema widths, test counts, and internal state names belong on the slide only when they materially explain the user task or output semantics.

For a computational method screenshot or schematic, apply the same evidence discipline as software: every visible state, field, control, and workflow claim must be present in the inspected version or verified by its authoritative contract. Do not fill an explanatory gap with a plausible interface behavior.

## Closing rule

End with **completed, verifiable outputs**. Add blockers, decisions, or next actions only when they are genuinely discussion-worthy; never add a generic “next step” page for symmetry.

## Storyboard minimum

Each slide entry in `scientific_handoff.md` must contain:

- audience priority and required takeaway;
- starting premise and authoritative source priority when needed to interpret the result;
- slide job;
- single result/conclusion;
- displayed evidence;
- analysis unit;
- conclusion boundary;
- status if relevant;
- software release snapshot when relevant;
- method-stage input, operation, and output when relevant;
- execution evidence and result artifact for a claimed completed process when relevant;
- parameter evidence class and wording boundary for an exact decision value when relevant;
- reusable rule versus current-instance example when transfer or generalization is discussed;
- speaker-note job.

Before handoff, run an audience-language pass on the slide roster: expand abbreviations at first use, keep quantities in Arabic numerals, replace internal labels with audience-readable terms, and ensure no title depends on an unexplained method name or metric.
