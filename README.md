# ReoNa PPT Skill

A Codex skill for PI-facing scientific presentations in a fixed Tsinghua-purple visual system. It plans the scientific narrative, evidence boundaries, assets, and speaker-note jobs before handing visual production to `ppt-master`.

## What It Adds

- Section-level routing for **Progress Update**, **Journal Club**, **Idea Discussion**, and mixed lab-meeting decks.
- A mandatory Scientific Planning Gate before visual production.
- Progress workstream truth locks for starting premise, source priority, strongest completed result, and displayed evidence.
- Automatic Progress routing by claim dependency: computational, experimental, hybrid, or general.
- Parallel evidence locks for computational execution/parameters and wet-lab design/execution/measurement, loaded only when relevant.
- Software release snapshots and bidirectional slide–notes–manifest consistency checks.
- Source-verified claims tied to displayed evidence, analysis units, boundaries, and evidence status.
- Separate handling of scientific evidence, software UI, explanatory schematics, and formulas.
- Archetype-aware speaker notes and ReoNa-specific final QA.

## Architecture

```text
authoritative sources
        ↓
section routing and archetype-specific planning
        ↓
scientific_handoff.md
        ↓
ppt-master visual planning and production
        ↓
SVG / PPTX / PDF / speaker notes
```

`reona-ppt-skill` owns scientific content architecture and the fixed ReoNa presentation constraints. `ppt-master` remains responsible for visual strategy, page generation, export, and generic technical QA.

## Workflows

- `workflows/progress-update.md`: workstream truth locks, automatic evidence-profile routing, audience-priority teaching depth, optional external-validation grammar, and software release-aware user flows.
  - `references/progress-computational-evidence.md`: execution, parameter-comparison scope, transfer, and computational teaching logic.
  - `references/progress-wet-lab-evidence.md`: units and `n`, controls, performed execution, measurement validity, evidence maturity, and experimental teaching logic.
- `workflows/journal-club.md`: paper map, Figure evidence chain, teaching logic, and conclusion boundaries; Deep-read mode adds an `understanding_map.md` from a ChatGPT dialogue/notes file.
- `workflows/idea-discussion.md`: interactive planning-only by default (evidence-first interview + Design Freeze approval), scope freeze, evidence status, falsification, phase gates, and model/formula roles.

A mixed deck routes sections independently while sharing one visual identity and one canonical `scientific_handoff.md`.

## Requirements

- Codex skill support.
- An available `ppt-master` skill for visual production and export.
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

The v2 workflow was forward-tested against v1 on four realistic planning tasks: Progress Update, Journal Club, Idea Discussion, and Mixed Deck. Independent A/B evaluation scored v1 at `76/80` and v2 at `79/80`; a targeted Journal Club fix then scored `20/20` in re-evaluation. Later refinements use clearly labeled maintenance or internal adversarial audits and do not inherit the independent A/B score. See [VALIDATION.md](VALIDATION.md).

## Scope

This is a scientific planning, narrative, fixed-style, and QA layer. It is not a general-purpose presentation framework, a promotional pitch-deck template, or a replacement for `ppt-master`.

## License

No license has been selected yet.
