# Claude Code Agents - Kiro Development Method

This folder contains AI agent personas that embody the **Kiro Development Method** - a structured, developer-focused approach to feature specification, design, and implementation.

## What Are These Agents?

These are personalized AI personas designed to guide you through structured development workflows. Each agent has a specific role in the feature development lifecycle and can be activated in Claude Code to provide specialized guidance.

## Kiro Agents (5)

### 1. **kiro-assistant** - General Development Support
**Best for**: General development tasks, quick questions, troubleshooting

Provides fast, efficient help with a warm, supportive tone. This is your go-to agent for:
- Quick coding questions and advice
- Troubleshooting issues
- Code review feedback
- General development support

**Style**: Relaxed, developer-to-developer conversation; knowledgeable but not instructive

### 2. **kiro-spec-creator** - Feature Specification Workflow
**Best for**: Creating comprehensive feature specifications from scratch

Guides you through the complete specification workflow in three phases:
- **Phase 1**: Requirements gathering (user stories, acceptance criteria)
- **Phase 2**: Design document (architecture, components, data models)
- **Phase 3**: Task list (actionable implementation plan)

Gets explicit approval at each phase before proceeding.

**Workflow**: Rough idea → Requirements → Design → Tasks

### 3. **kiro-feature-designer** - Design Document Creation
**Best for**: Designing features and system architectures

Creates comprehensive design documents based on requirements:
- Researches relevant technologies and patterns
- Develops system architecture
- Defines component interfaces and contracts
- Plans testing strategy
- Documents error handling

Conducts research during the design process to inform architecture decisions.

**Output**: `.kiro/specs/{feature}/design.md`

### 4. **kiro-task-planner** - Task List Generation
**Best for**: Converting designs into actionable implementation tasks

Transforms approved design documents into concrete, executable tasks:
- Breaks down design into incremental steps
- Focuses on code implementation only
- Uses test-driven approach
- References requirements for traceability
- Prioritizes incremental building

**Output**: `.kiro/specs/{feature}/tasks.md`

### 5. **kiro-task-executor** - Task Implementation
**Best for**: Executing specific tasks from specifications

Implements individual tasks with precision and focus:
- Reads requirements, design, and task documents for context
- Executes one task at a time
- Writes minimal, focused code
- Follows the design architecture
- Stops after each task for review

One task at a time - never assumes you want multiple tasks done.

## Kiro Method Overview

```
Feature Idea
    ↓
[kiro-spec-creator] → Requirements.md
    ↓
[kiro-feature-designer] → Design.md
    ↓
[kiro-task-planner] → Tasks.md
    ↓
[kiro-task-executor] → Code Implementation (task by task)
    ↓
Working Feature
```

## File Organization

The Kiro method uses this structure:

```
.kiro/specs/
├── feature-name-1/
│   ├── requirements.md    (Phase 1 output)
│   ├── design.md          (Phase 2 output)
│   └── tasks.md           (Phase 3 output)
├── feature-name-2/
│   ├── requirements.md
│   ├── design.md
│   └── tasks.md
```

## How to Use These Agents

### Option 1: Using Agents in Claude Code

1. Install agents in your project:
   ```bash
   mkdir -p .claude/agents
   cp agents/kiro-*.md .claude/agents/
   ```

2. Reference agents in your Claude Code context or prompt

### Option 2: Using with Workflows

The Kiro method agents complement the Specify framework workflows:

- **`/specify-feature`** + **kiro-spec-creator** for detailed specs
- **`/feature-plan`** + **kiro-feature-designer** + **kiro-task-planner** for design & planning
- **kiro-task-executor** for focused implementation

### Option 3: Direct Usage

Mention the agent's role in your prompt:

```
Using the kiro-spec-creator approach, create a specification for:
[your feature description]
```

## Key Characteristics of the Kiro Method

✅ **User-Driven**: Explicit approval at each phase
✅ **Iterative**: Refine based on feedback
✅ **Structured**: Clear phases and outputs
✅ **Minimal Code**: Only what's necessary
✅ **Test-Driven**: Tests as part of implementation
✅ **Developer-Focused**: Practical, efficient workflows
✅ **Supportive Tone**: Encouraging, non-instructive

## Integration with Commands

These agents work well with:
- `/workflows:specify-feature` - Feature specification
- `/workflows:feature-plan` - Implementation planning
- `/tools:think` - Design exploration
- `/workflows:deep-web-research` - Research decisions
- `/tools:context-save` / `/tools:context-restore` - Preserve specs across sessions

## Example Usage

### Create a Feature Specification

Use kiro-spec-creator to build:
```
Feature: User authentication system
- Requirements phase: User stories, acceptance criteria
- Design phase: Auth flow, security approach, data models
- Tasks phase: Actionable implementation steps
```

### Implement Tasks

Use kiro-task-executor to build one task at a time:
```
Execute Task 1: Set up authentication middleware
Read requirements/design/tasks context
Implement minimal authentication setup
Stop and wait for approval before continuing
```

## Best Practices

1. **Follow the phases**: Don't skip specification, design, or planning
2. **Get approval**: Get explicit approval before proceeding to next phase
3. **One task at a time**: Complete and review before moving to next task
4. **Use context**: Kiro agents read and reference spec files for context
5. **Ask for clarification**: Agents will ask questions to clarify requirements
6. **Iterate quickly**: Agents are designed for rapid iteration

## Philosophy

The Kiro method is built on these principles:

- **Clarity First**: Know what you're building before you build it
- **Incremental Progress**: Small, verifiable steps
- **Developer-Centric**: Practical workflows, minimal ceremony
- **Quality by Design**: Architecture decisions made upfront, tested early
- **Efficiency**: Only do what's necessary

## References

- **Agents**: `.claude/agents/kiro-*.md`
- **Specify Framework**: `.specify/`
- **Main Commands**: See root README.md

