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
