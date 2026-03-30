# Use Case Narratives Specification

## 1. What This Artifact Is For

Use Case Narratives describe how the solution should behave when a user or external actor tries to achieve a specific outcome.

This artifact answers one simple question:

**How does this module help an actor reach a goal, and what must happen when things go right, go differently, or fail?**

Use it to make behavior clear enough for review, design, build, testing, training, audit, and acceptance.

Well-written use cases are:

- goal-oriented rather than screen-oriented
- written from outside the system as a business-facing "black box"
- bounded to approved scope
- detailed enough that another person can understand correct behavior without guessing

## 2. When to Use It

Use this artifact in Stage 4 after Solution Modules are defined.

It is especially useful when:

- user goals and expected outcomes need to be made explicit
- approvals, exception handling, validation rules, or sensitive actions matter
- several roles or systems participate in one business outcome
- testers and reviewers need a shared view of correct behavior

Use cases may be stored in one combined use case document or inside the related `Solution Module Definition`. For non-trivial systems, module-by-module organization is often easier to review and maintain.

## 3. Stage Fit and Handoffs

- Stage 4: define expected business behavior and acceptance-relevant flow detail.
- Stage 6: use the use cases to validate delivered behavior and collect evidence.
- Stage 7: use the use cases as part of the acceptance basis when mapping evidence to approved behavior.

Upstream sources:

- [Functional Capabilities Specification](functional_capabilities_specification.md)
- [Solution Modules Specification](solution_modules_specification.md)
- [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)

Downstream artifacts:

- [Deployed Solution Specification](deployed_solution_specification.md)
- [Acceptance Record Specification](acceptance_record_specification.md)
- [Training and Enablement Materials Specification](../user_adoption_and_change_enablement_deliverables/training_and_enablement_materials_specification.md)

## 4. Before You Start

Make sure you have:

- the related Solution Module
- the related `Solution Module Definition`, if the team is using one document per module
- the approved `FC-###` IDs that the use case must stay within
- the agreed user roles, personas, and access assumptions
- important rules, controls, data sensitivity, and acceptance concerns
- any known open questions that could affect behavior or scope

## 5. How to Draft It

Follow these steps:

1. Pick one module and the related approved capabilities.
2. Name the primary actor as a role, then state the actor's goal in plain language.
3. State the trigger that starts the use case, the preconditions that must already be true, and the postconditions that must hold when the use case ends.
4. State the success outcome and, where useful, the minimum guaranteed state if the use case cannot complete successfully.
5. Write the main flow as numbered actor-system steps that show the normal path to the goal.
6. Keep conditions, failures, and branch logic out of the main flow where possible. Put them in alternate flows instead.
7. Add alternate flows that say what condition causes the branch, which main-flow step they branch from, and whether they rejoin the main flow or end the use case.
8. Add business rules, validations, and access expectations where they materially affect behavior or acceptance. Treat access expectations as business rules for users.
9. Add data processing notes and auditability requirements where traceability or audit matters.
10. Add non-functional requirements where quality, security, privacy, or timing conditions affect acceptance.
11. Finish with clear acceptance criteria that can be observed or evidenced.

Useful tests:

- If the use case reads like a click-by-click screen script, pull it back to business behavior.
- If the preconditions say obvious things such as "the system is available," remove them unless they matter to the reader.
- If an alternate flow does not explain what happens next, finish it so the outcome is clear.
- If it introduces behavior not found in the approved baseline, remove or escalate it.

## 6. Minimum Structure

Use this structure for each use case.

### 6.1. Identification and Scope

Must include:

1. `Use Case ID`: the stable identifier for the use case, such as `UC-001`
2. `Use Case Name`: a short goal-oriented title such as `Submit service request`
3. `Module ID`: the one `SM-###` module this use case belongs to
4. `Related Functional Capabilities`: the approved `FC-###` items this use case supports, each paired with the capability statement or a shortened version of it
5. `Primary Actor`: the role that initiates the use case
6. `Supporting Actors or Systems`: other roles or systems that materially participate

This section anchors the use case to the approved solution structure.

Example values:

```text
Use Case ID: UC-001
Use Case Name: Submit service request
Module ID: SM-001
Related Functional Capabilities:
  FC-001 – Allow staff to submit service requests through a defined channel
  FC-002 – Route submitted requests to the appropriate support queue
Primary Actor: Staff member
Supporting Actors or Systems: Request management system, notification service
```

### 6.2. Goals

Must include:

1. `Actor Goal`: what the primary actor is trying to achieve
2. `Trigger`: what starts the use case
3. `Preconditions`: what must already be true before the use case starts
4. `Postconditions`: what must be true after the use case ends, regardless of outcome
5. `Success Outcome` or `Success Guarantee`: what must be true when the use case completes successfully

May include:

1. `Minimum Guarantee` or `Failure Outcome`: what must still be true if the use case cannot complete successfully

This section distinguishes the actor's goal, the event that starts the use case, the conditions it depends on, and the states it leaves behind.

Example values:

```text
Actor Goal: Submit a valid request and receive confirmation that it is being handled
Trigger: Staff member decides to request support
Preconditions:
- Staff member is authenticated
- Staff member has access to the request channel
Postconditions:
- An audit record exists for the attempt, whether or not it completed
Success Outcome:
- A valid request is recorded, assigned an identifier, and routed for action
Minimum Guarantee:
- No incomplete request is treated as submitted
```

### 6.3. Main Flow

Must include:

1. `Main Flow`: the normal path of behavior, written as numbered steps in business language

Each step should make clear:

- who is acting
- what action is taken
- what meaningful response or state change follows

The main flow should describe the typical successful path with as little branching as practical.

Example values:

```text
Main Flow:
1. Staff member enters the request details.
2. The system checks that required information is present.
3. The system records the request.
4. The system confirms successful submission.
5. The system routes the request to the correct queue.
```

### 6.4. Alternate Flows

Must include:

1. `Alternate Flows`: important variations, failures, rejections, exception handling, or recovery paths

Each alternate flow should say:

- which main-flow step it branches from
- what condition causes the branch
- what the system or actor does next
- whether the use case returns to the main flow or ends

This section is where most ambiguity is removed.

Example values:

```text
Alternate Flows:
- 2a. Required information is missing. The system shows the missing fields and the use case stays with the staff member until the information is completed or the attempt is abandoned.
- 5a. Routing fails. The system records the request, flags it for support follow-up, and ends the use case with manual routing required.
```

### 6.5. Business Rules

Must include where relevant:

1. `Business Rules and Validations`: the checks, rules, or conditions that affect correct behavior
2. `Access Expectations`: who is allowed to perform the action and any access limits, treated as business rules for users

May include where materially relevant:

1. `Open Issues`: unresolved items that affect review or later elaboration

Keep this section behavior-linked. Do not turn it into technical design.

Example values:

```text
Business Rules and Validations:
- Request type must be selected.
- Required fields must be completed.
- Submission time must be recorded.
Access Expectations:
- Only authenticated staff members can submit a request.
- Staff members can view only their own requests unless given a support role.
Open Issues:
- Confirm whether routing fallback should create a support alert automatically.
```

### 6.6. Data Processing and Auditing

Must include where relevant:

1. `Data Processed`: the key data items created, read, updated, or used during the use case
2. `Auditability Requirements`: what must be traceable or recorded for control or review purposes

Keep this section behavior-linked. Do not describe internal data structures or storage schema.

Example values:

```text
Data Processed: Request type, staff identifier, request timestamp, routing destination, submission status.
Auditability Requirements:
- The system records who submitted the request and when.
- The system records the assigned queue or the routing failure state.
```

### 6.7. Non-Functional Requirements

May include where materially relevant:

1. `Non-Functional Requirements`: security, privacy, timing, availability, or other quality conditions that change how the use case is accepted

State only the non-functional conditions that directly affect acceptance of this use case. Keep technical detail out.

Example values:

```text
Non-Functional Requirements:
- Confirmation must be issued immediately after successful submission.
- The request form must be accessible to staff members with assistive technology.
```

### 6.8. Acceptance Criteria

Must include:

1. `Acceptance Criteria`: the observable results that show the use case is working correctly

Should make clear:

- what success looks like
- what important failure or alternate outcomes must also be verified
- what evidence or traceability matters for review, audit, or acceptance

Example values:

```text
Acceptance Criteria:
- A valid request is saved with a unique identifier.
- The staff member receives a confirmation.
- The request is routed to the correct queue or flagged for follow-up when routing fails.
- Submission activity is traceable in the system record.
```

## 7. Writing Rules

Each use case must:

- reference one defined module
- reference approved capabilities only
- describe one actor goal at a useful business level
- stay at business-behavior level and treat the solution as a black box
- distinguish trigger, preconditions, postconditions, success outcome, and alternate flows clearly
- be complete enough that reviewers do not have to guess

In a behavior-centered module model, use cases are the main content that gives the module its shape. They still must map back to approved capabilities.

When the team uses one module document per module, the use case content may sit inside that module document instead of in one separate combined use case file.

Keep the following out:

- technical design
- detailed screen layouts
- API, integration, or database design
- full test scripts
- detailed field-by-field form specifications unless they are essential to the business rule
- new unapproved scope

Useful drafting cautions:

- If a use case is so broad that it spans many loosely related goals, split it.
- If a use case is so narrow that it describes only a single click or UI gesture, raise it back to a meaningful user outcome.
- Use the same role names and access assumptions as the User Roles, Personas & Access Model artifact.

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- each use case maps to one `SM-###` module and one or more `FC-###` IDs
- acceptance criteria can be linked to evidence references during delivery
- role names match the role and access artifact

Minimum ownership expectation:

- Solution lead or analyst owns behavioral clarity.
- Delivery Owner confirms scope boundaries are respected.
- Reviewers and testers confirm the narratives are usable for validation.

## 9. Done When

This artifact is ready when:

- the actor, goal, trigger, postconditions, and outcome are clear
- preconditions are meaningful rather than filler
- the main flow shows the normal path without unnecessary branching
- important alternate flows, business rules, and data processing and auditing needs are visible
- access expectations are stated as business rules and match the agreed role model
- non-functional requirements that affect acceptance are captured
- acceptance criteria are observable
- the use case is traceable to one module and approved capabilities, with capability statements included

## 10. What Comes Next

After use cases are ready:

1. use them to guide design, build, validation, and evidence collection
2. keep them aligned with the [Solution Module Definition Specification](solution_module_definition_specification.md) when module-level detail documents are used
3. keep them aligned with the [User Roles, Personas & Access Model Specification](user_roles_personas_and_access_model_specification.md)
4. keep the live record current in the [Deployed Solution Specification](deployed_solution_specification.md)
5. use them as part of the basis for the [Acceptance Record Specification](acceptance_record_specification.md)

## 11. Prompt Guide

Starter prompt:

```text
Draft a Use Case Narrative for Stage 4.
Use one defined module, approved FC IDs paired with their capability statements, and the required use case structure.
State the actor goal, trigger, preconditions, postconditions, success outcome, main flow, alternate flows, business rules, access expectations, data processing, auditability requirements, non-functional requirements, and observable acceptance criteria.
Keep the writing at business-behavior level. Do not add UI design or unapproved scope.
```

Validation prompts:

```text
Check whether this use case introduces behavior outside the approved Functional Capabilities, leaves the actor goal or success outcome unclear, or mixes technical design into business behavior.
```

```text
Check whether each alternate flow states what triggers it, what happens next, and whether the use case returns to the main flow or ends.
```
