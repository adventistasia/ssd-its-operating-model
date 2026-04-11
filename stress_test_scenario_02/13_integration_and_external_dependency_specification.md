# Integration And External Dependency Specification - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 - Work Definition Details
Reference baseline: [Functional Capabilities](10_functional_capabilities.md)

## 1. Integration summary

| INT-### | Name / System | Purpose | Data exchanged | Protocol / interface | Frequency / timing | Owner | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| INT-001 | HR leave records source | Provide authoritative leave status | Leave status, dates, employee identifier, last updated time | Controlled internal record access | As needed / scheduled refresh | HR Leave Records Owner | Leave data remains HR-controlled |
| INT-002 | Itinerary approval source | Provide authoritative itinerary status | Approved itinerary status, revision, dates, employee identifier, approval metadata | Controlled internal record access | As needed / event or scheduled refresh | Committee Secretary | Formal approval source of record |
| INT-003 | Staff identity source | Match the right staff member across records | Staff identifier, name, department, role | Internal directory lookup | On lookup / refresh | IT Service Owner | Needed to avoid duplicate identity mapping |

## 2. Detailed dependency notes

### INT-001 - HR leave records source

- **Description and purpose:** Supplies the approved leave signal used in the combined availability view.
- **Data exchanged:** leave status, date range, employee identifier, and last updated time.
- **Interface details:** controlled access to HR-owned data; no duplicate manual encoding inside the tracker.
- **Timing and frequency:** refresh should be frequent enough that the view is useful for office coordination; the exact interval is a design decision.
- **Operational behavior:** if the leave feed is unavailable, the tracker should show leave status as unavailable or stale rather than guessing.
- **Ownership and SLAs:** HR owns the source data quality and timeliness.
- **Monitoring and alerting:** stale or missing refresh should be visible to support.
- **Security and compliance:** leave data is sensitive and must follow least privilege.
- **Testing and validation:** confirm read access, update frequency, and stale-data flagging.
- **Assumptions and dependencies:** HR will allow controlled visibility but keep ownership.

### INT-002 - Itinerary approval source

- **Description and purpose:** Supplies the approved itinerary signal and revision basis.
- **Data exchanged:** itinerary approval state, revision identifier, dates, and approval metadata.
- **Interface details:** controlled access to the formal approval record; no informal status entry.
- **Timing and frequency:** refresh should reflect the latest approved revision.
- **Operational behavior:** if the itinerary source is unavailable, the tracker should mark itinerary status as stale or unknown.
- **Ownership and SLAs:** Committee Secretary or delegated approval owner owns the record authority.
- **Monitoring and alerting:** missing refresh or revision mismatch should be visible.
- **Security and compliance:** approval records are controlled operational records.
- **Testing and validation:** confirm latest-revision behavior and history visibility.
- **Assumptions and dependencies:** revision history remains available from the source record path.

### INT-003 - Staff identity source

- **Description and purpose:** Ensures the tracker maps the right employee to the right leave and itinerary records.
- **Data exchanged:** staff identifier, name, department, role.
- **Interface details:** internal directory or roster lookup.
- **Timing and frequency:** on view load or periodic refresh.
- **Operational behavior:** mismatched identifiers should block or flag the view rather than silently combine the wrong records.
- **Ownership and SLAs:** IT Service Owner maintains the identity source path.
- **Monitoring and alerting:** unmatched identity records should be visible to support.
- **Security and compliance:** identity data should be handled under normal internal access controls.
- **Testing and validation:** confirm one staff record maps to one combined availability view.
- **Assumptions and dependencies:** the source systems share a stable employee identifier.

## 3. Overall considerations

- the solution depends more on authoritative record access than on heavy technical integration
- failure to keep the identity mapping clean would create false status
- the solution should degrade by flagging stale or unavailable source data rather than inventing status
- the combined view is only trustworthy if the source owners remain visible and accountable
