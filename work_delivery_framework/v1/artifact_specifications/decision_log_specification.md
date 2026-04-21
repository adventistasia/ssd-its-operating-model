# Decision Log Specification

## 1. Purpose

The `Decision Log` is the durable record of material initiative decisions, options considered, rationale, ownership, and implications.

## 2. When Required

Always required for every initiative.

## 3. Required By

Must exist no later than Gate 2.

It remains a persistent critical artifact from Gate 2 through Gate 8.

## 4. Required Contents

The artifact contains decision entries. Each entry should include:

1. decision statement
2. date
3. owner
4. status
5. options considered
6. rationale
7. implications

## 5. Completeness Rules

The log is complete when:

1. material stop/proceed, scope, requirement, risk-treatment, and approach decisions are recorded when made
2. open decisions are clearly distinguishable from settled decisions
3. downstream teams can understand why the decision exists without reconstructing context

## 6. Common Failure Conditions

1. important decisions exist only in meeting memory or other artifacts
2. entries omit enough rationale or status detail that intent must be reinterpreted
3. omission or waiver decisions are not recorded

## 7. Related Files

1. `../templates/decision_log_template.md`
2. `../examples/decision_log_example.md`
