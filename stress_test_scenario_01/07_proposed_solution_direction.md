# Proposed Solution Direction

Status: working draft  
Purpose: capture the Delivery Owner's practical solution direction without pretending detailed design is already authorized.

## 1. Delivery Owner recommendation

Preferred first-release direction:

- implement a structured Microsoft 365-based visibility tracker
- treat it as a reporting and coordination view, not as a new system of record

Why this direction:

- faster than a custom build
- more controlled than a shared spreadsheet
- proportionate to the current request size
- better able to show status, permissions, and change history than an unmanaged sheet

## 2. What the first release should do

The first release should let office staff answer:

- is the staff member on an approved itinerary
- is the staff member on leave / vacation
- is the staff member otherwise expected in the office
- when is the next known return or office date
- is the visible itinerary status based on the latest approved record

## 3. Proposed status model

### 3.1. Availability categories

- On approved itinerary
- On leave / vacation
- Expected in office
- Status unclear / pending verification

### 3.2. Itinerary record states

Where itinerary detail is shown, the working note assumes:

- Pending approval
- Approved
- Revised pending approval
- Revised approved
- Cancelled
- Completed

## 4. Source-of-truth recommendation

Working recommendation:

- the approved itinerary record remains the source of truth for itinerary status
- the leave record remains the source of truth for leave / vacation status
- the tracker is the visibility layer that resolves what to display from those authoritative inputs

This keeps the first release proportionate, but it also means the Delivery Owner has to keep the record owners visible.

## 5. Revision-handling recommendation

- a revision should not silently overwrite the fact that an earlier version existed
- the displayed current itinerary should point to the latest approved version
- if a revision is pending but not yet approved, the tracker should not label it as approved
- users should be able to tell whether they are looking at current approved status or a pending change

## 6. Minimum data shown in the tracker

For the office visibility view, show only the minimum needed to coordinate work:

- staff member
- current availability category
- itinerary status, if applicable
- leave status, if applicable
- next known return / office date
- last approved / authoritative update date
- record source indicator

Do not show extra fields unless they are needed for the stated use case.

## 7. Major unresolved decisions before execution

- Who exactly is the operational owner after go-live?
- Who is the final acceptance authority for the first release?
- Does one authority accept both usefulness and record correctness, or is acceptance split?
- Who owns the leave-side source data?
- Who is allowed to request, encode, revise, or override status updates?

## 8. Why the Delivery Owner stopped here

The framework helped narrow the solution direction, but it did not eliminate the need for human decisions on ownership and source of truth.

Stopping here is intentional:

- enough direction exists to mobilize
- not enough control clarity exists to pretend execution has started
- the first release remains small, but still governed
