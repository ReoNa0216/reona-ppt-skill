---
name: reona-ppt-skill
description: Develop, discuss, create, or revise PI-facing scientific PowerPoint decks. Route progress updates, journal clubs, idea discussions, and mixed decks through source-verified scientific planning and iterative review. Preserve an accepted reference deck's style or use ReoNa's Tsinghua-purple defaults, then produce and verify the requested deliverable.
---

# ReoNa PPT Skill

Use this skill for scientific reasoning, narrative, evidence, speaker notes, and presentation QA. Reuse a project's working production pipeline when available; otherwise use `ppt-master` for visual planning, generation, formula rendering, export, and generic technical QA.

## Scientific Planning Gate

Resolve the scientific decisions needed for the requested production or revision. Reuse accepted decisions and existing source records.

### 1. Route each scientific section

- **Progress Update** — recent work, completed analyses or experiments, software/tool progress, and project status. Read [workflows/progress-update.md](workflows/progress-update.md); it automatically routes each workstream as computational, experimental, hybrid, or general and loads only the relevant evidence reference.
- **Journal Club** — a paper or small paper set whose evidence chain must be taught and critiqued. Read [workflows/journal-club.md](workflows/journal-club.md).
- **Idea Discussion** — a proposed scientific direction, model, experiment, or project requiring scope control and testable design. Support discussion, authorized production, and iterative revision. Read [workflows/idea-discussion.md](workflows/idea-discussion.md).

Route mixed decks section by section. Cover, agenda, transition, and closing pages inherit the routed scientific sections; they do not need their own archetype. Keep one visual system without forcing sections into one narrative grammar. Honor production authorization and agreed review steps. For Idea sections, use the [task and review agreement](workflows/idea-discussion.md#task-and-review-agreement). Resolve consequential missing choices while continuing independent work.

### 2. Audit sources and freeze claims

- For research results, read the authoritative manuscript/report, methods, legends, and available results before outlining. For Progress workstreams, establish the actual starting premise and source priority before selecting the most informative supported progress. For software, inspect source and records for the version being reported.
- Record the planning information required by the routed workflow. Use its named worksheets for new projects, or equivalent sections in an existing authoritative content source; avoid duplicate records.
- Freeze each consequential claim as `claim → source → displayed evidence → analysis unit → boundary → evidence status`.
- For each Progress workstream, infer its evidence profile from what the claim depends on, not from topic keywords. Route a hybrid claim stage by stage; do not require the user to preselect dry-lab or wet-lab mode.
- For computational Progress claims, distinguish `implemented in source → executed in the recorded work → supported by a result artifact`. A source-code path alone does not prove execution. Record consequential parameter provenance and actual comparison scope using the computational reference.
- For experimental Progress claims, distinguish `planned protocol → performed procedure → QC-passed measurement → observed result → independent repetition or corroboration`. Do not infer controls, independence, execution, or validation from a plausible protocol or polished plot.
- Use audience-readable descriptions, never internal folder or module names. Introduce each dataset before its result: what was sampled, the comparison, and the readout. Explain a limitation when it changes interpretation or a decision.
- Distinguish **established / source-supported / inference / proposal** in planning. Do not expose these audit labels on slides unless they help the audience.

### 3. Produce the scientific handoff

Read [references/scientific-content-contract.md](references/scientific-content-contract.md). Maintain one production source containing section routing, claims, page-level storyboard, asset plan, and note jobs. Use `scientific_handoff.md` for a new handoff or the project's existing equivalent. Keep scientific content consistent before producing affected pages.

## Shared Scientific Rules

- Give each slide one scientific job and a clear message: a question, an operation to understand, or a supported result. The title should communicate that job, not merely name a dataset, file, module, or figure number.
- Put the analysis or experimental unit on the slide when it affects interpretation. When observations are nested, state what `n` counts rather than using cells, fields, wells, or repeated measurements as implicit independent units.
- Match every conclusion to the displayed evidence. Correlation is not causality; gene-level change is not pathway proof; an uncorrected trend is not a validated result.
- Do not force weakly annotated measurements into a biological identity to make a cleaner story. If a result is not integrated into the current workflow, show it as a standalone result and break the pipeline connection visually.
- Define unfamiliar abbreviations at first relevant use. Put the expansion on the slide when it is needed to read the evidence; place supporting definitions in notes. Follow the requested slide and note languages. Use Arabic numerals for quantities in slides and notes.
- For Chinese content, use ordinary Chinese for the object, operation, and decision; retain necessary software names, standard abbreviations, and clearer technical terms after definition. Separate prose with punctuation, line breaks, arrows, or aligned columns according to meaning; avoid centered dots as prose separators.
- Verify consequential literature and method claims against primary sources within the requested research scope. Use external context when it serves the question; distinguish it from the user's own results.
- Write the content directly: question, evidence, interpretation, operation, and decision. Keep qualifications that affect these; remove repeated disclaimers, debate history, and ritual statements of what each slide does not claim. Follow `anti-defensive-writing` when available; the notes protocol contains the core rule.
- Never use AI-generated images as experimental evidence. Use them only for clearly explanatory schematics, workflows, conceptual mechanisms, or non-data illustrations.
- If a formula belongs in the main deck, pair it with one plain-language sentence stating its scientific role. Define every displayed symbol before or beside the formula. Render it as mathematics; never simulate subscripts or superscripts with ordinary body text. Use notes for intermediate reasoning that would crowd the slide, and backup slides for extended derivations requiring visual inspection.

## Software Storytelling

- Lead with the user's task and the friction removed, then show one concrete review flow and how the work is saved or handed off. Do not lead with implementation facts, test counts, file-format lists, or internal module names.
- Use the reported version's source, screenshots, and execution records consistently; state its development or release status. Label demo data as demo data; never present an interface screenshot as an experimental result.
- A claimed interaction must be visible in the screenshot or supported by the matching source or execution record, with its evidence basis clear in the notes.

## Visual System And Reference Decks

When the user asks to match an accepted deck, inspect representative rendered pages and notes first. Identify each page's scientific job and why the sequence works, alongside its typography, hierarchy, spacing, figure treatment, semantic colors, citations, and notes. Inherit applicable conventions; verify reused scientific claims against their sources. Preserve a designated baseline as a separate file and verify it remains unchanged after producing a derivative. Otherwise use these defaults:

- Canvas: 16:9, `1280 × 720`.
- Palette: primary `#5B2C83`; dark purple `#321748`; secondary `#76529B`; pale purple `#F3F0F6`; text `#17131A`; secondary text `#655E6B`; border `#D8D2DC`. Green `#27856A` means completed/positive; red `#B84A62` means risk/failure.
- Chinese title/body: Microsoft YaHei. Latin body: Arial. Large metrics: Georgia. Displayed and inline equations: Cambria Math, Latin Modern Math, or Computer Modern through math rendering; choose the font that survives the target PPTX/PDF export. Technical identifiers only: Consolas.
- Size starting points: cover title `64`; slide title `34–36`; context line `18`; body `18`; annotation `13–14`; metric `30–42`; footer `11`. Defaults, not hard limits.
- Vertical starting points: section label near `y=49`; title near `y=91`; context line near `y=137`; main content from `y≈177`. Adjust for readability, never to compress an overloaded page.
- Keep titles to one line when reasonable. Give title, context line, and main content visibly separate vertical space.
- Prefer white space, large evidence, simple dividers, and at most one pale information box. Avoid decorative card grids, repeated badges, and generic takeaway bars.
- Do not use a pale-purple field merely to fill an empty region. Every colored region must group content, encode state, or create a necessary hierarchy.

## Literature Screenshots

Use authentic source captures according to their role:

- **Article title:** retain the title, journal identity, and DOI or publication information from the publication PDF or official page. Preserve original typography and color; add a compact author, journal, year citation outside the capture.
- **Figure:** display the experimental comparison supporting the judgment, with its exact panel locator and reading context.
- **Short passage:** capture the original wording and enough context to preserve its meaning. Highlight only the relevant text without obscuring words; record the page or passage locator.

Choose the combination the argument needs. Title and passage captures do not replace experimental evidence for a claim that requires inspecting results. Usually show a paper's full title once in a continuous presentation; later uses retain a short citation and locator.

If using an author manuscript or supplement, identify that source accurately. Never fabricate a publisher header or present retyped text as an original capture. Keep source files, crop provenance, and locators in the asset record. Apply passage highlighting separately from the figure guardrails below.

## Figure And Layout Guardrails

- Never place a badge, caption, or added label over a scientific figure or software screenshot. Put interpretation outside the image frame.
- Crop a source figure only to isolate a claim-bearing panel. Start from the highest-resolution authoritative source and retain the axes, legends, group labels, and annotations needed to interpret that panel; exclude neighboring panels and slide chrome. Check the embedded crop's effective resolution at its final display size; recover a sharper source or split the panel when details are blurred.
- Check every metric and annotation against its container. No text may cross a divider, card edge, figure frame, or page edge.
- Give non-intuitive charts readable axis labels and enough room to explain the statistic. Give complex equations dedicated width or split the explanation; never solve overflow by shrinking symbols until they are unreadable.
- Prefer fewer legible panels over a comprehensive but unreadable collage. Evidence must remain readable at presentation scale.
- Before generating a schematic, define the meaning of each object, arrow, and color. Depict the claimed location, interaction, or state change explicitly with recognizable structures, then check these relationships in the rendered slide. Keep generated assets and prompts alongside their source records.

## Speaker Notes

Read [references/speaker-notes-protocol.md](references/speaker-notes-protocol.md). Notes must explain scientific reasoning that the slide cannot carry visually and must follow the routed archetype; they must not merely restate visible text.

## Handoff And Final Review

Give the production pipeline the authoritative content source, source manifest, and asset plan. When using `ppt-master`, pass the chosen visual system as brand constraints and style guidance, with sizes and coordinates as soft starting points. Reuse the `reona_tsinghua` Brand workspace when applying the default palette.

Record the production tool, authoritative editable source, and latest deliverable in the existing project record. Select the matching generation, template, or native-PPTX workflow. After merging or manual edits, point the record to the current artifact and preserve its native layout and objects during focused revisions.

Map accepted content and style decisions and existing user authorization to the production workflow's prerequisites; resume at the first unmet requirement.

After generation, inspect the source render, then re-inspect every page rendered from the final PPTX or exported PDF at presentation scale. Sign off on the final exported artifact; a correct source render is not sufficient. Apply these ReoNa-specific checks:

- the shown panel or screenshot directly supports the stated claim;
- figure identity, sample counts, analysis units, abbreviations, and evidence status are correct;
- scientific figures are legible, schematics cannot be mistaken for data, formula meaning is explicit, and equation fonts, symbols, subscripts, superscripts, minus signs, and relation signs survive export without empty glyphs;
- no text, caption, or label overlaps or crosses its container;
- notes explain the page's question, method or evidence, and supported takeaway; transitions or decisions appear where useful, with material qualifications at the relevant point;
- slides, notes, screenshots, and source manifests agree on numbers, analysis units, terminology, evidence identity, and software version; removed or replaced claims, visuals, terms, and versions do not survive in any of them;
- parameter wording agrees with its recorded provenance and comparison scope; a current numerical example is not presented as a transferable constant;
- each Progress workstream has the correct evidence profile; hybrid claims preserve both stage-level chains, while experimental claims keep units and `n`, performed execution, run validity, and repetition/corroboration distinct;
- changes to scope are reflected in the current design and all dependent pages;
- no generic summary or next-step page appears only for symmetry. End with completed outputs, critical synthesis, or an evidence-gated decision appropriate to the routed workflow.

Keep the delivery directory limited to the canonical deliverables requested by the user. Preserve designated baselines, original sources, and reconstructable assets. Move superseded exports out of the delivery directory; when the user explicitly requests deletion, remove those generated versions after verifying the final deliverable and the exact target paths. Do not regenerate historical PPT copies during cleanup. Deliver only the requested formats.
