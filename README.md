# K5K3D

K5K3D is a writing skill for producing formal product judgment documents using the `5 Looks + 3 Decisions` framework.

It is designed for product direction analysis, opportunity assessment, scope narrowing, and go/no-go style decision documents. It is not meant for generic PRDs, simple market overviews, or feature list roundups.

## What It Does

This skill helps turn scattered research into a decision-oriented document with:

- a clear recommendation up front
- structured reasoning through `5 Looks`
- execution guidance through `3 Decisions`
- explicit handling of assumptions, evidence gaps, and next validation steps

It is suitable for two common workflows:

- starting from scratch and doing the minimum required research before writing
- taking existing research materials and converging them into a final judgment

## Best Use Cases

- Assess whether an AI capability should enter a product roadmap
- Evaluate a new product direction or opportunity area
- Narrow scope before MVP definition
- Convert research notes, VOC summaries, and competitor findings into an executable decision memo

## Not Suitable For

- generic PRDs
- requirement specifications
- broad industry reports
- pure competitor listings
- strategy writing without evidence

## Core Framework

### 5 Looks

- Look at the industry
- Look at the users
- Look at the competition
- Look at the opportunity
- Look at yourself

### 3 Decisions

- Decide control points
- Decide goals
- Decide strategy

## Output Characteristics

This skill enforces the following output behavior:

- formal written output, not conversational writing
- title format: `<topic>_Opportunity Insights`
- `Executive Summary` must come first
- the main body must follow `5 Looks` and `3 Decisions`
- the conclusion must be actionable
- at least one comparison table or judgment matrix must appear
- dividers must be inserted between heading levels for readability
- AI sections must describe capability boundaries, trigger logic, input/output, Agent-Skill split, and cost constraints
- assumptions, guesses, and evidence gaps must be moved to the appendix instead of being mixed into the main body

## User and Competition Requirements

### User Section Must Include

- VOC
- scenario chain
- benchmark standards
- a user journey table
- a matching Mermaid journey flow diagram

### Competition Section Must Include

- direct competitors
- substitutes and default alternatives
- comparison beyond feature count
- at least 2 UI screenshots for each core benchmark product

## Working Modes

### 1. Research-First Mode

Use this when the user only provides a topic or a direction.

Expected behavior:

- complete the minimum necessary research for industry, users, and competition
- then write the final judgment document

### 2. Material-Convergence Mode

Use this when the user already provides research materials, VOC summaries, or competitor analysis.

Expected behavior:

- separate usable evidence from uncertain or missing evidence
- converge the materials into a decision document

## Standard Document Structure

1. Executive Summary
2. 5 Looks
3. 3 Decisions
4. Conclusion and Next Steps
5. Appendix

See [references/output_template.md](./references/output_template.md) for the template structure.

## Evidence Rules

K5K3D is strict about evidence handling:

- prefer user-provided materials and first-hand evidence
- do not present suggested sample sizes as completed research
- do not present guesses as facts
- keep the main body limited to confirmed conclusions
- move assumptions, evidence gaps, and follow-up validation needs into the appendix

Detailed standards are documented in [references/research_standards.md](./references/research_standards.md).

## Writing Constraints

This skill explicitly avoids:

- chatty explanation style
- marketing language for AI
- weak conclusions such as "everything has value" or "we can keep observing"
- rhetorical contrast patterns such as:
  - "not A, but B"
  - "it does not depend on A, it depends on B"
  - "the real value is not A, but B"

## Repository Structure

```text
K5K3D/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── optional_models.md
    ├── output_template.md
    └── research_standards.md
```

## Reference Files

- [SKILL.md](./SKILL.md)
  Full skill definition, workflow, output contract, and required constraints.

- [references/output_template.md](./references/output_template.md)
  Canonical output template for the final document.

- [references/research_standards.md](./references/research_standards.md)
  Evidence policy, VOC requirements, competitor matrix rules, and opportunity filtering standards.

- [references/optional_models.md](./references/optional_models.md)
  Optional supporting models such as `PESTEL`, `Persona`, `CJM`, `SWOT`, and `VRIO`.

## Style of Output

K5K3D is optimized for documents that are:

- explicit in judgment
- structurally stable
- operationally useful
- evidence-sensitive

It is intentionally not optimized for exploratory essays or loosely framed strategy writing.

## License

No explicit open-source license is included yet. Add one later if you want to distribute the skill publicly.
