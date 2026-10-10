# ReoNa PPT Skill

A Codex skill for developing, discussing, creating, and revising PI-facing scientific presentations. It connects scientific decisions, evidence, narrative, figures, and speaker notes, then verifies the exported deck. It inherits an accepted reference deck's style or uses Tsinghua-purple defaults.

## What It Adds

- Section-level routing for **Progress Update**, **Journal Club**, **Idea Discussion**, and mixed lab-meeting decks.
- A mandatory Scientific Planning Gate before visual production.
- Iterative Idea Discussion: compare designs, record accepted decisions, produce when authorized, and revise affected content from feedback.
- Different emphasis for exploratory and execution decks, with optional pilot and prediction design guidance.
- Progress workstream truth locks for starting premise, source priority, strongest completed result, and displayed evidence.
- Automatic Progress routing by claim dependency: computational, experimental, hybrid, or general.
- Parallel evidence locks for computational execution/parameters and wet-lab design/execution/measurement, loaded only when relevant.
- Conditional Progress method teaching: audience prerequisites, complete examples, complementary schematics and notes, and evidence-matched comparisons.
- Software release snapshots and bidirectional slide–notes–manifest consistency checks.
- Source-verified claims tied to displayed evidence, analysis units, boundaries, and evidence status.
- Separate handling of scientific evidence, software UI, explanatory schematics, and formulas.
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

- `workflows/progress-update.md`: workstream truth locks, automatic evidence-profile routing, audience-priority teaching depth, optional external-validation grammar, and software release-aware user flows.
  - `references/progress-computational-evidence.md`: execution, parameter-comparison scope, transfer, and computational teaching logic.
  - `references/progress-wet-lab-evidence.md`: units and `n`, controls, performed execution, measurement validity, evidence maturity, and experimental teaching logic.
  - `references/progress-method-teaching.md`: audience-level method explanation and comparison, with worked examples, purposeful visuals and notes, and evidence-scoped attribution.
- `workflows/journal-club.md`: paper map, Figure evidence chain, teaching logic, and conclusion boundaries; Deep-read mode adds an `understanding_map.md` from a ChatGPT dialogue/notes file.
- `workflows/idea-discussion.md`: evidence-first discussion, feasible alternatives, current design, authorized production, feedback-driven revision, and a decision-oriented ending.
  - `references/idea-validation-design.md`: conditional guidance for preliminary evidence, prediction tasks, appropriate metrics, and intervention tests.

A mixed deck routes sections independently while sharing one visual identity and one canonical content source. Existing structured slide sources can serve as that record.

## What Idea Discussion Does

It helps answer seven questions: why the problem matters, what evidence exists, what is feasible, what exactly to test, why the proposed approach is needed, how to evaluate it, and what decision follows. These are reasoning aids rather than a fixed set of slides.

A discussion-only request stays in discussion. A request to create or revise authorizes production within that scope. The current design carries accepted choices forward; new feedback reopens the affected decisions and updates their dependent slides, notes, and figures. A separate approval ritual is not required.

The workflow preserves scientific rigor through source verification, credible alternatives, novelty beyond reproducing known results, and tests that can change the conclusion. It keeps internal audit concerns separate from audience-facing explanation.

## Requirements

- Codex skill support.
- A working presentation production pipeline, or an available `ppt-master` skill.
- Microsoft YaHei, Arial, Georgia, and Consolas are the preferred text fonts; displayed and inline equations use Computer Modern or Latin Modern through math rendering.

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

The v2 workflow was forward-tested against v1 on four realistic planning tasks: Progress Update, Journal Club, Idea Discussion, and Mixed Deck. Independent A/B evaluation scored v1 at `76/80` and v2 at `79/80`; a targeted Journal Club fix then scored `20/20` in re-evaluation. Later refinements use clearly labeled maintenance audits or forward applications and do not inherit the independent A/B score. The current Progress teaching refinement narrows an earlier method-comparison patch; its scope and validation are recorded separately from that patch's synthetic forward application. See [VALIDATION.md](VALIDATION.md).

## Scope

This skill focuses on scientific planning, narrative, reference-aware style, and QA. It delegates rendering and export to the production pipeline.

## License

No license has been selected yet.
