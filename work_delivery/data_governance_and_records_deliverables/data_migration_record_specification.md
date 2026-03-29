# Data Migration Record Specification

## 1. What This Artifact Is For

The Data Migration Record documents both the planned migration approach and the evidence confirming that the migration was completed successfully.

It exists to make migration controlled, reviewable, and attributable rather than an informal technical exercise. A useful migration record shows what is moving, how it is being transformed or reconciled, what the cutover and recovery considerations are, and how correctness was verified.

The intended outcome is that migration can be approved, executed, validated, and later reviewed with a clear record of what changed, how it was controlled, and how success was confirmed.

Intended readers include: Data Steward, migration and delivery leads, IT Operations / Service Owner, security and audit reviewers, and Acceptance Authorities.

## 2. When to Use It

This artifact is required when data is materially migrated, transformed, restructured, consolidated, or loaded into a new authoritative location.

Use this artifact when migration correctness, reconciliation, cutover, rollback, or stewardship sign-off matter. It is most useful where data integrity and traceability must be demonstrated, not just assumed.

It should align with NIST planning and integrity expectations by making migration scope, validation, and rollback thinking explicit. It should also align with practical governance expectations for stewardship sign-off and exception handling.

In the Work Delivery Framework lifecycle, migration planning is typically prepared in Stage 4, executed and evidenced in Stage 6, and finalized as acceptance input in Stage 7.

## 3. Stage Fit and Handoffs

**Upstream inputs:**

- [Data Asset Specification](data_asset_specification.md) — provides authoritative context on source and target data assets, system-of-record boundaries, and lifecycle treatment
- [Technical Design Document](../operational_readiness_deliverables/technical_design_document_specification.md) — informs migration architecture, transformation logic, and sequencing approach
- [Backup, Restore & Recovery Plan](../operational_readiness_deliverables/backup_restore_and_recovery_plan_specification.md) — confirms rollback and recovery options available during migration

**Downstream consumers:**

- [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) — receives validation evidence and exception dispositions from this record
- [Formal Acceptance & Closure Record](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) — references this record as evidence that migration was controlled and validated

**Also relates to:**

- [Delivery Roadmap](../governance_and_control_deliverables/delivery_roadmap_specification.md) — migration activities and waves should be visible in the delivery schedule
- [Decision Record Log](../governance_and_control_deliverables/decision_record_log_specification.md) — material migration decisions such as scope changes, exception acceptance, or authority transfer should be logged

## 4. Before You Start

Confirm the following inputs are available before drafting:

- source and target systems identified
- migration scope confirmed
- Data Steward named
- mapping and transformation logic understood
- rollback and recovery approach agreed
- validation method and thresholds defined

## 5. How to Draft It

1. **Draft the migration plan** (§6.1) — document source and target systems, scope, mapping or transformation summary, sequencing or cutover approach, rollback considerations, responsibilities, and authority transfer.
2. **Populate validation evidence as execution progresses** (§6.2) — record the reconciliation or validation approach, summarize results, note exceptions and their disposition, and apply agreed thresholds or tolerances.
3. **Record exceptions and dispositions** (§6.3 table) — use the validation table to show each check, method, result, exception, and disposition clearly.
4. **Obtain Data Steward or Acceptance Authority sign-off** on results before the record is finalized.

## 6. Minimum Structure

This artifact normally has two major parts.

### 6.1. Migration Plan

Must include:

- source and target systems or datasets
- scope of migrated data
- mapping or transformation summary
- sequencing or cutover approach
- rollback or recovery considerations
- responsibilities and prerequisites
- statement of which source and target become authoritative before and after cutover where that matters

This section explains how the migration is intended to happen.

### 6.2. Validation Evidence

Must include:

- reconciliation or validation approach
- summary of results
- exceptions identified and their disposition
- steward or Acceptance Authority sign-off
- validation thresholds, tolerances, or acceptance basis where results are not expected to be exact-match in every case

This section shows whether the migration was successful and trustworthy.

### 6.3. Template Guide

Recommended validation table:

| Check | Method | Result | Exception | Disposition |
| --- | --- | --- | --- | --- |

Use the `Disposition` field to show how each exception was resolved, accepted, deferred, or escalated.

## 7. Writing Rules

Keep the record focused on migration logic, validation basis, exceptions, and sign-off. Reference detailed scripts or mapping files instead of copying them wholesale.

Keep the following out of this artifact:

- full script bodies unless the record is the approved execution artifact
- raw export files
- unrelated transformation design detail
- hidden exception handling in free-text notes

## 8. Traceability, Ownership, and Review

The migration lead or data lead usually prepares the record with steward involvement.

The Data Steward and other relevant Acceptance Authorities should review and confirm the validation outcome.

The Delivery Owner is accountable for ensuring migration evidence is complete, attributable, and available for acceptance and closure decisions.

## 9. Maintenance Expectations

Keep the record current through planning, execution, and final validation. If migration occurs in waves, maintain versioned records or clearly separate each wave.

## 10. Done When

- Migration plan covers scope, source and target systems, mapping, cutover approach, and rollback
- Validation approach is documented
- Results summary is complete
- Exceptions are explicitly dispositioned
- Authority transfer from source to target is visible
- Data Steward or Acceptance Authority sign-off is recorded

## 11. What Comes Next

1. Provide validation evidence to the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) as confirmation that migration was controlled and successful.
2. Reference in the [Formal Acceptance & Closure Record](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md) as closure evidence.
3. Update the [Data Asset Specification](data_asset_specification.md) to reflect the new authoritative location and any changed lifecycle treatment after cutover.
4. Archive source-system access and access records per retention obligations.

## 12. Prompt Guide

### 12.1. Starter Prompt

```
Draft a Data Migration Record for this initiative.
Include the migration plan, mapping or transformation summary, cutover and rollback considerations, validation method, results, exceptions, and steward sign-off.
Keep it practical, traceable, and exception-aware.
```

### 12.2. Validation Prompt

```
Review this Data Migration Record.
Check that the migration plan covers scope, source and target systems, mapping, cutover, and rollback; the validation approach is documented; results are summarized; exceptions are explicitly dispositioned; authority transfer from source to target is visible; and Data Steward or Acceptance Authority sign-off is recorded.
Note any gaps in exception handling, reconciliation evidence, or sign-off coverage.
```
