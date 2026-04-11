# Data Governance And Impact Assessment - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 - Work Definition Details
Reference baseline: [Functional Capabilities](10_functional_capabilities.md)

## 1. Assessment context

- Initiative or solution name: SSD staff itinerary tracker
- Scope of data handling being assessed: itinerary status, leave status, staff identity, revision metadata, and display timestamps
- Date or version: 2026-04-10 / working draft
- Assessment owner: Delivery Owner / Project Manager

## 2. Data categories and sensitivity

- staff identity data
- itinerary approval status and revision metadata
- leave status and leave date ranges
- display timestamps and freshness indicators

Sensitivity view:

- staff identity is internal operational data
- itinerary status is controlled operational data
- leave status is personal and controlled HR data
- revision and freshness metadata are internal control data

## 3. Governance and obligation impacts

- HR remains the owner of leave data and the associated privacy handling
- Committee Secretary remains the owner of itinerary approval authority
- the tracker is an operational view and must not become a second source of truth
- retention and traceability are needed so the combined view can be explained later
- auditability matters because staff may rely on the display to make scheduling decisions

## 4. Accountability and stewardship

- Data Steward: Data Steward / Records Custodian
- Operational custody: IT Service Owner / Support Lead
- Business ownership: Angie for the combined outcome, HR for leave data, Committee Secretary for itinerary data
- Ownership split: the combined view is owned as a solution, but the underlying records stay with their source owners

## 5. Risks, issues, and required actions

| Item ID | Type | Description | Impact | Related artifacts | Owner | Status | Target resolution | Resolution summary / Decision reference |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| DG-001 | Issue | Confirm how much leave status can be displayed without exposing unnecessary detail | Privacy and access risk | FC-002, FC-005, BR-002 | HR Leave Records Owner | Open | Stage 4 | To be resolved before mobilization |
| DG-002 | Assumption | A stable employee identifier exists across HR and itinerary records | Wrong matching would create false status | INT-001, INT-002, INT-003 | IT Service Owner | Under investigation | Stage 4 | Needs confirmation from source owners |
| DG-003 | Issue | The tracker must not become a second system of record | Governance and trust risk | FC-005, BR-005 | Delivery Owner | Resolved | Stage 2 | Captured in the initiative baseline and business rules |
| DG-004 | Risk | Combined status could be interpreted as a formal approval statement | Operational and reputational risk | FC-001 to FC-007 | Angie | Open | Stage 5 | To be controlled by display wording and role boundaries |
