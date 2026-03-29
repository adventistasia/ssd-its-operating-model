# Deployed Solution Specification

## 1. What This Artifact Is For

The Deployed Solution artifact records what approved solution behavior is actually live, where it is live, and under what conditions.

This artifact answers one simple question:

**What is live right now, and how does it relate to the approved scope?**

Use it to make the live state visible to business, delivery, and operational readers.

## 2. When to Use It

Use this artifact in Stage 6 whenever a new or materially changed solution enters a live or formally controlled environment.

It is especially useful for:

- phased rollouts
- pilot releases
- limited releases
- any release where ownership, evidence, or live boundary must be explicit

## 3. Stage Fit and Handoffs

- Stage 6: maintain a clear record of what approved scope is live, where, and under what conditions.
- Stage 7: use this artifact as one primary acceptance and closure evidence source.

Upstream sources:

- [Solution Module Definition Specification](solution_module_definition_specification.md)
- [Use Case Narratives Specification](use_case_narratives_specification.md)
- [Operational Readiness Confirmation Record Specification](../operational_readiness_deliverables/operational_readiness_confirmation_record_specification.md)

Downstream artifacts:

- [Acceptance Record Specification](acceptance_record_specification.md)
- [Formal Acceptance and Closure Record Specification](../governance_and_control_deliverables/formal_acceptance_and_closure_record_specification.md)

## 4. Before You Start

Make sure you have:

- the release or deployment identifier
- the environment or live instance
- the approved scope items represented in the release
- the named deployment, service, and support owners
- links to the evidence that supports the release

## 5. How to Draft It

Follow these steps:

1. Record what release this is and where it is live.
2. State the live boundary clearly, including who or what is included.
3. List the approved capabilities or modules represented in the release.
4. Reference the related Solution Module Definitions where module-level detail is important.
5. Note what is deferred, excluded, or still limited.
6. Identify the main dependencies and operational owners.
7. Link the validation, deployment, and readiness evidence.
8. Record any open conditions or follow-up actions.

Useful test:

- If a reader asks "what is live?" or "what is still limited?" the answer should be visible immediately.

## 6. Minimum Structure

### 6.1. Release header

Include:

- solution or service name
- release or deployment ID
- environment
- deployment date
- deployment owner
- live status such as `pilot`, `limited release`, `live`, `rolled back`, or `retired`

### 6.2. Live boundary

Include:

- which users, sites, business units, or channels are included
- whether this is full scope or partial scope

### 6.3. Scope delivered

Use a table like this:

| Area live | Scope reference | Evidence reference | Status | Notes |
| --- | --- | --- | --- | --- |
| Request submission | `FC-001`, `SM-001` | `TE-001`, release note 1 | live | Staff only in pilot sites |

### 6.4. Operational status

Include:

- Service Owner
- Support Owner
- monitoring/support/recovery status
- temporary operating conditions

### 6.5. Open conditions

Include:

- known issues or accepted defects
- temporary workarounds
- follow-up owners and due dates where useful

## 7. Writing Rules

Keep this artifact concise and evidence-based.

Keep the following out:

- detailed deployment procedures
- full architecture explanation
- full runbooks
- raw test execution logs

Reference the authoritative technical and operational artifacts instead.

## 8. Traceability, Ownership, and Review

Minimum traceability expectation:

- each live area links back to approved scope references (`FC-###`, `SM-###`, and `UC-###` where relevant)
- each live area links to supporting evidence and release references
- partial scope, deferred scope, and open conditions are explicit

Minimum ownership expectation:

- Delivery Owner maintains scope-to-live clarity.
- Service Owner and Support Owner confirm live ownership and operating conditions.

## 9. Done When

This artifact is ready when:

- the live boundary is clear
- readers can see what approved scope is live
- operational ownership is visible
- evidence links are present
- open conditions are not hidden

## 10. What Comes Next

Use this artifact as part of the basis for:

1. the [Acceptance Record](acceptance_record_specification.md)
2. operational handover and service readiness reviews
3. closure and formal acceptance records where needed

## 11. Prompt Guide

Starter prompt:

```text
Draft a Deployed Solution record for Stage 6.
Show what approved scope is live, where it is live, who owns it operationally, what evidence supports it, and what conditions remain open.
```

Validation prompt:

```text
Check whether the record makes the live boundary, scope delivered, ownership, and evidence clear without duplicating design or runbook content.
```
