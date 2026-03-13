# Project Delivery Framework

## Purpose

This framework governs planned delivery initiatives, including projects and significant enhancements.

It puts the Define–Decide–Deliver (DDD) Work Management Model into practice by defining the required documents, decision points, and sign-off steps for disciplined delivery at scale.

## Outcome

When applied consistently:

- No initiative enters delivery without explicit sponsorship and formal authorization.
- Scope, ownership, funding, Acceptance Authority (sign-off owner), and material impacts are defined before work begins.
- Delivery teams execute against approved capabilities and documented design.
- Acceptance is evidence-based, attributable, and aligned to defined outcomes.
- Systems transition to operations with defined support ownership and sustainability controls.
- Projects conclude with formal acceptance rather than informal completion.

The organization operates with clear, auditable delivery decisions.

## End-to-End Stages and Artifacts

## Stage 1 — Opportunity Assessment

**Purpose:** Determine whether an idea or request is worth any further investment before entering Delivery Definition.

This stage applies the Opportunity Assessment Framework to determine whether an initiative may proceed to Delivery Definition.

### Primary Artifact

- Opportunity Assessment Report

All validation discussions, feasibility notes, and stakeholder findings are incorporated into the Opportunity Assessment Report. Stage 1 does not produce separate validation documents.

### Activities

| Activity                              | Required / Optional                               | Must Attend                                                    | Artifacts Used                                        |
| ------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------- | ----------------------------------------------------- |
| Intake & Sponsorship Alignment        | Required                                          | Requestor, Sponsor (or candidate), ITS Intake / Portfolio role | Intake submission, preliminary problem statement      |
| Validation and feasibility check  | Optional (as needed for clarity or risk exposure) | Sponsor, subject matter experts, Technical Lead (as applicable)                  | Notes incorporated into Opportunity Assessment Report |
| Decision meeting (Proceed / Defer / Reject) | Required                                          | Decision Authority, Sponsor, Portfolio / Governance role       | Opportunity Assessment Report                         |

### Exit Criteria

- Problem and opportunity clearly articulated
- Sponsorship confirmed
- Strategic alignment and early risk indicators understood
- Decision recorded (Proceed / Defer / Reject)
- If Proceed, ready to enter Stage 2 — Delivery Definition

## Stage 2 — Delivery Definition

**Purpose:** Define enough to enable an informed Delivery Authorization decision — no more, no less.

Stage 2 stays at approval-level detail: enough clarity on scope, value, owners, risks, and cost to approve delivery — without producing build-level design details.

Stage 2 determines which Deliverable Domains (deliverable categories), as defined in the Standard Deliverables & Acceptance Guide, are in scope.
Each domain must be explicitly scoped in or excluded, and a named Acceptance Authority identified for every in-scope domain.

### Delivery Definition Package

The Delivery Definition Package documents, at approval-level detail, the intended deliverables organized by Deliverable Domain, consistent with the Standard Deliverables & Acceptance Guide.

Within each in-scope domain, only deliverables relevant to the initiative’s nature, scale, and risk are required.

**1. Solution Deliverables**

- Problem and current-state summary
- Future-state and value positioning
- Outcome statement and measurable success criteria
- Functional Capabilities with Capability IDs
- Acceptance focus and named Acceptance Authority

**2. Data, Records & Knowledge Deliverables**

- Impacted data sets and systems of record
- Data governance considerations and stewardship
- Data-related acceptance focus

**3. Operational Readiness Deliverables**

- Support Owner and Operational (Run) Owner identified
- High-level operational impact summary
- Feasibility-level recovery concept

**4. Governance & Control Deliverables**

- In-scope / out-of-scope boundaries
- Approval-level cost estimate
- Financial impact summary (CapEx/OpEx: upfront vs ongoing costs)
- Cost of inaction
- Feasibility summary

**5. Security, Privacy & Compliance Deliverables**

- High-level security impact summary
- Control intent (e.g., access control, logging)
- Regulatory considerations (if applicable)

**6. User Adoption & Change Enablement Deliverables**

- Impacted user groups
- Organizational impact level
- High-level enablement approach

Keep this at approval-level detail; do not include build-level design details, runbooks, task plans, or detailed test scripts.

### Activities

| Activity                                          | Required / Optional                                                    | Must Attend                                                 | Artifacts Used                                                 |
| ------------------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------- | -------------------------------------------------------------- |
| Definition & Capability Structuring Session(s)    | Required                                                               | Outcome Owner, Delivery Owner, Key Stakeholders, subject matter experts       | Draft Delivery Definition Package, capability definitions      |
| Scope, Acceptance & Stakeholder Validation Review | Required                                                               | Outcome Owner, Named Acceptance Authorities, Delivery Owner | Defined scope boundaries, acceptance focus, Deliverable Domains |
| Operational & Support Impact Review               | Conditionally Required (for system-impacting or medium/high-risk work) | Delivery Owner, Support / Ops representatives               | Support model summary, operational impact summary              |

### Exit Criteria

- Problem, value, outcomes, and scope boundaries clearly defined (WHAT, not HOW)
- Deliverable Domains in scope explicitly identified or excluded, and Acceptance Authorities named for each in-scope domain
- Support and Operational Owners identified
- Approval-level cost estimate and financial impact summarized
- Risk exposure and delivery feasibility clearly documented at authorization depth
- Definition sufficient for an informed go / no-go Delivery Authorization decision
- Ready to seek Delivery Authorization

## Stage 3 — Delivery Authorization

**Purpose:** Explicitly authorize delivery by committing people, time, funding, and risk to the defined outcomes, capabilities, and scope.

This stage is the go/no-go commitment point and protects delivery teams from informal, unfunded, or implied starts.

### Primary Artifacts

- Decision Record (Approve / Defer / Reject)
- Project Charter

### Activities

| Activity                                        | Required / Optional | Must Attend                                                | Artifacts Used                                                   |
| ----------------------------------------------- | ------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- |
| Project Proposal Authorization Meeting          | Required            | Decision Authority, Sponsor, Outcome Owner, Delivery Owner | Delivery Definition Package, risk summary, draft Project Charter |
| Sponsorship, funding, and priority confirmation | Required            | Sponsor, Finance (if applicable), Decision Authority       | Budget estimate, priority ranking, capacity overview             |
| Conditional approval discussion                 | Optional            | Decision Authority, Sponsor                                | Risk mitigation summary, dependency analysis                     |
| Phased or constrained authorization discussion  | Optional            | Decision Authority, Sponsor, Delivery Owner                | Phased delivery concept, milestone outline                       |

### Exit Criteria

- Delivery explicitly authorized
- Project Charter approved
- Delivery Owner confirmed
- Funding source formally confirmed (budget line, cost center, or approved allocation identified)
- Implementation budget approved at required authority level
- Ongoing OpEx impact acknowledged and accepted
- Financial risks explicitly reviewed and accepted by Decision Authority
- Work may proceed to Delivery Elaboration

### Hard Rule

No delivery work may start without explicit Delivery Authorization

## Stage 4 — Delivery Elaboration

**Purpose:** Develop the detailed design needed to build what was approved in Stage 2 — without changing scope, outcomes, capabilities, or acceptance structure.

Stage 4 develops the Detailed Design Package that the delivery team will use to build, test, and transition the solution.

### Detailed Design Package

- Confirmed technical approach
- Detailed design and elaboration artifacts required for each in-scope Deliverable Domain (for example, Solution Modules and Use-Case Specifications within the Solution Deliverables domain)
- Integration points and external dependencies
- Performance, reliability, and security needs
- Acceptance test plan aligned to Stage 2 acceptance focus
- Data move and rollout plan
- Operational design summary

If elaboration introduces new or expanded capabilities not defined in Stage 2, the work must return to Stage 2 for review and potential re-authorization.

### Exit Criteria

- Detailed Design Package complete and internally consistent
- Integration points and dependencies validated
- Acceptance test plan aligned to Stage 2 acceptance focus
- No material scope creep from the approved definition
- Ready to set up the delivery team

## Stage 5 — Delivery Mobilization

**Purpose:** Prepare the organization and delivery team to execute the detailed design with clear governance, roles, meeting rhythm, and ways of working.

### Primary Artifacts

- Delivery Charter
- Communication Plan
- Change and Escalation Rules
- Initial Task Breakdown / Delivery Plan

### Exit Criteria

- Execution structure and meeting rhythm confirmed
- Task breakdown supports controlled execution
- Ready to begin execution

## Stage 6 — Execution & Control

**Purpose:** Produce the authorized deliverables, validate them against the acceptance focus defined in Stage 2, and ensure completion with evidence and sign-off.

Within the Solution Deliverables domain, validation and incremental deployment occur at the Solution Module level, as defined in the Solution Documentation Process.

Artifacts must be clearly linked to what was approved in Stage 2 for each in-scope Deliverable Domain.

Within the Solution Deliverables domain, this includes clear links to approved Functional Capabilities, Solution Modules, and Use-Case Specifications.

### Expectation Rule

Progress is measured by accepted deliverables, not effort or activity.

A deliverable is not complete until:

- It meets the acceptance focus defined in Stage 2
- Required evidence is produced
- The named Acceptance Authority formally accepts it

### Exit Criteria

- All in-scope Deliverable Domains validated against defined acceptance focus
- Required acceptance evidence complete and clearly linked
- No unresolved sign-off issues
- Ready for Stage 7 Acceptance, Transition & Closure

## Stage 7 — Acceptance, Transition & Closure

**Purpose:** Formally accept outcomes and transition into operations.

### Hard Rule

Delivered without acceptance is not complete

## Artifact Summary by Stage

| Stage                  | Artifacts                                                       |
| ---------------------- | --------------------------------------------------------------- |
| Opportunity Assessment | Opportunity Assessment Report                                   |
| Delivery Definition    | Delivery Definition Package including Functional Capabilities   |
| Delivery Authorization | Decision record, approved Project Charter, funding confirmation |
| Delivery Elaboration   | Detailed Design Package based on approved scope      |
| Delivery Mobilization  | Delivery Charter, communication plan, task breakdown            |
| Execution & Control    | Deliverables, evidence, documentation, change records           |
| Acceptance & Closure   | Acceptance records, handover, closure                           |

