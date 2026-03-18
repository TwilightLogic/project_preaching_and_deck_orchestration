## 1. Package the repository as a Codex skill

- [x] 1.1 Rewrite the root `SKILL.md` with valid frontmatter, a market-ready trigger description, and concise core workflow instructions
- [x] 1.2 Keep the repository root as the skill package and add the required `agents/` directory structure for UI metadata
- [x] 1.3 Create the minimal `references/` files needed to hold detailed output contracts and narrative guidance, and link them from `SKILL.md`

## 2. Encode the preaching workflow and output contract

- [x] 2.1 Define the mandatory five-stage workflow in `SKILL.md` so the skill cannot skip from intake directly to deck output
- [x] 2.2 Add structured output requirements for project understanding, argumentation map, narrative comparison, deck blueprint, and page-by-page script generation
- [x] 2.3 Add evidence-grading and cautious-language rules so unsupported claims are surfaced as weak evidence or assumptions

## 3. Add market-facing metadata

- [x] 3.1 Generate or refresh `agents/openai.yaml` so its display name, short description, and default prompt match the finished skill behavior
- [x] 3.2 Confirm the packaged skill does not introduce unnecessary auxiliary documentation outside `SKILL.md`, `agents/`, and purposeful support resources

## 4. Validate release readiness

- [x] 4.1 Run the standard skill validation workflow against the repository root package and fix any reported issues
- [x] 4.2 Smoke-test the packaged skill against a representative project-pitch request and tighten wording where the output contract is still ambiguous
