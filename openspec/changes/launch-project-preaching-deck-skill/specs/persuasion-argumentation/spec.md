## ADDED Requirements

### Requirement: Skill maps claims, evidence, and reasoning explicitly
The skill SHALL produce an argumentation map with 3 to 7 core claims, and each claim MUST include linked evidence, reasoning, evidence strength, potential objections, and recommended wording.

#### Scenario: Argument map is requested after project understanding
- **WHEN** the user proceeds from project understanding into persuasive structuring
- **THEN** the skill returns a claim-by-claim map that separates the claim itself from the supporting evidence and the reasoning that connects them

### Requirement: Skill compares multiple narrative options
The skill SHALL compare at least three presentation narratives and recommend one based on the audience, available proof, and the project's strongest differentiated advantage.

#### Scenario: Narrative options are evaluated
- **WHEN** the skill reaches the narrative design stage
- **THEN** it presents multiple narrative structures, explains the fit and risk of each one, and recommends the most persuasive option for the likely audience

### Requirement: Skill calibrates language to evidence quality
The skill SHALL distinguish direct evidence, indirect evidence, and assumptions, and it MUST avoid unsupported superlatives or certainty claims.

#### Scenario: A strong claim lacks proof
- **WHEN** the project materials do not support words such as "industry-leading", "best", or "significantly improved"
- **THEN** the skill marks the point as weakly supported or assumed and rewrites it using more defensible language
