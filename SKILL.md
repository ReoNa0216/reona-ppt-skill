---
name: reona-ppt-skill
description: Create or revise PI-facing scientific PowerPoint decks in ReoNa's fixed Tsinghua-purple style. Use section-level routing for progress updates, journal clubs, idea discussions, or mixed lab-meeting decks; complete source-verified scientific planning before handing content to ppt-master for visual production.
---

# ReoNa PPT Skill

Use this skill as the scientific narrative, evidence, claim-boundary, and ReoNa-specific QA layer above `ppt-master`. `ppt-master` owns visual planning and production: design specification, SVG/PPTX/PDF generation, formula rendering, export, and generic technical QA.

## Scientific Planning Gate

Complete this gate before entering the `ppt-master` Strategist.

### 1. Route each scientific section

- **Progress Update** — recent work, completed analyses, software/tool progress, and project status. Read [workflows/progress-update.md](workflows/progress-update.md).
- **Journal Club** — a paper or small paper set whose evidence chain must be taught and critiqued. Read [workflows/journal-club.md](workflows/journal-club.md).
- **Idea Discussion** — a proposed scientific direction, model, experiment, or project requiring scope control and falsifiable design. Interactive planning-only by default: no approved Design Freeze, no PPT production. Read [workflows/idea-discussion.md](workflows/idea-discussion.md).

Route mixed decks section by section. Cover, agenda, transition, and closing pages inherit the routed scientific sections; they do not need their own archetype. Keep one visual system across all sections without forcing them into one narrative grammar. Deck-level production waits until every Idea section has an approved freeze.

### 2. Audit sources and freeze claims

- For research results, read the authoritative manuscript/report, methods, legends, and final figures before outlining. For Progress workstreams, also freeze the actual starting premise and source priority before selecting the strongest completed result. For software, inspect the current official repository and release documentation, not an older local copy.
- Build the planning artifact required by each routed workflow: `progress_map.md`, `journal_map.md` (plus `understanding_map.md` when the Journal Club runs in Deep-read mode), or `design_freeze_draft.md` → `design_freeze.md` plus `claim_evidence_map_draft.md` → `claim_evidence_map.md`.
- Freeze each consequential claim as `claim → source → displayed evidence → analysis unit → boundary → evidence status`.
- For computational Progress claims, distinguish `implemented in source → executed in the recorded work → supported by a result artifact`. A source-code path alone does not prove execution. Classify exact parameters by the comparison scope defined in the Progress workflow; do not relabel fixed-axis slices or local diagnostics as full sensitivity tests.
- Use audience-readable descriptions, never internal folder or module names. Introduce each dataset before its result: what was sampled, what comparison it supports, and what it cannot answer.
- Distinguish **established / source-supported / inference / proposal** in planning. Do not expose these audit labels on slides unless they help the audience.

### 3. Produce the scientific handoff

Read [references/scientific-content-contract.md](references/scientific-content-contract.md). Create one `scientific_handoff.md` containing the section routing, claim registry, page-level scientific storyboard, asset plan, note jobs, and do-not-claim list. Do not enter `ppt-master` until every scientific section has a defensible handoff.

## Shared Scientific Rules

- Give each slide one scientific job and one defensible conclusion. The title should communicate the question or conclusion, not merely name a dataset, file, module, or figure number.
- Put the analysis unit on the slide when it affects interpretation: cell, embryo, biopsy, patient, event, feature, replicate, software release, etc.
- Match every conclusion to the displayed evidence. Correlation is not causality; gene-level change is not pathway proof; an uncorrected trend is not a validated result.
- Do not force weakly annotated measurements into a biological identity to make a cleaner story. If a result is not integrated into the current workflow, show it as a standalone result and break the pipeline connection visually.
- Expand each abbreviation at first audience-facing use with a Chinese explanation or English full name. Use Arabic numerals for quantities in slides and notes.
- Prefer ordinary Chinese for the object, operation, and decision. Retain English only when it is a necessary software name, standard abbreviation, or clearer technical term after definition. Do not use a centered dot as a prose separator; use Chinese punctuation, line breaks, arrows, or aligned columns according to meaning.
- External research or model knowledge may expand context only when the user requests it; keep it distinguishable from source-derived claims.
- Never use AI-generated images as experimental evidence. Use them only for clearly explanatory schematics, workflows, conceptual mechanisms, or non-data illustrations.
- If a formula belongs in the main deck, pair it with one plain-language sentence stating its scientific role. Define every displayed symbol before or beside the formula. Render it as mathematics; never simulate subscripts or superscripts with ordinary body text. Put derivations, dense objectives, and long lexicographic rules in backup slides.

## Software Storytelling

- Lead with the user's task and the friction removed, then show one concrete review flow and how the work is saved or handed off. Do not lead with implementation facts, test counts, file-format lists, or internal module names.
- Use the current official release as the source of truth. Label demo data as demo data; never present an interface screenshot as an experimental result.
- A claim about linked views, event editing, state recovery, or another interaction must be visible in the screenshot or explicitly verified from current source/release contracts in the notes.

## Fixed Visual System

Keep this identity unless the user explicitly overrides it:

- Canvas: 16:9, `1280 × 720`.
- Palette: primary `#5B2C83`; dark purple `#321748`; secondary `#76529B`; pale purple `#F3F0F6`; text `#17131A`; secondary text `#655E6B`; border `#D8D2DC`. Green `#27856A` means completed/positive; red `#B84A62` means risk/failure.
- Chinese title/body: Microsoft YaHei. Latin body: Arial. Large metrics: Georgia. Displayed and inline equations: Cambria Math, Latin Modern Math, or Computer Modern through math rendering; choose the font that survives the target PPTX/PDF export. Technical identifiers only: Consolas.
- Size starting points: cover title `64`; slide title `34–36`; context line `18`; body `18`; annotation `13–14`; metric `30–42`; footer `11`. Defaults, not hard limits.
- Vertical starting points: section label near `y=49`; title near `y=91`; context line near `y=137`; main content from `y≈177`. `ppt-master`'s Strategist may adjust these for readability, but never to compress an overloaded page.
- Keep titles to one line when reasonable. Give title, context line, and main content visibly separate vertical space.
- Prefer white space, large evidence, simple dividers, and at most one pale information box. Avoid decorative card grids, repeated badges, and generic takeaway bars.
- Do not use a pale-purple field merely to fill an empty region. Every colored region must group content, encode state, or create a necessary hierarchy.

## Figure And Layout Guardrails

- Never place a badge, caption, or added label over a scientific figure or software screenshot. Put interpretation outside the image frame.
- Keep source figures and screenshots uncropped unless the user explicitly approves a crop. Do not duplicate a title already visible inside a source figure unless the external caption adds interpretation.
- Check every metric and annotation against its container. No text may cross a divider, card edge, figure frame, or page edge.
- Give non-intuitive charts readable axis labels and enough room to explain the statistic. Give complex equations dedicated width or split the explanation; never solve overflow by shrinking symbols until they are unreadable.
- Prefer fewer legible panels over a comprehensive but unreadable collage. Evidence must remain readable at presentation scale.

## Speaker Notes

Read [references/speaker-notes-protocol.md](references/speaker-notes-protocol.md). Notes must explain scientific reasoning that the slide cannot carry visually and must follow the routed archetype; they must not merely restate visible text.

## Handoff And Final Review

Give `ppt-master` the authoritative `scientific_handoff.md`, source manifest, and asset plan, then follow its production and export pipeline without duplicating it here. Hand the Fixed Visual System as brand constraints: palette and fonts via the `reona_tsinghua` Brand workspace, whitespace/guardrail preferences as a style brief, and the size/vertical numbers as soft starting points — never a locked layout template.

After generation, inspect the source render, then re-inspect every page rendered from the final PPTX or exported PDF at presentation scale. Sign off on the final exported artifact; a correct source render is not sufficient. Apply these ReoNa-specific checks:

- the shown panel or screenshot directly supports the stated claim;
- figure identity, sample counts, analysis units, abbreviations, and evidence status are correct;
- scientific figures are legible, schematics cannot be mistaken for data, formula meaning is explicit, and equation fonts, symbols, subscripts, superscripts, minus signs, and relation signs survive export without empty glyphs;
- no text, caption, or label overlaps or crosses its container;
- notes explain question, production/readout, result, boundary, and transition where relevant;
- slides, notes, screenshots, and source manifests agree on numbers, analysis units, terminology, evidence identity, and software version; removed or replaced claims, visuals, terms, and versions do not survive in any of them;
- parameter wording agrees with its recorded provenance and comparison scope; a current numerical example is not presented as a transferable constant;
- no section silently expands beyond its frozen scope;
- no generic summary or next-step page appears only for symmetry. End with completed outputs, critical synthesis, or an evidence-gated decision appropriate to the routed workflow.

Keep the delivery directory limited to the canonical deliverables requested by the user. Move superseded working exports to a designated backup or working area rather than leaving multiple equally plausible final versions.
