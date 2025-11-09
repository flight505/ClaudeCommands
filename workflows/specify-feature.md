description: Create a structured feature specification that feeds into planning and implementation workflows.
argument-hint: "<feature description>"

# Specify Feature

Create a comprehensive, implementation-ready feature specification using the Specify framework. The output becomes the starting point for `/feature-plan`, TDD workflows, and delivery teams.

## Usage

```bash
/workflows:specify-feature <feature description>
```

## What This Does

Generates a structured feature specification that captures:
- **User scenarios** - How people interact with the capability
- **Functional requirements** - Testable, measurable requirements
- **Data entities** - Models and data structures needed
- **Acceptance criteria** - Clear pass/fail conditions
- **Clarification flags** - Areas needing additional details

## Specification Output

The workflow creates:

```
specs/[###-feature-name]/
├── spec.md          # The feature specification
├── plan.md          # (Created in next step)
└── research.md      # (Created during planning)
```

## Examples

### Example 1: ML Model Feature
```bash
/workflows:specify-feature create a neural network model for genomic sequence classification that takes raw DNA sequences and predicts disease risk with confidence scores
```

### Example 2: Bioinformatics Tool
```bash
/workflows:specify-feature build a data preprocessing pipeline that validates FASTA files, removes low-quality sequences, and normalizes expression data for downstream analysis
```

### Example 3: Research Workflow
```bash
/workflows:specify-feature implement variant calling workflow that identifies genetic variations from sequencing data with quality filtering and annotation
```

## Process

1. **Read the template** - Load `.specify/templates/spec-template.md` to understand the required structure
2. **Read the constitution** - Load `.specify/memory/constitution.md` to understand project principles
3. **Parse your description** - Extract key concepts, actors, and data flows from the user's feature description
4. **Identify user scenarios** - How will researchers/users interact with this feature?
5. **Generate requirements** - Break down into testable, measurable requirements following the template format
6. **Flag clarifications** - Mark areas that need more detail with [NEEDS CLARIFICATION: specific question]
7. **Create specification** - Output structured spec.md following the template structure, ready for planning
8. **Verify constitution compliance** - Ensure the spec aligns with project principles

## Specification Sections

### User Scenarios & Testing
- Primary research workflow
- Acceptance scenarios (Given/When/Then format)
- Edge cases and error handling

### Functional Requirements
- Testable capabilities and system behaviors
- Data requirements and transformations
- Performance or quality targets
- Validation, error handling, and observability needs

### Key Entities
- Data models and schemas
- Inputs, outputs, and transformations
- Storage, transport, and lifecycle considerations

## Next Steps

After creating your specification:

1. **Review the spec** - Verify all requirements are clear
2. **Resolve clarifications** - Address any [NEEDS CLARIFICATION] markers
3. **Plan implementation** - Use `/workflows:feature-plan` to generate implementation plan
4. **Generate tasks** - Break plan into specific development tasks

## Integration with Specify Framework

This workflow uses your project's Specify framework:

1. **Template**: Reads `.specify/templates/spec-template.md` to structure the output
2. **Constitution**: References `.specify/memory/constitution.md` for project principles
3. **Output**: Creates `specs/[###-feature-name]/spec.md` following the template structure
4. **Format**: Output is compatible with `/workflows:feature-plan` for planning

**Instructions for Claude Code**:
- Read `.specify/templates/spec-template.md` first to understand the required format
- Read `.specify/memory/constitution.md` to understand project principles
- Follow the template structure exactly, filling in all mandatory sections
- Use [NEEDS CLARIFICATION: specific question] for any ambiguities
- Ensure all requirements are testable and measurable

## Best Practices

- **Be specific**: "Classify genomic sequences by pathogenicity" vs "create a model"
- **Include context**: What data sources? What validation methods?
- **Think like a researcher**: What's the user journey from raw data to insights?
- **Identify constraints**: Performance needs? Data privacy? Resource limits?

## Domain-Specific Considerations

Adjust the specification to address:
- **Success criteria** (metrics, SLAs, service levels)
- **Data quality standards** (validation rules, filtering criteria)
- **Operational constraints** (latency, throughput, capacity)
- **Traceability needs** (auditing, lineage, reproducibility)
- **Integration requirements** (APIs, file formats, contracts)

