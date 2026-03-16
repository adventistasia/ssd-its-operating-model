# Solution Modules Specification

## 1. What This Artifact Is For

Solution Modules group related user behaviors and use cases into delivery and acceptance units that people can actually understand.

This artifact answers one simple question:

**How is the approved scope grouped into meaningful user-behavior slices for delivery, validation, and acceptance?**

Use modules to organize approved scope around coherent user outcomes and behaviors. Do not use them to create new scope.

## 2. When to Use It

Use this artifact in Stage 4 after Functional Capabilities are approved.

It is especially useful when:

- the scope is large enough to need clear groupings
- the team wants modules to reflect user journeys or behavior areas
- the team will deliver in waves, releases, or meaningful chunks
- reviewers need to see what will be demonstrated and accepted together

## 3. Before You Start

Make sure you have:

- the approved Functional Capabilities
- a working view of user roles and access expectations
- an early view of the main user behaviors or use cases
- a clear idea of how delivery and acceptance will be grouped
- named owner and reviewer

## 4. How to Draft It

Follow these steps:

1. Read the approved Functional Capabilities, actor model, and early use case ideas.
2. Identify meaningful user behaviors or outcome areas that business reviewers can recognize.
3. Group related use cases and behaviors into modules that can be explained, demonstrated, and accepted as one unit.
3. Assign a stable `SM-###` ID to each module.
4. Name each module in plain language.
5. List the primary users or roles and the planned `UC-###` IDs.
6. Map the module back to the supporting `FC-###` IDs.
7. Check that every approved capability is covered by one or more modules and that every module stays inside the approved capability baseline.

Useful test:

- If the grouping only exists because of team ownership or sprint timing, it is probably not a good module.
- If the grouping reflects a recognizable user outcome or behavior area, it is probably stronger.
- If the grouping can be explained, demonstrated, and accepted as one unit, it is probably a strong module.

## 5. Minimum Structure

### 5.1. Document header

Include:

- initiative or solution name
- version and status
- owner and reviewer
- reference to the approved Functional Capabilities
- short note on how modules will be used in this initiative
- short note confirming that modules are behavior-centered groupings and not new scope definitions

### 5.2. Module summary table

Use a table like this:

| Module ID | Module name | Behavior focus | Primary roles | Planned use cases | Supporting capabilities | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| `SM-001` | Request submission | Lets staff raise and track a new request. | Staff member | `UC-001`, `UC-002` | `FC-001`, `FC-002` | Add only short notes. |

### 5.3. Coverage check

Add a simple mapping table:

| Module ID | Use case or behavior area | Supporting capability IDs | Notes |
| --- | --- | --- | --- |
| `SM-001` | Request submission | `FC-001`, `FC-002` |  |

## 6. Writing Rules

Each module should:

- stay inside approved scope
- group user behavior in a way business reviewers can understand
- help delivery, testing, and acceptance
- be traceable back to approved capabilities even when the module is defined mainly through behaviors and use cases

Keep the following out:

- new capabilities
- detailed use case flows
- task plans
- sprint plans
- technical design detail

## 7. Done When

This artifact is ready when:

- all approved capabilities are covered
- module boundaries are easy to explain
- modules reflect meaningful user behaviors or outcomes
- reviewers can see what will be delivered and accepted together
- the set supports straightforward use case drafting

## 8. What Comes Next

After the modules are stable:

1. write the related behavior using the [Use Case Narratives Specification](use_case_narratives_specification.md)
2. keep the actor model aligned using the [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)
3. use the module structure to plan evidence and acceptance

## 9. Prompt Guide

Starter prompt:

```text
Draft a Solution Modules artifact for Stage 4.
Group related user behaviors and planned use cases into clear delivery and acceptance units.
Assign SM IDs, identify primary roles, list planned UC IDs, map each module back to approved FC IDs, and do not add new scope.
```

Validation prompt:

```text
Check whether any behavior-centered module implies scope that is not present in the approved Functional Capabilities.
```
