# Claude Code Slash Commands - ML & Bioinformatics Edition

A streamlined collection of **20 production-ready slash commands** for ML, deep learning, bioinformatics, and scientific computing workflows.

## Overview

This customized command set is optimized for:
- **Machine Learning & Deep Learning** pipelines
- **Bioinformatics** data analysis and research
- **Scientific Computing** with test-driven development
- **Research Projects** with structured feature specification and planning
- **Data Science** workflows with ETL and literature research

## Quick Command Reference

### Workflows (10 commands)

| Command | Purpose | Use Case |
|---------|---------|----------|
| `/workflows:tdd-cycle` | Test-driven development orchestration | Implement algorithms with test coverage |
| `/workflows:data-driven-feature` | ML-powered functionality development | Feature engineering, model deployment |
| `/workflows:ml-pipeline` | ML pipeline orchestration | End-to-end model training, validation, optimization |
| `/workflows:smart-fix` | Intelligent debugging | Investigate model bugs, data issues, research problems |
| `/workflows:full-review` | Multi-perspective code analysis | Review model code, architecture, research implementations |
| `/workflows:performance-optimization` | System-wide optimization | Optimize model inference, query performance, data loading |
| `/workflows:workflow-automate` | CI/CD pipeline automation | Automate experiments, training runs, batch processing |
| `/workflows:deep-web-research` | Comprehensive literature research | Find papers, methodologies, benchmark results, state-of-art |
| `/workflows:specify-feature` | Structured feature specification | Create detailed requirements for ML/research features |
| `/workflows:feature-plan` | Implementation planning | Generate design, contracts, and task strategy from specifications |

### Tools (10 commands)

| Command | Purpose | Use Case |
|---------|---------|----------|
| `/tools:tdd-red` | Failing test creation | Create edge case tests for algorithms |
| `/tools:tdd-green` | Minimal implementation | Implement code to pass tests |
| `/tools:tdd-refactor` | Code optimization | Refactor while maintaining test integrity |
| `/tools:data-pipeline` | ETL/ELT architecture | Build data ingestion, transformation, loading pipelines |
| `/tools:code-explain` | Code documentation | Document complex algorithms, ML models, research code |
| `/tools:think` | Structured reasoning framework | Multi-angle problem analysis for design decisions |
| `/tools:newskill` | Create custom skills | Build domain-specific Claude skills on-the-fly |
| `/tools:context-save` | State persistence | Save architecture decisions, experimental configurations |
| `/tools:context-restore` | State recovery | Restore previous decisions, configurations, context |
| `/tools:open-research` | Access research reports | Retrieve saved literature reviews and research findings |

## Installation

```bash
# Navigate to Claude configuration directory
cd ~/.claude

# Clone the commands repository
git clone https://github.com/flight50/ClaudeCommands.git

# Or use the existing customized version
```

## Command Invocation

Commands are invoked using directory prefixes:

```bash
# Workflow invocation
/workflows:tdd-cycle implement batch normalization algorithm

# Tool invocation
/tools:tdd-red create edge case tests for sequence alignment

# Start a data pipeline
/workflows:data-driven-feature extract features from genomic sequences

# Research literature
/workflows:deep-web-research latest advances in transformer models for protein structure prediction

# Specify a feature
/workflows:specify-feature create neural network for genomic classification

# Plan implementation
/workflows:feature-plan specs/001-genome-classifier/spec.md
```

## Recommended Workflow: From Idea to Implementation

This section provides a clear path from initial idea to working implementation. Choose the path that best fits your needs.

### 🎯 Primary Path: Structured Development (Recommended for ML/Bioinformatics)

**Best for**: ML/bioinformatics projects, structured development, team collaboration, template-driven workflows

```bash
# Step 1: Research (if exploring new technologies)
/workflows:deep-web-research [technology or methodology]

# Step 2: Think through design decisions
/tools:think comparing [approach A] vs [approach B] for [problem]

# Step 3: Create structured specification
/workflows:specify-feature [detailed feature description]
# Creates: specs/[###-feature-name]/spec.md

# Step 4: Generate implementation plan
/workflows:feature-plan specs/001-feature-name/spec.md
# Creates: plan.md, research.md, data-model.md, contracts/, quickstart.md

# Step 5: Review generated documents
# - Check research.md for technical decisions
# - Verify data-model.md for data structures
# - Review contracts/ for interface definitions

# Step 6: Implement with TDD
/tools:tdd-red create failing tests based on contracts and requirements
/tools:tdd-green implement minimal solution to pass tests
/tools:tdd-refactor improve code quality while keeping tests green

# OR use complete TDD workflow for larger features
/workflows:tdd-cycle implement feature based on plan.md

# Step 7: Integration & optimization (as needed)
/workflows:ml-pipeline [if ML feature]
/workflows:performance-optimization [if needed]

# Step 8: Documentation & context
/tools:code-explain document architecture and components
/tools:context-save save progress and configuration
```

**Output Structure**:
```
specs/[###-feature-name]/
├── spec.md          # Feature specification
├── plan.md          # Implementation plan
├── research.md      # Technical research
├── data-model.md    # Data structures
├── contracts/       # API contracts
└── quickstart.md    # Quick start guide
```

### 🔄 Alternative Path: Interactive Development (Kiro Method)

**Best for**: Exploratory work, interactive guidance, solo development, conversational workflows

```bash
# Step 1: Use kiro-spec-creator agent interactively
# Creates: .kiro/specs/{feature}/requirements.md
# Guides through: Requirements → Design → Tasks

# Step 2: Implement tasks one at a time
# Use kiro-task-executor agent for focused implementation

# Step 3: Use TDD tools for implementation
/tools:tdd-red create failing tests
/tools:tdd-green implement minimal solution
/tools:tdd-refactor improve code quality
```

**Output Structure**:
```
.kiro/specs/{feature}/
├── requirements.md  # Requirements and user stories
├── design.md       # Architecture and design
└── tasks.md        # Implementation tasks
```

### 📊 Workflow Comparison

| Aspect | Specify Framework | Kiro Method |
|--------|------------------|-------------|
| **Best For** | ML/bioinformatics, structured projects, teams | Exploratory work, interactive guidance |
| **Approach** | Template-driven, automated | Conversation-based, approval-driven |
| **Output Location** | `specs/[###-feature-name]/` | `.kiro/specs/{feature}/` |
| **Templates** | Uses `.specify/templates/` | Custom structure |
| **Constitution** | Enforces `.specify/memory/constitution.md` | Flexible principles |
| **Research** | Integrated in planning phase | Manual or embedded |
| **Speed** | Faster (automated) | Slower (interactive) |
| **Consistency** | High (template-driven) | Medium (conversation-based) |
| **Convergence** | Both paths use same TDD tools for implementation | Same TDD tools |

### 🤔 Which Path Should I Choose?

**Choose Specify Framework if:**
- ✅ Building ML/bioinformatics projects
- ✅ Working with a team (consistent structure)
- ✅ Want template-driven output
- ✅ Need constitution compliance
- ✅ Prefer automation over interaction

**Choose Kiro Method if:**
- ✅ Exploring new ideas interactively
- ✅ Want step-by-step guidance
- ✅ Prefer conversational workflow
- ✅ Working solo on exploratory features
- ✅ Need flexibility in structure

**Both paths converge at implementation:**
- Both use the same TDD tools (`/tools:tdd-red`, `/tools:tdd-green`, `/tools:tdd-refactor`)
- Both can use `/workflows:ml-pipeline` for ML features
- Both can use optimization and debugging workflows

## Common Workflows

### Research-Driven Feature Development (Complete Workflow)

This is the most powerful workflow - from discovery to implementation:

```bash
# Step 1: Discover and research
/workflows:deep-web-research latest approaches for [your technology/domain]

# Step 2: Think through design tradeoffs
/tools:think comparing [approach A] vs [approach B] for [specific problem]

# Step 3: Create structured specification
/workflows:specify-feature [detailed feature description with requirements]

# Step 4: Plan implementation with architecture and contracts
/workflows:feature-plan specs/001-feature-name/spec.md

# Step 5: Review the generated plan
# - Check generated research.md for tech decisions
# - Verify data-model.md for entity/data structures
# - Review contracts/ for interface definitions

# Step 6: Start TDD development
/tools:tdd-red create failing tests based on contracts and requirements

# Step 7: Implement
/tools:tdd-green implement minimal solution to pass tests

# Step 8: Optimize
/tools:tdd-refactor improve code quality while keeping tests green

# Step 9: Build complete system
/workflows:ml-pipeline or custom workflow for integration

# Step 10: Performance tune
/workflows:performance-optimization optimize critical paths and bottlenecks

# Step 11: Document
/tools:code-explain document architecture and key components

# Step 12: Save project state
/tools:context-save save progress and configuration for later sessions
```

### Test-Driven Algorithm Development

```bash
# Create failing test with edge cases
/tools:tdd-red create comprehensive tests with edge cases for [your algorithm]

# Implement minimal algorithm
/tools:tdd-green implement algorithm to pass all tests

# Optimize and refactor
/tools:tdd-refactor optimize performance while keeping tests green

# Or orchestrate complete TDD cycle
/workflows:tdd-cycle [feature description] with comprehensive test coverage
```

### Feature Implementation with ML/Data Focus

```bash
# Complete feature with data/model orchestration
/workflows:data-driven-feature [feature description with data/model components]

# Analyze and optimize performance
/workflows:performance-optimization optimize [critical component] performance

# Debug behavior
/workflows:smart-fix investigate [specific issue or unexpected behavior]
```

### Data Pipeline Development

```bash
# Build data pipeline
/tools:data-pipeline build ETL pipeline for [data source] with [transformations]

# Create training or processing workflow
/workflows:ml-pipeline [workflow description] with validation

# Automate experiments or jobs
/workflows:workflow-automate [experiment/task] with [parameters]
```

### Research and Learning (Simplified)

```bash
# Conduct comprehensive research
/workflows:deep-web-research [topic, technology, or methodology]

# Think through design decisions
/tools:think analyzing [approach A] vs [approach B] tradeoffs

# Save findings for later
/tools:context-save save research notes and references

# Retrieve previous research
/tools:open-research [topic or keyword]

# Code review and documentation
/workflows:full-review [code/architecture for review]
/tools:code-explain document [complex component or algorithm]
```

### Creating Domain-Specific Skills

```bash
# Create a reusable skill for your domain
/tools:newskill create a skill for [domain-specific task] with [specific requirements]

# Create a skill for specialized workflows
/tools:newskill create a skill for [specialized workflow] with [key features]
```

## Feature Development Framework

Your project includes two complementary approaches for structured development:

### Specify Framework (.specify) - Primary Path

The Specify framework provides templates and project principles for consistent feature development. **This is the recommended path for ML/bioinformatics projects.**

```
.specify/
├── memory/
│   └── constitution.md       # Project principles and guidelines (ML/bioinformatics focused)
├── templates/
│   ├── spec-template.md      # Feature specification template
│   ├── plan-template.md      # Implementation plan template
│   ├── tasks-template.md     # Task generation template
│   └── agent-file-template.md # AI agent instruction template
└── scripts/bash/
    ├── setup-plan.sh         # Initialize new features
    ├── create-new-feature.sh # Create feature directories
    └── update-agent-context.sh # Update AI agent context
```

**Constitution Principles**:
- Test-Driven Development (mandatory)
- Reproducibility First
- Data Quality & Validation
- Performance & Scalability
- Documentation & Clarity
- Simplicity & YAGNI

**Workflow**:
1. **Specification** (`/workflows:specify-feature`) → Creates `spec.md`
2. **Planning** (`/workflows:feature-plan`) → Creates `plan.md`, `research.md`, `data-model.md`, `contracts/`
3. **Implementation** → Uses TDD tools or workflows

### Kiro Method Agents (agents/) - Alternative Path

Five specialized agent personas for interactive, conversational development. **Use this for exploratory work or when you want step-by-step guidance.**

| Agent | Role | Use For |
|-------|------|---------|
| **kiro-assistant** | General support | Quick help, code review, troubleshooting |
| **kiro-spec-creator** | Spec workflow | Feature requirements, design, tasks |
| **kiro-feature-designer** | Architecture | System design, components, data models |
| **kiro-task-planner** | Task generation | Creating actionable implementation tasks |
| **kiro-task-executor** | Implementation | Executing tasks one at a time |

**Workflow**:
1. **Requirements** (kiro-spec-creator) → Creates `requirements.md`
2. **Design** (kiro-feature-designer) → Creates `design.md`
3. **Tasks** (kiro-task-planner) → Creates `tasks.md`
4. **Implementation** (kiro-task-executor) → Executes tasks one by one

See `agents/README.md` for detailed information.

### Integration Notes

- **Both paths converge** at the implementation phase using the same TDD tools
- **Specify Framework** is recommended for ML/bioinformatics projects
- **Kiro Method** is good for exploratory or interactive development
- You can mix approaches: use Specify for structure, Kiro agents for implementation guidance

## Execution Best Practices

### Context Optimization
1. **Technology Stack**: Specify frameworks (PyTorch, TensorFlow, scikit-learn), data formats (FASTA, HDF5, Parquet)
2. **Data Constraints**: Include dataset size, memory requirements, compute resources
3. **Integration Requirements**: Specify databases, external tools, APIs
4. **Output Preferences**: Indicate testing framework (pytest), documentation format

### Research Workflow
```bash
# 1. Discover literature
/workflows:deep-web-research machine learning approaches to protein function prediction

# 2. Think through methodology
/tools:think comparing supervised vs unsupervised learning for protein classification

# 3. Save research context
/tools:context-save research papers and recommended methodologies

# 4. Later: retrieve research
/tools:open-research protein classification
```

### Feature Specification Workflow (Specify Framework)

```bash
# 1. Create specification with requirements
/workflows:specify-feature <your feature description>
# Creates: specs/001-feature-name/spec.md

# 2. Plan implementation from spec
/workflows:feature-plan specs/001-feature-name/spec.md
# Creates: plan.md, research.md, data-model.md, contracts/, quickstart.md

# 3. Review generated documents
# - research.md: technical decisions
# - data-model.md: data structures
# - contracts/: API contracts
# - quickstart.md: quick start guide
```

### Kiro Method Workflow (Alternative)

```bash
# 1. Use kiro-spec-creator agent interactively
# Creates: .kiro/specs/{feature}/requirements.md
# Guides through: Requirements → Design → Tasks

# 2. Use kiro-task-executor for implementation
# Executes tasks one at a time from tasks.md
```

### Command Chaining
```bash
# Complete research pipeline
/workflows:specify-feature extract features from bioinformatics dataset
/workflows:feature-plan specs/001-feature/spec.md
/workflows:ml-pipeline train and validate predictive model
/workflows:performance-optimization optimize model inference speed
/tools:code-explain document model architecture and methods
/tools:context-save save model configuration and results
```

### Multi-Session Projects
```bash
# Save project state
/tools:context-save deep learning model checkpoints and experiment parameters

# Later, restore context
/tools:context-restore continue model development with saved parameters
```

## Performance Considerations

- Workflows typically require 30-90 seconds for complete orchestration
- Tools execute in 5-30 seconds for focused operations
- Research workflows take 3-5 minutes for comprehensive literature review
- Feature planning typically takes 2-3 minutes for design generation
- Provide detailed requirements upfront to minimize iteration cycles
- Use `context-save`/`context-restore` for multi-session projects
- Use `deep-web-research` + `open-research` for building research libraries

## File Organization

```
~/.claude/commands/
├── workflows/          # Multi-agent orchestration
│   ├── tdd-cycle.md
│   ├── data-driven-feature.md
│   ├── ml-pipeline.md
│   ├── deep-web-research.md
│   ├── specify-feature.md
│   ├── feature-plan.md
│   └── ...
├── tools/             # Single-purpose utilities
│   ├── tdd-red.md
│   ├── tdd-green.md
│   ├── tdd-refactor.md
│   ├── think.md
│   ├── newskill.md
│   ├── open-research.md
│   └── ...
└── README.md

.specify/              # Specify framework (integrated)
├── memory/
│   └── constitution.md # Project principles (ML/bioinformatics)
├── templates/         # Specification and planning templates
│   ├── spec-template.md
│   ├── plan-template.md
│   ├── tasks-template.md
│   └── agent-file-template.md
└── scripts/bash/      # Helper scripts (optional utilities)

docs/                  # Generated by workflows
├── research/          # Research reports from deep-web-research
│   ├── index.jsonl    # Index of research reports
│   └── YYYY-MM-DD_HH-mm-topic-slug.md

specs/                 # Feature specifications and plans
├── 001-feature-name/
│   ├── spec.md        # Specification
│   ├── plan.md        # Implementation plan
│   ├── research.md    # Technical research
│   ├── data-model.md  # Data structures
│   ├── contracts/     # API contracts
│   ├── quickstart.md  # Quick start guide
│   └── tasks.md       # Implementation tasks
```

## Example: Complete Feature Development Workflow

```bash
# 1. Research technologies and approaches
/workflows:deep-web-research [technology/approach for your feature]

# 2. Think through design decisions
/tools:think comparing [option A] vs [option B] for [specific concern]

# 3. Create detailed feature specification
/workflows:specify-feature [complete feature description]

# 4. Generate implementation plan
/workflows:feature-plan specs/001-feature-name/spec.md

# 5. Review specifications
# - Verify research.md explains architectural decisions
# - Check data-model.md for data structures
# - Ensure contracts/ define clear boundaries

# 6. Create failing tests
/tools:tdd-red create comprehensive failing tests

# 7. Implement minimal solution
/tools:tdd-green implement to pass tests

# 8. Optimize and refactor
/tools:tdd-refactor improve code quality

# 9. Build complete system
/workflows:data-driven-feature [full feature integration]

# 10. Validate and optimize
/workflows:performance-optimization optimize critical components

# 11. Document code
/tools:code-explain document architecture and components

# 12. Save project state
/tools:context-save save progress for future sessions
```

## Research and Reference Management

```bash
# Session 1: Research a topic
/workflows:deep-web-research [your research topic]
/tools:open-research  # Open the saved research

# Session 2: Research another topic
/workflows:deep-web-research [another research topic]
/tools:think [analyze findings and tradeoffs]

# Later: Retrieve previous research
/tools:open-research [keyword or partial topic name]

# Build knowledge base
/tools:context-save save important research and references
```

## Additional Resources

- [Claude Code Official Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Slash Commands Reference](https://docs.anthropic.com/en/docs/claude-code/slash-commands)
- [GitHub Spec Kit](https://github.com/github/spec-kit) - Source of `.specify` framework

## License

MIT License - See LICENSE file for complete terms.
