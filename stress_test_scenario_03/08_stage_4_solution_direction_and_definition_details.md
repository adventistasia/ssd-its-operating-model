# Stage 4 Solution Direction and Definition Details

Status: working draft  
Stage: Stage 4 - Work Definition Details  
Reference: [Project Charter](07_stage_3_project_charter.md)

## 1. Proposed solution direction

The preferred solution direction is a custom application that acts as a controlled availability status layer over the official itinerary and leave sources.

Why this direction:

- a shared tracker is too weak for the precedence and audit requirements
- the request needs explicit role-based update rules
- multiple authoritative sources need a controlled display and conflict model
- sponsor willingness remains conditional on governance, not convenience

The app should not replace the underlying authoritative records. It should display and govern their combined operational meaning.

## 2. Functional capabilities

| FC-ID | Capability statement | Business value | Primary role or beneficiary | Notes |
| --- | --- | --- | --- | --- |
| FC-001 | Staff can view a current availability status for a person. | Reduces manual follow-up. | Office staff | Shows itinerary, leave, or expected-in-office state. |
| FC-002 | The app can show the latest approved itinerary status. | Prevents outdated itinerary visibility. | Office staff and committee secretariat | Must preserve approved version history. |
| FC-003 | The app can show leave status from the leave source. | Keeps leave ownership clear. | Office staff and HR owner | Leave is not inferred from itinerary data. |
| FC-004 | The app can apply status precedence when sources conflict. | Avoids ambiguity. | Office staff and reviewers | Precedence rule must be explicit. |
| FC-005 | Authorized roles can create, revise, approve, or override status. | Keeps control with named owners. | Committee secretary, HR owner, delegates | Access is role-based. |
| FC-006 | The app records history and an audit trail for changes. | Supports audit and dispute resolution. | Internal audit and records management | No silent overwrite. |
| FC-007 | The app can surface status exceptions or conflicts for review. | Prevents false certainty. | Approvers and support staff | Conflict states must be visible. |
| FC-008 | The app can support a supportable handover to IT operations. | Prevents key-person dependency. | IT Operations / Service Owner | Includes support notes and ownership. |

## 3. User roles, personas, and access model

| Role | Business purpose | Goals or user needs | Main actions | Decision or approval authority | Access boundary | Data sensitivity or control notes | Related IDs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Office staff user | Needs visibility to staff availability. | Check current status quickly. | View availability | No approval authority | View only; no edits | Can see only approved visibility fields | FC-001, FC-004, FC-007 |
| Jane, Administrative Assistant | Requestor and frequent operational user. | Reduce follow-up and coordination time. | View status, raise issues | No approval authority | View only; limited admin input if delegated | Should not edit authoritative records | FC-001, FC-006 |
| Committee Secretary | Owns the itinerary approval record. | Keep itinerary truth correct. | Create, revise, approve itinerary status | Approval authority for itinerary changes | Can edit itinerary source records | Highest itinerary correctness sensitivity | FC-002, FC-005, FC-006 |
| HR Leave Records Owner | Owns leave status source. | Keep leave records correct and private. | Create, revise, approve leave status | Approval authority for leave changes | Can edit leave source records | Personal data and privacy sensitive | FC-003, FC-005, FC-006 |
| Office Operations Lead | Outcome Owner candidate. | Reduce confusion and improve coordination. | Review status outcomes, accept usefulness | Business acceptance authority candidate | Read-only on source records; may approve business rules | Owns usefulness, not source correction | FC-001, FC-004, FC-007 |
| Delivery Owner / PM | Governs stage discipline and traceability. | Keep work controlled and visible. | Coordinate, log decisions, manage readiness | Stage governance authority | No source ownership; oversight only | Must not become shadow owner of data truth | FC-006, FC-008 |
| Programmer / Technical SME | Designs and builds the app. | Implement rule logic safely. | Configure, code, test | No business approval authority | Technical implementation access only | Must not approve scope or record truth | FC-001 to FC-008 |
| Internal Audit / Records Management | Reviews evidence and traceability. | Confirm records and history are defensible. | Review logs, evidence, and retention | Audit review authority | Read-only review access | Sensitive because it validates control quality | FC-006, FC-007 |
| Security / Privacy reviewer | Reviews access and privacy controls. | Reduce unnecessary disclosure. | Review access model and logging | Security review authority | Review access only | Highest sensitivity around personal status data | FC-003, FC-005, FC-006 |

## 4. Business rules catalog

### BR-001 - Latest approved itinerary is controlling

- Rule statement: The latest approved itinerary record controls itinerary status display unless a later approved revision exists.
- Rationale / Policy basis: Approved itinerary records must remain authoritative and traceable.
- Affected modules / use cases: FC-002, FC-004, FC-006
- Decision impact: prevents older itinerary versions from being shown as current.
- Validation & evidence: test with revised approved and pending records.
- Notes: pending revisions must not replace approved status.

### BR-002 - Leave status comes from the leave owner

- Rule statement: Leave status is sourced only from the HR leave record owner or an explicitly delegated role.
- Rationale / Policy basis: leave data has its own ownership and privacy obligations.
- Affected modules / use cases: FC-003, FC-005, FC-006
- Decision impact: prevents itinerary users from inventing leave status.
- Validation & evidence: access tests and change history review.
- Notes: leave cannot be inferred from itinerary absence.

### BR-003 - Conflicts must be visible

- Rule statement: When itinerary status and leave status conflict or overlap, the app must show both and display the precedence outcome.
- Rationale / Policy basis: false certainty is worse than visible conflict.
- Affected modules / use cases: FC-001, FC-004, FC-007
- Decision impact: users can see when a status needs review.
- Validation & evidence: conflict-state scenario tests.
- Notes: conflict view is a control feature, not a defect workaround.

### BR-004 - No silent overwrite

- Rule statement: A new revision must not silently erase the prior approved history.
- Rationale / Policy basis: auditability and records traceability.
- Affected modules / use cases: FC-002, FC-006
- Decision impact: preserves revision lineage.
- Validation & evidence: version-history review.
- Notes: both current and historical records must be discoverable by reviewers.

### BR-005 - Role-based edit rights

- Rule statement: Only named roles may create, revise, approve, or override controlled status records.
- Rationale / Policy basis: explicit ownership and separation of duties.
- Affected modules / use cases: FC-005, FC-006
- Decision impact: limits unauthorized edits.
- Validation & evidence: permission matrix test.
- Notes: delegated rights must be recorded.

### BR-006 - Overrides require logging

- Rule statement: Any manual override must record the role, date, reason, and reviewer.
- Rationale / Policy basis: audit and accountability.
- Affected modules / use cases: FC-005, FC-006, FC-007
- Decision impact: prevents hidden exceptions.
- Validation & evidence: audit log verification.
- Notes: no undocumented override path.

## 5. Non-functional requirements

### QA-001 - Response time

- Attribute / category: performance
- Target / threshold: 95 percent of status lookups return in under 2 seconds during normal office use
- Applies to: FC-001, FC-002, FC-003, FC-004
- Measurement & monitoring: application telemetry and test results
- Notes: office coordination depends on quick lookups.

### QA-002 - Availability

- Attribute / category: availability
- Target / threshold: 99.5 percent monthly availability during business hours
- Applies to: all user-facing functions
- Measurement & monitoring: uptime monitoring
- Notes: this is an internal service, not a public customer portal.

### QA-003 - Auditability

- Attribute / category: audit logging
- Target / threshold: 100 percent of status-affecting changes are attributable to a role, record, and timestamp
- Applies to: FC-005, FC-006, FC-007
- Measurement & monitoring: log review and change reconciliation
- Notes: no unlogged administrative bypass.

### QA-004 - Privacy and access control

- Attribute / category: security and privacy
- Target / threshold: minimum necessary visibility by role, with default deny for edit rights
- Applies to: all personal-status functions
- Measurement & monitoring: access review and test accounts
- Notes: leave data must not be overshared.

### QA-005 - Supportability

- Attribute / category: maintainability and support
- Target / threshold: the app can be supported by IT operations and documented without dependence on the original programmer
- Applies to: all modules
- Measurement & monitoring: operations handover review
- Notes: key-person dependency is a control risk.

## 6. Integration and external dependencies

| INT-ID | Name / System | Purpose | Data exchanged | Protocol / interface | Frequency / timing | Owner | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| INT-001 | Itinerary approval record source | Provide authoritative itinerary status | itinerary approvals, revisions, dates | controlled application or records interface | as records change | Committee Secretary / records owner | controlling source for itinerary truth |
| INT-002 | HR leave record source | Provide authoritative leave status | leave status, leave dates, approvals | controlled HR record source | as records change | HR Leave Records Owner | personal data; privacy sensitive |
| INT-003 | Identity / directory service | Resolve user roles and access | user identity, role membership | directory / SSO integration | at login and on role sync | IT Operations | required for role-based access |
| INT-004 | Notification service | Send status or exception alerts | change alerts, exception notices | email or messaging service | event-driven | IT Operations | useful for change awareness |

## 7. Definition and delivery notes

The Stage 4 definition set should include a module for status capture and precedence, a module for staff-facing status display, a module for authoritative source synchronization, a module for administrative review and exception handling, and a module for audit and history review.

The solution direction is intentionally custom-app oriented because the rule set is too specific for a weak visibility layer.

## 8. Stage 4 decision record

- Decision taken: proceed with custom app definition
- Decision authority: Delivery Owner with sponsor awareness
- Decision date: 2026-04-10
- Evidence basis used: Stage 1 assessment, sponsor willingness, stakeholder input, rule complexity
- Conditions / cautions: no scope expansion beyond the approved problem, no hidden change to the authoritative source model, and no build until Stage 5 mobilization controls are ready
