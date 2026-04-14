# Framework Overview

## 1. Purpose

This document provides the operating overview for the Work Delivery Framework.

It explains:

1. what the framework is for
2. when it applies
3. how initiatives move through the lifecycle
4. what each gate means
5. how scaling works without weakening readiness standards

## 2. System Overview

The framework defines how internal teams, PMO, delivery managers, and internal engineers turn a new business request into delivery-ready project documentation.

Its purpose is to produce documentation that is:

1. complete enough to build from
2. explicit enough to review and govern
3. supportable after delivery
4. usable by internal teams, external teams, or AI-assisted delivery teams without redefining the problem during execution

The framework is an operating model, not optional guidance.

## 3. Scope of Applicability

### 3.1 In Scope

1. greenfield software projects
2. brownfield software projects

### 3.2 Out of Scope

1. minor low-risk changes
2. research spikes
3. support work
4. small internal process changes

### 3.3 Conditionally In Scope

1. complex operational changes affecting multiple organizations when the work is still primarily a software initiative
2. complex internal process changes affecting the whole organization when the work is still primarily a software initiative

## 4. Core Behavioral Contract

The framework exists to ensure that teams can:

1. intake and qualify a request
2. define the initiative clearly enough for downstream execution
3. authorize work where authorization is required
4. define the solution and delivery model without hidden assumptions
5. define acceptance explicitly and observably
6. define supportability before transition
7. close work formally with visible evidence

The framework also forbids silent assumption-making. Missing business inputs, unclear dependencies, ambiguous acceptance conditions, or undocumented operational gaps must stop progression rather than being absorbed downstream.

## 5. Lifecycle Stages

The lifecycle is a formal stage-and-gate sequence.

| Stage | Purpose | Ends At |
| --- | --- | --- |
| Intake | Capture the request, assign provisional ownership, open the record | No gate |
| Assessment / Qualification | Decide whether the request is a qualified framework candidate | Gate 1: Qualified Request |
| Discovery / Initiative Definition | Bound scope, outcomes, constraints, and initial direction | Gate 2: Initiative Defined |
| Authorization | Record explicit authorization when required | Gate 3: Authorized |
| Solution Definition | Produce solution definition sufficient for planning and task breakdown | Gate 4: Specification Complete |
| Planning / Project Team Mobilization / MVP Plan | Define MVP scope, success measures, and feasibility | Gate 5: MVP Identified |
| Delivery / Execution | Deliver against the approved specification and acceptance basis | Gate 6: All Deliverables Accepted |
| Handoff / Transition | Establish supported operating state | Gate 7: Transition Complete |
| Closure | Record final closure basis and disposition | Gate 8: Closure Complete |

## 6. Gate Model

| Gate | Meaning | Minimum Threshold |
| --- | --- | --- |
| Gate 1: Qualified Request | The request is in scope and owned well enough to proceed | `adequate` |
| Gate 2: Initiative Defined | The initiative is bounded well enough to decide the next path | `adequate` |
| Gate 3: Authorized | Explicit authorization to invest resources exists where required | `adequate` |
| Gate 4: Specification Complete | The documentation set is strong enough for downstream planning without inventing requirements | `strong` |
| Gate 5: MVP Identified | MVP scope, success measures, and acceptance criteria are explicit and approved | `adequate` |
| Gate 6: All Deliverables Accepted | The delivered solution is accepted against the defined acceptance criteria | `adequate` |
| Gate 7: Transition Complete | Operating ownership, support model, observability, and maintainability are accepted | `adequate` |
| Gate 8: Closure Complete | Closure evidence and rationale are complete and recorded | `adequate` |

## 7. Authorization Rule

Authorization is conditional.

At Gate 2, the named Gate Decision Owner must declare authorization as either:

1. `Required`
2. `Not Required`

If authorization is not required, the initiative moves from Discovery directly to Solution Definition after Gate 2.

## 8. Acceptance and Validation Rule

Acceptance criteria must be:

1. observable
2. quantifiable where feasible
3. testable with explicit validation methods
4. written in hybrid Gherkin form for the Project Brief

Gate 4 fails if acceptance criteria still require downstream interpretation.

## 9. Supportability Rule

Before transition is complete, the documentation set must make supportability explicit, including:

1. named support ownership
2. support model and response expectations
3. observability expectations
4. maintainability commitments
5. transition checklist evidence

## 10. Scaling Model

The framework uses one path for all in-scope initiatives.

Scaling happens by changing the depth and explicitness of evidence, not by changing the gate model.

The Delivery Owner calibrates rigor using:

1. scope
2. business impact
3. delivery complexity
4. operational consequence

Scaling may change how much detail is required, but it does not waive:

1. formal gates
2. named Gate Decision Owners
3. the primary artifact
4. the `Decision Log`
5. the `Open Items Register`
6. any triggered conditional artifact

## 11. Primary Artifact Rule

Every in-scope initiative uses one primary definition artifact:

1. `Initiative Definition / Project Brief`

Conditional artifacts supplement the Project Brief when their trigger conditions are true. They do not replace it.

## 12. External Engagement Modes

When external participation is expected, the initiative must declare one provisional mode by Gate 2 and finalize it no later than Gate 4.

The canonical modes are:

1. `Staff augmentation`
2. `Co-delivery`
3. `Full external delivery`

Only `Co-delivery` and `Full external delivery` trigger a `Delivery Charter`.

## 13. Review Discipline

Reviewers must judge evidence based on what is written, not on informal context or confidence in the team.

If an artifact or gate fails completeness, the output must include an explicit deficiency list tied to the failed criteria.

If the failure includes AI-sufficiency issues, the review must identify them as AI-sufficiency failures.

## 14. Related Documents

1. `artifact_catalog.md`
2. `completeness_and_review_model.md`
3. `artifact_specifications/`
4. `templates/`
5. `machine_readable/`
