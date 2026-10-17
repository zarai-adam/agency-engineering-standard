---
name: agency-review
description: Review code changes for correctness, security, regressions, maintainability, and test coverage. Use after implementation or before committing code.
---

# Code Review Workflow

Act as an independent reviewer. Prioritize finding real defects over praising the implementation.

## 1. Inspect the Changes

- Read CLAUDE.md and relevant project documentation.
- Run git status and inspect the diff against the appropriate base.
- Identify changed files and understand their surrounding code.
- Do not modify files during review unless the user explicitly requests fixes.

## 2. Review Priorities

Check for:

- Incorrect logic, edge cases, and runtime errors.
- Missing input validation and unsafe data handling.
- Authentication, authorization, and access-control weaknesses.
- Secret exposure, sensitive data leakage, and insecure configuration.
- Database consistency, race conditions, and destructive operations.
- API compatibility and unintended regressions.
- Missing or ineffective tests.
- Unnecessary dependencies and avoidable complexity.

## 3. Report Findings

List findings in descending severity:

- Critical: likely severe compromise, data loss, or system-wide impact.
- High: serious security or correctness defect.
- Medium: meaningful defect that should normally be fixed.
- Low: limited-impact issue or improvement.

For each finding, include:
- Severity.
- File and line number when available.
- The specific problem.
- The scenario in which it occurs.
- A practical recommended fix.

Do not invent vulnerabilities. Distinguish confirmed defects from risks that need further verification.

## 4. Verification

- Report which tests or checks were run and their actual results.
- Identify important checks that were not run.
- Do not claim that code is secure or bug-free based only on inspection.

## Final Report

Start with the highest-severity finding, or explicitly state when no actionable findings were identified.

Then summarize test coverage, remaining risks, and recommended next steps.

## Final Constraint

Review only. Do not change files, install dependencies, commit, push, or deploy unless the user explicitly requests that action.
