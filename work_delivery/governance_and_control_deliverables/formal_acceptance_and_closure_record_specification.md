# Formal Acceptance & Closure Record Specification

## 1. What This Artifact Is For

The Formal Acceptance & Closure Record confirms that required deliverables or deliverable domains have been accepted, that the relevant authorities have signed off, that operational handover has been confirmed where needed, and that the initiative is formally closed or conditionally closed.

It exists to prevent informal completion and to preserve a clear decision trail at the end of the initiative. A useful record shows what was accepted, what remains open, and who authorized closure.

Intended readers include: Sponsor, Decision Authorities, Delivery Owner, Acceptance Authorities, and audit and governance reviewers.

## 2. When to Use It

This artifact is required when the initiative reaches final acceptance, handover, or closure in Stage 7 — Acceptance, Transition & Closure.

Use it after the required deliverable domains have been accepted or formally dispositioned. It is most useful where final closure must be explicit, attributable, and auditable, and where it must align closure to accepted deliverables, unresolved obligations, and formal decision authority.

The record is normally finalized once closure is approved. If closure is conditional, update the record or issue a superseding version once conditions are resolved.

## 3. Stage Fit and Handoffs

This artifact is produced in Stage 7 — Acceptance, Transition & Closure.

**Upstream sources:**

- [Initiative Definition Document](initiative_definition_document_specification.md) — the deliverables and acceptance structure this record closes out
- [Project Charter](project_charter_specification.md) — the authorization basis being closed
- Domain acceptance records — the prior acceptance evidence that supports closure
- [Decision Record Log](decision_record_log_specification.md) — decisions and conditions relevant to closure
- Operational readiness confirmation and handover records

**This record is the final governance artifact.** No downstream artifact supersedes it.

## 4. Before You Start

Before drafting, confirm you have:

- completed acceptance records for all required deliverable domains (or formal disposition decisions for any not accepted)
- confirmation of operational handover where the initiative impacts a service or system
- final financial and delivery position at an appropriate level
- named closing authority (Sponsor or delegated Decision Authority) available to confirm closure
- clarity on any residual obligations, open conditions, or exception-based closures

If domain acceptance records are incomplete or handover is unconfirmed, label this document as a **working draft** and identify what is outstanding.

## 5. How to Draft It

1. **Complete the closure record identity section.** State the initiative name, record version, preparing party, closure status, and scope of closure (full, phase, or exception-based).
2. **Populate the acceptance summary table.** For each required deliverable or domain, record acceptance status, reference to the acceptance record, open conditions, and owner.
3. **List residual obligations and transition items.** Record any unresolved items that remain after closure, with owners and due dates.
4. **Confirm operational handover.** Where operations are impacted, record the receiving operational or support owner, handover status and date, and reference to handover evidence.
5. **Summarize the final financial and delivery position.** Record approved versus actual at an appropriate level and note any material variance.
6. **Record the closure decision.** State the final closure statement, closing authority, decision date, and approval reference. Where closure is being granted despite outstanding items, make that explicit.

## 6. Minimum Structure

This artifact is usually a short record with a summary table.

### 6.1. Closure record identity

Must include:

- initiative name
- record version or date
- prepared by
- closure status
- statement of the closure boundary (full initiative closure, phase closure, or closure by exception)

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
- owner for each material follow-up item
- due date or next review point for each material follow-up item where timing matters

This section makes it clear what closure does and does not mean.

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

This section keeps closure attributable to what was committed and what was actually delivered.

### 6.6. Closure decision

Must include:

- final closure statement
- named closing authority
- decision date
- approval reference
- explicit statement when closure is being granted despite outstanding items, risks, or conditions

This section is the formal act of closure.

### 6.7. Template guide

Keep entries short:

- `Acceptance reference`: point to the authoritative acceptance record, not a narrative summary
- `Open conditions`: record only what still matters after closure
- `Closed by exception`: use only when formal authority has approved closure despite outstanding items
- Residual obligations should remain actionable, with clear owners and due dates rather than general comments
- Handover confirmation should identify who is now accountable for running and supporting the outcome

## 7. Writing Rules

Keep the record concise and decision-focused. Include enough detail to show what has been accepted, what obligations remain, and who approved closure. Link to supporting records rather than duplicating them.

Keep the following out:

- full evidence packs
- detailed retrospective content unless formally required
- repeated copies of all acceptance records

## 8. Traceability, Ownership, and Review

The Delivery Owner or governance lead usually prepares the record. Formal closure is normally confirmed by the Sponsor or delegated Decision Authority after relevant Acceptance Authorities have completed their part.

This artifact traces back to the [Initiative Definition Document](initiative_definition_document_specification.md) and all domain acceptance records. It should also reference the [Decision Record Log](decision_record_log_specification.md), operational readiness confirmation, residual risk acceptance where relevant, and final handover or contract records.

## 9. Done When

The record is ready to issue when:

- all required deliverables or domains have an acceptance status with a reference to the authoritative acceptance record
- any `accepted with conditions` or `closed by exception` entries have named owners and visible conditions
- operational handover is confirmed where operations are impacted
- residual obligations are explicitly listed with owners and due dates
- the final financial and delivery summary is complete or referenced
- the named closing authority, decision date, and approval reference are recorded

## 10. Validation Guide

- Does the record show clearly that required acceptance happened before closure?
- Where operations are impacted, does the record clearly confirm handover and receiving ownership?
- Are residual obligations or exceptions explicit?
- Does the record make it obvious whether closure is full, phased, or exception-based?
- Is there a concise final financial and delivery summary or reference?
- Is the closing decision attributable to a named authority and date?
- Does the artifact avoid becoming a full narrative history of the initiative?

If weak, improve the acceptance references, clarify the closure status, and make outstanding conditions more explicit.

## 11. What Comes Next

1. Distribute the signed closure record to the Sponsor, Delivery Owner, Acceptance Authorities, and audit or governance record holders.
2. Update the [Initiative Definition Document](initiative_definition_document_specification.md) status to Final and record the closure reference.
3. Ensure any residual obligations are transferred to named owners with due dates visible outside this record.
4. Archive the initiative record set including the closure record, acceptance records, and decision log.

## 12. Prompt Guide
Summarize accepted deliverables or domains, any residual obligations or exceptions, and the final closure decision with named authority and date.
Keep it concise, attributable, and evidence-linked.
```

### Validation prompt

```
Check whether this record proves that closure is supported by prior acceptance and not just by completion of activity.
Check whether any residual obligation is hidden in narrative text instead of being stated as an explicit follow-up item.
```
