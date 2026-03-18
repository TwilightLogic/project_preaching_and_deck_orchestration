# Project Preaching & Deck Orchestration

A Codex skill for turning raw project materials into a credible, evidence-aware, Slidev-ready presentation package.

This repository packages a reusable workflow for:
- understanding a project before writing slides
- separating claims, evidence, and reasoning
- comparing multiple narrative options
- producing a deck blueprint
- writing page-by-page speaker notes
- rescuing weak or incomplete materials with cautious, defensible framing

## What This Skill Is For

Use this skill when you need more than generic slide copy.

It is designed for cases such as:
- product launches
- internal reviews
- demos
- stakeholder presentations
- project pitches that need both structure and persuasion

The skill is especially useful when teams tend to jump straight into slides and end up with feature lists instead of a convincing story.

## Why It Is Different

This skill does not treat presentation work as a slide-writing task.

It first models the project, then builds a persuasion chain, then chooses the narrative, and only then moves into deck structure and speaking notes. That makes it more useful when the source material is messy, incomplete, or stronger in logic than in polished proof.

## Core Workflow

The skill enforces a five-stage flow:

1. Project Understanding Brief
2. Argumentation Map
3. Narrative Comparison
4. Deck Blueprint
5. Page-by-Page Talk Script

By default, it works one stage at a time during collaborative use. If you explicitly ask for an end-to-end run, it keeps the full stage order intact instead of collapsing everything into free-form output.

## Output Style

This skill is built to be:
- evidence-aware rather than hype-driven
- structured rather than ad hoc
- Slidev-friendly rather than office-slide heavy
- persuasive without making unsupported claims
- useful even when the materials are still early or uneven

It distinguishes between direct evidence, indirect evidence, assumptions, and missing information, and it prefers cautious wording when proof is limited.

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── output-contracts.md
│   └── narrative-patterns.md
└── openspec/
    └── changes/
        └── launch-project-preaching-deck-skill/
```

## Key Files

- `SKILL.md`: Core skill contract, trigger description, and workflow rules
- `agents/openai.yaml`: UI-facing metadata for the skill
- `references/output-contracts.md`: Required output structure for each stage
- `references/narrative-patterns.md`: Audience lenses, narrative options, and wording guidance
- `openspec/changes/launch-project-preaching-deck-skill/`: OpenSpec proposal, design, specs, and implementation tasks

## Local Use

If you want to use the skill locally in Codex, install this repository as a skill package under your local skills directory.

Example local install target:

```bash
~/.codex/skills/project-preaching-deck-orchestration/
```

Once installed, invoke it explicitly in a prompt:

```text
Use $project-preaching-deck-orchestration to turn these project materials into a staged project brief, argument map, Slidev deck blueprint, and speaker notes.
```

## Validation

This repository was validated with the standard skill validator:

```bash
python3 /Users/zibin/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
```

## Publishing Notes

The skill package is ready for local Codex use.

Publishing through the ChatGPT Skills UI depends on account and workspace availability. At the time this repository was prepared, local installation works independently of whether the ChatGPT Skills publishing surface is available for your account.

## Development Notes

This repository uses OpenSpec to track the packaging work:

```bash
openspec status --change "launch-project-preaching-deck-skill"
```

If you want to evolve the skill further, create a new OpenSpec change rather than editing the completed change history in place.
