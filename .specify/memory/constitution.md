---
description: Project constitution that defines the engineering principles followed by specify and planning workflows.
argument-hint: ""
---

# Project Development Constitution

**Version**: 1.1.0&nbsp;&nbsp;|&nbsp;&nbsp;**Ratified**: 2025-01-27&nbsp;&nbsp;|&nbsp;&nbsp;**Last Amended**: 2025-01-27

## Core Principles

### I. Test-Driven Development (Non-Negotiable)
Work from failing tests toward working code. Apply the red → green → refactor cycle and keep the test suite fast, focused, and trustworthy.

### II. Reproducible Delivery
Make every outcome repeatable:
- Version and lock dependencies
- Capture environment and configuration details
- Track important decisions and rationales
- Provide clear instructions to rerun workflows end-to-end

### III. Data & Contract Integrity
- Validate inputs and outputs aggressively
- Describe data transformations and side effects
- Keep interfaces stable, versioned, and well documented
- Log and trace for observability and audits

### IV. Performance & Scale Awareness
- Define target service levels early (latency, throughput, capacity)
- Profile before optimizing and measure after changes
- Remove bottlenecks in priority order while protecting correctness

### V. Documentation & Clarity
- Record why a decision was made, not just what was done
- Provide onboarding-quality guides for new contributors
- Keep quickstart instructions up to date

### VI. Simplicity & Incrementalism
Favor the minimal solution that solves the problem:
- Prefer proven patterns and libraries
- Break work into reviewable increments
- Justify any added complexity and document trade-offs

## Specification → Plan → Delivery Workflow
1. **Specify** – Capture intent, scenarios, requirements, and unknowns.
2. **Plan** – Design architecture, contracts, and research agendas.
3. **Test** – Generate failing tests that define desired behavior.
4. **Implement** – Make tests pass with minimal code.
5. **Refine** – Refactor for quality, maintainability, and readability.
6. **Document** – Update guides, changelogs, and reference materials.

## Review & Quality Gates
- All automated checks pass (tests, lint, coverage, security as applicable)
- Reviewers confirm compliance with this constitution
- Performance budgets and operational guidelines remain intact
- Documentation reflects the delivered changes

## Governance
- Amendments require a documented rationale and approval from maintainers.
- Breaking changes must include a migration or rollback strategy.
- Exceptions are temporary, tracked, and resolved quickly.

**Guiding Philosophy**: Deliver reliable, maintainable software by making intentions explicit, validating with tests, and communicating clearly. Quality and clarity outlast velocity.
