# Use Case Narratives Specification

## 1. What This Artifact Is For

Use Case Narratives describe how the solution should behave from the user's point of view.

This artifact answers one simple question:

**How does this module work when a user tries to achieve an outcome?**

Use it to make behavior clear enough for walkthroughs, build, testing, and acceptance.

## 2. When to Use It

Use this artifact in Stage 4 after Solution Modules are defined.

It is especially useful when:

- user behavior could be misunderstood
- approvals, exceptions, or sensitive actions matter
- testers and reviewers need a shared view of correct behavior

## 3. Before You Start

Make sure you have:

- the related Solution Module
- the approved `FC-###` IDs that the use case must stay within
- the relevant user roles and access expectations
- important rules, controls, and acceptance concerns

## 4. How to Draft It

Follow these steps:

1. Pick one module and the related approved capabilities.
2. Identify the primary actor and any supporting actors or systems.
3. State the trigger.
4. State the intended outcome.
5. Write the main flow in business language.
6. Add alternate paths and exception paths where they matter.
7. Add business rules, access expectations, and audit notes where relevant.
8. Finish with clear acceptance criteria.

Useful test:

- If the use case reads like screen-click instructions, pull it back to business behavior.
- If it introduces behavior not found in the approved baseline, remove or escalate it.

## 5. Minimum Structure

Use this structure for each use case:

- Use Case ID: `UC-###`
- Use case name
- Module ID: one `SM-###`
- Related Functional Capabilities: one or more `FC-###`
- Primary actor
- Supporting actors or systems
- Trigger
- Intended outcome
- Preconditions
- Main flow
- Alternate and exception paths
- Business rules and validations
- Access expectations
- Auditability requirements
- Acceptance criteria

## 6. Writing Rules

Each use case must:

- reference one defined module
- reference approved capabilities only
- stay at business-behavior level
- be complete enough that reviewers do not have to guess

In a behavior-centered module model, use cases are the main content that gives the module its shape. They still must map back to approved capabilities.

Keep the following out:

- technical design
- detailed screen layouts
- API or database design
- full test scripts
- new unapproved scope

## 7. Done When

This artifact is ready when:

- the actor, trigger, outcome, and flow are clear
- important alternate paths and rules are visible
- acceptance criteria are observable
- the use case is traceable to one module and approved capabilities

## 8. What Comes Next

After use cases are ready:

1. use them to guide design, build, validation, and evidence collection
2. keep the live record current in the [Deployed Solution Specification](deployed_solution_specification.md)
3. use them as part of the basis for the [Acceptance Record Specification](acceptance_record_specification.md)

## 9. Prompt Guide

Starter prompt:

```text
Draft a Use Case Narrative for Stage 4.
Use one defined module, approved FC IDs, and the required use case structure.
Keep the writing at business-behavior level and make the acceptance criteria observable.
```

Validation prompt:

```text
Check whether this use case introduces behavior outside the approved Functional Capabilities or leaves key behavior too vague to validate.
```
