# Functional Capabilities Specification

## 1. What This Artifact Is For

Functional Capabilities define the approved business abilities the solution must provide.

This is the scope baseline for solution design. It answers one simple question:

**What must the solution be able to do?**

Use this artifact to make scope clear before the team starts detailed structuring, design, build, testing, and acceptance.

Functional Capabilities remain the approved scope baseline even when later Solution Modules are grouped mainly around user behaviors and use cases.

## 2. When to Use It

Use this artifact in Stage 2 when solution behavior is in scope and you need an approval-level baseline.

It should be based on the approved Stage 2 definition baseline, normally the Initiative Definition Document or a Work Brief for small governed work.

It is especially useful when:

- more than one stakeholder needs to agree on scope
- the initiative needs formal acceptance later
- the team needs stable IDs for traceability

## 3. Stage Fit and Handoffs

- Stage 2: use this artifact to define the approved solution scope baseline.
- Stage 3: use this artifact as part of the authorization basis.
- Stage 4 onward: treat this artifact as the scope control reference for modules, use cases, design, delivery evidence, and acceptance.

Upstream source:

- [Initiative Definition Document specification](../governance_and_control_deliverables/initiative_definition_document_specification.md)

Downstream artifacts:

- [Solution Modules Specification](solution_modules_specification.md)
- [Use Case Narratives Specification](use_case_narratives_specification.md)
- [Technical Design Document Specification](../operational_readiness_deliverables/technical_design_document_specification.md)
- [Acceptance Record Specification](acceptance_record_specification.md)

## 4. Before You Start

Make sure you have:

- the approved initiative objective
- in-scope and out-of-scope boundaries
- named owner and reviewer
- known exclusions, assumptions, or dependencies that affect scope understanding

If any of these are missing, treat the draft as a working draft only.

## 5. How to Draft It

Follow these steps:

1. Start with the approved outcome and scope notes.
2. Split the scope into individual business abilities.
3. Write one capability statement for each business ability.
4. Assign a stable `FC-###` ID to each capability.
5. Add a short value note so readers know why the capability matters.
6. Remove wording that sounds like workflow, screen steps, or technical design.
7. Review for overlap, duplication, and hidden new scope.

Useful test:

- If the statement reads like a user journey, move that detail to a Use Case Narrative.
- If the statement reads like design or implementation, remove it.

## 6. Minimum Structure

### 6.1. Document header

Include:

- initiative or solution name
- version and status
- owner and reviewer
- reference to the Initiative Definition Document or approved scope source
- short statement of the scope boundary this baseline controls

### 6.2. Scope notes

Include:

- short outcome statement
- in-scope summary
- out-of-scope summary
- material exclusions, assumptions, or dependencies

### 6.3. Capability table

Use a simple table like this:

| Capability ID | Capability statement | Business value | Primary role or beneficiary | Notes |
| --- | --- | --- | --- | --- |
| `FC-001` | Staff can submit a service request. | Creates a controlled intake path for support demand. | Staff member | Keep notes short. |

## 7. Writing Rules

Each capability should be:

- one business ability
- easy to understand on its own
- inside the approved scope boundary
- stable enough to reference later

Keep the following out:

- workflow sequences
- detailed business rules
- screen designs
- technical architecture
- test scripts
- backlog items

## 8. Traceability, Ownership, and Review

Each capability entry should be traceable forward to at least one downstream behavior artifact.

Minimum ownership expectations:

- Delivery Owner confirms this artifact stays inside approved scope.
- Outcome Owner or delegate confirms the capability statements still reflect intended outcomes.
- Acceptance Authority for the solution domain should be known by the end of Stage 2, even if acceptance occurs later.

## 9. Done When

This artifact is ready when:

- each capability is clear and atomic
- IDs are assigned and stable
- business readers and delivery readers understand the scope the same way
- exclusions are visible
- no detailed design has leaked in

## 10. What Comes Next

After this baseline is approved:

1. clarify the actor model in the [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)
2. group the approved scope into behavior-centered modules using the [Solution Modules Specification](solution_modules_specification.md)
3. write one detailed module document per non-trivial module using the [Solution Module Definition Specification](solution_module_definition_specification.md)
4. describe behavior using the [Use Case Narratives Specification](use_case_narratives_specification.md)

## 11. Prompt Guide

Starter prompt:

```text
Draft a Functional Capabilities artifact for Stage 2.
Rewrite the approved scope as business abilities with stable FC IDs and short value notes.
Keep the entries atomic and free of workflow, design, and implementation detail.
```

Validation prompt:

```text
Check whether any capability statement includes workflow, technical design, or hidden new scope.
```
