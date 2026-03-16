# Data Migration Record Specification

## 1. Purpose and Intended Outcome

The Data Migration Record documents both the planned migration approach and the evidence confirming that the migration was completed successfully.

It exists to make migration controlled, reviewable, and attributable rather than an informal technical exercise. A useful migration record shows what is moving, how it is being transformed or reconciled, what the cutover and recovery considerations are, and how correctness was verified.

The intended outcome is that migration can be approved, executed, validated, and later reviewed with a clear record of what changed, how it was controlled, and how success was confirmed.

## 2. When It Is Required

This artifact is required when data is materially migrated, transformed, restructured, consolidated, or loaded into a new authoritative location.

## 3. Intended Readers and Users

- Data Steward
- migration and delivery leads
- IT Operations / Service Owner
- security and audit reviewers
- Acceptance Authorities

## 4. Intended Project Context

Use this artifact when migration correctness, reconciliation, cutover, rollback, or stewardship sign-off matter. It is most useful where data integrity and traceability must be demonstrated, not just assumed.

It should align with NIST planning and integrity expectations by making migration scope, validation, and rollback thinking explicit. It should also align with practical governance expectations for stewardship sign-off and exception handling.

## 5. How Much Detail to Include

Keep the record focused on migration logic, validation basis, exceptions, and sign-off. Reference detailed scripts or mapping files instead of copying them wholesale.

## 6. Required Content or Minimum Structure

This artifact normally has two major parts.

### 6.1. Migration plan

Must include:

- source and target systems or datasets
- scope of migrated data
- mapping or transformation summary
- sequencing or cutover approach
- rollback or recovery considerations
- responsibilities and prerequisites
- statement of which source and target become authoritative before and after cutover where that matters

This section explains how the migration is intended to happen.

### 6.2. Validation evidence

Must include:

- reconciliation or validation approach
- summary of results
- exceptions identified and their disposition
- steward or Acceptance Authority sign-off
- validation thresholds, tolerances, or acceptance basis where results are not expected to be exact-match in every case

This section shows whether the migration was successful and trustworthy.

### 6.3. Template guide

Recommended validation table:

| Check | Method | Result | Exception | Disposition |
| --- | --- | --- | --- | --- |

Use the `Disposition` field to show how each exception was resolved, accepted, deferred, or escalated.

## 7. What to Keep Out

Keep the following out of this artifact:

- full script bodies unless the record is the approved execution artifact
- raw export files
- unrelated transformation design detail
- hidden exception handling in free-text notes

## 8. Relationships to Other Artifacts

This artifact should align with the Data Asset Specification, Technical Design Document, Backup, Restore & Recovery Plan, Acceptance Record, and decision or risk records where migration risk is material.

## 9. Ownership, Review, and Acceptance Expectations

The migration lead or data lead usually prepares the record with steward involvement.

The Data Steward and other relevant Acceptance Authorities should review and confirm the validation outcome.

## 10. Maintenance Expectations

Keep the record current through planning, execution, and final validation. If migration occurs in waves, maintain versioned records or clearly separate each wave.

## 11. Validation Guide

- Does the record explain what is moving, how, and under what control?
- Is the validation method clear enough to trust the result?
- Are exceptions explicit and formally dispositioned?
- Can a reviewer tell when authority moved from source to target and on what validation basis that shift was accepted?
- Is steward or acceptance sign-off visible?

If weak, clarify the migration boundary, make reconciliation evidence more specific, and show who accepted the result.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Data Migration Record for this initiative.
> Include the migration plan, mapping or transformation summary, cutover and rollback considerations, validation method, results, exceptions, and steward sign-off.
> Keep it practical, traceable, and exception-aware.
