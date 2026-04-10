# Initiative Definition Document - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 2 - Work Definition
Document basis: [Work Assessment Report](06_stage_1_work_assessment_report.md)

## 1. Document identity and control

- Initiative name: SSD staff itinerary tracker
- Initiative ID: IDD-SSD-2026-001
- Version: 0.1
- Status: Draft
- Last updated: 2026-04-10
- Outcome Owner: Angie, office operations decision-maker
- Delivery Owner: Delivery Owner / Project Manager
- Sponsor: Angie
- Decision Authority: Angie acting as delegated office operations decision authority
- Change log: created from Stage 1 assessment outputs for scenario 02

## 2. Executive summary

This initiative will create a controlled visibility layer for SSD staff availability so office staff can quickly see whether a staff member is on an approved itinerary, on leave, or expected in the office.

The work exists because current availability checking is fragmented, informal, and unreliable. The initiative is not trying to replace HR leave ownership or formal itinerary approval ownership. It is trying to make those authoritative records visible in one trusted view.

This is a medium-complexity governed item because it crosses office operations, HR data ownership, itinerary approval ownership, and support ownership.

## 3. Business need and rationale

### 3.1. Current problem

Office staff spend time reconstructing availability from chats, email, and separate records. That creates delays, confusion, and repeated follow-up.

### 3.2. Who is affected

- secretarial and administrative staff
- travelers
- HR leave records owner
- Committee Secretary and itinerary approval support staff
- office leaders who schedule meetings or follow-up work

### 3.3. Why action is justified

The problem is recurring, visible, and operationally wasteful. A controlled visibility layer will reduce confusion without changing the underlying formal ownership of the source records.

### 3.4. Consequences of inaction

Without action, staff will continue to rely on informal parallel views and the organization will continue to lose time reconciling status.

## 4. Outcomes and success measures

### 4.1. Intended outcomes

- one trusted office view for staff availability
- clear distinction between itinerary, leave, and in-office states
- no duplicate encoding of the same authoritative status
- visible revision history where itinerary status changes
- controlled access to leave-related information

### 4.2. Success measures

- office staff can find current status without multiple follow-ups
- status shown in the view is traceable to the source owner record
- itinerary revisions remain visible
- leave data remains HR-controlled
- the solution remains low-maintenance and supportable

### 4.3. Non-goals

- this is not a travel approval redesign
- this is not a leave-management redesign
- this is not an attendance system
- this is not a new system of record

## 5. Scope boundaries

### 5.1. In scope

- staff availability visibility for itinerary, leave, and office expectation
- latest approved itinerary status
- next known office or return date where available
- revision visibility for itinerary changes
- read-only or controlled update access based on role
- authoritative source references rather than duplicate records

### 5.2. Out of scope

- expense liquidation
- leave approval redesign
- committee approval workflow redesign
- broad workforce management reporting
- custom app build if a controlled visibility layer is sufficient

### 5.3. Assumptions

- formal itinerary approval records exist
- HR leave records exist and are governed separately
- office staff need visibility more than they need transactional editing
- the first release can be built around existing controlled records

### 5.4. Constraints

- leave data must remain HR-controlled
- itinerary approval status must remain authoritative to the committee record owner
- the solution must not become a second source of truth
- privacy and access boundaries must be explicit

## 6. Deliverables and acceptance structure

| Deliverable or domain | Description | Delivery Owner | Acceptance Authority | Acceptance focus | Status | Reference |
| --- | --- | --- | --- | --- | --- | --- |
| Functional Capabilities | Approval-level business abilities the solution must provide | Delivery Owner | Angie | Scope is clear and bounded | Planned | [10_functional_capabilities.md](10_functional_capabilities.md) |
| User Roles, Personas and Access Model | Roles, personas, and access boundaries | Delivery Owner | HR Leave Records Owner and Committee Secretary | Actors and permissions are explicit | Planned | [11_user_roles_personas_access_model.md](11_user_roles_personas_access_model.md) |
| Business Rules Catalog | Core decision and status rules | Delivery Owner / Technical SME | HR Leave Records Owner and Committee Secretary | Rules are unambiguous and traceable | Planned | [12_business_rules_catalog.md](12_business_rules_catalog.md) |
| Integration and External Dependency Specification | Data sources and external dependencies | Delivery Owner / Technical SME | HR Leave Records Owner, Committee Secretary, IT Service Owner | Dependencies and failure handling are clear | Planned | [13_integration_and_external_dependency_specification.md](13_integration_and_external_dependency_specification.md) |
| Data Governance and Impact Assessment | Data categories, stewardship, and lifecycle impacts | Delivery Owner | HR Leave Records Owner / Data Steward | Data obligations are explicit | Planned | [14_data_governance_and_impact_assessment.md](14_data_governance_and_impact_assessment.md) |
| Security and Privacy Risk Assessment | Threats, privacy issues, and controls | Delivery Owner | Security / Privacy reviewer | Risks and controls are visible | Planned | [15_security_and_privacy_risk_assessment.md](15_security_and_privacy_risk_assessment.md) |
| Decision Record Log | Material decisions across the initiative | Delivery Owner | Angie | Decisions are traceable and current | Planned | [17_decision_record_log.md](17_decision_record_log.md) |
| Solution Assumptions and Issues Register | Open assumptions, issues, and risks | Delivery Owner | Angie / domain owners | Unknowns are tracked to resolution | Planned | [16_solution_assumptions_and_issues_register.md](16_solution_assumptions_and_issues_register.md) |
| Project Charter | Stage 3 authorization record | Delivery Owner | Angie | Formal approval basis is visible | Planned | [18_project_charter.md](18_project_charter.md) |
| Delivery Roadmap | Stage-by-stage delivery sequence and readiness plan | Delivery Owner | Angie and delivery team leads | Sequence, dependencies, and readiness are visible | Planned | [19_delivery_roadmap.md](19_delivery_roadmap.md) |
| Delivery Charter | Stage 5 operating agreement | Delivery Owner | Angie and delivery team leads | Mobilization controls are ready | Planned | [20_delivery_charter.md](20_delivery_charter.md) |

## 7. Key risks, dependencies, and major impacts

### 7.1. Major risks

- a combined status view could be mistaken for a second system of record
- leave data could be exposed too broadly
- itinerary revision logic could be oversimplified
- ownership could be blurred between HR, committee support, and office operations

### 7.2. Dependencies

- HR leave records owner agreement
- Committee Secretary agreement on itinerary status source
- IT support agreement on the hosting and support path
- a stable employee identifier across records
- sponsor agreement on the low-maintenance control model

### 7.3. Major impacts

- improves office coordination
- creates a small but real data-governance obligation
- introduces access-control and audit expectations
- needs named operational support ownership

## 8. Operational support summary

- Service Owner: IT Service Owner / Support Lead
- Support Owner: IT Service Owner / Support Lead
- Business correctness owner: HR Leave Records Owner for leave data and Committee Secretary for itinerary approvals
- Support expectation: the live solution must be supportable without relying on the Delivery Owner
- Monitoring and recovery intent: status issues, access issues, and source-refresh failures must be visible and recoverable

## 9. Related references and supporting decisions

- [06_stage_1_work_assessment_report.md](06_stage_1_work_assessment_report.md)
- [09_conversations_and_decisions.md](09_conversations_and_decisions.md)
- [10_functional_capabilities.md](10_functional_capabilities.md)
- [11_user_roles_personas_access_model.md](11_user_roles_personas_access_model.md)
- [12_business_rules_catalog.md](12_business_rules_catalog.md)
- [13_integration_and_external_dependency_specification.md](13_integration_and_external_dependency_specification.md)
- [14_data_governance_and_impact_assessment.md](14_data_governance_and_impact_assessment.md)
- [15_security_and_privacy_risk_assessment.md](15_security_and_privacy_risk_assessment.md)
