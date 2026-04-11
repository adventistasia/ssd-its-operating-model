# Functional Capabilities - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 2 - Work Definition
Reference baseline: [Initiative Definition Document](08_initiative_definition_document.md)

## 1. Scope note

This baseline controls the approved solution scope for the staff itinerary tracker. It is a controlled visibility layer over authoritative records, not a second system of record.

## 2. Scope notes

### 2.1. Outcome statement

Office staff need one trusted view of staff availability so they can quickly see itinerary, leave, and expected office status.

### 2.2. In-scope summary

- display current availability status
- distinguish itinerary, leave, and office expectation
- show latest approved itinerary basis
- show next known return or office date where available
- show revision visibility for itinerary changes
- respect access boundaries for leave-related information

### 2.3. Out-of-scope summary

- travel approval redesign
- leave approval redesign
- attendance management
- duplicate encoding of source records

### 2.4. Material exclusions, assumptions, or dependencies

- authoritative itinerary and leave records already exist
- the solution may consume controlled source data, but it must not replace the source owners
- privacy and access boundaries are required

## 3. Capability table

| Capability ID | Capability statement | Business value | Primary role or beneficiary | Notes |
| --- | --- | --- | --- | --- |
| FC-001 | Staff can view whether a person is on an approved itinerary. | Supports coordination and travel awareness. | Office staff | Must point to the latest approved record. |
| FC-002 | Staff can view whether a person is on leave or vacation. | Reduces unnecessary follow-up and wrong assumptions. | Office staff | Leave data remains HR-controlled. |
| FC-003 | Staff can view whether a person is expected in the office. | Improves meeting planning and follow-up timing. | Office staff | This is a derived availability view, not a new authority. |
| FC-004 | Staff can see the latest approved status basis and revision visibility. | Prevents stale or unofficial status display. | Office staff, Committee Secretary | Revision history must stay visible. |
| FC-005 | The tracker can present one combined availability view without duplicating the source records. | Reduces manual reconciliation and duplicate encoding. | Office staff, Data Steward | The view is an aggregator, not a source of truth. |
| FC-006 | Authorized roles can maintain the underlying source records in their own owning process, not in the tracker. | Preserves record authority and control. | HR Leave Records Owner, Committee Secretary | Read access and maintenance rights are separate. |
| FC-007 | The tracker can flag stale or unverified data when source freshness is unclear. | Reduces the risk of acting on outdated information. | Office staff | Requires agreed freshness rules. |
