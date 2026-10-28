# Validation

## Purpose

The comparison tested observable planning behavior rather than whether the proposed `SKILL.md` looked cleaner. Both versions stopped immediately before `ppt-master`; the downstream visual pipeline was unchanged and therefore excluded from the causal comparison.

## Test Set

Four realistic scientific presentation tasks were used:

1. **Progress Update** — four independent research/software workstreams.
2. **Journal Club** — a complex multi-Figure mechanism paper.
3. **Idea Discussion** — a new direction with authoritative scope, storyboard, and asset guidance.
4. **Mixed Deck** — Progress and Idea sections in one visually unified lab-meeting deck.

The v1 and v2 runners received the same source boundaries and were isolated from each other, the rubric, existing finished decks, and prior outputs. A separate evaluator received only anonymized A/B artifacts and the scoring rubric.

## First A/B Evaluation

| Task | v1 | v2 | Observed difference |
|---|---:|---:|---|
| Progress Update | 19 | 20 | v2 separated user workflow evidence from software release maturity. |
| Journal Club | 20 | 19 | v2 initially compressed readout qualification and mechanistic proximity from one Figure into one slide. |
| Idea Discussion | 18 | 20 | v2 made evidence status, success/failure criteria, and claim-level falsifiers explicit. |
| Mixed Deck | 19 | 20 | v2 produced a more executable section-routed production contract. |
| **Total** | **76** | **79** | **v2 passed the upgrade threshold without new severe claim risks.** |

## Targeted Journal Recheck

One narrow rule was added: when a source Figure supports sequential claims at different evidence levels, the claims should be split across slides when necessary rather than merged because they share a Figure number.

The Journal task was regenerated and evaluated anonymously:

- baseline output: `18/20`;
- patched v2 output: `20/20`.

The recheck also led to two general safeguards:

- preserve the source's exact statistic name, denominator/subset, threshold, analysis unit, and locator;
- treat archetype maps as planning worksheets and `scientific_handoff.md` as the single canonical production contract.

## Release Decision

The v2 skill was accepted because:

- Progress did not regress;
- Idea and Mixed showed substantive improvements;
- no new severe scientific-claim risk was found;
- the only Journal weakness was corrected and re-tested;
- the final skill passed structural validation and contains no project-specific scientific example.

## Post-v2 Additions (historical; unvalidated by A/B)

After the v2 release above, two features were added and have not yet gone through the same A/B evaluation:

- **Journal Club Deep-read mode** — `understanding_map.md` derived from a ChatGPT dialogue/notes file, with a paper/dialogue source hierarchy.
- **Idea Discussion interactive planning-only gate** — evidence-first interview, `USER_REVIEW` hard stop, and Design Freeze approval before production.

These additions carried no new validation score. The later iterative Idea maintenance update below replaces the approval hard stop with authorization-aware discussion and revision.

## Targeted Progress Maintenance Audit

The later Progress refinement was intentionally narrower than a new major version and was not assigned a new A/B score. It was reviewed against four generic failure classes:

| Scenario class | Required invariant |
|---|---|
| A workstream starts from a preset scientific or operational premise | The premise and authoritative source order are frozen before result or figure selection. |
| An internal discovery is tested in one or more external datasets | Candidate definition and dataset roles remain fixed; primary-unit evidence is not promoted to independent-unit validation. |
| A software workstream changes release or interface version | Repository reference, release maturity, screenshot provenance, data identity, notes, and manifest remain on one release snapshot. |
| Visible content is deleted or replaced late in production | Notes are checked in both directions and cannot retain page-specific descriptions of removed content. |

The update passed the skill structural validator, Markdown-reference check, diff whitespace check, and a project-specific-term sweep. It adds no domain-specific project name, result, dataset, software version, fixed page count, or locked layout. A new independent A/B score should be reserved for a future full four-archetype validation cycle rather than inferred from this maintenance audit.

## Targeted Idea And Export Maintenance Audit

The later Idea/QA refinement was also treated as a narrow maintenance update and was not assigned a new A/B score. It was reviewed against these generic failure classes:

| Scenario class | Required invariant |
|---|---|
| A costly modality or complex model is proposed | The strongest credible simpler alternative is explicit, and failure to outperform it limits the necessity claim. |
| A named method appears before the scientific data object is understood | The audience first learns the data object, information lost by a simpler summary, required representation, candidate methods, and selection criteria. |
| Generalization or transfer is claimed | The held-out unit, grouping rule, allowed calibration, and claim boundary are defined. |
| An indirect readout may be confounded | An independent cross-check is included when it changes the scientific decision. |
| Source rendering and final export differ | Final sign-off uses pages rendered from the delivered PPTX or PDF and rechecks formula typography and layout. |

The maintenance patch passed the skill structural validator, Markdown-reference check, diff whitespace check, and a project-specific-term sweep. It added no new planning artifact, did not enlarge the 13-item Design Freeze, and made conditional checks explicit rather than mandatory on every slide.

## Targeted Progress Method-Evidence And Teaching Audit

The later Progress refinement was derived from a method-heavy scientific progress deck that required multiple rounds of source, terminology, formula, notes, and layout correction. Project-specific details were not copied into the skill. The update instead preserves these generic failure classes:

| Scenario class | Required invariant |
|---|---|
| A method exists in source but may not have run | Implementation, recorded execution, and result evidence are separate; only their intersection supports a completed-process claim. |
| Several threshold values are shown on one frozen axis | A fixed-axis slice is not called a full pipeline sensitivity test. |
| A local recall or deletion check is available | Local diagnostics, perturbation stability, refitting, and end-to-end reruns keep distinct labels. |
| A reusable method produces one dataset-specific number | The transferable rule, re-estimated quantity, and current numerical instance are taught separately. |
| A complex method is compressed to fit a nominal page budget | Conceptual dependencies determine slide count; one missing prerequisite is not traded for brevity. |
| An old deck is visually useful but scientifically stale | Style/teaching references are separated from current claim-bearing evidence. |
| A group, fold, axis, statistic, or formula is non-intuitive | Construction, analysis unit, symbols, axes, and reading direction are defined before the conclusion. |
| A final source render looks correct | The delivered PPTX/PDF is re-rendered and checked for overflow, stale notes, and missing mathematical glyphs. |

This maintenance update introduces no new mandatory planning artifact. The execution and parameter ledgers remain conditional sections of `progress_map.md`, and their relevant fields flow into the existing canonical `scientific_handoff.md`. The patch passed the structural validator, Markdown-reference check, diff whitespace check, project-specific-term sweep, and a targeted invariant check for execution evidence, parameter scope, method expansion, transfer wording, typography, and delivery hygiene. It should receive a new independent A/B score only in a future full validation cycle rather than inheriting a score from the motivating deck.

## Targeted Progress Evidence-Profile And Wet-Lab Audit

The Progress router was extended to infer `computational`, `experimental`, `hybrid`, or `general` from claim dependency. The experimental branch was grounded in cross-cutting requirements from the [Nature Portfolio life-sciences reporting summary](https://www.nature.com/documents/nr-reporting-summary-flat.pdf), [NIH rigor and reproducibility guidance](https://www.grants.nih.gov/policy-and-compliance/policy-topics/reproducibility), [NIH key-resource authentication guidance](https://grants.nih.gov/grants/guide/notice-files/NOT-OD-17-068.html), [ARRIVE 2.0](https://arriveguidelines.org/arrive-guidelines), and [MIQE 2.0](https://doi.org/10.1093/clinchem/hvaf043). Modality-specific requirements were reduced to conditional prompts rather than copied into a universal checklist.

Before the final workflow edits, 10 synthetic cases and 10 failure mutations were fixed in [validation/progress-evidence-profile-cases.md](validation/progress-evidence-profile-cases.md). Same-agent forward application then produced the expected route and claim boundary for all 10 cases and rejected all 10 mutations, including pseudoreplication, cage-level assignment hidden by animal counts, representative-image overclaim, technical qPCR repeats, batch/treatment confounding, one-run optimization overclaim, computational code-without-run evidence, and one-sided auditing of a hybrid claim.

A post-hoc false-positive challenge also confirmed that routine instrument acquisition, export, and standard plotting do not automatically turn a simple wet-lab workstream into `hybrid`; a claim-bearing computational decision is required.

This result establishes rule coverage and internal coherence, not real-world effectiveness or independent generalization. No new mandatory planning artifact was added: the router uses two dependency questions, the computational and experimental references load conditionally, and both feed the existing `progress_map.md` and `scientific_handoff.md`. The first real wet-lab deck should be treated as a held-out validation and may justify a narrow follow-up correction.

## Iterative Idea Discussion Maintenance — 2026-10-09

This update distilled general lessons from an exploratory scientific deck and its execution-focused derivative. Those decks were produced without invoking this skill; they supplied examples for improvement, not a test of skill effectiveness. No project-specific scientific content or private artifacts were added to the repository.

The update preserves source verification, simpler alternatives, novelty beyond replication, and explicit validation. It replaces the one-way approval gate with a current design that can be revised within the user's authorization, makes reference style and existing production sources reusable, and removes mandatory defensive narration. Specialized validation guidance is loaded only when relevant.

[Ten generic scenarios](validation/idea-iteration-cases.md) received a same-agent desk review of routing and design decisions. The record includes the decisions reached; it is not an independent forward test or a rendered-deck evaluation. Structural validation, relative Markdown links, metadata, and Git whitespace checks also passed. Existing Progress evidence references and its workflow remain unchanged.

## Progress Method-Comparison Maintenance — 2026-10-10

Historical candidate: commit `7afc1c9`, subsequently narrowed by the convergence update below. Its independent application results describe that candidate.

This update distilled reusable lessons from a method-comparison Progress deck: audience prerequisites, an actual requested baseline, worked arithmetic connected to scientific objects, purposeful schematics, substantive notes, measured cost scopes, and whole-output agreement. The motivating deck informed the changes; it is not treated as a test of the revised skill. No project data, scientific result, fixed page count, dataset count, or repeat count was added to the production instructions.

The historical [method-comparison reference](https://github.com/ReoNa0216/reona-ppt-skill/blob/7afc1c9e24a0214dd2236da9c7c70cf68fde54c6/references/progress-method-comparison.md) served this workstream without enlarging ordinary experimental or status updates. Existing maps and the production source carried question coverage and audience preparation; no new mandatory planning file was introduced. This patch also changed shared wording about explanatory pages and notes; those shared edits are restored to the preceding version by the convergence update.

An independent agent applied the candidate to [three synthetic requests](validation/progress-method-comparison-cases.md): a full method comparison, a focused performance revision, and a simple wet-lab update. The main agent reviewed the resulting artifacts against eight criteria. All eight passed, including actual-baseline identity, valid boundary/count teaching, supplied repeat counts, retained memory tradeoff, phase-attribution limits, all-eligible-pair and annotated-subset scope, local revision, and experimental independence. The case record preserves sources, decisions, the synthetic-source correction, and a teaching-note excerpt.

This was a planning-only forward application, not an independent A/B score or a rendered-deck test. Structural validation, relative Markdown references, Git whitespace, and a project-specific-term sweep also passed. Journal Club and Idea workflows were unchanged; the existing reference-style and revision rules remain in force.

## Progress Teaching Convergence — 2026-10-10

Historical candidate: commit `0f5c69d`. The consistency update below subsequently revises its shared-contract wording and planning requirements.

The final guidance is confined to the Progress workflow and one conditional [method-teaching reference](references/progress-method-teaching.md). It retains four reusable principles: match the audience's starting knowledge, connect scientific objects to a complete small example, give schematics and notes complementary teaching jobs, and match comparisons and attribution to evidence. The reference applies to explanation-only work as well as method changes.

Implementation-category taxonomies, particular interval arithmetic, and prescribed output or annotation plot inventories were removed from production guidance. Performance checks remain conditional on a performance claim. The shared skill entrypoint, scientific content contract, speaker-notes protocol, and computational evidence reference were restored byte-for-byte to `0007ef6`, removing overlapping additions. Existing reference-style and revision guidance, Journal Club, Idea Discussion, and UI metadata retain that preceding version. No extra planning artifact or default benchmark is introduced.

Two additional synthetic requests received a [same-agent transfer desk application](validation/progress-method-comparison-cases.md#converged-guidance-transfer-desk-application): explaining classification readouts without an earlier method, and comparing physical staining procedures with multiple changed factors and day alignment. The record includes a complete calculation note and the resulting routing, figure, and attribution decisions. These applications support internal coherence across different requests; they provide no independent effectiveness or rendering score. The earlier cases A/B closely resemble the motivating method comparison, so their results are retained as narrow historical evidence.

The converged files passed the skill structural validator, relative Markdown-link check, and Git whitespace check. A file-content scope check against `0007ef6` confirmed that all runtime differences are limited to `workflows/progress-update.md` and its new method-teaching reference; other changes document the skill and its validation. The Linux installation is synchronized from the pushed repository after these checks.

## Progress Contract Consistency — 2026-10-10

A read-only audit of `0f5c69d` found conflicting guidance on note-only intermediate values and official versus reported software versions, a parameter-category gap for unexecuted implementations, and ambiguity between analysis objects and independent-repeat units. It also identified repeated per-page fields and wording that fit completed-result reports more naturally than blocked investigations.

This update repairs those seams in the shared entrypoint, handoff, and notes protocol while simplifying the Progress workflow and computational reference. Pages inherit common workstream facts and supply only relevant local context. Parameter provenance and actual comparison scope replace the closed category list; implementation, execution, and result remain distinct. Method explanations still require a complete valid example and useful notes. Software evidence follows the reported snapshot, including development versions. Supported failed or unfinished work can supply the central progress. The handoff maps accepted decisions and existing authorization to production prerequisites.

A fresh agent applied the candidate to [four fixed synthetic requests](validation/progress-method-comparison-cases.md#consistency-regression-application) without the audit findings, intended fixes, or previous validation records. Its plans preserved note-only calculation detail, implementation-only status, failed-QC interpretation, development-version evidence, and cell-level versus donor-level scope. The main agent reviewed the actual outputs; no planning conflict was found in those cases. The record preserves the source packet and observed decisions. This is planning validation, with no new A/B score, generated PPT, visual-quality claim, or exercised downstream production gate.

Structural validation, local Markdown links, Git whitespace, and a runtime consistency review passed. Journal Club and Idea workflows, their dedicated references, wet-lab evidence guidance, and UI metadata were unchanged. Changes to shared files resolve the identified interfaces; this update adds no planning artifact or default experiment. A future rendered-deck test should newly generate a small set of pages from fixed inputs using the revised skill, then inspect the exported pages and notes; an existing finished deck can supply a style reference or verified material, but does not test the revised production behavior by itself.

## Idea Literature And Narrative — 2026-10-28

This update adds conditional full-paper selection and argument guidance, authentic literature captures, usable page-and-notes drafts, and research context in Idea notes. Shared files own screenshot and note requirements; the Idea workflow owns review sequencing. Existing authorization, focused revision, formal-design preservation, and other archetypes remain in scope.

[Eight same-agent planning applications and a fresh three-page export](validation/idea-iteration-cases.md#literature-and-narrative-applications--2026-10-28) checked evidence roles, missing sources, readout scope, unlike prediction tasks, approval, and mode boundaries. The new pages were inspected in source renders and actual Microsoft PowerPoint renders; their final notes and seven embedded images matched the source, with no text overflow. These are planning and rendering checks, with no independent A/B score or new literature-discovery evaluation.

The final audit checks metadata, local links and anchors, whitespace, and cross-file rule ownership. Journal Club, Progress and its three dedicated references, and UI metadata retain their preceding content. The main Idea workflow is shorter; detailed literature guidance loads only when needed. No project-specific scientific content or private source assets enter the runtime instructions.
