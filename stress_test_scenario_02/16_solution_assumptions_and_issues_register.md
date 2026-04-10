# Solution Assumptions And Issues Register - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 to Stage 5
Reference baseline: [Initiative Definition Document](08_initiative_definition_document.md)

## 1. Register overview

This register keeps the open assumptions, issues, and risks visible while the solution is defined and mobilized.

## 2. Register

| Item ID | Type | Description | Impact | Related artifacts | Owner | Status | Target resolution | Resolution summary / Decision reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AI-001 | Assumption | HR can provide controlled read access or a safe refresh of leave status | If false, the combined view cannot be shown safely | FC-002, INT-001, DG-001 | HR Leave Records Owner | Under investigation | Stage 4 | Needs confirmation from HR |
| AI-002 | Assumption | The Committee Secretary can expose itinerary approval status and revision identifiers | If false, itinerary status cannot be trusted | FC-001, FC-004, INT-002 | Committee Secretary | Under investigation | Stage 4 | Needs confirmation from itinerary owner |
| AI-003 | Issue | The tracker must not become a second source of truth | Governance, trust, and support risk | BR-005, DG-003 | Delivery Owner | Resolved | Stage 2 | Captured in baseline and business rules |
| AI-004 | Issue | Leave status detail must be limited to avoid unnecessary exposure | Privacy risk | DG-001, FC-002 | HR Leave Records Owner | Open | Stage 4 | To be defined with access model |
| AI-005 | Risk | Stale source data could misstate availability | Operational risk | FC-007, BR-004 | IT Service Owner | Open | Stage 5 | Freshness flag and refresh checks required |
| AI-006 | Assumption | A stable employee identifier exists across HR and itinerary records | Wrong matching would create false status | INT-001, INT-002, INT-003 | IT Service Owner | Under investigation | Stage 4 | Needs confirmation from source owners |
| AI-007 | Issue | Combined status wording could be misread as formal approval | Reputational and process risk | FC-001 to FC-007 | Angie | Open | Stage 5 | Needs display wording control |

## 3. Maintenance note

Items that become decisions should move to the Decision Record Log rather than stay here.

