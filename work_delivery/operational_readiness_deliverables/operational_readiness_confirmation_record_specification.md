# Operational Readiness Confirmation Record Specification

## 1. What This Artifact Is For

The Operational Readiness Confirmation Record provides formal confirmation that the solution is ready to be accepted into operational responsibility, or it records the explicit conditions under which that readiness is accepted.

It exists to make handover explicit, attributable, and reviewable. A useful readiness record shows what evidence was reviewed, who is assuming service ownership, what gaps remain, and what decision was made.

The intended outcome is that transfer into operational responsibility is a clear, evidence-based decision with named ownership, visible conditions, and no hidden assumptions about readiness.

Intended readers include: IT Operations / Service Owner, Support Owner, Delivery Owner, and governance and audit reviewers.

## 2. When to Use It

This artifact is required when operational ownership is being assigned or confirmed before go-live or transition into steady state.

Use this artifact near go-live, handover, or production transition. It is most useful where operational acceptance must be explicit and where readiness depends on documentation, support ownership, monitoring, and recovery arrangements being in place.

It should align with ITIL 4 Change Enablement and service validation intent by making the readiness basis for operational acceptance visible and attributable.

## 3. Stage Fit and Handoffs

- Stage 6: prepare and update this record as readiness evidence becomes available.
- Stage 7: finalize this record to support operational acceptance, transition, and closure.

Upstream sources:

- [Technical Design Document Specification](technical_design_document_specification.md)
- [DevOps Guide Specification](devops_guide_specification.md)
- [Operations & Support Model Specification](operations_and_support_model_specification.md)
- [Backup, Restore & Recovery Plan Specification](backup_restore_and_recovery_plan_specification.md)
- [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md)

Downstream artifacts:

- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)
- [Formal Acceptance and Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

This record should reference the Solution Module Definitions, Technical Design Document, DevOps Guide, Operations & Support Model, Backup, Restore & Recovery Plan, monitoring or audit designs, and relevant release evidence.

## 4. Before You Start

Confirm the following inputs are available before drafting:

- all referenced upstream artifacts exist and are complete or conditionally complete: Technical Design Document, DevOps Guide, Operations & Support Model, Backup, Restore & Recovery Plan, and Deployed Solution
- named Service Owner and Support Owner confirmed with effective dates or transition conditions
- readiness boundary defined (full production handover, limited release, or conditional operational acceptance)
- agreed controlled status values for readiness rows (`ready`, `ready with conditions`, `not ready`)

## 5. How to Draft It

1. **Complete the record identity header** — record the solution name, readiness record ID or version, date, preparer, and readiness boundary statement (see [6.1](#6.1.-record-identity)).
2. **Confirm service and support ownership** — name the Service Owner and Support Owner with effective dates or transition conditions (see [6.2](#6.2.-ownership-confirmation)).
3. **Summarize readiness evidence by area** — confirm which design, administration, support, monitoring, and recovery artifacts exist and note any that are incomplete or conditionally accepted (see [6.3](#6.3.-readiness-evidence-summary)).
4. **Populate the readiness table with status, gaps, and owners** — complete each row with readiness area, evidence reference, controlled status value, gap or condition, owner, and due date where follow-up is required (see [6.4](#6.4.-required-content-for-each-readiness-row)).
5. **Record the formal operational decision** — state the decision outcome, approving authority, decision date, follow-up actions, and any conditions under which operations is accepting responsibility despite open gaps (see [6.5](#6.5.-operational-decision)).

## 6. Minimum Structure

### 6.1. Record Identity

Must include:

- solution or service name
- readiness record ID or version
- date prepared
- prepared by
- statement of the readiness boundary, such as full production handover, limited release, or conditional operational acceptance

This section identifies the formal readiness record.

### 6.2. Ownership Confirmation

Must include:

- named Service Owner
- named Support Owner
- any effective date or transition condition for those responsibilities

This section makes the receiving ownership explicit.

### 6.3. Readiness Evidence Summary

Must include:

- confirmation that required design, administration, support, monitoring, and recovery artifacts exist
- reference to the evidence or authoritative artifacts reviewed
- note of any required artifact, support arrangement, or dependency that is still incomplete or accepted only under condition

This section shows the basis for readiness review.

### 6.4. Required Content for Each Readiness Row

If a readiness table is used, each row must include:

- readiness area
- evidence reference
- status
- gap or condition
- owner
- due date or next review point where follow-up is required

Recommended columns:

| Readiness area | Evidence reference | Status | Gap or condition | Owner | Due date or next review |
| --- | --- | --- | --- | --- | --- |

Use controlled status values such as:

- `ready`
- `ready with conditions`
- `not ready`

This row structure keeps the readiness decision clear and reviewable.

### 6.5. Operational Decision

Must include:

- operational decision outcome
- approving operational authority
- decision date
- follow-up actions if readiness is conditional
- explicit statement of any conditions under which operations is accepting responsibility despite open gaps

This section is the formal handover decision.

## 7. Writing Rules

Keep it short. Include enough detail to show ownership, readiness evidence, material gaps, and the formal operational decision. Link to detailed artifacts instead of copying them.

Keep the following out of this artifact:

- full runbooks
- full design detail
- raw test logs
- repeated copies of every referenced artifact

## 8. Traceability, Ownership, and Review

The Delivery Owner or operational readiness coordinator usually prepares the record. Formal operational acceptance is normally given by the IT Operations / Service Owner or delegated authority.

Minimum traceability expectation:

- readiness rows link to the underlying evidence artifacts
- readiness status values are controlled and consistent
- conditions and follow-up ownership are explicit and visible

Minimum ownership expectation:

- Delivery Owner prepares the record and tracks completion of open conditions.
- Service Owner and Support Owner confirm readiness and operational responsibilities.
- Approving operational authority records the formal decision.

## 9. Maintenance Expectations

Update until the operational decision is final. If acceptance is conditional, track the conditions or issue a superseding version once closed.

## 10. Validation Guide

- Does the record show clearly whether operational ownership is willing to accept the solution?
- Are material readiness gaps or conditions explicit and owned?
- Does the record make the readiness boundary and any condition-based acceptance explicit enough for audit and handover?
- Does it rely on references instead of copying detailed content?
- Is the formal operational decision unambiguous?

If weak, tighten the evidence references and make the operational decision statement more explicit.

## 11. Done When

- Readiness boundary is explicit (full production, limited release, or conditional acceptance).
- Service Owner and Support Owner are named with transition conditions visible.
- Readiness evidence is referenced by area with controlled status values applied to each row.
- Gaps and conditions are owned with due dates for follow-up actions.
- The formal operational decision is recorded by the approving authority.

## 12. What Comes Next

1. Use this record as input to the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md).
2. Reference it in the [Formal Acceptance and Closure Record](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md).
3. Track any open conditions to closure, issuing a superseding version when conditions are met.
4. Keep until closure is formally confirmed.

## 13. Prompt Guide

**Starter prompt:**

```
Draft an Operational Readiness Confirmation Record for this solution.
Show named service and support ownership, what readiness evidence was reviewed, any gaps or conditions that remain, and the formal operational decision.
Keep it concise and table-driven.
```

**Validation prompt:**

```
Review this Operational Readiness Confirmation Record against the following questions:
- Does the record show clearly whether operational ownership is willing to accept the solution?
- Are material readiness gaps or conditions explicit, owned, and dated?
- Is the readiness boundary and any condition-based acceptance explicit enough for audit and handover?
- Does it rely on references to detailed artifacts rather than copying their content?
- Is the formal operational decision unambiguous and attributed to the approving authority?
Flag any section that is missing, vague, or that would prevent a clean handover or audit review.
```

