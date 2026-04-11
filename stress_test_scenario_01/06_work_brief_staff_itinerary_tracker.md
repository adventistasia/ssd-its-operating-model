# Work Brief - SSD Staff Itinerary Tracker

Status: working draft  
Current stage: Define  
Specification used: [Work Brief Specification](../work_delivery/work_brief/work_brief_specification.md)

## 1. Document information

- Work brief title: SSD staff itinerary tracker
- Work brief ID: WB-SSD-2026-001
- Current status: Approved for mobilization readiness, but execution has not started
- Current stage: Define
- Date raised: 2026-04-10
- Last updated: 2026-04-10
- Parent reference: [04_stage_1_work_assessment_report.md](04_stage_1_work_assessment_report.md)
- Tracking reference: stress test scenario only

## 2. Accountable owners

- Requester: Jane, Administrative Assistant / Secretary
- Outcome Owner: office operations / administrative coordination owner, provisional
- Delivery Owner: Delivery Owner / Project Manager
- Acceptance Authority: office operations owner for usability, with Committee Secretary and leave-record owner reviewing correctness assumptions
- Decision Authority: Angie, the Sponsor, acting as delegated decision authority for this small item
- Implementer / contributors: Programmer / Technical SME
- Operational / Support Owner: ITS support for the platform layer, with business record owners retaining content authority

Working draft note:

Per the repository guardrails, this record remains a working draft because a few control inputs are still provisional even though the work is now judged small enough to proceed proportionately.

## 3. Why this work needs to be done

SSD office staff need a reliable way to see whether a staff member is:

- on an approved itinerary
- on leave or vacation
- expected to be in the office

Today, staff reconstruct this from informal communication and fragmented records. That creates confusion, repeated follow-up, and avoidable delays in coordination and meeting planning.

## 4. Intended outcome and how success will be known

### 4.1. Intended outcome

Create a small, trustworthy office visibility solution that allows staff to check current status without relying on repeated ad hoc follow-up.

### 4.2. Success criteria

- office staff can determine whether a staff member is on approved itinerary, on leave, or expected in office
- the tracker shows the latest valid status basis rather than informal assumptions
- the tracker makes next known return / office date visible where available
- office coordination effort is reduced

### 4.3. Scope boundaries

In scope:

- SSD staff status visibility for itinerary / leave / in-office states
- indication of whether the displayed itinerary status is based on the latest approved record
- a first-release reporting view with clear status interpretation
- revision visibility for itinerary changes

Out of scope:

- full itinerary approval workflow redesign
- leave-management system redesign
- travel expense and liquidation workflow redesign
- enterprise attendance system
- custom platform build unless later justified

Assumptions:

- approved itinerary records exist today
- leave records exist today
- a lightweight first release can consume or reflect authoritative records rather than replace them

Constraints:

- source-of-truth model is not yet agreed in this working draft
- acceptance ownership is not yet fully locked
- the requestor wants low maintenance and low process overhead

## 5. What is going to be delivered

| Deliverable | What must be produced | Delivery owner | Acceptance authority | Evidence of completion |
| --- | --- | --- | --- | --- |
| Controlled work record | This Work Brief maintained through the scenario | Delivery Owner | Decision Authority once named | current brief with visible decisions and unresolved gaps |
| Proposed solution direction | a practical first-release direction and scope boundary | Delivery Owner with Programmer input | Outcome Owner candidate once named | [07_proposed_solution_direction.md](07_proposed_solution_direction.md) |
| Status visibility design basis | minimum agreed status concepts, source-of-truth framing, and revision handling assumptions | Delivery Owner with stakeholder input | review by Committee Secretary and leave-record owner | reflected in this brief and [08_conversations_and_decisions.md](08_conversations_and_decisions.md) |

## 6. When and how this is going to be delivered

### 6.1. Delivery approach

Current approach:

- use this Work Brief as the scaled definition record
- seek confirmation of sponsor, outcome owner, acceptance authority, and source-of-truth model
- if those controls are confirmed, proceed toward a small Microsoft 365-based visibility solution

### 6.2. Target timing

Requested urgency signal: high from the requestor

Governance readiness signal: now ready to mobilize, but not to execute build tasks yet

### 6.3. Material risks and dependencies

- unresolved source-of-truth boundaries
- clarity needed on who can edit or revise itinerary status
- acceptance must not collapse into a vague "looks useful" check
- leave-record owner must remain visible in the control model

### 6.4. Operational / support / security considerations

- personal status information may need limited visibility
- support ownership for the technical platform is different from ownership of record correctness
- a simple tracker must still avoid displaying unofficial status as approved truth

## 7. Acceptance criteria

### 7.1. Deliverable-level acceptance focus

For the proposed solution direction:

- the scope remains small and explicit
- the source-of-truth approach is visible
- itinerary revision handling is visible
- the interaction with leave status is visible

For the work as a whole:

- named owners are visible before execution starts
- no build starts without a recorded authorization decision
- the Acceptance Authority model is explicit enough to support the first release

### 7.2. Closure criteria

This work item is not ready to close unless:

- acceptance authority confirms the defined deliverables
- resulting operational ownership is confirmed
- any remaining conditions are visible and owned

## 8. Decision log

| Decision requested or made | Decision taken | Decision authority | Date | Evidence basis used | Rationale | Conditions / risk acceptance | Follow-up owner |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Stage 1 triage | Proceed to Validation Assessment | simulated intake authority | 2026-04-10 | Initial Review | real operational problem, no immediate dealbreaker | confirm sponsor candidate | Delivery Owner |
| Stage 1 validation gate | Proceed to focused analysis | simulated governance authority | 2026-04-10 | Validation Assessment | need is credible; rule and ownership ambiguity remains | keep analysis light | Delivery Owner |
| Stage 3 authorization | Approve with conditions | Angie, Sponsor / delegated decision authority | 2026-04-10 | Work Assessment Report and stakeholder conversations | small governed work still fits one brief | use existing authoritative records; do not start build until mobilization controls exist | Delivery Owner |

## 9. Closure

Not closed.

Closure note:

This scenario intentionally stops at mobilization readiness. The work is approved in a small governed form, but no execution or deployment has started.
