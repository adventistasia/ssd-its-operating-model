# Solution Modules Specification

## 1. What This Artifact Is For

This specification describes the overall solution-module overview document.

This artifact answers one simple question:

**How is the approved scope grouped into meaningful user-behavior slices for delivery, validation, and acceptance?**

Use modules to organize approved scope around coherent user outcomes and behaviors. Do not use them to create new scope.

A key part of drafting the module list is deciding the behavior focus of each module. The module list is not only a list of names. It is the working view that defines what user-behavior area each module is meant to cover.

Practical naming recommendation:

- call the overall document the `Solution Modules Register`
- call each detailed module document a `Solution Module Definition`

This keeps the overview and the per-module detail clearly separate.

## 2. When to Use It

Use this artifact in Stage 4 after Functional Capabilities are approved.

It is especially useful when:

- the scope is large enough to need clear groupings
- the team wants modules to reflect user journeys or behavior areas
- the team will deliver in waves, releases, or meaningful chunks
- reviewers need to see what will be demonstrated and accepted together

For non-trivial systems, use this as the register that lists all modules, then create one `Solution Module Definition` for each module.

## 3. Stage Fit and Handoffs

- Stage 4: create the module register as the behavior-centered structure for approved scope.
- Stage 5: use modules to organize delivery sequencing and acceptance-readiness tracking.
- Stage 6 and Stage 7: use modules as the evidence and acceptance grouping reference.

Upstream sources:

- [Functional Capabilities Specification](functional_capabilities_specification.md)
- [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)

Downstream artifacts:

- [Solution Module Definition Specification](solution_module_definition_specification.md)
- [Use Case Narratives Specification](use_case_narratives_specification.md)
- [Deployed Solution Specification](deployed_solution_specification.md)
- [Acceptance Record Specification](acceptance_record_specification.md)

## 4. Before You Start

Make sure you have:

- the approved Functional Capabilities
- a working view of user roles and access expectations
- an early view of the main user behaviors or use cases
- a clear idea of how delivery and acceptance will be grouped
- named owner and reviewer

## 5. How to Draft It

Follow these steps:

1. Read the approved Functional Capabilities, actor model, and early use case ideas.
2. Identify meaningful user behaviors or outcome areas that business reviewers can recognize.
3. Decide the behavior focus for each proposed module.
4. Group related use cases and behaviors into modules that can be explained, demonstrated, and accepted as one unit.
5. Assign a stable `SM-###` ID to each module.
6. Name each module in plain language.
7. List the primary users or roles and the planned `UC-###` IDs.
8. Map the module back to the supporting `FC-###` IDs.
9. Create one `Solution Module Definition` for each non-trivial module.
10. Check that every approved capability is covered by one or more modules and that every module stays inside the approved capability baseline.

Useful test:

- If the grouping only exists because of team ownership or sprint timing, it is probably not a good module.
- If the grouping reflects a recognizable user outcome or behavior area, it is probably stronger.
- If the grouping can be explained, demonstrated, and accepted as one unit, it is probably a strong module.

## 6. Minimum Structure

### 6.1. Document header

Include:

- initiative or solution name
- version and status
- owner and reviewer
- reference to the approved Functional Capabilities
- short note on how modules will be used in this initiative
- short note confirming that modules are behavior-centered groupings and not new scope definitions
- short note confirming whether detailed module content will be held in separate `Solution Module Definition` documents

### 6.2. Module summary table

Use a table like this:

| Module ID | Module name        | Behavior focus                            | Primary roles | Planned use cases  | Supporting capabilities | Notes                 |
| --------- | ------------------ | ----------------------------------------- | ------------- | ------------------ | ----------------------- | --------------------- |
| `SM-001`  | Request submission | Lets staff raise and track a new request. | Staff member  | `UC-001`, `UC-002` | `FC-001`, `FC-002`      | Add only short notes. |

The `Behavior focus` field is important. When drafting the module list, the team should decide and state the behavior focus of each module clearly enough that readers can understand what kind of user outcome or activity the module is meant to cover.

### 6.3. Coverage check

Add a simple mapping table:

| Module ID | Use case or behavior area | Supporting capability IDs | Notes |
| --- | --- | --- | --- |
| `SM-001` | Request submission | `FC-001`, `FC-002` |  |

### 6.4. Linked module detail set

For non-trivial systems, include or reference a detail set such as:

| Module ID | Module detail document | Status | Notes |
| --- | --- | --- | --- |
| `SM-001` | `solution_module_sm_001_request_submission.md` | draft | Holds use cases and module acceptance criteria |

## 7. Writing Rules

Each module should:

- stay inside approved scope
- group user behavior in a way business reviewers can understand
- help delivery, testing, and acceptance
- be traceable back to approved capabilities even when the module is defined mainly through behaviors and use cases

The `Solution Modules Register` should stay concise. Put the deeper explanation, use cases, and module acceptance criteria into the related `Solution Module Definition`.

Keep the following out:

- new capabilities
- detailed use case flows
- task plans
- sprint plans
- technical design detail

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- every `SM-###` entry maps to one or more `FC-###` IDs
- planned `UC-###` IDs are visible for each module
- each non-trivial module links to one detailed module definition

Minimum ownership expectation:

- Delivery Owner is accountable for scope alignment and stage-control use.
- Solution lead or analyst owns module quality and behavior clarity.
- Acceptance Authority should be known for each module or module grouping before delivery starts.

## 9. Done When

This artifact is ready when:

- all approved capabilities are covered
- module boundaries are easy to explain
- modules reflect meaningful user behaviors or outcomes
- the behavior focus of each module is explicit and understandable
- reviewers can see what will be delivered and accepted together
- the set supports straightforward use case drafting
- each non-trivial module has a linked `Solution Module Definition`

## 10. What Comes Next

After the modules are stable:

1. write the detailed module documents using the [Solution Module Definition Specification](solution_module_definition_specification.md)
2. write the related behavior using the [Use Case Narratives Specification](use_case_narratives_specification.md)
3. keep the actor model aligned using the [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)
4. use the module structure to plan evidence and acceptance

## 11. Prompt Guide

Starter prompt:

```text
Draft a Solution Modules artifact for Stage 4.
Group related user behaviors and planned use cases into clear delivery and acceptance units.
Produce a concise Solution Modules Register: assign SM IDs, identify primary roles, list planned UC IDs, map each module back to approved FC IDs, and do not add new scope.
```

Validation prompt:

```text
Check whether any behavior-centered module implies scope that is not present in the approved Functional Capabilities.
```
