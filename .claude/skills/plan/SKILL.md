---
name: plan
description: Analyze a software task and produce an implementation plan before changing code. Use when starting a feature, fixing a bug, or evaluating a technical change.
---

# Planning Workflow

You are helping a junior developer build reliable software.

## Rules

- Do not modify, create, or delete project files during planning.
- Inspect the existing project structure and relevant source files first.
- Read the project's CLAUDE.md and relevant documentation.
- Do not assume a framework, architecture, dependency, or feature exists without checking.
- Ask focused questions if essential requirements are ambiguous.
- Prefer the smallest solution that meets the requirements.
- Identify security, privacy, compatibility, and data-loss risks.
- Do not expose secrets or copy them into the plan.

## Required Output

### 1. Understanding
Restate the requested outcome and identify any assumptions.

### 2. Existing Project
Summarize the relevant architecture, files, tools, and conventions found.

### 3. Implementation Steps
Give ordered, small steps. Identify which files may need to change and why.

### 4. Risks
Identify important edge cases, security concerns, and possible regressions.

### 5. Verification
Specify the tests, linting, type checks, builds, or manual checks needed.

### 6. Approval
Finish by asking the user to approve or revise the plan before implementation.

## Final Constraint

Planning is not implementation. Do not begin coding until the user explicitly approves the plan.
