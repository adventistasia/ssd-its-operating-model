# Initiative Definition Document - SSD Staff Itinerary Status Control App

Status: working draft  
Stage: Stage 2 - Work Definition  
Reference: [Work Assessment Report](04_stage_1_work_assessment_report.md)

## 1. Document identity and control

- Initiative name: SSD Staff Itinerary Status Control App
- Initiative ID: IDD-SSD-2026-001
- Version: 0.1
- Status: Draft
- Last updated: 2026-04-10
- Outcome Owner: Office Operations Lead (provisional)
- Delivery Owner: Delivery Owner / Project Manager (simulated)
- Sponsor: Angie, Sponsor and budget holder (provisional)
- Sponsoring body: SSD office operations governance
- Decision Authority: simulated sponsor / governance authority
- Authorization record or reference: [04_stage_1_work_assessment_report.md](04_stage_1_work_assessment_report.md)

## 2. Executive summary

This initiative will create a controlled custom app for SSD staff itinerary and availability status so office staff can see the latest approved itinerary status, leave status, and expected office status in one trusted view.

Why the initiative exists now:

- office staff are spending time reconciling multiple sources
- itinerary revisions happen often enough that status can go stale
- leave records are managed in a separate control path
- current practice does not make status precedence or audit trail visible

Intended outcome:

- a single controlled app that shows availability status accurately, with role-based updates, visible history, and auditable precedence logic

High-level delivery statement:

- build a custom status control app, not a casual spreadsheet tracker

## 3. Business need and rationale

The office cannot reliably answer a simple question: what is the current authoritative status for a staff member when itinerary, leave, and office attendance signals do not align?

Affected parties include office operations staff, secretarial staff, travelers, managers scheduling meetings, committee secretariat staff, HR leave records owners, finance staff, and audit or records management reviewers.

Action is justified because repeated manual reconciliation wastes time, status disputes create friction, and revision history plus auditability need to be explicit.

## 4. Outcomes and success measures

Intended outcomes:

- one trusted staff availability view
- clear source precedence across itinerary and leave status
- role-based update rules
- visible revision history
- auditable change trail
- supportable ownership after delivery

Success measures:

- staff can tell whether a person is on itinerary, on leave, or expected in office
- the latest approved status is visible without reconstructing history
- changes are attributable to a role and a record
- the office no longer relies on ad hoc messages as the primary status source
- support staff can explain the status logic without consulting the programmer

## 5. Scope boundaries

In scope:

- controlled itinerary and availability status app
- role-based create / revise / approve / override rules
- precedence logic when multiple authoritative sources exist
- revision history and audit trail
- staff-facing status view
- admin and governance views
- support and operational handover requirements

Out of scope:

- leave system replacement
- expense liquidation redesign
- attendance management redesign
- unrelated office workflow automation

Assumptions:

- official itinerary approval records are available
- official leave records are available
- the app will integrate with or reference those sources rather than replace them

Constraints:

- personal status information must be protected
- rule ownership must be explicit
- audit trail is not optional
- support ownership must be named before go-live

## 6. Deliverables and acceptance structure

| Deliverable or domain | Description | Delivery Owner | Acceptance Authority | Acceptance focus | Status | Reference |
| --- | --- | --- | --- | --- | --- | --- |
| Solution Deliverables | Functional scope, roles, rules, and behavior definition for the app | Delivery Owner with solution lead support | Office Operations Lead / Angie, depending on final acceptance model | Scope is clear, atomic, and traceable | Planned | Supporting Stage 4 artifacts |
| Governance and Control | Project Charter, Delivery Roadmap, decision log | Delivery Owner | Sponsor / governance authority | Authorization, funding, and governance are explicit | Planned | [07_stage_3_project_charter.md](07_stage_3_project_charter.md) |
| Operational Readiness | Technical design, support model, recovery, and readiness | Delivery Owner with IT Operations | IT Operations / Service Owner | Supportability and recoverability are explicit | Planned | Stage 4-5 readiness artifacts |
| Data Governance and Records | Data ownership, retention, and record handling | Delivery Owner with data steward | Data steward / records reviewer | Data stewardship and record rules are explicit | Planned | Stage 4 supporting artifacts |
| Security, Privacy and Compliance | Access, audit, and privacy controls | Delivery Owner with security reviewer | Security / privacy reviewer | Access, logging, and privacy are controlled | Planned | Stage 4 supporting artifacts |
| User Adoption and Change Enablement | Impact, communication, and training | Delivery Owner with change lead | Office Operations Lead | Users can adopt the new control model | Planned | Stage 4 supporting artifacts |

## 7. Key risks, dependencies, and major impacts

Major risks:

- the app becomes a false system of record
- leave and itinerary precedence is not understood
- a role can change data it should only view
- the app is delivered but cannot be supported sustainably

Dependencies:

- Committee Secretary for itinerary source rules
- HR leave owner for leave source rules
- Security / Privacy reviewer for access and data handling
- IT Operations / Service Owner for support ownership
- Finance or sponsor authority for budget release

Major impacts:

- new status control behavior for office staff
- clearer accountability for who can edit what
- explicit audit trail requirements
- support model needed beyond the initial build team

## 8. Operational support summary

- operational / run owner: IT Operations / Service Owner (provisional)
- support owner: IT support team (provisional)
- business data ownership: Office Operations Lead for usefulness; Committee Secretary and HR owner for source correctness
- support tier model: first-line support via office operations, second-line via IT support, source corrections returned to record owners
- monitoring / recovery intent: track status changes, failed updates, and access exceptions; maintain backup and restore expectations

## 9. Related references and supporting decisions

- [04_stage_1_work_assessment_report.md](04_stage_1_work_assessment_report.md)
- [05_path_and_artifact_rationale.md](05_path_and_artifact_rationale.md)
- [10_conversations_and_decisions.md](10_conversations_and_decisions.md)

## 10. Stage 2 decision record

- Decision requested: proceed from definition into authorization path for a custom app build
- Decision taken: proceed, subject to Stage 3 conditions
- Decision authority: simulated sponsor / governance authority
- Decision date: 2026-04-10
- Evidence basis used: Work Assessment Report, sponsor signal, stakeholder interviews
- Conditions / follow-up actions: confirm acceptance authority split, confirm support owner, confirm data and record ownership, confirm security and privacy review path
- Owner for follow-up: Delivery Owner / Project Manager
