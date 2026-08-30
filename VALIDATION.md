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

## Post-v2 Additions (unvalidated)

After the v2 release above, two features were added and have not yet gone through the same A/B evaluation:

- **Journal Club Deep-read mode** — `understanding_map.md` derived from a ChatGPT dialogue/notes file, with a paper/dialogue source hierarchy.
- **Idea Discussion interactive planning-only gate** — evidence-first interview, `USER_REVIEW` hard stop, and Design Freeze approval before production.

These are documented in their workflows but carry no validation score yet.

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
