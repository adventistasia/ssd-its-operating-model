# Solution Design Process

## Related Documents

- [Work Delivery Framework](work_delivery_framework.md)
- [Standard Deliverables Guide](standard_deliverables_guide.md)
- [AI-Assisted Authoring Standard](ai_assisted_authoring_standard.md)
- [Functional Capabilities Specification](solution_deliverables/functional_capabilities_specification.md)
- [Solution Modules Specification](solution_deliverables/solution_modules_specification.md)
- [Use Case Narratives Specification](solution_deliverables/use_case_narratives_specification.md)
- [User Roles, Personas & Access Model Specification](solution_deliverables/user_roles_personas_and_access_model_specification.md)
- [Deployed Solution Specification](solution_deliverables/deployed_solution_specification.md)
- [Acceptance Record Specification](solution_deliverables/acceptance_record_specification.md)
- [Delivery Roadmap Specification](governance_and_control_deliverables/delivery_roadmap_specification.md)
- [Delivery Charter Specification](governance_and_control_deliverables/delivery_charter_specification.md)

## Quick Start

Use this guide when your initiative includes new or changed solution behavior and you need a simple, governed path from approved scope to formal acceptance.

In this guide, stage references mean stages in the Work Delivery Framework. You can still use this process as a practical solution-design guide even if your team is not applying the full framework strictly. In that case, use the stages as a helpful sequence and control check, not as a hard dependency.

This guide is mainly for:

- Delivery Owners and project managers
- analysts and solution leads
- developers and testers
- reviewers and Acceptance Authorities

If you are new to the process, follow this order:

1. In Stage 2, define the approved scope in [Functional Capabilities](solution_deliverables/functional_capabilities_specification.md).
2. In Stage 4, clarify actors in the [User Roles, Personas & Access Model](solution_deliverables/user_roles_personas_and_access_model_specification.md), group the scope into behavior-centered [Solution Modules](solution_deliverables/solution_modules_specification.md), and describe behavior in [Use Case Narratives](solution_deliverables/use_case_narratives_specification.md).
3. In Stage 6, record what is actually live in the [Deployed Solution](solution_deliverables/deployed_solution_specification.md) and gather evidence.
4. In Stage 7, prepare the [Acceptance Record](solution_deliverables/acceptance_record_specification.md) and get an explicit acceptance decision.

What to produce by stage:

| Stage | Main solution deliverables |
| --- | --- |
| Stage 2 - Work Definition | Functional Capabilities |
| Stage 4 - Work Definition Details | User Roles, Personas & Access Model, Solution Modules, Use Case Narratives |
| Stage 6 - Work Delivery | Deployed Solution, linked evidence, related operational artifacts as needed |
| Stage 7 - Acceptance, Transition & Closure | Acceptance Record and final acceptance decision |

What not to do:

- do not add new scope in modules, use cases, or design notes
- do not turn Stage 2 scope into detailed design too early
- do not treat working drafts as approved baselines
- do not wait until the end to reconstruct evidence
- do not mark anything accepted without the named human authority

## 1. Purpose

This document is the practical operating guide for solution design inside the Work Delivery Framework.

It shows teams how to move from approved scope to structured behavior, delivery evidence, and formal acceptance in a way that is easy to follow and easy to review.

## 2. Where This Process Fits

This process works inside the Work Delivery Framework. In this document, stage references refer to stages in the Work Delivery Framework. It does not replace stage decisions or governance controls.

The process can still be used outside strict Work Delivery Framework adoption. When teams use it that way, the stages should be read as practical checkpoints for scope, structure, evidence, and acceptance rather than as mandatory framework gates.

| Stage | What solution design is doing |
| --- | --- |
| Stage 2 | Define the approval-level solution scope |
| Stage 4 | Turn approved scope into delivery-ready, behavior-centered structure and behavior |
| Stage 5 | Use the Delivery Charter and Delivery Roadmap to mobilize controlled execution |
| Stage 6 | Implement, validate, and record evidence |
| Stage 7 | Present the acceptance package and get a clear decision |

Coordination artifacts matter here:

- the [Delivery Roadmap](governance_and_control_deliverables/delivery_roadmap_specification.md) shows when solution work, validation, and acceptance checkpoints will happen
- the [Delivery Charter](governance_and_control_deliverables/delivery_charter_specification.md) shows how the team will operate, escalate, and manage acceptance readiness

These artifacts support the process. They do not replace solution scope, behavior, traceability, or acceptance controls.

## 3. Who Does What

| Role | What to focus on in this guide |
| --- | --- |
| Delivery Owner | Keep the artifact set moving, controlled, owned, and ready for stage reviews |
| Project Manager | Coordinate review cycles, version control, roadmap timing, follow-up actions, and evidence readiness |
| Solution Lead / Analyst | Make scope, module boundaries, roles, and behavior clear enough to build and validate |
| Developer / Tester | Build and validate only what traces back to approved scope and documented behavior |
| Reviewer / SME | Check that the content is correct, practical, and still inside scope |
| Acceptance Authority | Decide based on visible scope, evidence, open conditions, and readiness for use |

Simple usage guidance:

- IT managers should use this guide to check that scope, ownership, and acceptance decisions are visible.
- Delivery Owners and PMs should use it to keep drafting, review, evidence, and handoff in the right order.
- Analysts and solution leads should use it to write the artifacts in sequence without mixing stages.
- Developers and testers should use it to confirm what behavior is approved and what evidence is needed.

## 4. Before You Start

Before drafting a governed solution artifact, make sure you have at least:

- a clear objective
- the current stage
- the in-scope and out-of-scope boundary
- the named owner and reviewer
- the IDs already assigned, or the ID pattern you will use
- the acceptance focus or validation intent

If any of these are missing, you can still draft a working document, but label it clearly as a working draft and do not treat it as controlled or decision-ready.

## 5. Step Summary

Use this table as the day-to-day entry point.

| Step | Minimum inputs | Required outputs | Completion check | Accountable owner |
| --- | --- | --- | --- | --- |
| 1. Define authorized scope | approved initiative intent, scope boundary, owner, reviewer, acceptance focus | Functional Capabilities | scope is clear, IDs are stable, no design detail added | Delivery Owner with Solution Lead / Analyst |
| 2. Structure the solution | approved Functional Capabilities, user context, business rules, review inputs | User Roles, Personas & Access Model, Solution Modules, Use Case Narratives | every module and use case traces to approved capabilities, actors are clear, modules reflect meaningful behaviors, no new scope added | Delivery Owner with Solution Lead / Analyst |
| 3. Implement and evidence | approved design set, test and evidence approach, delivery roadmap, operational inputs | Deployed Solution, linked evidence, related delivery and operational records | delivered behavior can be traced back to approved scope and supported with evidence | Delivery Owner with delivery and operational leads |
| 4. Prepare for formal acceptance | evidence, open issues, deployment status, operational handoff status | Acceptance Record and acceptance-ready package | acceptance authority can see what is being accepted, on what basis, and under what conditions | Delivery Owner with Acceptance Authority |

## 6. Guided Workflow

### 6.1. Step 1 - Define Authorized Scope

Use this step in Stage 2.

Goal:
State clearly what the solution must be able to do before the team starts detailed design.

Use these specs:

- [Functional Capabilities Specification](solution_deliverables/functional_capabilities_specification.md)

Do this:

1. Start from the approved initiative outcome, scope boundary, and exclusions.
2. Write one Functional Capability per approved business ability.
3. Assign stable `FC-###` IDs.
4. Remove workflow detail, screen detail, and technical design.
5. Review for overlap, ambiguity, and hidden scope growth.

Produce:

- Functional Capabilities

Do:

- keep statements short and business-focused
- make exclusions visible
- keep IDs stable once assigned

Do not:

- write use case flows
- group by sprint, team, or system layer
- add technical design or test evidence

Step 1 is done when:

- the approved scope is understandable to business and delivery readers
- each capability is atomic enough to trace later
- the owner and reviewer are named

### 6.2. Step 2 - Structure the Solution

Use this step in Stage 4.

Goal:
Turn approved scope into delivery-ready, behavior-centered structure and reviewable behavior without expanding scope.

Use these specs:

- [User Roles, Personas & Access Model Specification](solution_deliverables/user_roles_personas_and_access_model_specification.md)
- [Solution Modules Specification](solution_deliverables/solution_modules_specification.md)
- [Use Case Narratives Specification](solution_deliverables/use_case_narratives_specification.md)

Do this in order:

1. Confirm who the users are and what boundaries matter.
2. Identify meaningful user outcomes, behavior areas, or use case clusters.
3. Group those behaviors into Solution Modules that can be explained, validated, and accepted as meaningful units.
4. Write Use Case Narratives that show how each module behaves.
5. Check that every use case references a module and approved capability IDs, and that every module maps back to approved capabilities.
6. Remove anything that introduces behavior not covered by the approved baseline.

Produce:

- User Roles, Personas & Access Model
- Solution Modules
- Use Case Narratives

Do:

- use actors and access expectations consistently
- keep module boundaries easy to explain in user terms
- make acceptance criteria observable

Do not:

- turn modules into task plans
- turn use cases into UI scripts or technical specs
- use personas to add hidden scope
- let behavior grouping quietly replace capability traceability

Step 2 is done when:

- every module maps back to approved `FC-###` IDs even when the module is mainly defined by behaviors or use cases
- every use case references one `SM-###` and one or more `FC-###` IDs
- reviewers can understand expected behavior without guessing

### 6.3. Step 3 - Implement and Evidence

Use this step in Stage 6.

Goal:
Show what was delivered, what is live, and what evidence proves the delivered behavior stays inside approved scope.

Use these specs:

- [Deployed Solution Specification](solution_deliverables/deployed_solution_specification.md)
- related operational and technical specs when design, support, deployment, or recovery records are required

Do this:

1. Build and validate only what is approved or formally changed.
2. Collect evidence as work is completed.
3. Record what is actually live, where it is live, and under what conditions.
4. Link evidence back to capabilities, modules, and use cases where appropriate.
5. Confirm operational ownership and support readiness for what is going live.

Produce:

- Deployed Solution
- linked validation and deployment evidence
- related technical or operational records where required

Do:

- keep evidence attributable and reviewable
- note any phased, deferred, or conditional live scope
- make support conditions visible

Do not:

- invent evidence
- hide defects or conditions in narrative text
- claim that live scope is larger than what was approved

Step 3 is done when:

- evidence exists for what is claimed as delivered
- the live boundary is clear
- support and handoff expectations are visible where required

### 6.4. Step 4 - Prepare for Formal Acceptance

Use this step in Stage 7.

Goal:
Give the Acceptance Authority a clean, reviewable, evidence-based package for a clear decision.

Use these specs:

- [Acceptance Record Specification](solution_deliverables/acceptance_record_specification.md)

Do this:

1. Define the acceptance boundary clearly.
2. List what was reviewed and the evidence used.
3. Show whether delivered behavior stayed within approved scope.
4. Make conditions, exclusions, deferred items, and open issues visible.
5. Record the named authority, date, and decision outcome.

Produce:

- Acceptance Record
- acceptance-ready package with linked evidence

Do:

- keep the record concise
- use controlled statuses
- state conditions plainly

Do not:

- bury open items in notes
- present conditional acceptance as full acceptance
- approve on behalf of the named authority

Step 4 is done when:

- the acceptance basis is clear
- the evidence trail is reviewable
- the Acceptance Authority knows exactly what they are being asked to accept

## 7. How the Artifacts Fit Together

Use this traceability path throughout the process:

`Initiative Definition -> Functional Capabilities -> User Roles -> Behavior-Centered Solution Modules -> Use Case Narratives -> Delivery Evidence / Deployed Solution -> Acceptance Record`

Practical reading order for first-time practitioners:

1. Read this guide.
2. Draft [Functional Capabilities](solution_deliverables/functional_capabilities_specification.md).
3. Draft [User Roles, Personas & Access Model](solution_deliverables/user_roles_personas_and_access_model_specification.md).
4. Draft [Solution Modules](solution_deliverables/solution_modules_specification.md).
5. Draft [Use Case Narratives](solution_deliverables/use_case_narratives_specification.md).
6. During delivery, maintain the [Deployed Solution](solution_deliverables/deployed_solution_specification.md).
7. At acceptance time, prepare the [Acceptance Record](solution_deliverables/acceptance_record_specification.md).

## 8. AI-Assisted Authoring Workflow

When AI is helping with solution artifacts, use this simple loop:

1. Human states the artifact, stage, scope boundary, IDs, and review intent.
2. AI drafts only within that boundary.
3. Human reviews for scope, clarity, and traceability.
4. AI revises using explicit comments.
5. Human validates the result against the step checks in this guide.
6. The named owner accepts the artifact for use.
7. The Acceptance Authority signs only where formal acceptance is required.

AI can help draft, revise, summarize, and check traceability.

AI must not:

- invent new scope
- invent evidence
- approve acceptance
- hide missing ownership, missing IDs, or missing review inputs

## 9. Prompting Standard for Solution Artifacts

When prompting AI for a solution artifact, use this order:

1. artifact type
2. current stage
3. objective
4. in-scope and out-of-scope boundary
5. required IDs and source references
6. required structure
7. review criteria

Prompt skeleton:

```text
Draft a [artifact type] for Stage [stage].
Objective: [what this artifact must achieve]
In scope: [items]
Out of scope: [items]
Required IDs and references: [IDs and source artifacts]
Required structure: [sections or table fields]
Review criteria: [clarity, traceability, no new scope, etc.]
```

## 10. Appendix A - Acceptance-Readiness Checklist

Use this checklist before asking for formal solution acceptance.

- [ ] The acceptance boundary is clear.
- [ ] All in-scope `FC-###` items are implemented, deferred, or otherwise explicitly dispositioned.
- [ ] Solution Modules and Use Case Narratives are complete enough to support validation.
- [ ] Evidence is linked and attributable.
- [ ] The live release boundary is clear where deployment has occurred.
- [ ] Operational ownership, support, and handoff conditions are visible where required.
- [ ] Open defects, exceptions, exclusions, and conditions are stated clearly.
- [ ] The named Acceptance Authority is identified.
- [ ] The Acceptance Record states what was reviewed, on what basis, and with what decision outcome.

## 11. Governance Health Signals

Good signs:

- approved capabilities stay stable through elaboration
- modules organize the scope around meaningful user behaviors without changing it
- use cases explain behavior in plain language
- evidence is gathered during delivery, not reconstructed at the end
- acceptance decisions are explicit and attributable

Warning signs:

- capabilities keep being renumbered or rewritten late
- modules are grouped by team ownership only or have no clear user-behavior focus
- use cases introduce new behavior not found in approved scope
- evidence is missing, unclear, or not traceable
- acceptance is being prepared before readiness gaps are visible
