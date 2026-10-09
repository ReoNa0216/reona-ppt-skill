# Workflow: Idea Discussion

Use for proposed projects, scientific directions, modeling ideas, experiment design, or a deck whose purpose is to decide what is worth testing and how to test it.

## Start from the user's current task

- **Discuss first:** investigate the question, compare options, and present a design recommendation. If the user asks to discuss before making slides, stay in discussion until they authorize production.
- **Create or revise:** a request to make the deck, proceed with a discussed plan, or revise named pages authorizes that work. Resolve routine choices from existing context; do not require an additional approval phrase or a separate Design Freeze ceremony.
- **Continue an existing deck:** read its visible content, notes, sources, and relevant decision history. Carry accepted decisions forward. Ask again only when new evidence or the requested change materially reopens them.

The Design Freeze is the current agreed design, not a permanent prohibition on change. Maintain it in the project's existing content source or in a concise design memo. Do not create duplicate files just to satisfy a template.

```text
read evidence and prior decisions → identify the decision → compare feasible designs
    → record the current design → produce when authorized → inspect and discuss
                                    ↑                         ↓
                                    └── revise affected decisions and pages ──┘
```

In mixed decks, route each section independently. An unresolved Idea section blocks only production that depends on the missing decision; continue authorized work on the other sections.

## Read first, then ask

Follow [the evidence-first interview](../references/evidence-first-interview.md). Read supplied material relevant to the decision, including methods and legends behind consequential claims. Recover accepted choices from existing notes or project records when earlier conversations are unavailable.

Ask a small number of questions that change the scientific question, feasibility, comparison, or intended claim. Continue independent research and planning while answers are pending. When an answer is essential, hold only the dependent design choice. Record ordinary assumptions and proceed within the user's authorization.

## What the design must explain

Use these questions as reasoning aids, not a mandatory slide sequence or questionnaire:

1. **Value:** what important question is unresolved, and what new information would answering it provide?
2. **Evidence:** what is established, what follows by inference, and what remains a proposed test?
3. **Feasibility:** what can be measured or manipulated with the available resources? Which unresolved resource changes the design?
4. **Target:** what is the smallest independently valuable question, with a defined experimental/analysis unit, input, comparison, and output?
5. **Necessity:** what is the strongest credible simpler or lower-cost alternative, and what information would the proposed approach add?
6. **Test:** which experiment or held-out comparison would support, revise, or reject the hypothesis? What confounding would change that interpretation?
7. **Decision:** what result determines the next action or a justified expansion of scope?

Preserve the user's declared source priority when reconciling existing design memos, storyboards, and asset lists. For a large new proposal, `design_freeze.md` and `claim_evidence_map.md` can hold this reasoning. For an existing project, update the equivalent fields in its current source. Use a separate open-question list only when unresolved decisions need tracking.

For each consequential claim, retain:

`claim → evidence status → source → displayed evidence → analysis unit → material qualification`

Use `established`, `source-supported`, `inference`, and `proposal` internally to select accurate wording. Add a discriminating test to central hypotheses. These fields do not all belong on the visible slide.

## Make discussion change the design

Compare plausible alternatives before selecting one. Recommend a design and explain the evidence and resource tradeoff; do not turn every uncertainty into a question for the user.

When several novel components are proposed together, identify which are essential to the central question and which require preliminary evidence. Link each decisive preliminary result to a scope choice. A simpler design should still answer a worthwhile question; retain a combined design when its interaction is the actual question and can be tested with the available resources.

Read [validation design](../references/idea-validation-design.md) when the proposal involves pilot-based scope selection, prediction, transfer, or model-derived intervention candidates. Apply only the relevant sections.

Reproducing an established result provides a validity anchor. Establish the additional information supplied by the new measurement or analysis before claiming novelty. If the increment is unresolved, make it the question to test.

## Build the argument for this meeting

A useful chain is:

`important problem → what evidence has established → remaining question → proposed measurement/design → analysis or model → decisive validation → decision`

Introduce the data object and the information the method must preserve before teaching a named method. Organize literature by the role each result plays in this argument, rather than giving every paper equal space.

Adapt the deck to its job. An exploratory deck may compare competing explanations and teach the evidence in depth. An execution deck should foreground comparisons, operations, readouts, dependencies, and decision rules. Derive the execution deck from accepted decisions rather than mechanically shortening the exploratory deck.

Give each page one scientific job. Split when the audience must first interpret evidence, then choose a design, then understand a different validation output. Respect the requested page budget by selecting evidence and moving teaching detail to notes; propose a scope adjustment if essential reasoning cannot fit legibly.

## Explain methods at the level needed for a decision

- State the input, operation, output, and scientific purpose. Pair a main-deck formula with its plain-language meaning and define its symbols.
- Distinguish existing demonstrated capability from a proposed extension. Assess an extension through its assumptions, required data, and validation plan; missing implementation alone does not invalidate a coherent proposal.
- Define held-out units, grouping, and allowed calibration for generalization or transfer. Match evaluation to the output actually produced by the model.
- Compare unresolved method choices by scientific information preserved, stability, validation performance, and interpretability. Mathematical complexity is not itself a contribution.
- Use a short, clearly labeled teaching example when it makes a method understandable. Keep derivations and full objectives in notes or requested backup material.

## Treat visual feedback as scientific feedback

Before drawing a schematic, specify what each object and arrow means: a group, stage, measurement, operation, relationship, or prediction. Distinguish separate comparisons from successive stages. Keep colors and symbols stable across pages.

Use original figures for evidence and redraws or image generation for explanatory schematics. Show hypotheses as hypotheses; conceptual trajectories and state diagrams are allowed when their illustrative role is clear.

When feedback exposes an ambiguous figure, unsupported transition, or mismatched metric, repair the design or explanation first. Then update the affected slide, notes, figure, and source record together. Do not substitute a defensive paragraph for that repair.

## Iterate and deliver

For each feedback round:

1. Identify the changed decision and its dependencies.
2. Preserve accepted content and visual conventions outside that change.
3. Revise the canonical source, then regenerate or edit the affected pages.
4. Check the exported pages, notes, and cross-page consistency. Verify protected reference files remain unchanged when a derivative deck is requested.

Close with the decision the meeting needs: a recommended design, the next decisive experiment, a validation comparison, or a conditional roadmap when later stages matter. Do not add phases merely to complete a template.

Use [the scientific content contract](../references/scientific-content-contract.md) for the production handoff and the main skill's final review for export QA. Reuse a working project pipeline; otherwise use `ppt-master` for visual production.
