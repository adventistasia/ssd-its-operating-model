# Data Migration Plan Specification

## 1. Purpose

The `Data Migration Plan` is the execution-level migration approach artifact that explains sequencing, cutover, validation, and rollback for data movement.

## 2. When Required

Required when the initiative includes data migration.

## 3. Required By

Gate 4: `Specification Complete`

## 4. Required Contents

1. migration approach and sequencing
2. cutover plan and downtime expectations where applicable
3. validation plan
4. rollback or backout approach

## 5. Completeness Rules

The plan is complete when:

1. sequencing, validation, and recovery are explicit enough to assess feasibility and delivery risk
2. the plan aligns with the Data Asset Specification and business continuity expectations

## 6. Common Failure Conditions

1. validation or rollback is missing or not credible
2. migration sequencing depends on undocumented assumptions

## 7. Related Files

1. `../templates/data_migration_plan_template.md`
