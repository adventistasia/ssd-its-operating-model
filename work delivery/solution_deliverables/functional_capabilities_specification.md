# Functional Capabilities Specification

## 1. What This Artifact Is For

Functional Capabilities define the approved business abilities the solution must provide.

This is the scope baseline for solution design. It answers one simple question:

**What must the solution be able to do?**

Use this artifact to make scope clear before the team starts detailed structuring, design, build, testing, and acceptance.

Functional Capabilities remain the approved scope baseline even when later Solution Modules are grouped mainly around user behaviors and use cases.

## 2. When to Use It

Use this artifact in Stage 2 when solution behavior is in scope and you need an approval-level baseline.

It is especially useful when:

- more than one stakeholder needs to agree on scope
- the initiative needs formal acceptance later
- the team needs stable IDs for traceability

## 3. Before You Start

Make sure you have:

- the approved initiative objective
- in-scope and out-of-scope boundaries
- named owner and reviewer
- known exclusions, assumptions, or dependencies that affect scope understanding

If any of these are missing, treat the draft as a working draft only.

## 4. How to Draft It

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

## 5. Minimum Structure

### 5.1. Document header

Include:

- initiative or solution name
- version and status
- owner and reviewer
- reference to the Initiative Definition Document or approved scope source
- short statement of the scope boundary this baseline controls

### 5.2. Scope notes

Include:

- short outcome statement
- in-scope summary
- out-of-scope summary
- material exclusions, assumptions, or dependencies

### 5.3. Capability table

Use a simple table like this:

| Capability ID | Capability statement | Business value | Primary role or beneficiary | Notes |
| --- | --- | --- | --- | --- |
| `FC-001` | Staff can submit a service request. | Creates a controlled intake path for support demand. | Staff member | Keep notes short. |

## 6. Writing Rules

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

## 7. Done When

This artifact is ready when:

- each capability is clear and atomic
- IDs are assigned and stable
- business readers and delivery readers understand the scope the same way
- exclusions are visible
- no detailed design has leaked in

## 8. What Comes Next

After this baseline is approved:

1. clarify the actor model in the [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)
2. group the approved scope into behavior-centered modules using the [Solution Modules Specification](solution_modules_specification.md)
3. describe behavior using the [Use Case Narratives Specification](use_case_narratives_specification.md)

## 9. Prompt Guide

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
