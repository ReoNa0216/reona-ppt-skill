# ReoNa PPT Skill

A Codex skill for PI-facing scientific presentations in a fixed Tsinghua-purple visual system. It plans the scientific narrative, evidence boundaries, assets, and speaker-note jobs before handing visual production to `ppt-master`.

## What It Adds

- Section-level routing for **Progress Update**, **Journal Club**, **Idea Discussion**, and mixed lab-meeting decks.
- A mandatory Scientific Planning Gate before visual production.
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

- `workflows/progress-update.md`: independent workstreams, strongest evidence, completion status, and software user flows.
- `workflows/journal-club.md`: paper map, Figure evidence chain, teaching logic, and conclusion boundaries.
- `workflows/idea-discussion.md`: scope freeze, evidence status, falsification, phase gates, and model/formula roles.

A mixed deck routes sections independently while sharing one visual identity and one canonical `scientific_handoff.md`.

## Requirements

- Codex skill support.
- An available `ppt-master` skill for visual production and export.
- Microsoft YaHei, Arial, Georgia, and Consolas are the preferred fonts for the fixed visual system.

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

The v2 workflow was forward-tested against v1 on four realistic planning tasks: Progress Update, Journal Club, Idea Discussion, and Mixed Deck. Independent A/B evaluation scored v1 at `76/80` and v2 at `79/80`; a targeted Journal Club fix then scored `20/20` in re-evaluation. See [VALIDATION.md](VALIDATION.md).

## Scope

This is a scientific planning, narrative, fixed-style, and QA layer. It is not a general-purpose presentation framework, a promotional pitch-deck template, or a replacement for `ppt-master`.

## License

No license has been selected yet.

