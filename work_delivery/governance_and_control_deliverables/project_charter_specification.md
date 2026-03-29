# Project Charter Specification

## 1. What This Artifact Is For

The Project Charter formally records sponsorship, authority, priority, funding commitment, and the Stage 3 Work Authorization decision.

Its purpose is to confirm that the initiative has been intentionally authorized and that the Delivery Owner has clear authority to act within the approved boundary. A useful charter makes the authorization basis, key commitments, and accountability model easy to understand and audit.

The intended outcome: delivery starts only when explicit authorization exists, with visible sponsorship, approved authority, and clear accountability.

## 2. When to Use It

Use this artifact in Stage 3 - Work Authorization when formal authorization, budget commitment, resource assignment, or named delivery authority is needed before delivery starts.

It aligns with PMI charter practice by recording purpose, high-level scope, authority, key constraints, and decision accountability in a single concise record.

## 3. Stage Fit and Handoffs

- **Stage 2:** the [Initiative Definition Document](initiative_definition_document_specification.md) provides the scope, outcomes, deliverables, and ownership baseline this charter authorizes.
- **Stage 3:** draft and approve this charter. Record the authorization decision. Delivery does not start without it.
- **Stage 4 onward:** this charter governs the authority boundary and commitment record. Any material re-authorization produces a new charter version.

Upstream source:

- [Initiative Definition Document Specification](initiative_definition_document_specification.md)

Downstream artifacts:

- [Functional Capabilities Specification](../solution_deliverables/functional_capabilities_specification.md)
- domain-specific solution, operational readiness, and acceptance artifacts
- condition log or follow-up record where authorization is conditional

## 4. Before You Start

Make sure you have:

- the approved or near-final Initiative Definition Document
- a confirmed Sponsor and Decision Authority
- a confirmed Delivery Owner
- the approval mechanism (committee resolution, delegated sign-off, or equivalent)
- confirmed budget and funding source, or a clear statement that funding is a condition

If any of these are missing, label the output as a working draft and state the gaps explicitly. Do not record an authorization decision before it has been made.

## 5. How to Draft It

1. Confirm the authorization mechanism. Know who will formally approve and how.
2. Start with the authorization statement. Everything else in the charter supports that single decision record.
3. Write the commitment summary from the Initiative Definition Document. Reference the IDD version rather than copying its content.
4. List authorization conditions explicitly and assign a named owner to each condition.
5. Keep the document short. If it starts to look like a project plan or a scope document, move that content out.
6. Use table format for fields where possible. It is easier to review and audit than narrative paragraphs.
7. Record the decision outcome using only the controlled values: Approve, Defer, Reject, or Approve with Conditions.

**If the outcome is Defer or Reject:** record that clearly and state that delivery must not start.

## 6. Minimum Structure

### 6.1. Charter identity

Include:

- project or initiative name
- charter version or date
- Sponsor
- Delivery Owner or project lead
- author or preparing party

### 6.2. Authorization statement

Include:

- formal statement of the decision outcome
- Decision Authority or approving body
- authorization date
- decision outcome using one of: **Approve, Defer, Reject, Approve with Conditions**
- authority granted to the Delivery Owner
- any explicit conditions, limits, or decision assumptions attached to the authorization

**If the decision outcome is Defer or Reject, the charter must clearly state that delivery is not authorized to start.**

### 6.3. Commitment summary

Include:

- purpose and expected outcomes summary
- approved scope summary
- approved budget or funding commitment
- key constraints and high-level risks
- named owner for each authorization condition where applicable
- reporting or acceptance expectations
- reference to the authoritative Initiative Definition Document version this authorization is based on

### 6.4. Template guide

Use short, decision-focused entries rather than narrative paragraphs:

| Field | What to record |
| --- | --- |
| Authorization basis | Resolution, signed decision, committee action, or delegated approval |
| Decision outcome | Approve, Defer, Reject, or Approve with Conditions |
| Purpose | Short statement of why the initiative is being authorized |
| Scope summary | High-level only, with reference to the Initiative Definition Document |
| Funding | Approved amount, funding source, and conditions if any |
| Authority granted | What the Delivery Owner is empowered to do |
| Constraints | Major limitations or conditions that shape delivery |
| Condition owner | Who is accountable for each condition or follow-up action |
| Acceptance expectations | Who must accept the outcome or domain-level deliverables before closure |

## 7. What to Keep Out

Keep the following out of this artifact:

- detailed scope breakdown
- design decisions
- task schedules
- full risk registers
- repeated copies of the Initiative Definition Document

## 8. Writing Rules

- Be concise. A charter is a decision record, not a project document.
- Use tables over narrative. Fields are easier to review and audit.
- Name everyone. Every authority, condition, and accountability needs a named person.
- Reference, do not copy. Point to the Initiative Definition Document version rather than restating its content.
- Use only the controlled decision values: Approve, Defer, Reject, Approve with Conditions. Do not invent variants.
- Make conditions specific. Vague conditions become assumed authority. Write each condition so it can be confirmed closed.
- Keep it stable. The charter should not need routine updates. Issue a new version only when sponsorship, funding, authority, or approved scope changes materially.

## 9. Traceability and Ownership Minimum

**Upstream:** reference the Initiative Definition Document version this authorization is based on. Also reference relevant funding or governance approvals and major decision records.

**Downstream:** where authorization is conditional, reference the tracked condition log or follow-up record used during delivery governance.

**Ownership:**

- The charter is usually prepared by the Delivery Owner or governance lead.
- It is approved by the Sponsor or Decision Authority.
- The approval reference is recorded in the authorization statement.

**Alignment rule:** the charter must not contradict the Initiative Definition Document. If authorization, funding, or scope changes materially after the charter is approved, issue a new charter version and update the IDD in controlled parallel.

## 10. Done When

This artifact is ready when:

- the decision outcome is recorded using one of the four controlled values
- the approving authority and date are named
- the authority granted to the Delivery Owner is explicit
- any authorization conditions have a named owner and a clear description
- if Defer or Reject, the document clearly states that delivery must not start
- the commitment summary references the authoritative IDD version rather than copying it
- no detailed design, schedules, or full risk registers have been included

## 11. What Comes Next

After the charter is approved:

1. confirm delivery mobilization readiness using the [Work Delivery Framework](../../its_work_management_model.md)
2. close any authorization conditions before proceeding with dependent scope
3. carry this charter's authority boundary forward as the governance reference for scope changes, escalations, and acceptance decisions through delivery and closure

## 12. Prompt Guide

### 12.1. Starter prompt

```text
Draft a Project Charter that formally records sponsorship, authority, purpose, high-level scope,
funding commitment, major constraints, and the decision to proceed.
Keep it short, attributable, and suitable for formal governance review.
```

### 12.2. Section prompts

```text
Draft the authorization statement so it clearly identifies the approving authority, date,
and the authority granted to the Delivery Owner.
```

```text
Create a charter summary table using the required fields in this specification.
```

### 12.3. Validation prompt

```text
Check whether this charter functions as a formal authorization artifact rather than a shortened project plan.
Rewrite any section that duplicates Initiative Definition content beyond what is needed for authorization.
```
