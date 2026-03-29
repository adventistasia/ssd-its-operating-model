# Solution Module Definition Specification

## 1. What This Artifact Is For

The Solution Module Definition is the detailed document for one solution module.

This artifact answers one simple question:

**What exactly will this module deliver, how will it behave, and what will be used to accept it?**

Use this artifact when a module is large enough or important enough to need its own detailed document. It should help both future development work and later operational support.

Practical naming recommendation:

- artifact name: `Solution Module Definition`
- file name pattern: `solution_module_sm_###_<short_name>.md`

Example:

- `solution_module_sm_001_request_submission.md`

## 2. When to Use It

Use this artifact in Stage 4 after the `Solution Modules Register` identifies the module.

It is especially useful when:

- the system is non-trivial
- one module contains several use cases
- reviewers need a module-by-module acceptance view
- development teams will work module by module

## 3. Stage Fit and Handoffs

- Stage 4: create module detail that is ready for build, review, and validation.
- Stage 6: use this artifact as one evidence anchor for what was delivered.
- Stage 7: use this artifact to support the acceptance boundary and acceptance decision.

Upstream sources:

- [Solution Modules Specification](solution_modules_specification.md)
- [Functional Capabilities Specification](functional_capabilities_specification.md)
- [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)

Downstream artifacts:

- [Use Case Narratives Specification](use_case_narratives_specification.md)
- [Deployed Solution Specification](deployed_solution_specification.md)
- [Acceptance Record Specification](acceptance_record_specification.md)
- [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md)

## 4. Before You Start

Make sure you have:

- the related `SM-###` entry in the Solution Modules Register
- the approved supporting `FC-###` IDs
- the relevant user roles and access expectations
- the use cases that belong to the module
- the acceptance focus for the module
- the known support, administration, monitoring, or recovery concerns where relevant

## 5. How to Draft It

Follow these steps:

1. Start with the module ID, name, and behavior focus from the Solution Modules Register.
2. State the module purpose in plain language.
3. List the related roles and supporting `FC-###` IDs.
4. Include the module's use cases or link to them if they sit elsewhere.
5. Write the module-level acceptance criteria.
6. Note supportability, monitoring, administration, and recovery considerations where they matter.
7. Note dependencies, exclusions, assumptions, and open questions that matter.
8. Check that the module stays inside approved scope.

## 6. Minimum Structure

Use this structure:

- Module ID and module name
- Module purpose
- Behavior focus / user outcome
- Related roles
- Supporting `FC-###` IDs
- Included `UC-###` IDs
- Module scope notes and exclusions
- Use case narratives for this module, or links to them
- Module-level acceptance criteria
- Operational and support notes where relevant
- Dependencies and assumptions

Example heading pattern:

- `## SM-001 Request Submission`

## 7. Writing Rules

This artifact should:

- stay centered on one module
- explain the behavior clearly enough for build, walkthrough, testing, and acceptance
- keep capability traceability visible
- keep module acceptance criteria visible
- make support-sensitive design choices visible where operations will need them later

Keep the following out:

- new scope not supported by approved `FC-###` IDs
- unrelated modules
- detailed task planning
- deep technical design that belongs elsewhere

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- module detail references one `SM-###` ID, supporting `FC-###` IDs, and included `UC-###` IDs
- module acceptance criteria are observable and can be linked to evidence in Stage 6 and Stage 7

Minimum ownership expectation:

- Solution lead or analyst owns this artifact's behavior clarity and traceability quality.
- Delivery Owner confirms scope control and review readiness.
- Operational reviewers provide input when module behavior affects supportability.

## 9. Done When

This artifact is ready when:

- the module purpose and boundary are clear
- the included use cases are visible
- the supporting capabilities are visible
- the module acceptance criteria are clear enough to review and test
- reviewers can understand what this module will deliver without reading the whole solution set first

## 10. What Comes Next

Use this artifact to support:

1. walkthroughs and reviews
2. detailed validation and test planning
3. technical and operational readiness documentation
4. delivery evidence and acceptance records

## 11. Prompt Guide

Starter prompt:

```text
Draft a Solution Module Definition for one module.
Use the module ID and behavior focus from the Solution Modules Register, include the related use cases, map the module back to approved FC IDs, and write clear module-level acceptance criteria.
```

Validation prompt:

```text
Check whether this Solution Module Definition stays inside approved scope, clearly explains the module's behavior, and makes module-level acceptance criteria reviewable.
```
