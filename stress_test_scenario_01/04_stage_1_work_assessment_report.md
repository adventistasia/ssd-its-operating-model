# Stage 1 Work Assessment Report

Status: working draft  
Stage: Stage 1 - Work Assessment  
Specification used: [Work Assessment Report Specification](../work_delivery/work_assessment/work_assessment_report_specification.md)

## 1. Report identity and control

- Work name: SSD staff itinerary tracker
- Assessment date: 2026-04-10
- Assessment Owner: Delivery Owner / Project Manager (simulated)
- Sponsor: Angie the Sponsor
- Outcome Owner candidate: office operations / administrative coordination owner
- Delivery Owner candidate: Project Manager / Delivery Owner for the item
- Intended decision authority: Angie, acting within a small delegated authority band for this simulation
- Upstream references:
  - [02_stage_1_initial_review.md](02_stage_1_initial_review.md)
  - [03_stage_1_validation_assessment.md](03_stage_1_validation_assessment.md)
- Analysis basis used:
  - stakeholder conversations summarized in [08_conversations_and_decisions.md](08_conversations_and_decisions.md)
  - Delivery Owner interpretation journal in [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)

## 2. Executive summary

The request addresses a real and recurring operational need: office staff need one reliable way to see whether a staff member is on approved itinerary, on leave, or expected to be in the office.

Recommendation: proceed to Work Definition using a Work Brief.

Why now:

- the current operating problem is real
- the likely solution footprint remains small
- the main risk is ownership and source-of-truth logic, which can be handled through a scaled definition path rather than a full initiative pack

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
- revisions to itinerary status are visible and not silently overwritten

### 3.4. Consequence of inaction

The office will continue to operate with fragmented and low-trust visibility, recurring interruptions, and preventable planning delays.

## 4. Assessment scope boundary

### 4.1. Likely in scope for definition

- staff itinerary / leave / in-office visibility problem
- latest-valid-record question
- revision visibility for itineraries
- role and ownership clarity for maintaining trustworthy status

### 4.2. Clearly out of scope at this point

- end-to-end travel management redesign
- leave-management redesign
- finance process redesign
- enterprise workforce scheduling
- custom app build as the default answer

### 4.3. Key assumptions and constraints

- official itinerary records exist today
- leave records exist today, but may not share the same owner
- staff need a visibility tool more urgently than they need a new transaction system

## 5. Preferred path and option summary

Options considered:

- do nothing
- simple shared tracker
- structured Microsoft 365 tracker
- custom app

Preferred path:

- define a small governed work item aimed at a controlled visibility tracker, likely using existing Microsoft 365 capabilities

Why this path is better at this stage:

- it addresses the need without assuming a large implementation
- it fits the current size and urgency better than a custom build
- it allows ownership, source-of-truth, revision, and acceptance questions to be made explicit before delivery

## 6. Current-state, stakeholder, and analysis findings summary

### 6.1. Current-state summary

- office staff do not have one trusted status view
- itinerary records have an official recorder but are not easily visible in the needed operational form
- leave records sit in another owner path
- informal communications are filling the visibility gap

### 6.2. Key stakeholder needs

- Jane wants a low-maintenance, fast, useful tracker
- Angie wants proportionate control and does not want overbuild
- the Committee Secretary wants approved-record correctness and revision traceability
- the Programmer wants rule clarity before build
- the leave-record owner wants leave status preserved as a separate authoritative record

### 6.3. Key findings

1. This is small work in delivery footprint.
2. This is not small in authority ambiguity.
3. The likely first release should be a visibility layer, not a full approval workflow.
4. The framework's lightweight path remains plausible.
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

Governance size signal: small governed work item.

Reason:

- limited scope
- likely single-office use case
- low technical complexity
- but still enough control sensitivity to need named owners, decision rights, and acceptance basis

## 8. Major risks, dependencies, and viability considerations

### 8.1. Major risks

- sponsor must stay engaged and proportionate
- outcome owner remains provisional
- acceptance authority needs to be explicit
- leave-status authority may sit outside itinerary ownership
- a combined tracker could accidentally become a false system of record

### 8.2. Dependencies

- office operations leadership engagement
- leave-record owner engagement
- committee secretary confirmation on approved itinerary source
- decision on reporting view versus workflow tool

### 8.3. Viability

The work is viable if definition stays small and focuses on control clarity rather than over-design.

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

Recommended artifact: [Work Brief](../work_delivery/work_brief/work_brief_specification.md)

Why:

- the request still behaves like one small governed item
- one controlled record can still reasonably hold problem, scope, owners, decision basis, and closure logic
- a full Initiative Definition Document would likely be disproportionate at this point

### 9.3. Deliverables that appear needed in definition

- Work Brief: required
- concise functional scope statement: required, can sit inside the Work Brief or as a small linked note
- decision log: required, can sit inside the Work Brief
- source-of-truth and rule clarification note: required as a working support artifact because the programmer and official record owners are blocked by unresolved rules

### 9.4. Deliverables not yet justified

- Initiative Definition Document
- Project Charter
- full delivery governance pack
- detailed solution modules
- detailed operational-readiness pack

Reason:

- disproportionate for the current request size
- not justified until the work becomes broader, riskier, or more operationally significant

### 9.5. Acceptance authority signals

Current signal:

- utility acceptance likely belongs with an office operations owner
- record-correctness acceptance needs the Committee Secretary and leave-record owner involved
- no final unified Acceptance Authority should be assumed unless the working brief says so explicitly

## 10. Work assessment recommendation

Recommendation: proceed to Work Definition.

Conditions:

- use the Work Brief path
- keep the work explicitly small
- do not start execution until source-of-truth, access, and acceptance questions are visible

## 11. Decision record

- Decision authority: simulated governance / administrative decision owner
- Decision taken: proceed to Work Definition
- Decision date: 2026-04-10
- Evidence basis used:
  - Initial Review
  - Validation Assessment
  - stakeholder interview notes
- Conditions / follow-up actions:
  - confirm sponsor
  - confirm outcome owner
  - confirm acceptance authority arrangement
  - clarify source of truth and leave / itinerary interaction
- Follow-up owner: Delivery Owner / Project Manager

## 12. Handoff references

- [00_request_context.md](00_request_context.md)
- [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)
- [02_stage_1_initial_review.md](02_stage_1_initial_review.md)
- [03_stage_1_validation_assessment.md](03_stage_1_validation_assessment.md)
- [05_path_and_artifact_rationale.md](05_path_and_artifact_rationale.md)
- [08_conversations_and_decisions.md](08_conversations_and_decisions.md)
