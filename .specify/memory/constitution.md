# ML & Bioinformatics Development Constitution

**Version**: 1.0.0 | **Ratified**: 2025-01-27 | **Last Amended**: 2025-01-27

## Core Principles

### I. Test-Driven Development (NON-NEGOTIABLE)
TDD mandatory: Tests written → User approved → Tests fail → Then implement. Red-Green-Refactor cycle strictly enforced. For ML models, include performance benchmarks, accuracy metrics, and edge case validation. For bioinformatics, include data validation tests and format compatibility checks.

### II. Reproducibility First
All experiments, models, and analyses must be reproducible:
- Fixed random seeds for ML models
- Versioned dependencies (requirements.txt, environment.yml)
- Data lineage tracking
- Clear documentation of preprocessing steps
- Reproducible computational environments

### III. Data Quality & Validation
- Validate input data formats and quality before processing
- Document data transformations and preprocessing steps
- Handle missing data, outliers, and edge cases explicitly
- Validate model outputs meet specified constraints
- Log data quality metrics

### IV. Performance & Scalability
- Document computational constraints (memory, time, scale)
- Optimize critical paths (data loading, model inference)
- Consider scalability from the start
- Profile and measure before optimizing
- Set realistic performance targets

### V. Documentation & Clarity
- Document why technical decisions were made
- Include usage examples and quickstart guides
- Explain complex algorithms and domain-specific concepts
- Maintain clear API contracts and data schemas
- Code should be self-documenting where possible

### VI. Simplicity & YAGNI
Start simple, add complexity only when justified:
- Prefer standard libraries over custom implementations
- Use established patterns and frameworks
- Justify complexity deviations in design documents
- Refactor incrementally, not preemptively

## ML/Bioinformatics Specific Constraints

### Data Handling
- Use appropriate data formats (FASTA, HDF5, Parquet, BAM/VCF for bioinformatics)
- Handle large datasets efficiently (streaming, chunking, lazy loading)
- Validate data formats and schemas before processing
- Document data provenance and lineage

### Model Development
- Define clear evaluation metrics (accuracy, precision, recall, AUC, etc.)
- Include model versioning and checkpointing
- Document hyperparameters and training configurations
- Validate model outputs meet domain requirements
- Handle edge cases and failure modes gracefully

### Testing Requirements
- Unit tests for data processing functions
- Integration tests for pipelines
- Performance benchmarks for critical paths
- Validation tests for model outputs
- Edge case tests for error handling

### Integration & Compatibility
- Define clear input/output formats and contracts
- Support standard data formats for the domain
- Document API contracts and interfaces
- Version APIs and data schemas appropriately
- Handle backward compatibility when needed

## Development Workflow

### Feature Development Process
1. **Specify** - Create detailed feature specification with requirements
2. **Plan** - Generate implementation plan with research, design, and contracts
3. **Test** - Create failing tests following TDD approach
4. **Implement** - Write minimal code to pass tests
5. **Refactor** - Improve code quality while maintaining tests
6. **Document** - Update documentation and examples

### Code Review Standards
- Tests must pass before review
- Code must follow project conventions
- Performance implications must be considered
- Documentation must be updated
- Complexity must be justified

### Quality Gates
- All tests pass (unit, integration, performance)
- Code coverage meets minimum thresholds
- Documentation is complete and accurate
- Performance benchmarks meet targets
- Data validation and error handling are comprehensive

## Governance

This constitution supersedes all other development practices. Amendments require:
- Documentation of the change and rationale
- Approval from project maintainers
- Migration plan if breaking changes

All PRs, reviews, and implementations must verify compliance with this constitution. Complexity deviations must be documented and justified.

**Guiding Philosophy**: Build reliable, reproducible, and maintainable software for ML and bioinformatics research. Quality and correctness over speed. Test everything. Document decisions. Start simple.
