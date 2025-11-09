description: Turn a feature specification into research, design, and contract deliverables that guide implementation.
argument-hint: "<path to spec file>"

# Feature Plan

Generate a comprehensive implementation plan from a feature specification using the Specify framework. The outputs unblock delivery teams, the tdd-cycle workflow, and downstream automation.

## Usage

```bash
/workflows:feature-plan <path to spec.md>
```

## What This Does

Transforms a feature specification into a detailed implementation plan that includes:
- **Technical research** (Phase 0) - Investigation of technologies and approaches
- **System design** (Phase 1) - Architecture, data models, contracts
- **Task generation strategy** (Phase 2) - How to break work into manageable tasks
- **Constitution compliance** - Verify design aligns with project principles

## Plan Output

The workflow creates/updates:

```
specs/[###-feature-name]/
├── spec.md              # (Input: your specification)
├── plan.md              # The implementation plan
├── research.md          # Technical research and decisions
├── data-model.md        # Data entities and relationships
├── contracts/           # API contracts and schemas
├── quickstart.md        # Quick start guide
└── tasks.md             # (Created by /tasks command next)
```

## Examples

### Example 1: ML Model Implementation
```bash
/workflows:feature-plan specs/001-genome-classifier/spec.md
```

Creates plan for:
- Research on transformer vs CNN architectures for sequences
- Data preprocessing pipeline design
- Model interface contracts
- Training workflow

### Example 2: Bioinformatics Pipeline
```bash
/workflows:feature-plan specs/002-variant-calling/spec.md
```

Creates plan for:
- Research on variant calling tools (bcftools, GATK)
- Data model for variants and annotations
- Pipeline stages and data flow
- Quality control contracts

### Example 3: Research Workflow
```bash
/workflows:feature-plan specs/003-expression-analysis/spec.md
```

Creates plan for:
- Research on RNA-seq analysis methods
- Data transformations and normalizations
- Statistical test contracts
- Performance and accuracy targets

## Process

1. **Read the template** - Load `.specify/templates/plan-template.md` to understand the required structure
2. **Read the constitution** - Load `.specify/memory/constitution.md` to understand project principles
3. **Load specification** - Read the spec.md file from the path provided
4. **Identify technical unknowns** - Extract [NEEDS CLARIFICATION] markers from spec
5. **Plan research** (Phase 0) - What technical decisions need to be made? Create research.md
6. **Design system** (Phase 1):
   - Define data models → `data-model.md`
   - Create API contracts → `contracts/` directory
   - Generate failing tests (TDD approach)
   - Write quickstart guide → `quickstart.md`
7. **Verify constitution** - Ensure design aligns with project principles from constitution
8. **Create plan** - Generate `plan.md` following the template structure
9. **Plan tasks** (Phase 2) - Describe task generation approach (don't create tasks.md yet)

## Plan Sections

### Technical Context
- Language/framework versions
- Dependencies and tools
- Storage and performance requirements
- Testing framework
- Computational constraints for ML

### Constitution Check
- Verify design follows project principles
- Document any necessary deviations
- Justify complexity if needed

### Phase 0: Research Plan
- Technical decisions to investigate
- Best practices for this domain
- Alternatives to evaluate
- Output: `research.md`

### Phase 1: Design & Contracts
- Data model specification
- API/workflow contracts
- Test-first approach (failing tests)
- Quick start implementation
- Output: `data-model.md`, `contracts/`, `quickstart.md`

### Phase 2: Task Planning
- Strategy for generating tasks
- Estimated number of tasks
- Parallel execution opportunities
- Order dependencies

## ML/Bioinformatics Examples

### Data Science Context
- **Language**: Python 3.11, PyTorch 2.0
- **Dependencies**: scikit-learn, pandas, numpy
- **Storage**: HDF5 for data, SQLite for metadata
- **Testing**: pytest with parametrization
- **Performance**: <5 min training per epoch, <100MB memory

### Bioinformatics Context
- **Language**: Python 3.11, Bash scripts
- **Dependencies**: biopython, pysam, bcftools
- **Storage**: FASTA/BAM files, PostgreSQL for results
- **Testing**: pytest with fixture-based test data
- **Performance**: Linear in sequence count, <10sec per sample

## Next Steps

1. **Review the plan** - Verify technical approach is sound
2. **Resolve research gaps** - Run additional research if needed
3. **Validate design** - Ensure data models and contracts work
4. **Generate tasks** - Use `/workflows:tasks` to create actionable tasks
5. **Begin implementation** - Follow TDD approach: tests first, then code

## Integration with Specify Framework

This workflow uses your project's Specify framework:

1. **Template**: Reads `.specify/templates/plan-template.md` to structure the output
2. **Constitution**: References `.specify/memory/constitution.md` for project principles and compliance checks
3. **Input**: Uses feature spec created by `/workflows:specify-feature`
4. **Output**: Creates multiple files in `specs/[###-feature-name]/`:
   - `plan.md` - Main implementation plan following template
   - `research.md` - Technical research and decisions
   - `data-model.md` - Data entities and relationships
   - `contracts/` - API contracts and schemas
   - `quickstart.md` - Quick start implementation guide

**Instructions for Claude Code**:
- Read `.specify/templates/plan-template.md` first to understand the required format
- Read `.specify/memory/constitution.md` to understand project principles
- Follow the template structure exactly, filling in all sections
- Verify constitution compliance at each gate
- Generate outputs in the specified locations

## Best Practices

- **Research first**: Understanding technologies prevents redesign
- **Contract-driven design**: Define interfaces before implementation
- **TDD from the start**: Generate failing tests, then code
- **Document decisions**: Capture the "why" for future reference
- **Think about testing**: How will you validate model performance?

## Complexity Management

If the plan suggests complexity:
- Document why it's necessary (not just "YAGNI")
- Consider simpler approaches first
- Justify deviations from project principles
- Plan for refactoring/simplification

## Output Characteristics

A good implementation plan:
- ✅ Resolves all [NEEDS CLARIFICATION] from spec
- ✅ Defines clear contracts/interfaces
- ✅ Includes failing tests ready for TDD
- ✅ Has realistic task estimates
- ✅ Aligns with project constitution
- ✅ Considers edge cases and error handling

