# Acceptance Record Specification

## 1. What This Artifact Is For

The Acceptance Record is the decision-ready summary of what was reviewed, what evidence supports acceptance, what conditions remain, and what decision the named authority made.

This artifact answers one simple question:

**What exactly is being accepted, on what basis, and under what conditions?**

Use it to keep acceptance explicit, attributable, and easy to review.

## 2. When to Use It

Use this artifact in Stage 7 whenever Solution Deliverables are being formally accepted.

It is especially useful when:

- acceptance is phased
- some items are conditional or deferred
- evidence comes from more than one source

## 3. Before You Start

Make sure you have:

- the acceptance boundary
- the items being reviewed
- links to the supporting evidence
- the named Acceptance Authority
- visibility of any exclusions, conditions, deferred items, or unresolved issues

## 4. How to Draft It

Follow these steps:

1. State the acceptance boundary clearly.
2. List each item being reviewed.
3. Link each item to approved scope references and evidence.
4. Use controlled status values for each row.
5. Add a scope compliance statement.
6. Record the decision, date, authority, and any follow-up actions.

Recommended status values:

- `accepted`
- `accepted with conditions`
- `deferred`
- `not accepted`

## 5. Minimum Structure

### 5.1. Record header

Include:

- initiative or solution name
- record version or ID
- preparation date
- prepared by
- acceptance scope or domain

### 5.2. Acceptance basis

Include:

- approved scope references being accepted
- related Solution Module Definition reference where module-level documents are being used
- evidence references
- deployment or release reference if relevant
- statement of whether this is full scope or partial scope acceptance

### 5.3. Acceptance table

Use a table like this:

| Item reviewed | Scope reference | Evidence reference | Status | Notes |
| --- | --- | --- | --- | --- |
| Request submission module | `SM-001`, `FC-001`, `UC-001` | `TE-001`, pilot sign-off | accepted with conditions | One reporting issue tracked for follow-up |

### 5.4. Scope compliance statement

Include:

- whether delivered behavior stayed within approved scope
- whether any in-scope items are deferred or excluded
- any approved waivers, exclusions, or conditions

### 5.5. Decision section

Include:

- Acceptance Authority
- decision date
- formal decision outcome
- conditions, follow-up actions, and owners if needed

## 6. Writing Rules

Keep this artifact concise.

Keep the following out:

- full test scripts
- raw defect logs
- long design explanations
- meeting narrative that does not affect the decision

Reference the evidence instead of copying it.

## 7. Done When

This artifact is ready when:

- a reviewer can understand the acceptance basis quickly
- evidence is linked clearly
- scope variance, exclusions, and conditions are visible
- the named authority and decision are explicit

## 8. What Comes Next

Use this artifact to support:

1. formal sign-off
2. transition and closure records
3. future audit or review of what was accepted

## 9. Prompt Guide

Starter prompt:

```text
Draft a Solution Deliverables Acceptance Record for Stage 7.
Show what was reviewed, what approved scope it maps to, what evidence supports acceptance, what conditions remain, and the formal decision of the named Acceptance Authority.
```

Validation prompt:

```text
Check whether any open issue is hidden in notes instead of being stated clearly as a condition, deferral, or non-acceptance item.
```
