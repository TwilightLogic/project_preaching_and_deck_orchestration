## Why

The repository already contains a strong prompt for project preaching and deck orchestration, but it is still a raw instruction block rather than a market-ready Codex skill. We need to turn it into a publishable skill package with a clear operating contract, phased workflow, and Slidev-oriented outputs so it can be reused reliably across projects and audiences.

## What Changes

- Package the existing "Project Preaching & Deck Orchestration" prompt as a Codex market skill with proper metadata, installable structure, and reusable support files.
- Formalize the skill into a five-phase workflow that must progress from project understanding to argument mapping, narrative selection, deck blueprinting, and speaker script generation.
- Define structured output contracts for each phase so the skill produces predictable deliverables instead of free-form copy.
- Add evidence-aware guardrails so the skill distinguishes strong evidence, weak evidence, assumptions, and risky claims before using persuasive language.
- Add Slidev-oriented deliverable requirements so the final output is ready to translate into markdown slides and speaker notes.
- Add skill-facing support resources so Codex can understand expected inputs, output structure, and safe usage without relying on ad hoc prose.

## Capabilities

### New Capabilities
- `project-preaching-workflow`: Orchestrate a mandatory five-stage workflow that starts with project understanding and ends with Slidev-ready deck and talk-track outputs.
- `persuasion-argumentation`: Build explicit claim/evidence/reasoning structures, audience-aware narratives, and cautious wording rules for unsupported assertions.
- `codex-market-skill-packaging`: Package the skill with market-facing metadata, `agents/openai.yaml`, and minimal reusable references/assets for Codex skill distribution.

### Modified Capabilities
- None.

## Impact

- Root skill definition in [`SKILL.md`](/Users/zibin/Downloads/Project%20Preaching%20%26%20Deck%20Orchestration/SKILL.md)
- New market-ready skill packaging files and any supporting references or assets needed for Codex distribution
- Skill-facing metadata and supporting references that describe intended audience, workflow, input expectations, and output format
- Future implementation and validation flow for this repository's Codex skill package
