# ReoNa PPT Skill

A Codex skill for developing, discussing, creating, and revising PI-facing scientific presentations. It connects scientific decisions, evidence, narrative, figures, and speaker notes, then verifies the exported deck. It inherits an accepted reference deck's style or uses Tsinghua-purple defaults.

## What It Adds

- Section-level routing for **Progress Update**, **Journal Club**, **Idea Discussion**, and mixed lab-meeting decks.
- A mandatory Scientific Planning Gate before visual production.
- Iterative Idea Discussion: build the argument from full-paper evidence, draft pages and notes for agreed review, then produce and revise within authorization.
- Different emphasis for exploratory and execution decks, with optional pilot and prediction design guidance.
- Progress workstream truth locks for starting premise, source priority, current supported progress, and displayed evidence.
- Automatic Progress routing by claim dependency: computational, experimental, hybrid, or general.
- Parallel evidence locks for computational execution/parameters and wet-lab design/execution/measurement, loaded only when relevant.
- Conditional Progress method teaching: audience prerequisites, complete examples, complementary schematics and notes, and evidence-matched comparisons.
- Reported software snapshots, including development versions, and bidirectional slide–notes–manifest consistency checks.
- Source-verified claims tied to displayed evidence, analysis units, boundaries, and evidence status.
- Authentic article-title, figure, and passage captures, distinct from explanatory schematics, software UI, and formulas.
- Archetype-aware speaker notes and ReoNa-specific final QA.
- Direct explanatory writing, reference-deck preservation, and one clear set of requested deliverables.

## Architecture

```text
authoritative sources
        ↓
section routing and archetype-specific planning
        ↓
canonical content source (scientific_handoff.md or existing equivalent)
        ↓
existing project pipeline or ppt-master production
        ↓
requested deliverable + export review → discussion and focused revision
```

`reona-ppt-skill` owns scientific content architecture and presentation requirements. The production pipeline handles visual strategy, page generation, and export. Reuse a working project pipeline; otherwise use `ppt-master`.

## Workflows

- `workflows/progress-update.md`: shared workstream facts inherited by pages, automatic evidence-profile routing, audience-priority teaching depth, optional external-validation grammar, and software version-aware user flows.
  - `references/progress-computational-evidence.md`: implementation/execution/result evidence, parameter provenance and actual comparison scope, transfer, and computational explanation.
  - `references/progress-wet-lab-evidence.md`: units and `n`, controls, performed execution, measurement validity, evidence maturity, and experimental teaching logic.
  - `references/progress-method-teaching.md`: audience-level method explanation and comparison, with worked examples, purposeful visuals and notes, and evidence-scoped attribution.
- `workflows/journal-club.md`: paper map, Figure evidence chain, teaching logic, and conclusion boundaries; Deep-read mode adds an `understanding_map.md` from a ChatGPT dialogue/notes file.
- `workflows/idea-discussion.md`: evidence-first discussion, feasible alternatives, current design, authorized production, feedback-driven revision, and a decision-oriented ending.
  - `references/idea-literature-narrative.md`: conditional guidance for full-paper selection, evidence roles, page relationships, and method comparisons.
  - `references/idea-validation-design.md`: conditional guidance for preliminary evidence, prediction tasks, appropriate metrics, and intervention tests.

A mixed deck routes sections independently while sharing one visual identity and one canonical content source. Existing structured slide sources can serve as that record.

## What Idea Discussion Does

It connects the problem's value, existing evidence, a specific unresolved question, feasible measurements and analysis, and decisive validation. Literature serves that argument; page relationships determine how studies are combined or expanded.

New or substantially restructured arguments receive a page-and-notes draft. The [task and review agreement](workflows/idea-discussion.md#task-and-review-agreement) governs whether it awaits review or proceeds within existing authorization. Accepted designs carry forward; focused revisions update only affected content and dependencies.

The workflow preserves scientific rigor through source verification, credible alternatives, novelty beyond reproducing known results, and tests that can change the conclusion. It keeps internal audit concerns separate from audience-facing explanation.

## Requirements

- Codex skill support.
- A working presentation production pipeline, or an available `ppt-master` skill.
- Typography follows the [shared visual system](SKILL.md#visual-system-and-reference-decks) or the user's accepted reference.

This repository does not vendor `ppt-master`.

## Installation

```bash
git clone https://github.com/ReoNa0216/reona-ppt-skill.git ~/.codex/skills/reona-ppt-skill
```

Invoke it explicitly when needed:

```text
Use $reona-ppt-skill to plan this mixed lab-meeting deck and complete the scientific planning gate before visual production.
```

## Validation

The v2 workflow received an independent four-task A/B evaluation. Later refinements have separately scoped planning, consistency, and export checks; they do not inherit its score. See [VALIDATION.md](VALIDATION.md) for tested versions, methods, and results.

## Scope

This skill focuses on scientific planning, narrative, reference-aware style, and QA. It delegates rendering and export to the production pipeline.

## License

No license has been selected yet.
