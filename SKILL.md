---
name: project-preaching-deck-orchestration
description: Project understanding, persuasion design, and Slidev-ready deck orchestration for launches, reviews, demos, internal pitches, and stakeholder presentations. Use when Codex needs to turn raw project materials into a credible presentation storyline with claim/evidence/reasoning, narrative comparison, deck blueprint, and speaker notes instead of generic PPT copy.
---

# Project Preaching & Deck Orchestration

Convert raw project materials into a persuasive, evidence-aware presentation flow. Optimize for credibility, clarity, and Slidev-ready structure rather than generic marketing copy.

## Operate the workflow

1. Start with project understanding before writing slides, deck structure, or scripts.
2. Work through the stages in order:
   - Stage A: Project Understanding Brief
   - Stage B: Argumentation Map
   - Stage C: Narrative Comparison
   - Stage D: Deck Blueprint
   - Stage E: Page-by-Page Talk Script
3. Stay in the earliest incomplete stage. If the user asks to jump ahead, explain what is missing and deliver the required earlier stage first.
4. Default to one stage per response during collaborative work. Only continue through multiple stages in one response when the user explicitly asks for an end-to-end pass and the available material is sufficient.
5. When the user asks for the full workflow in one pass, keep the stage order intact in the response rather than collapsing everything into free-form prose.
6. Use the exact output structures in [references/output-contracts.md](references/output-contracts.md), including the stage heading and field order.

## Model the project before persuading

- Extract the project definition, problem, goals, users or stakeholders, differentiated value, strongest proof, weakest proof, and likely objections.
- Separate observed facts from reasonable inference.
- Infer the likely audience when possible, but state the assumption when audience cues are weak.
- Convert feature lists into a persuasion chain: problem, gap, approach, proof, value, and why now.
- Surface missing information before using a point in a persuasive claim.

## Build persuasion deliberately

- Use the claim/evidence/reasoning discipline in [references/narrative-patterns.md](references/narrative-patterns.md).
- Compare at least three narrative options before recommending one.
- Grade support as direct evidence, indirect evidence, assumption, or missing information.
- Prefer defensible wording over impressive wording. Replace unsupported claims like "industry-leading", "best", or "significant" with evidence-calibrated alternatives.
- Explain why each piece of evidence supports a claim and where that reasoning might be challenged.

## Produce Slidev-ready outputs

- Keep each slide focused on one idea.
- Optimize for markdown-based slides, not dense document pages.
- Make the deck blueprint easy to translate into Slidev with a clear title, key message, suggested content, speaker intent, and transition per slide.
- Make speaker notes sound like natural delivery, not a verbatim reading of the slide.
- Keep the blueprint and script aligned so every page has a clear job in the overall story.

## Respond with discipline

- Keep outputs structured. Use the stage-specific section headings from the references instead of free-form prose.
- If evidence is weak, say so plainly and suggest what data, comparison, case, or demo would make the story stronger.
- When the user adds new project context, update the current model before revising later-stage deliverables.
- Avoid unsupported superlatives, absolute certainty, or inflated business claims.
