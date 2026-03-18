## ADDED Requirements

### Requirement: Skill package includes valid Codex metadata
The repository SHALL expose the skill through a valid `SKILL.md` with required frontmatter and an `agents/openai.yaml` file whose interface values accurately describe the skill's purpose and trigger conditions.

#### Scenario: Skill package is prepared for listing
- **WHEN** the package is reviewed for Codex skill distribution
- **THEN** the repository contains a valid skill name, an accurate trigger description, and aligned UI metadata for the packaged skill

### Requirement: Skill package keeps core instructions concise
The repository SHALL keep the primary `SKILL.md` focused on workflow and invocation guidance, and SHALL move detailed output contracts or pattern libraries into linked `references/` files when that detail would otherwise bloat the main skill body.

#### Scenario: Detailed guidance exceeds the main skill body
- **WHEN** output schemas, narrative patterns, or audience heuristics require more space than is appropriate for the core skill instructions
- **THEN** those details are placed in one-level-deep `references/` files that are linked from `SKILL.md`

### Requirement: Skill package supports validation before release
The repository SHALL support running the standard skill validation workflow before the skill is published or shared.

#### Scenario: Maintainer validates the finished package
- **WHEN** the skill package is ready for release
- **THEN** a maintainer can run the standard validation script against the package and confirm the required files and metadata are present
