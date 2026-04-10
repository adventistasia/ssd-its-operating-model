# Stage 1 Work Assessment Report

Status: working draft  
Stage: Stage 1 - Work Assessment  
Specification used: [Work Assessment Report Specification](../work_delivery/work_assessment/work_assessment_report_specification.md)

## 1. Report identity and control

- Work name: SSD staff itinerary status control
- Assessment date: 2026-04-10
- Assessment Owner: Delivery Owner / Project Manager (simulated)
- Sponsor: Angie, Sponsor and budget holder, subject to Stage 2 confirmation
- Outcome Owner candidate: Office Operations Lead
- Delivery Owner candidate: Project Manager / Delivery Owner for the item
- Intended decision authority: simulated governance / sponsor authority
- Upstream references: [02_stage_1_initial_review.md](02_stage_1_initial_review.md), [03_stage_1_validation_assessment.md](03_stage_1_validation_assessment.md)
- Analysis basis used: stakeholder conversations summarized in [10_conversations_and_decisions.md](10_conversations_and_decisions.md) and Delivery Owner interpretation journal in [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)

## 2. Executive summary

The request addresses a real and recurring operational need: office staff need one reliable way to see whether a staff member is on approved itinerary, on leave, or expected to be in the office.

Recommendation: proceed to Work Definition using an [Initiative Definition Document](../work_delivery/governance_and_control_deliverables/initiative_definition_document_specification.md), not a Work Brief.

Why now:

- the current operating problem is real
- sponsor interest exists if governance is clear
- the work has crossed into custom app territory because of multiple authoritative sources, role-based updates, and auditability requirements
- a light path would understate the control needs

## 3. Assessed need, desired outcome, and success measures

Current staff availability is being reconstructed manually from mixed sources, creating confusion, delays, low trust, and audit weakness. The desired outcome is a trusted status view that shows itinerary, leave, and expected-in-office status. Success means fewer interruptions, visible latest-approved status, and auditable change history. The consequence of inaction is ongoing fragmented visibility and unresolved audit questions.

## 4. Assessment scope boundary

Likely in scope for definition: the visibility problem, source precedence rules, revision history and audit trail, role and ownership clarity, access rules, support ownership, and custom app build as the likely solution direction.

Clearly out of scope at this point: full HR leave-management replacement, travel expense redesign, enterprise attendance platform, and unrelated office automation.

## 5. Preferred path and option summary

Options considered: do nothing, simple shared tracker, structured Microsoft 365 tracker, and custom app.

Preferred path: define a full initiative and build a custom app with controlled workflow, role-based updates, precedence logic, and audit logging.

Why this path is better: it addresses the need without pretending the work is small, it fits the governance and audit burden better than a casual tracker, and it makes ownership and acceptance explicit before delivery.

## 6. Current-state, stakeholder, and analysis findings summary

The current state is split across itinerary approval, leave records, and informal communication. Key stakeholders have different needs: Jane wants speed, Angie wants governance, the Committee Secretary wants approved-record correctness, the HR leave owner wants leave handled from the correct source, the Programmer wants rule clarity, and Internal Audit / Records Management wants traceability.

Key findings: this is small in user count but not small in control complexity; the work is not just a visibility layer; a custom app is justified because the rules are specific and audit-sensitive; and source-of-truth plus acceptance questions must be surfaced early or the solution will not be trusted.

## 7. High-level requirements, capabilities, and work profile summary

The work definition should preserve a staff availability view across itinerary / leave / in-office states, latest valid record basis, visible revision handling, clear status distinctions, role-based access, visible precedence, and auditable change history.

Governance size signal: full initiative.

Reason: multiple stakeholder owners, multiple authoritative sources, role-based update rules, auditability concerns, and support ownership beyond the initial builder.

## 8. Major risks, dependencies, and viability considerations

Major risks: sponsor remains conditional on governance clarity, Outcome Owner remains to be confirmed, Acceptance Authority may need split acceptance, leave-status authority sits outside itinerary ownership, and a weaker solution could become a false system of record.

Dependencies: office operations leadership, committee secretariat, HR leave owner, security and privacy review, records management / audit review, and support ownership plus budget confirmation.

Viability: good if definition stays disciplined and the custom app is treated as a controlled answer to an explicit rule set.

## 9. Recommended definition focus and assessment reference basis

Work Definition must clarify who sponsors the work, who owns the business outcome, who accepts the solution, what the source-of-truth hierarchy is, what the status precedence rule is, who may create / revise / approve / override statuses, how audit logging works, and who owns support after launch.

Recommended next definition artifact: [Initiative Definition Document](../work_delivery/governance_and_control_deliverables/initiative_definition_document_specification.md).

Deliverables that appear needed in definition: Initiative Definition Document, Functional Capabilities, User Roles / Personas / Access Model, Business Rules Catalog, Non-Functional Requirements, Integration & External Dependency Specification, Technical Design Document, Operations and Support Model, Security and Privacy Risk Assessment, Access Control and Authorization Model, Audit and Monitoring Design Summary, and User Impact / Change and Communication planning.

Acceptance authority signals: business usefulness likely with the Office Operations Lead, record correctness and revision control likely with the Committee Secretary, leave-status governance with the HR leave owner, and audit / records concerns with a formal reviewer.

## 10. Work assessment recommendation

Recommendation: Proceed to Work Definition.

Conditions: use the Initiative Definition Document path, treat the solution as a custom app build unless definition proves otherwise, and do not start build until source-of-truth and acceptance questions are made visible and agreed.

## 11. Decision record

- Decision authority: simulated governance / sponsor authority
- Decision taken: proceed to Work Definition
- Decision date: 2026-04-10
- Evidence basis used: Initial Review, Validation Assessment, stakeholder interview notes
- Conditions / follow-up actions: confirm sponsor, confirm Outcome Owner, confirm Acceptance Authority arrangement, define source precedence and role-based update rules, confirm support ownership before mobilization
- Follow-up owner: Delivery Owner / Project Manager

## 12. Handoff references

- [00_request_context.md](00_request_context.md)
- [01_delivery_owner_framework_journal.md](01_delivery_owner_framework_journal.md)
- [02_stage_1_initial_review.md](02_stage_1_initial_review.md)
- [03_stage_1_validation_assessment.md](03_stage_1_validation_assessment.md)
- [05_path_and_artifact_rationale.md](05_path_and_artifact_rationale.md)
- [10_conversations_and_decisions.md](10_conversations_and_decisions.md)
