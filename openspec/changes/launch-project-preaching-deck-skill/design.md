## Context

This repository currently contains a single root [`SKILL.md`](/Users/zibin/Downloads/Project%20Preaching%20%26%20Deck%20Orchestration/SKILL.md) with rich prompt content, but it is not yet packaged as a reusable Codex skill. It lacks required frontmatter, market-facing UI metadata, a concise loading strategy, and a validation path. The target behavior is a publishable skill package that preserves the existing five-phase preaching workflow while making the output contract explicit and reusable.

The skill-creator guidance adds important constraints: keep `SKILL.md` concise, avoid auxiliary README-style docs, use `agents/openai.yaml` for UI metadata, and move detailed guidance into `references/` only when it materially reduces prompt bloat.

## Goals / Non-Goals

**Goals:**
- Turn the repository root into a valid Codex skill package without introducing unnecessary nesting.
- Preserve the current five-stage preaching workflow while making stage transitions and output structure explicit.
- Externalize detailed output schemas and narrative heuristics into minimal `references/` files only where that helps keep `SKILL.md` lean.
- Add a repeatable validation path so the skill can be checked before publication or sharing.

**Non-Goals:**
- Build a slide renderer, Slidev theme, or automated deck generator.
- Add external tools, MCP dependencies, or data integrations for project ingestion.
- Promise unsupported claims such as market leadership, performance gains, or ROI benchmarks without project-specific evidence.
- Create auxiliary user documentation that duplicates what should live in `SKILL.md` or `references/`.

## Decisions

### 1. Treat the repository root as the packaged skill
We will keep the skill package at the repository root instead of introducing an additional nested skill folder.

Why:
- The repository already centers on a single skill concept and already contains a root `SKILL.md`.
- This minimizes restructuring and keeps publication simple.

Alternatives considered:
- Create a nested skill directory and leave the current root file untouched. Rejected because it adds indirection without solving a real packaging problem.

### 2. Split the skill into a concise core instruction file plus targeted references
We will rewrite `SKILL.md` into market-compatible frontmatter plus concise operational guidance, and move verbose schemas into a small set of linked `references/` files.

Why:
- The current prompt is long and mixes workflow rules, output schemas, and rhetorical constraints into one file.
- A lean main skill improves trigger quality and keeps context overhead manageable.

Alternatives considered:
- Keep all instructions in `SKILL.md`. Rejected because it increases context cost and makes future edits harder to reason about.

### 3. Encode the workflow as a deterministic five-stage contract
The core skill will explicitly require the sequence: project understanding, argumentation map, narrative comparison, deck blueprint, and page-by-page script. Each stage will define required headings and stage-specific output expectations.

Why:
- The main value of this skill is not generic writing quality; it is the disciplined movement from understanding to persuasion to deck output.
- Explicit stage contracts make the skill easier to test and improve.

Alternatives considered:
- Allow one-shot free-form execution. Rejected because it weakens the main differentiator and makes output quality more inconsistent.

### 4. Use standard skill metadata and validation tooling
We will add `agents/openai.yaml` aligned with the rewritten `SKILL.md`, generate or refresh it with the standard helper script, and validate the finished package with the standard quick validation workflow.

Why:
- Market packaging needs machine-readable metadata in addition to the skill body.
- Reusing the standard generator and validator reduces format drift.

Alternatives considered:
- Hand-author metadata and skip validation. Rejected because it is more error-prone and harder to maintain.

### 5. Keep the first release text-first and evidence-aware
The initial release will focus on text instructions, structured outputs, and cautious rhetorical rules rather than scripts or rich assets.

Why:
- The current problem is primarily workflow packaging and persuasion structure, not deterministic file transformation.
- We do not yet have stable brand assets, canonical examples, or code-heavy operations that justify additional bundled resources.

Alternatives considered:
- Add example-heavy assets or automation scripts immediately. Rejected for the first release because they would increase maintenance cost before the core behavior is validated.

## Risks / Trade-offs

- [Risk] The rewritten `SKILL.md` could become too compressed and lose useful nuance. → Mitigation: move only repeatable detail into `references/` and keep essential guardrails in the main file.
- [Risk] The skill may still over-claim if project materials are weak. → Mitigation: make evidence grading, missing-information reporting, and cautious wording explicit requirements.
- [Risk] The package may be valid structurally but weak in practical usage. → Mitigation: include compact reference material for output structure and narrative choices, then validate the package and iterate after real use.
- [Risk] Future maintainers may drift `agents/openai.yaml` away from the skill body. → Mitigation: regenerate metadata when the skill changes and include validation in the release flow.

## Migration Plan

1. Rewrite the root `SKILL.md` into market-compatible frontmatter plus concise workflow instructions.
2. Add `agents/openai.yaml` with generated interface metadata based on the rewritten skill.
3. Add only the minimal `references/` files needed to hold detailed output contracts and narrative patterns.
4. Run the standard validation workflow and fix any packaging issues before release.

Rollback strategy:
- Revert the packaging files added by this change and restore the previous standalone prompt-only `SKILL.md`.

## Open Questions

- Should the published skill be named after the workflow (`project-preaching-deck-orchestration`) or optimized for a shorter market-facing label?
- Do we want to infer audience type automatically by default, or require the user to specify it when the project context is ambiguous?
- Is a compact example reference helpful for first-release usability, or would it add more maintenance than value before the skill is exercised?
