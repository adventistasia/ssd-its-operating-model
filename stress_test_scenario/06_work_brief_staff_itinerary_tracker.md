# Work Brief - SSD Staff Itinerary Tracker

Status: working draft  
Current stage: Define  
Specification used: [Work Brief Specification](../work_delivery/work_brief/work_brief_specification.md)

## 1. Document information

- Work brief title: SSD staff itinerary tracker
- Work brief ID: WB-SSD-2026-001
- Current status: Draft
- Current stage: Define
- Date raised: 2026-04-10
- Last updated: 2026-04-10
- Parent reference: [04_stage_1_work_assessment_report.md](04_stage_1_work_assessment_report.md)
- Tracking reference: stress test scenario only

## 2. Accountable owners

- Requester: Jane, Administrative Assistant / Secretary
- Outcome Owner: unresolved; proposed office operations / administrative coordination owner
- Delivery Owner: Project Manager / Delivery Owner (simulated)
- Acceptance Authority: unresolved; likely split between business usefulness acceptance and record-correctness acceptance
- Decision Authority: unresolved; sponsor / delegated administrative authority still needs confirmation
- Operational / Support Owner: unresolved; likely ITS support if built on Microsoft 365, with business data stewardship remaining outside ITS

Working draft note:

Per the repository guardrails, this record remains a working draft because key control inputs are still unresolved.

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

- source-of-truth model is not yet agreed
- acceptance ownership is not yet agreed
- the requestor wants low maintenance and low process overhead

## 5. What is going to be delivered

| Deliverable | What must be produced | Delivery owner | Acceptance authority | Evidence of completion |
| --- | --- | --- | --- | --- |
| Controlled work record | This Work Brief maintained through the scenario | Delivery Owner | Decision Authority once named | current brief with visible decisions and unresolved gaps |
| Proposed solution direction | a practical first-release direction and scope boundary | Delivery Owner with Programmer input | Outcome Owner candidate once named | [07_proposed_solution_direction.md](07_proposed_solution_direction.md) |
| Status visibility design basis | minimum agreed status concepts, source-of-truth framing, and revision handling assumptions | Delivery Owner with stakeholder input | unresolved | reflected in this brief and [08_conversations_and_decisions.md](08_conversations_and_decisions.md) |

## 6. When and how this is going to be delivered

### 6.1. Delivery approach

Current approach:

- use this Work Brief as the scaled definition record
- seek confirmation of sponsor, Outcome Owner, Acceptance Authority, and source-of-truth model
- if those controls are confirmed, proceed toward a small Microsoft 365-based visibility solution

### 6.2. Target timing

Requested urgency signal: high from the requestor  
Governance readiness signal: not yet ready for authorization

### 6.3. Material risks and dependencies

- unresolved sponsor
- unresolved Outcome Owner
- unresolved Acceptance Authority
- unclear interaction between itinerary records and leave records
- risk of duplicate encoding
- risk that a tracker becomes a false system of record

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

- named owners are confirmed before delivery starts
- no delivery starts without a recorded authorization decision
- the Acceptance Authority model is confirmed before build

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
| Stage 1 final assessment | Proceed to Work Definition via Work Brief | simulated decision authority | 2026-04-10 | Work Assessment Report | small governed work still fits one brief | do not start build before control gaps are addressed | Delivery Owner |

## 9. Closure

Not closed.

Closure note:

This scenario intentionally stops with a working draft Work Brief because the framework test is more useful at the point where the work is small, clearly useful, and still blocked by real ownership and source-of-truth questions.
