# Validation & Evidence Matrix Specification

## 1. What This Artifact Is For

The Validation & Evidence Matrix is a planning and tracking tool that maps approved scope items to validation methods and the evidence needed for acceptance. It ensures that evidence is designed and gathered proactively instead of reconstructed at the end of delivery.

The matrix answers: What must be validated (each FC, SM, and UC)? How will it be validated (test type, demonstration, audit, inspection)? What evidence will count (test result, screenshot, report, log extract)? Who is responsible? What is the current status?

By making evidence design visible in Stage 4, the matrix supports early alignment between delivery and acceptance expectations and reduces later surprises.

Intended readers include the Delivery Owner, QA lead, Acceptance Authority, delivery team, and any compliance or audit reviewer.

## 2. When to Use It

Use this artifact in Stage 4 — Work Definition Details when modules and use cases are being drafted. Identify validation methods and evidence types for each scope item at this stage.

Maintain and update the matrix in Stage 6 — Work Delivery as work is completed and evidence is collected. Use it in Stage 7 — Acceptance, Transition & Closure as part of the acceptance package.

It is especially useful when:

- the initiative contains multiple modules or capabilities that need clear evidence for acceptance
- different stakeholders have different expectations about what counts as sufficient evidence
- evidence must satisfy compliance, audit, or regulatory requirements
- there is a risk that evidence will be forgotten, lost, or misaligned with acceptance criteria

## 3. Stage Fit and Handoffs

**Upstream sources:**

- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md) — the FC-### IDs the matrix maps to
- [Solution Modules Specification](../solution_deliverables/solution_modules_specification.md) — the SM-### IDs
- [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md) — module-level acceptance criteria
- [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md) — UC-### IDs and use case acceptance criteria

**Downstream artifacts:**

- [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md) — evidence collected feeds the deployment record
- [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md) — the completed matrix supports the acceptance package

| Stage | How the matrix is used |
| --- | --- |
| Work Definition Details (Stage 4) | Draft the matrix; define validation methods and evidence types for each scope item |
| Work Delivery (Stage 6) | Update with evidence references as work is completed; track completion status |
| Acceptance, Transition & Closure (Stage 7) | Include in the acceptance package; note deferred or conditional items |

## 4. Before You Start

Before creating the matrix, confirm you have:

- the complete list of approved FC IDs, SM IDs, and UC IDs
- module-level acceptance criteria and use case acceptance criteria
- agreement on validation methods (testing types, demonstrations, inspections, reviews)
- knowledge of regulatory or compliance evidence requirements where applicable
- named individuals responsible for validation and evidence collection

## 5. How to Draft It

1. **List scope items.** Create rows for each Functional Capability, Solution Module, and Use Case. You may group related use cases under one module row for simplicity.
2. **Define validation method.** For each row, specify how the item will be validated (for example: unit test, integration test, system test, demo, inspection, compliance audit).
3. **Specify evidence type.** State what type of evidence will be produced (for example: test result, report, log file, screenshot, demonstration recording, code review record).
4. **Assign owner.** Record who is responsible for performing the validation and collecting the evidence.
5. **Track status.** Use: Planned, In Progress, Complete, Deferred, or N/A. Update during Stage 6 — Work Delivery.
6. **Link to evidence.** As evidence is collected, provide a reference or link to where the evidence is stored (for example: repository path, ticket ID, artifact name).
7. **Review and update regularly** with the delivery team, testers, and Acceptance Authority to ensure evidence requirements are being met.

## 6. Minimum Structure

Use a table like this as a starting point:

| ID (FC/SM/UC) | Description | Validation method | Evidence type | Owner | Status | Evidence reference |
| --- | --- | --- | --- | --- | --- | --- |
| FC-001 | Staff can submit a service request | Integration test; demo | Test result; demo recording | QA lead | Planned | |
| SM-002 | Reporting module | User acceptance test | UAT sign-off | Delivery owner | In progress | |
| UC-005 | Approve request | Peer code review; functional test | Code review record; test result | Developer | Complete | /evidence/uc005_test_result.pdf |

You may include additional columns for priority, risk, or notes as needed.

## 7. Writing Rules

Keep the matrix focused on what is being validated and what evidence proves it. Avoid adding narrative commentary in table cells — use references to external evidence rather than inline summaries.

Keep the following out:

- detailed test scripts or test procedures (these belong in test planning documents)
- narrative descriptions of how testing was performed (reference the evidence instead)
- items not traceable to an approved FC-###, SM-###, or UC-###

## 8. Traceability, Ownership, and Review

The Delivery Owner is accountable for completeness of validation planning. The Acceptance Authority is accountable for confirming adequacy of evidence.

This artifact traces back to the functional capabilities, modules, and use case specifications. It feeds forward to the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) and informs the [Formal Acceptance & Closure Record](formal_acceptance_and_closure_record_specification.md).

Acceptance evidence: completed Validation & Evidence Matrix with references to evidence for each scope item, plus sign-off from the Delivery Owner and Acceptance Authority confirming adequacy of evidence.

## 9. Maintenance Expectations

This is a living document. Update the matrix as validation is completed, evidence is collected, and item statuses change during Stage 6 — Work Delivery.

Keep evidence references and status current so the matrix remains an accurate view of validated and outstanding scope items through to acceptance.

## 10. Done When

The matrix is ready for acceptance review when:

- all approved Functional Capabilities, Solution Modules, and Use Cases have a defined validation method and evidence type
- owners are named for each item
- the matrix is current and reflects the latest delivery state
- evidence references are recorded for all completed items
- deferred or conditional items are clearly marked with rationale and handling instructions
- the Delivery Owner and Acceptance Authority have reviewed and confirmed it

## 11. What Comes Next
2. Resolve any deferred or N/A items with explicit rationale before acceptance.
3. Include the completed matrix in the acceptance package for Stage 7.
4. Reference it in the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) as evidence of validated scope coverage.

## 12. Prompt Guide

### Starter prompt

```
Create a Validation & Evidence Matrix for Work Definition Details (Stage 4).
List each FC, SM, and UC, the planned validation method, the expected evidence type, and the responsible owner.
Use a table format and leave evidence reference blank until Work Delivery (Stage 6).
```

### Validation prompt

```
Check whether every scope item in the Validation & Evidence Matrix has a validation method, evidence type, responsible owner, and that status and evidence references are updated appropriately.
```
