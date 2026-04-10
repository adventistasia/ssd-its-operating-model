# Business Rules Catalog - SSD Staff Itinerary Tracker

Status: working draft
Stage: Stage 4 - Work Definition Details
Reference baseline: [Functional Capabilities](10_functional_capabilities.md)

## 1. Status and authority rules

### BR-001 - Approved itinerary status must come from the itinerary owner record

- **Rule statement:** The tracker must treat the Committee Secretary's approved itinerary record as the authority for itinerary status.
- **Rationale / Policy basis:** Approved itinerary status is formally controlled and must not be inferred from informal messages.
- **Affected modules / use cases:** FC-001, FC-004, FC-005
- **Decision impact:** The tracker can display itinerary status only when a formal approved source exists.
- **Validation & evidence:** Review source mapping and confirm the displayed status matches the approved record.
- **Notes:** Prior revisions remain visible for history.

### BR-002 - Leave status must come from HR-controlled leave records

- **Rule statement:** The tracker must treat HR leave records as the only authority for leave status.
- **Rationale / Policy basis:** Leave data is HR-controlled and may be personal or sensitive.
- **Affected modules / use cases:** FC-002, FC-005, FC-006
- **Decision impact:** Leave status cannot be manually re-entered as an independent truth source.
- **Validation & evidence:** Confirm leave source ownership and access restrictions.
- **Notes:** Read access may be narrower than office visibility access.

## 2. Revision and freshness rules

### BR-003 - Latest approved itinerary revision wins

- **Rule statement:** When more than one itinerary revision exists, the latest approved revision is the current status basis.
- **Rationale / Policy basis:** Staff need the current approved record, not a stale copy.
- **Affected modules / use cases:** FC-001, FC-004
- **Decision impact:** Older revisions remain visible in history but do not override the latest approved status.
- **Validation & evidence:** Confirm revision ordering against a sample itinerary history.
- **Notes:** If freshness cannot be confirmed, the view should flag it.

### BR-004 - Stale or unverified source data must be flagged

- **Rule statement:** If the source freshness or revision status is unclear, the tracker must flag the result as stale or unverified.
- **Rationale / Policy basis:** Staff should not act on uncertain status as if it were approved truth.
- **Affected modules / use cases:** FC-004, FC-007
- **Decision impact:** The view can show status, but not as fully trusted until source freshness is confirmed.
- **Validation & evidence:** Check the freshness threshold and flag behavior.
- **Notes:** The threshold must be agreed during definition.

## 3. Combination and display rules

### BR-005 - Combined availability view must not duplicate source records

- **Rule statement:** The tracker may combine itinerary, leave, and office expectation into one view, but it must not duplicate or overwrite the owning records.
- **Rationale / Policy basis:** The work needs one trusted view without creating a second system of record.
- **Affected modules / use cases:** FC-005, FC-006
- **Decision impact:** The solution is an aggregator, not the owner of truth.
- **Validation & evidence:** Review architecture and data flow to confirm read-only aggregation.
- **Notes:** Manual edits in the tracker must not become the governing source.

### BR-006 - Overlapping itinerary and leave must show both statuses

- **Rule statement:** If itinerary and leave overlap, the tracker must show both statuses rather than infer availability from only one source.
- **Rationale / Policy basis:** Staff need a truthful combined view.
- **Affected modules / use cases:** FC-001, FC-002, FC-003, FC-005
- **Decision impact:** Office staff can see the full context instead of a simplified answer that might be wrong.
- **Validation & evidence:** Test an overlap scenario and confirm both statuses display.
- **Notes:** The tracker must not guess which record is more important outside the agreed rule set.
