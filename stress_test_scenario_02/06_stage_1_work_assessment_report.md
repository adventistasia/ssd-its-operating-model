# Stage 1 Work Assessment Report

Status: working draft
Stage: Stage 1 - Work Assessment
Specification used: [Work Assessment Report Specification](../work_delivery/work_assessment/work_assessment_report_specification.md)

## 1. Report identity and control

- Work name: SSD staff itinerary tracker
- Assessment date: 2026-04-10
- Assessment Owner: Delivery Owner / Project Manager (simulated)
- Sponsor: Angie, sponsor and office operations decision-maker
- Outcome Owner candidate: office operations / administrative coordination owner
- Delivery Owner candidate: Project Manager / Delivery Owner for the item
- Intended decision authority: Angie, acting as delegated office operations decision authority
- Upstream references:
  - [03_stage_1_initial_review.md](03_stage_1_initial_review.md)
  - [04_business_process_stage_analysis.md](04_business_process_stage_analysis.md)
  - [05_stage_1_validation_assessment.md](05_stage_1_validation_assessment.md)
- Analysis basis used:
  - stakeholder conversations summarized in [09_conversations_and_decisions.md](09_conversations_and_decisions.md)
  - Delivery Owner interpretation journal in [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)

## 2. Executive summary

The request addresses a real and recurring operational need: office staff need one reliable way to see whether a staff member is on approved itinerary, on leave, or expected to be in the office.

Recommendation: proceed to Work Definition using an Initiative Definition Document.

Why now:

- the current operating problem is real
- the likely solution footprint is still bounded
- the main risk is not just technical feasibility but cross-owner authority and record correctness
- a Work Brief would be too thin to hold the split ownership, acceptance, and data-governance story without creating ambiguity

## 3. Assessed need, desired outcome, and success measures

### 3.1. Validated need

Current staff availability is being reconstructed manually from mixed sources, creating confusion, delays, and low confidence.

### 3.2. Desired outcome

SSD office staff can quickly check one trusted status view and determine whether a staff member is:

- on approved itinerary
- on leave / vacation
- expected in office

### 3.3. Success measures

- staff availability questions can be answered from one view
- displayed status is tied to a valid underlying record
- staff no longer need repeated ad hoc follow-up to reconstruct availability
- itinerary revisions are visible and not silently overwritten
- leave data remains controlled by HR

### 3.4. Consequence of inaction

The office will continue to operate with fragmented and low-trust visibility, recurring interruptions, and preventable planning delays.

## 4. Assessment scope boundary

### 4.1. Likely in scope for definition

- staff itinerary / leave / in-office visibility problem
- latest-valid-record question
- revision visibility for itineraries
- role and ownership clarity for maintaining trustworthy status
- access boundaries for leave-related information

### 4.2. Clearly out of scope at this point

- end-to-end travel management redesign
- leave-management redesign
- finance process redesign
- enterprise workforce scheduling
- custom app build as the default answer

### 4.3. Key assumptions and constraints

- formal itinerary approval records exist today
- leave records exist today and remain HR-owned
- staff need a visibility tool more urgently than they need a new transaction system
- the solution must not become a second system of record

## 5. Preferred path and option summary

Options considered:

- do nothing
- simple shared tracker
- structured Microsoft 365 tracker
- custom app

Preferred path:

- define a controlled initiative baseline aimed at a visibility layer over authoritative itinerary and leave records, not a duplicate encoding layer

Why this path is better at this stage:

- it addresses the need without assuming a large implementation
- it fits the current size and urgency better than a custom build
- it makes ownership, source-of-truth, revision, privacy, and acceptance questions explicit before delivery
- it is clearer than a Work Brief for a cross-team, cross-owner problem

## 6. Current-state, stakeholder, and analysis findings summary

### 6.1. Current-state summary

- office staff do not have one trusted status view
- itinerary records have a formal approval path but are not easily visible in the needed operational form
- leave records sit in HR control
- informal communications are filling the visibility gap

### 6.2. Key stakeholder needs

- Jane wants a low-maintenance, fast, useful tracker
- Angie wants practical control and low overhead
- the Committee Secretary wants approved-record correctness and revision traceability
- the HR Leave Records Owner wants controlled use of leave data
- the Programmer wants rule clarity before build
- the Data Steward wants traceability and retention discipline

### 6.3. Key findings

1. This is still bounded work in delivery footprint.
2. This is not small in authority ambiguity.
3. The first release should be a controlled visibility layer, not a full approval workflow.
4. The framework's lightweight Work Brief path is no longer the best fit.
5. Source-of-truth and acceptance questions must be surfaced early or the tracker will not be trusted.

## 7. High-level requirements, capabilities, and work profile summary

### 7.1. High-level requirements / capabilities

Any viable work definition should preserve these baseline needs:

- staff availability view across itinerary / leave / in-office states
- latest valid record basis
- visible revision handling for itinerary changes
- clear distinction between approved, pending, revised, cancelled, and completed itinerary states where relevant
- access boundaries around who can view and who can update

### 7.2. Work profile summary

Governance size signal: Medium complexity / cross-team governed work item

Reason:

- limited user footprint
- but multiple authoritative owners
- a controlled data view over separate records
- privacy and access boundaries
- split acceptance expectations

## 8. Major risks, dependencies, and viability considerations

### 8.1. Major risks

- sponsor remains weak if the work drifts into "just a tracker"
- Outcome Owner remains unclear unless office operations owns the combined outcome
- Acceptance Authority is split across business usefulness, itinerary authority, and leave authority
- leave-status authority may sit outside itinerary ownership
- a combined tracker could accidentally create a false system of record

### 8.2. Dependencies

- office operations leadership engagement
- leave-record owner engagement
- itinerary approval owner engagement
- support owner engagement
- decision on reporting view versus workflow tool

### 8.3. Viability

The work is viable if definition stays controlled and respects the separate ownership of itinerary and leave data.

## 9. Recommended definition focus and assessment reference basis

### 9.1. What Work Definition must clarify next

- who sponsors the work
- who owns the business outcome
- who accepts the solution
- whether acceptance needs one authority or a split acceptance model
- what the source of truth is for itinerary status
- how leave records interact with itinerary records
- whether the first release is visibility-only or includes controlled updates

### 9.2. Recommended next definition artifact

Recommended artifact: [Initiative Definition Document](../work_delivery/governance_and_control_deliverables/initiative_definition_document_specification.md)

Why:

- the request spans multiple control domains
- one controlled record is still needed, but it must be more complete than a Work Brief
- the work has enough governance, data, and support implications to justify a fuller baseline

### 9.3. Deliverables that appear needed in definition

- Initiative Definition Document: required
- Functional Capabilities: required
- User Roles, Personas and Access Model: required
- Business Rules Catalog: required
- Integration and External Dependency Specification: required
- Data Governance and Impact Assessment: required
- Security and Privacy Risk Assessment: required
- Decision Record Log: required
- Solution Assumptions and Issues Register: required
- Project Charter: required
- Delivery Roadmap: required

### 9.4. Deliverables not yet justified

- detailed technical design
- deployment / release runbook
- delivery execution evidence
- acceptance record

Reason:

- these belong later in the framework
- the exercise stops at readiness and does not simulate build or deployment

### 9.5. Acceptance authority signals

Current signal:

- business usefulness acceptance belongs with Angie as office operations sponsor
- record-correctness acceptance belongs with the Committee Secretary and HR Leave Records Owner for their domains
- the Delivery Owner must keep the split acceptance model visible instead of pretending it is one simple sign-off

This is a real definition gap, not a drafting omission.

## 10. Work assessment recommendation

Recommendation: Proceed to Work Definition

Conditions:

- use the Initiative Definition Document path
- keep the work explicitly bounded to a visibility layer over authoritative records
- do not start build until source-of-truth, access, and acceptance questions are made visible

## 11. Decision record

- Decision authority: Angie, acting as delegated office operations decision authority
- Decision taken: proceed to Work Definition using an Initiative Definition Document
- Decision date: 2026-04-10
- Evidence basis used:
  - Initial Review
  - Validation Assessment
  - business process stage analysis
  - stakeholder interview notes
- Conditions / follow-up actions:
  - confirm sponsor, Outcome Owner, and Acceptance Authority split
  - confirm source of truth and leave / itinerary interaction
  - confirm that the first release is a controlled visibility layer, not duplicate encoding
- Follow-up owner: Delivery Owner / Project Manager

## 12. Handoff references

- [00_request_context.md](00_request_context.md)
- [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)
- [02_stakeholder_map_and_personas.md](02_stakeholder_map_and_personas.md)
- [03_stage_1_initial_review.md](03_stage_1_initial_review.md)
- [04_business_process_stage_analysis.md](04_business_process_stage_analysis.md)
- [05_stage_1_validation_assessment.md](05_stage_1_validation_assessment.md)
- [07_path_and_artifact_rationale.md](07_path_and_artifact_rationale.md)
