# Residual Risk Acceptance Record Specification

## 1. Purpose and Intended Outcome

The Residual Risk Acceptance Record documents the formal acknowledgment and acceptance of material risk that remains after planned controls or mitigations have been applied.

It exists to keep risk acceptance explicit, attributable, and reviewable rather than silent or assumed. A useful record shows what risk remains, why it remains, what controls are in place, and who accepted the exposure.

The intended outcome is that material residual risk is consciously accepted by the right authority with a clear record of the remaining exposure, its basis, and any conditions attached to that acceptance.

## 2. When It Is Required

This artifact is required when material security, privacy, operational, or compliance risk remains and a responsible authority must decide whether to accept it.

## 3. Intended Readers and Users

- Sponsor or delegated risk owner
- Security / Data Protection Officer
- Business Owner / Process Owner
- Delivery Owner
- audit and governance reviewers

## 4. Intended Project Context

Use this artifact after risk treatment decisions are understood and before the residual risk is allowed to remain in operation. It is most useful where formal risk acceptance authority must be clear and where time-bound acceptance or conditions may apply.

It should align with NIST risk-management practice by making residual exposure, approving authority, review timing, and acceptance conditions explicit and reviewable.

## 5. How Much Detail to Include

Keep it concise and decision-focused. Include enough detail to identify the residual risk, why it remains, what controls exist, the impact if realized, and who accepted it.

## 6. Required Content or Minimum Structure

### 6.1. Record identity

Must include:

- record ID
- date
- linked risk assessment reference
- owner or preparer

This section identifies the acceptance record and its source risk context.

### 6.2. Required content for each accepted risk row

Each row must include:

- risk ID
- residual risk description
- controls applied
- impact summary
- basis for acceptance, such as business necessity, implementation timing, or compensating control position
- review date
- accepting authority
- conditions

Recommended columns:

| Risk ID | Residual risk | Controls applied | Impact summary | Basis for acceptance | Review date | Accepting authority | Conditions |
| --- | --- | --- | --- | --- | --- | --- | --- |

This row structure ensures the decision basis is explicit rather than implied.

### 6.3. Acceptance statement

Must include:

- formal statement that the residual risk is being accepted
- scope or environment the acceptance applies to
- any time limit, condition, or required follow-up action

This section is the actual acceptance act and must not be vague.

## 7. What to Keep Out

Keep the following out of this artifact:

- the entire underlying risk register
- vague approval wording such as `noted` or `aware`
- hidden conditions that are not stated clearly

## 8. Relationships to Other Artifacts

This record should reference the Security & Privacy Risk Assessment, Compliance & Regulatory Alignment Statement, Decision Record Log, and closure or acceptance records where applicable.

## 9. Ownership, Review, and Acceptance Expectations

The security or governance lead usually prepares the record. The accepting authority must be the person or body empowered to accept the specific class of risk.

## 10. Maintenance Expectations

Review the record at the stated review date, when controls change, or when the residual risk changes materially. Supersede rather than overwrite accepted records.

## 11. Validation Guide

- Is the residual risk described clearly enough for a decision maker to understand it?
- Is the accepting authority explicit and appropriate?
- Are any conditions or review dates visible?
- Does the record explain why acceptance was chosen instead of further treatment or rejection?
- Does the record distinguish clearly between risk description and formal acceptance?

If weak, tighten the risk statement and make the formal acceptance wording explicit.

## 12. Prompt Guide for Drafting the Artifact

### 12.1. Starter prompt

> Draft a Residual Risk Acceptance Record for this initiative.
> Summarize the residual risk, the controls already applied, the impact if the risk is realized, any review date or conditions, and the formal acceptance by the appropriate authority.
> Keep it concise, explicit, and attributable.
