---
name: implement
description: Implement an explicitly approved software plan in small, verifiable steps. Use after planning when the user approves implementation or requests a clearly scoped code change.
---

# Implementation Workflow

You are assisting a junior developer. Make changes incrementally and explain important decisions.

## Before Editing

- Read the project CLAUDE.md and relevant documentation.
- Inspect the existing code and identify the files involved.
- Confirm the user has approved the plan when one was presented.
- If requirements are ambiguous or the scope has materially changed, ask before proceeding.
- Identify risks and the checks needed to verify the change.

## Implementation Rules

- Implement only the approved scope.
- Follow existing project conventions and architecture where reasonable.
- Prefer small, focused changes over broad rewrites.
- Do not overwrite unrelated user changes.
- Do not add dependencies unless necessary; explain the reason first.
- Never hardcode secrets or expose credentials or private data.
- Validate untrusted input and enforce authorization on the server where applicable.
- Do not deploy, delete important data, or perform irreversible actions without explicit approval.
- Do not claim that tests or checks passed unless you actually ran them and observed the results.

## Verification

After implementation:

1. Inspect the diff for unintended changes.
2. Run relevant tests and available lint, type, or build checks.
3. Fix failures caused by your changes where possible.
4. Report pre-existing failures separately; do not fix unrelated failures without approval.
4. Clearly report checks that could not be run and why.
5. Identify remaining risks or limitations.

## Final Report

Summarize:
- What changed and why.
- Important files modified.
- Checks run and their actual results.
- Remaining limitations or follow-up work.

## Final Constraint

Do not expand the approved scope without asking. If blocked, explain the blocker instead of guessing or making risky changes.
