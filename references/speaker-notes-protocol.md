# Speaker Notes Protocol

Write page-matched notes in formal, natural language. A typical content slide needs about `250–400` Chinese characters; use less for transitions and more only when a complex figure genuinely requires it.

## Shared Requirements

Explain, when relevant:

1. the current scientific or operational question and analysis unit;
2. how the displayed figure, result, screenshot, schematic, or formula was produced;
3. how to read axes, colors, groups, panels, thresholds, states, or interface interactions;
4. the key result or workflow benefit;
5. the supported conclusion and its boundary;
6. why the next slide follows.

Do not repeat the title, narrate page layout, expose internal filenames/folder names, or spell quantities with Chinese numeral words. Define abbreviations at first audience-facing use. If a visual is conceptual or demo data, say so explicitly.

Use audience-readable Chinese for the scientific object and operation. An internal term, acronym, or English label may follow after the meaning is clear, but must not carry the explanation by itself. When a fold, subset, window, or held-out group matters, state how it was constructed rather than replacing it with a looser analogy.

After the visible slide is final, run a bidirectional consistency check:

- every claim-bearing figure, table, screenshot, schematic, and formula on the slide is explained in the notes;
- every page-specific visual, number, version, label, or position mentioned in the notes still exists on the current slide;
- quantities, analysis units, thresholds, evidence status, terminology, and software versions agree across slide, notes, and source manifest.
- every exact parameter is described with the same role, derivation, comparison scope, and evidence class as the scientific handoff;
- no note upgrades a local diagnostic, fixed-axis slice, or deletion stress into a full rerun or refit;
- for an experimental claim, units and exact `n`, controls, performed execution, run validity, exclusions, and repeat/corroboration status agree with the handoff;
- every formula symbol, chart axis, and non-intuitive statistic shown on the slide has a readable explanation, and no explanation survives for a removed symbol or panel.

Remove stale narration instead of preserving explanations for deleted or replaced content.

## Progress Update

Use:

`starting premise / question → what materially changed → evidence/readout → result → boundary → status/decision`

For independent workstreams, provide a clean transition without inventing a scientific causal link. For software, explain the user task, the friction removed, what the shown screen state demonstrates, and how work is saved or handed off.

For a computational-method slide, use the relevant subset of:

`input object and analysis unit → operation → why the operation is needed → how to read the schematic/formula → output passed onward → evidence that this run executed it → parameter basis and comparison scope → boundary`

Do not narrate every implementation detail. Explain the details needed to understand the stage dependency, the displayed result, and whether a parameter was derived, compared end to end, sliced on a fixed axis, or only checked diagnostically.

For an experimental slide, use the relevant subset of:

`contrast and controls → independent unit and n → what was actually performed → readout and QC → result → repeat/corroboration status → boundary`

Explain only the design facts needed to interpret the evidence. For a hybrid workstream, make the handoff from specimen generation or acquisition to computational processing explicit and apply the appropriate note logic to each stage.

## Journal Club

Use:

`question → experiment → how to read the figure → result → what it proves → what it does not prove → why the next experiment is needed`

Figure-heavy slides may use longer notes. The notes should teach the audience how to interpret the selected evidence without forcing every panel onto the page.

## Idea Discussion

Use:

`problem/claim → why this step is necessary → what is evidence versus proposal → schematic/formula meaning → assumptions → validation/falsification → boundary or phase gate`

For each claim-bearing panel, connect it to the deck's main question as `panel role → visible cue → supported inference → consequence for the proposed analysis or experiment → boundary`. Do not narrate screen position as scientific meaning; name the score, coordinate, comparison, or dynamic analysis that supplies the evidence.

Explain the biological role of a main-deck formula before mathematical detail. When a costly modality or complex method is central to the proposal, explain which simpler alternative it must outperform and how failure would narrow the claim. State when a proposed capability depends on data or evidence not yet available.
