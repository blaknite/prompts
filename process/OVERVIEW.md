# Agentic Change Process

## Purpose

This process provides a structured approach to software change management by separating concerns into four independent phases with clean handoffs. Each phase has singular responsibility and clear deliverables, ensuring systematic and reliable implementation of code changes.

## Process Overview

The change process consists of four completely independent phases:

### 1. Analysis Phase (Analyst)
**Purpose**: Investigate and gather evidence
**Input**: User request and codebase
**Output**: `ANALYSIS.md` with findings and context
**Focus**: WHAT needs to be solved (evidence gathering, not solution design)

### 2. Planning Phase (Architect)
**Purpose**: Design implementation approach
**Input**: `ANALYSIS.md` from previous phase
**Output**: `PLAN.md` with step-by-step instructions
**Focus**: HOW to solve it (solution design, not implementation)

### 3. Execution Phase (Executor)
**Purpose**: Implement the solution
**Input**: `PLAN.md` from previous phase
**Output**: Implemented code with verified functionality
**Focus**: Building the solution (implementation, not design)

### 4. Review Phase (Reviewer)
**Purpose**: Critically review the executed solution for quality and correctness
**Input**: Implemented code and `PLAN.md` with execution status
**Output**: `REVIEW.md` with quality assessment and approval status
**Focus**: Code quality, requirements validation, and identifying issues

## Project Structure

Each project MUST be contained within its own subdirectory of `.projects/`:

```
.projects/
├── project-name/
│   ├── ANALYSIS.md    # Analyst output
│   ├── PLAN.md        # Architect output
│   ├── REVIEW.md      # Reviewer output
│   └── [other files]  # Additional project artifacts
└── another-project/
    ├── ANALYSIS.md
    ├── PLAN.md
    └── REVIEW.md
```

## Phase Transition

Phases execute sequentially but independently:
1. Analyst creates `ANALYSIS.md` in project subdirectory
2. Architect reads analysis, creates `PLAN.md` in same subdirectory
3. Executor reads plan, implements solution, updates progress in `PLAN.md`
4. Reviewer examines implementation, creates `REVIEW.md` with quality assessment

Each phase validates inputs and can request corrections from previous phases if handoff artifacts are insufficient or stale.
