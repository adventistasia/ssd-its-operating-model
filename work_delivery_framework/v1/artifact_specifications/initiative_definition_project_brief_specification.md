# Initiative Definition / Project Brief Specification

## 1. Purpose

The `Initiative Definition / Project Brief` is the primary definition artifact for every in-scope initiative.

It defines the initiative, its scope, outcomes, context, constraints, owners, and delivery direction well enough to support gate decisions and downstream solution definition.

## 2. When Required

Always required for every in-scope initiative.

## 3. Required By

Gate 2: `Initiative Defined`

It remains a persistent critical artifact from Gate 2 through Gate 8.

## 4. Required Contents

1. background, problem, or opportunity
2. desired outcomes and success measures
3. scope boundaries, including in-scope, out-of-scope, and assumptions
4. stakeholders and owners, including Gate Decision Owner assignments
5. constraints and dependencies
6. known unknowns and open questions
7. functional requirements and use cases
8. user roles
9. business rules
10. solution direction at a high level
11. delivery approach at a high level
12. support and operational considerations where applicable
13. user adoption considerations where applicable
14. acceptance criteria in the embedded hybrid Gherkin format

## 5. Embedded Acceptance Criteria Requirement

Acceptance Criteria is an embedded canonical artifact inside the Project Brief.

For each major criterion, the Project Brief must include:

1. `Given`
2. `When`
3. `Then`
4. `Metric`
5. `Validation method`
6. `Holdout example`

Example shape:

```text
Given [preconditions and context]
When [action or event occurs]
Then [observable outcome]
  - Metric: [threshold]
  - Validation method: [test, query, inspection, or holdout pattern]
  - Holdout example: [concrete example]
```

## 6. Completeness Rules

The Project Brief is complete when:

1. the initiative can be understood and bounded without tribal knowledge
2. business rules, scope boundaries, and known unknowns are explicit
3. ownership and decision authority are visible from the document itself
4. acceptance criteria are observable and testable without downstream reinterpretation
5. the document is strong enough to support Gate 4 once triggered supporting artifacts are present

## 7. Common Failure Conditions

1. business outcomes or scope boundaries remain materially ambiguous
2. ownership or decision authority is not visible
3. acceptance criteria use vague language such as "works well" or "user friendly"
4. the document appears complete but leaves foundational next-stage questions unresolved

## 8. Supportability Note

If a separate `Deployment Guide` is not required, the minimum supportability and maintainability content must still be represented in the Project Brief at a proportionate level.

## 9. Related Files

1. `../templates/initiative_definition_project_brief_template.md`
2. `../examples/project_brief_acceptance_criteria_example.md`
