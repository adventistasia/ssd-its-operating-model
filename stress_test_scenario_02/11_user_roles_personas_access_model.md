# User Roles, Personas And Access Model - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 - Work Definition Details
Reference baseline: [Functional Capabilities](10_functional_capabilities.md)

## 1. Document header and scope note

This model defines who uses the solution, what each role needs to do, and what access boundaries apply.

The scope covered by this model is the staff itinerary tracker visibility layer and the controlled source records it reads from.

## 2. Role catalog

| Role | Business purpose | Goals or user needs | Main actions | Decision or approval authority | Access boundary | Data sensitivity or control notes | Related IDs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Office staff consumer | Check staff availability for meetings and follow-up | Wants a fast trusted answer | View status, search staff, read current basis | No approval authority | Read-only, limited to approved visibility view | Should not see unnecessary leave detail | FC-001, FC-002, FC-003 |
| Jane, requestor / administrative coordinator | Represents the day-to-day office user | Wants low-friction coordination | Raise need, review usability, confirm fit | No approval authority | Read-only user for the tracker | Needs a simple, trustworthy interface | FC-001, FC-005 |
| Angie, sponsor / office operations decision-maker | Owns the business outcome | Wants coordination value without new bureaucracy | Sponsor the work, confirm outcome fit, approve baseline | Approval authority for the initiative baseline | Governance access only | Must not be treated as the source owner for leave or itinerary records | FC-001 to FC-007 |
| Committee Secretary | Owns formal itinerary approval records | Wants itinerary status to remain authoritative | Confirm itinerary basis, confirm revision trail | Authority over itinerary record interpretation | Can validate itinerary source and revision mapping | Formal approval status is control-sensitive | FC-001, FC-004, FC-006 |
| HR Leave Records Owner | Owns leave status data | Wants leave data to stay controlled by HR | Confirm leave source and visibility rules | Authority over leave data interpretation | Can validate leave source and access rules | Leave status is personal and controlled | FC-002, FC-005, FC-006 |
| Programmer / Technical SME | Shapes the technical solution | Wants feasible, maintainable implementation | Configure, integrate, troubleshoot | No business approval authority | Technical access only as required for delivery | Must not redefine business ownership | FC-005, FC-007 |
| Data Steward / Records Custodian | Protects record integrity and traceability | Wants clear record trail and retention discipline | Review traceability, confirm record boundaries | Governance review authority | Review access to metadata and control evidence | Must preserve source ownership and retention logic | FC-004, FC-005 |
| IT Service Owner / Support Lead | Owns live service support | Wants a supportable live service | Accept handoff, support issues, monitor health | Support approval authority | Operational access as support requires | Support ownership is separate from record ownership | FC-005, FC-007 |

## 3. Relationship and control notes

- Angie sponsors and approves the initiative baseline, but she does not own the HR or committee source records.
- Committee Secretary and HR Leave Records Owner are the domain authorities for their respective records.
- The Programmer may implement or configure the solution, but cannot decide source authority.
- The Data Steward keeps record traceability visible and warns against hidden duplication.
- IT Service Owner owns live support after handoff.

## 4. Access model

| Role | Resource or function | Allowed actions | Restricted actions | Conditions or limits | Approval or review basis | Audit notes | Related IDs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Office staff consumer | Availability view | Search, view, filter | Edit, approve, overwrite source data | Read-only | Business-approved access | View access should be logged | FC-001 to FC-007 |
| Jane, requestor / administrative coordinator | Tracker view | Search, view, provide feedback | Maintain authoritative records | Read-only unless separately delegated | Sponsorship review | User feedback should not become authority | FC-001, FC-005 |
| Angie, sponsor | Initiative baseline and summary status | Review, approve baseline, review progress | Change source records casually | Governance access only | Sponsor decision rights | Approval actions logged | FC-001 to FC-007 |
| Committee Secretary | Itinerary source status and mapping | Validate, confirm revisions, confirm authority | Change HR leave data | Must retain itinerary ownership | Committee record authority | Source changes remain in the original record path | FC-001, FC-004, FC-006 |
| HR Leave Records Owner | Leave source status and mapping | Validate, confirm visibility rules | Change itinerary approval records | Must retain HR ownership | HR governance review | Access to leave data is controlled | FC-002, FC-006 |
| Programmer / Technical SME | Technical configuration area | Configure, test, troubleshoot | Approve business scope or override authority | Least privilege, task-bound | Delivery Owner review | Technical changes should be attributable | FC-005, FC-007 |
| IT Service Owner / Support Lead | Live support controls | Monitor, support, recover | Redefine business rules | Support-only access | Support handoff approval | Operational access should be logged | FC-005, FC-007 |
