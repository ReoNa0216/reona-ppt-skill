# Speaker Notes Protocol

Write page-matched notes in natural, precise language. Match depth to the teaching job: a transition may need only a sentence; an unfamiliar experiment or model may need a fuller explanation. Inherit an accepted reference deck's note structure when requested. Length is a consequence of useful explanation, not a fixed quota.

## Shared Requirements

Explain, when relevant:

1. the current scientific or operational question and analysis unit;
2. how the displayed figure, result, screenshot, schematic, or formula was produced;
3. how to read axes, colors, groups, panels, thresholds, states, or interface interactions;
4. the key result or workflow benefit;
5. the supported conclusion, with any qualification that changes its interpretation;
6. why the next slide follows.

Use spatial cues to locate the relevant comparison, then explain what to notice and why it matters. Use Arabic numerals for quantities. At first relevant use, explain unfamiliar abbreviations, material or cell identities, treatments, intervention targets, and comparison groups before interpreting their results. If a visual is conceptual or demo data, identify that role clearly.

Keep the visible slide focused on its question, operation, or result. Use notes to teach the experiment, figure, or calculation. Keep citations, exact panel locators, source paths, and asset provenance in a compact source block or manifest, separate from the spoken explanation. Add supporting context only when it helps explain the current page, and identify it as context rather than a displayed panel.

Write affirmative explanations of what is studied, measured, inferred, or proposed. Retain uncertainty at the point where it affects a claim or decision; remove repeated caveats, defensive comparisons, obsolete debate history, and statements about unrelated capabilities. There is no mandatory limitation paragraph. If a sentence only explains what the page is not doing, replace it with the actual operation or delete it unless the distinction is essential.

Use audience-readable Chinese for the scientific object and operation. An internal term, acronym, or English label may follow after the meaning is clear, but must not carry the explanation by itself. When a fold, subset, window, or held-out group matters, state how it was constructed rather than replacing it with a looser analogy.

After the visible slide is final, run a bidirectional consistency check:

- every claim-bearing figure, table, screenshot, schematic, and formula on the slide is explained in the notes;
- references to on-slide objects, values, versions, labels, and positions identify the correct current elements;
- additional calculations, definitions, and background in notes agree with the current method and sources; their intermediate values need not appear on the slide, and illustrative calculations remain distinct from measured results;
- quantities, analysis units, thresholds, evidence status, terminology, and software versions agree across slide, notes, and source manifest.
- consequential parameter values, provenance, and comparison scope agree with the scientific handoff;
- no note upgrades a local diagnostic, fixed-axis slice, or deletion stress into a full rerun or refit;
- for an experimental claim, units and exact `n`, controls, performed execution, run validity, exclusions, and repeat/corroboration status agree with the handoff;
- every formula symbol, chart axis, and non-intuitive statistic shown on the slide has a readable explanation, and no explanation survives for a removed symbol or panel.

Remove stale narration instead of preserving explanations for deleted or replaced content.

## Progress Update

Use:

`starting premise / question → current progress → evidence/readout → interpretation → status/decision when useful`

For independent workstreams, provide a clean transition without inventing a scientific causal link. For software, explain the user task, the friction removed, what the shown screen state demonstrates, and how work is saved or handed off.

For a computational-method slide, use the relevant subset of:

`input object and analysis unit → operation → why it is needed → how to read the schematic/formula → output passed onward → implementation or execution status → parameter basis and comparison scope`

Do not narrate every implementation detail. Explain the details needed to understand the stage dependency, the displayed result, and whether a parameter was derived, compared end to end, sliced on a fixed axis, or only checked diagnostically.

For an experimental slide, use the relevant subset of:

`contrast and controls → independent unit and n → what was actually performed → readout and QC → result → repeat/corroboration status`

Explain only the design facts needed to interpret the evidence. For a hybrid workstream, make the handoff from specimen generation or acquisition to computational processing explicit and apply the appropriate note logic to each stage.

## Journal Club

For substantive pages, default to two sections in the requested note language:

- **Spoken script (讲稿)**: natural oral prose following `question → experiment → comparison to look at → visible result → supported conclusion → next question`. Name the groups and the feature that supports the inference. Keep qualifications needed to understand that conclusion in the script.
- **Deeper interpretation (深入解读)**: source-verified principles, control roles, experimental conditions, replication and statistics, calculations, and interpretation limits useful for questions. Explain the details that answer a concrete scientific question.

Adapt this structure to an accepted reference deck; short transitions need only a script. Read the scripts consecutively to check the section handoff, terminology, oral rhythm, and why each next experiment follows. Audit the deeper interpretation separately so preparation detail stays out of the spoken narrative.

## Idea Discussion

Use:

`question → evidence motivating the choice → proposed operation → schematic/formula meaning → validation → resulting decision`

For each claim-bearing panel, connect it to the deck's main question as `panel role → visible cue → supported inference → consequence for the proposed analysis or experiment`. Name the score, coordinate, comparison, or dynamic analysis that supplies the evidence; screen position alone supplies no scientific meaning.

Explain the biological role of a main-deck formula before mathematical detail. When a costly modality or complex method is central to the proposal, explain which simpler alternative it must outperform and how failure would narrow the claim. State when a proposed capability depends on data or evidence not yet available.

For an unfamiliar method, a short labeled numerical teaching example may explain inputs, intermediate operations, and output. Define the time coordinate and what remains fixed or changes when these affect interpretation. Keep this explanation tied to the current method and decision rather than adding a catalogue of unsupported applications.
