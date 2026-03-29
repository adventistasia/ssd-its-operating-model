# Validation & Evidence Matrix Specification

## 1. What This Artifact Is For

The **Validation & Evidence Matrix** is a planning and tracking tool that maps approved scope items to validation methods and the evidence needed for acceptance. It ensures that evidence is designed and gathered proactively instead of reconstructed at the end of delivery.

The matrix answers questions like:

* **What must be validated?** — each Functional Capability (FC), Solution Module (SM) and Use Case (UC).
* **How will it be validated?** — the test or validation method, such as unit test, integration test, demonstration, audit, or inspection.
* **What evidence will count?** — the kind of artifact (test result, screenshot, report, demonstration video, log extract, etc.).
* **Who is responsible?** — the owner of the validation and the evidence.
* **What is the status?** — planned, in progress, complete, or deferred.

By making evidence design visible in Work Definition Details (Stage 4), the matrix supports early alignment between delivery and acceptance expectations and reduces later surprises.

## 2. When to Use It

Use this artifact in **Work Definition Details (Stage 4)** when modules and use cases are being drafted. Identify validation methods and evidence types for each scope item. Maintain and update the matrix in **Work Delivery (Stage 6)** (Work Delivery) as work is completed and evidence is collected. Use it in **Acceptance, Transition & Closure (Stage 7)** (Acceptance) as part of the acceptance package.

It is especially useful when:

* The initiative contains multiple modules or capabilities that need clear evidence for acceptance.
* Different stakeholders have different expectations about what counts as sufficient evidence.
* Evidence must satisfy compliance, audit or regulatory requirements.
* There is a risk that evidence will be forgotten, lost or misaligned with acceptance criteria.

## 3. Stage Fit and Handoffs

* **Work Definition Details (Stage 4):** Draft the matrix using the list of approved Functional Capabilities, modules and use cases. Define the validation method and expected evidence type for each entry.
* **Work Delivery (Stage 6):** Update the matrix with references to actual evidence (test results, screenshots, logs, demonstrations, etc.) as work is completed. Track completion status.
* **Acceptance, Transition & Closure (Stage 7):** Include the matrix in the Acceptance Record package to show that each scope item has evidence. Note any deferred or conditional items.

Upstream sources:

* [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)
* [Solution Modules Specification](../solution_deliverables/solution_modules_specification.md)
* [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md)
* [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md)

Downstream artifacts:

* [Deployed Solution Specification](../solution_deliverables/deployed_solution_specification.md)
* [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md)

## 4. Before You Start

Make sure you have:

* The complete list of approved FC IDs, SM IDs and UC IDs.
* Module-level acceptance criteria and use case acceptance criteria.
* Agreement on validation methods (testing types, demonstrations, inspections, reviews).
* Knowledge of regulatory or compliance evidence requirements where applicable.
* Named individuals responsible for validation and evidence collection.

## 5. How to Draft It

1. **List scope items.** Create rows for each Functional Capability, Solution Module and Use Case. You may group related use cases under one module row for simplicity.
2. **Define validation method.** For each row, specify how the item will be validated (e.g. unit test, integration test, system test, demo, inspection, compliance audit).
3. **Specify evidence type.** State what type of evidence will be produced (e.g. test result, report, log file, screenshot, demonstration recording, code review record).
4. **Assign owner.** Record who is responsible for performing the validation and collecting the evidence.
5. **Track status.** Define status values such as Planned, In Progress, Complete, Deferred or N/A. Update these during Work Delivery (Stage 6).
6. **Link to evidence.** As evidence is collected, provide a reference or link to where the evidence is stored (e.g. repository path, ticket ID, artifact name).
7. **Review and update.** Regularly review the matrix with the delivery team, testers, and Acceptance Authority to ensure evidence requirements are being met.

## 6. Minimum Structure

Use a table like this as a starting point:

| ID (FC/SM/UC) | Description | Validation method | Evidence type | Owner | Status | Evidence reference |
| --- | --- | --- | --- | --- | --- | --- |
| FC-001 | Staff can submit a service request | Integration test; demo | Test result; demo recording | QA lead | Planned | |
| SM-002 | Reporting module | User acceptance test | UAT sign-off | Delivery owner | In progress | |
| UC-005 | Approve request | Peer code review; functional test | Code review record; test result | Developer | Complete | /evidence/uc005_test_result.pdf |

You may include additional columns for priority, risk, or notes as needed.

## 7. Writing Rules

- Keep evidence types specific. "Test report" or "UAT sign-off email" is useful; "document" is not. The acceptance authority needs to know exactly what to look for.
- Do not preemptively defer items without stating a reason. Mark deferred items with a rationale and a target date or condition for resolution.
- Align the validation method with acceptance authority expectations. If the acceptance authority expects a formal UAT sign-off, a developer unit test alone is not sufficient — agree early and make the expectation explicit in the matrix.
- Make status visible to both delivery and acceptance teams. The matrix should be readable by non-technical reviewers, not only the QA lead or developer.
- Evidence references should point to the actual stored artifact — a path, ticket ID, or repository link — not just say "TBD." Items marked complete with no evidence reference are not complete.

## 8. Traceability and Ownership Minimum

The Delivery Owner is accountable for ensuring the matrix is maintained and reflects current evidence status throughout delivery.

The Acceptance Authority is accountable for confirming that evidence is adequate at the acceptance stage.

This matrix links directly to:

* [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md), [Solution Module Definition Specification](../solution_deliverables/solution_module_definition_specification.md), and [Use Case Narratives Specification](../solution_deliverables/use_case_narratives_specification.md) — the scope items that require validation
* [Acceptance Record Specification](../solution_deliverables/acceptance_record_specification.md) — the matrix is included as part of the acceptance evidence package

Acceptance evidence: the completed matrix with references to evidence for each scope item, plus sign-off from the Delivery Owner and Acceptance Authority confirming adequacy of evidence.

## 9. Done When

The matrix is adequate when:

- all approved Functional Capabilities, modules and use cases have a defined validation method and evidence type
- each row has a named owner responsible for validation and evidence collection
- completed items have an evidence reference pointing to the actual stored artifact, not a placeholder
- deferred or conditional items are explicitly marked with a rationale and a target resolution condition or date
- the Delivery Owner and Acceptance Authority have reviewed and confirmed that the evidence is sufficient for acceptance

## 10. What Comes Next

After the matrix is complete and evidence is collected:

1. include the matrix as part of the acceptance evidence package in the [Acceptance Record](../solution_deliverables/acceptance_record_specification.md) to confirm that each scope item has evidence
2. carry any deferred or conditional items forward into the closure record with explicit conditions for resolution
3. use the evidence references to support post-implementation audits, compliance reviews, or operational handover documentation
4. archive the completed matrix as part of the permanent initiative record alongside the deployed solution artifacts

## 11. Prompt Guide

Starter prompt:

```text
Create a Validation & Evidence Matrix for Work Definition Details (Stage 4).
List each FC, SM and UC, the planned validation method, the expected evidence type, and the responsible owner.
Use a table format and leave evidence reference blank until Work Delivery (Stage 6).
```

Validation prompt:

```text
Check whether every scope item in the Validation & Evidence Matrix has a validation method, evidence type, responsible owner, and that status and evidence references are updated appropriately.
```
