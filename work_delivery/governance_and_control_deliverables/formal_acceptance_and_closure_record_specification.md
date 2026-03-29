# Formal Acceptance & Closure Record Specification

## 1. What This Artifact Is For

The Formal Acceptance & Closure Record confirms that required deliverables or deliverable domains have been accepted, that named authorities have signed off, and that the initiative is formally closed or conditionally closed.

It answers one simple question:

**Is the initiative actually closed, by whom, and on what basis?**

Use this artifact to make closure explicit, attributable, and auditable. A useful record shows what was accepted, what remains open, and who authorized closure. It is not a summary of activity — it is proof that acceptance happened and that closure was a conscious decision.

## 2. When to Use It

Use this artifact at Stage 7 when the initiative reaches final acceptance, handover, or closure.

It is required when:

- final deliverable domains have been accepted or formally dispositioned
- closure must be attributable to a named authority and date
- operational ownership is being transferred
- any domain is being closed by exception rather than full acceptance

It should align with PMI closeout practice by linking final closure to accepted deliverables, unresolved obligations, and formal decision authority.

## 3. Stage Fit and Handoffs

- Stage 6: delivery evidence and domain acceptance records are produced — these feed directly into this record.
- Stage 7: use this artifact to confirm, summarize, and formally close the initiative.

Upstream sources:

- [Initiative Definition Document Specification](initiative_definition_document_specification.md)
- Domain acceptance records (solution, operational readiness, data governance, security, change enablement)
- Operational Readiness and Technical Design confirmations

Downstream artifacts:

- Nothing — this is the final governance artifact for the initiative.

## 4. Before You Start

Make sure you have:

- all required domain acceptance records or formal dispositions
- named closing authority confirmed (Sponsor or delegated Decision Authority)
- handover confirmation if operational ownership is transferring
- a list of any residual obligations, conditions, or exceptions
- approved financial and delivery summary or reference to one

If domain acceptance records are incomplete, treat the closure record as a working draft only. Do not present it as a final closure decision.

## 5. How to Draft It

Follow these steps:

1. Identify every deliverable domain in scope for this initiative.
2. For each domain, confirm whether it has been accepted, accepted with conditions, not accepted, or closed by exception.
3. Populate the acceptance summary table with controlled status values and a reference to the authoritative acceptance record.
4. List any residual obligations explicitly — with a named owner and a due date or review point.
5. Confirm operational handover: name the receiving owner and the handover date.
6. Add the financial and delivery summary at an appropriate level, or reference the source document.
7. Write the closure decision with the closing authority's name, decision date, and an explicit statement if any exception-based closure applies.

Useful test:

- If you cannot point to an acceptance record for a domain, the closure decision is not yet supported. Do not write around this gap.
- If a residual obligation has no named owner, it will not be followed up. Name the owner or remove the item.

## 6. Minimum Structure

### 6.1. Closure record identity

Must include:

- initiative name
- record version or date
- prepared by
- closure status
- statement of the closure boundary, such as full initiative closure, phase closure, or closure by exception

This section identifies the closure decision record.

### 6.2. Acceptance summary

Must include a summary of required deliverables or deliverable domains and their acceptance status.

Recommended columns:

| Domain or deliverable | Acceptance status | Acceptance reference | Open conditions | Owner |
| --- | --- | --- | --- | --- |

Use controlled status values:

- `accepted`
- `accepted with conditions`
- `not accepted`
- `closed by exception`

This table shows whether closure is actually supported by prior acceptance.

If a required deliverable or domain was excluded from closure, the reason and authorizing decision must be visible.

### 6.3. Residual obligations and transition items

Must include:

- unresolved items, transition actions, contractual obligations, or residual conditions that remain after closure
- named owner for each material follow-up item
- due date or next review point where timing matters

This section makes clear what closure does and does not mean.

### 6.4. Operational handover confirmation

Required when operational ownership is impacted.

Must include:

- operational owner or support owner receiving responsibility
- handover status and date
- reference to handover or operational readiness evidence
- any operational conditions remaining at closure

This section confirms that closure does not leave support ownership ambiguous.

### 6.5. Final financial and delivery summary

Must include:

- approved versus actual delivery position at an appropriate level
- notable variance or condition affecting closure
- reference to the source financial or delivery summary where detailed values are maintained

### 6.6. Closure decision

Must include:

- final closure statement
- named closing authority
- decision date
- approval reference
- explicit statement when closure is granted despite outstanding items, risks, or conditions

This section is the formal act of closure.

### 6.7. Template guide

Keep entries short:

- `Acceptance reference`: point to the authoritative acceptance record, not a narrative summary
- `Open conditions`: record only what still matters after closure
- `Closed by exception`: use only when formal authority has approved closure despite outstanding items
- Residual obligations must have named owners and due dates, not general comments
- Handover confirmation must identify who is now accountable for running and supporting the outcome

## 7. What to Keep Out

Keep the following out of this artifact:

- full evidence packs
- detailed retrospective content unless formally required
- repeated copies of all acceptance records

## 8. Writing Rules

Write directly and concisely. Every section should support a clear closure decision, not narrate the initiative history.

Domain-specific rules:

- The closure record proves acceptance happened — it is not a summary of activity. Each domain must show its acceptance reference.
- Each domain entry in the acceptance summary must point to a specific acceptance record, not just state that the domain is complete.
- Residual obligations must have named owners. Do not write them as general comments or intentions.
- Handover confirmation must identify the receiving owner clearly. "Handover complete" is not sufficient on its own.
- If any domain is `closed by exception`, the authority and rationale must be explicit in both the acceptance summary table and the closure decision section.
- Do not write around missing acceptance records. If a domain has no acceptance record, state that clearly and mark the closure as a working draft.

## 9. Traceability and Ownership Minimum

This record must be traceable back to domain acceptance records and forward to no further artifacts — it is the final governance record.

Minimum ownership expectations:

- Delivery Owner or governance lead prepares the record.
- Relevant Acceptance Authorities must have completed their part before the closure decision is signed.
- Sponsor or delegated Decision Authority confirms final closure.

Link explicitly to:

- all domain acceptance records referenced in the acceptance summary table
- the Initiative Definition Document or approved scope baseline
- operational readiness confirmation where handover is in scope
- residual risk acceptance records where applicable

## 10. Maintenance Expectations

The record is normally finalized once closure is approved. If closure is conditional, update the record or issue a superseding version once conditions are resolved. Preserve the original version as part of the audit trail.

## 11. Done When

This artifact is ready when:

- every in-scope domain has an acceptance status and a reference to an acceptance record
- residual obligations have named owners and due dates
- handover is confirmed with a named receiving owner where operations are impacted
- the closure decision names the authority, date, and any exception basis
- no domain is described as complete without an acceptance reference
- the artifact does not contain full evidence packs or retrospective narrative

## 12. What Comes Next

After this record is approved:

1. distribute the closure record to the Sponsor, Decision Authorities, and relevant stakeholders
2. confirm residual obligation owners have been notified of their follow-up items
3. confirm that support and operational owners have received the handover confirmation
4. file this record and all referenced acceptance records in the initiative record set
5. close the initiative in any relevant tracking or governance systems

## 13. Prompt Guide

Starter prompt:

```text
Draft a Formal Acceptance & Closure Record for this initiative.
Summarize accepted deliverables or domains, any residual obligations or exceptions, and the final closure decision with named authority and date.
Keep it concise, attributable, and evidence-linked.
```

Section prompts:

```text
Create the acceptance summary table using the required columns and controlled status values in this specification.
```

```text
Draft the closure decision section so the authority, decision, and any exception-based closure are explicit.
```

Validation prompts:

```text
Check whether this record proves that closure is supported by prior acceptance and not just by completion of activity.
```

```text
Check whether any residual obligation is hidden in narrative text instead of being stated as an explicit follow-up item with a named owner.
```
