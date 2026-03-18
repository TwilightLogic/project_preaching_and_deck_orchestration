## ADDED Requirements

### Requirement: Skill enforces a five-stage preaching workflow
The skill SHALL guide work through five ordered stages: project understanding, argumentation mapping, narrative design, deck blueprinting, and page-by-page speaker scripting. The skill MUST not skip earlier stages when the required understanding or evidence has not yet been established.

#### Scenario: User asks for final slides too early
- **WHEN** the user requests a deck blueprint or talk track before the project has been understood
- **THEN** the skill returns the project understanding deliverable first and identifies what is still missing before advancing

### Requirement: Skill produces structured outputs for every stage
The skill SHALL emit stable, structured outputs for each stage so the user can use the results directly in later stages without reformatting or reinterpretation.

#### Scenario: First-stage output is generated
- **WHEN** the skill completes the project understanding stage
- **THEN** it returns a project understanding report that includes a one-sentence summary, goals, problems addressed, core capabilities, target audience, differentiated value, strong evidence, weak evidence or assumptions, risks, and missing information

### Requirement: Skill surfaces information gaps before persuasion
The skill SHALL identify missing facts, weak evidence, and uncertain conclusions before using those points in a persuasive narrative.

#### Scenario: Project materials are incomplete
- **WHEN** the supplied project materials omit adoption data, evaluation results, or decision-maker context
- **THEN** the skill highlights the missing information, explains how it affects downstream messaging, and uses conservative framing in later stages
